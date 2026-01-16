# 📚 Capítulo 3: Arquitetura Profissional: DTOs, Services e Tratamento de Exceções

### 📋 Tópicos deste Capítulo

1. [O Problema do Acoplamento e Exposição](https://www.google.com/search?q=%231-o-problema-do-acoplamento-e-exposi%C3%A7%C3%A3o)
2. [O Padrão DTO (Data Transfer Object)](https://www.google.com/search?q=%232-o-padr%C3%A3o-dto-data-transfer-object)
3. [A Camada de Serviço (Service Layer)](https://www.google.com/search?q=%233-a-camada-de-servi%C3%A7o-service-layer)
4. [Tratamento Centralizado de Erros](https://www.google.com/search?q=%234-tratamento-centralizado-de-erros)
5. [Prática: Refatoração Completa da API](https://www.google.com/search?q=%235-pr%C3%A1tica-refatora%C3%A7%C3%A3o-completa-da-api)
6. [Conclusão](https://www.google.com/search?q=%236-conclus%C3%A3o)

---

### 🎯 Objetivos do Capítulo

* Analisar os riscos de segurança e design ao expor **Entidades JPA** diretamente na API.
* Implementar o padrão **DTO** para desacoplar a representação externa da interna.
* Isolar a Regra de Negócio utilizando a **Service Layer**.
* Substituir o tratamento de erros genérico por **Exceções Personalizadas** e manipuladores globais (`@ControllerAdvice`).
* Compreender o uso de **Java Records** para imutabilidade de dados.

---

## 1. O Problema do Acoplamento e Exposição

No final do Capítulo 2, nossa API funcionava, mas violava princípios graves de arquitetura limpa ao retornar a classe `Tarefa` (nossa Entidade) diretamente no Controller. Ao expor a Entidade JPA para o mundo externo, incorremos em três riscos principais:

* **Vulnerabilidade de Segurança (Over-fetching):** Se adicionarmos campos sensíveis (como uma senha) na Entidade, eles serão enviados automaticamente no JSON.
* **Quebra de Contrato (Acoplamento Forte):** Se o nome de uma coluna no banco mudar, o JSON da API mudará instantaneamente, quebrando todos os clientes (Front-end/Mobile).
* **Ciclos de Referência:** Serializadores JSON podem entrar em loop infinito ao tentar converter relacionamentos bidirecionais entre objetos.

---

## 2. O Padrão DTO (Data Transfer Object)

O mundo externo deve ver apenas o que permitimos. O padrão **DTO** resolve o problema de exposição criando objetos simples destinados exclusivamente ao transporte de dados.

> **Definição 3.1 (DTO):** Um Objeto de Transferência de Dados é um padrão de arquitetura que tem como única finalidade transportar dados entre processos. Ele não contém lógica de negócios e é independente do esquema do banco de dados.

### 2.1 Implementação com Java Records

A partir do Java 16, os **Records** são a forma ideal de criar DTOs, pois são imutáveis por padrão.

#### Request DTO (Entrada de Dados)

```java
package com.exemplo.api.dto;

/**
 * Record que define apenas o que o cliente TEM PERMISSÃO para enviar 
 * ao criar uma nova tarefa.
 */
public record TarefaRequestDTO(
    String descricao
) {}

```

#### Response DTO (Saída de Dados)

```java
package com.exemplo.api.dto;

import com.exemplo.api.model.Tarefa;
import java.time.LocalDateTime;

/**
 * Define o contrato de saída. Protege a aplicação contra mudanças 
 * estruturais na Entity.
 */
public record TarefaResponseDTO(
    Long id,
    String descricao,
    boolean concluida,
    LocalDateTime dataCriacao
) {
    // Construtor de conveniência para converter Entity -> DTO
    public TarefaResponseDTO(Tarefa entidade) {
        this(
            entidade.getId(), 
            entidade.getDescricao(), 
            entidade.isConcluida(), 
            entidade.getDataCriacao()
        );
    }
}

```

---

## 3. A Camada de Serviço (Service Layer)

O Controller deve ser apenas um "guarda de trânsito": ele recebe a requisição, valida o formato e delega a tarefa. Quem "pensa" e executa a lógica é o **Service**.

> **Princípio da Responsabilidade Única:** A Camada de Serviço deve isolar a lógica de negócios e as transações, impedindo que o Controller acesse o Repository diretamente.

### 3.1 Implementação do TarefaService

```java
package com.exemplo.api.service;

import com.exemplo.api.dto.*;
import com.exemplo.api.model.Tarefa;
import com.exemplo.api.repository.TarefaRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.util.List;
import java.util.stream.Collectors;

@Service // Define que esta classe é um Bean gerenciado pelo Spring
public class TarefaService {

    private final TarefaRepository repositorio;

    public TarefaService(TarefaRepository repositorio) {
        this.repositorio = repositorio;
    }

    @Transactional(readOnly = true) 
    public List<TarefaResponseDTO> listarTodas() {
        return repositorio.findAll()
                .stream()
                .map(TarefaResponseDTO::new)
                .collect(Collectors.toList());
    }

    @Transactional
    public TarefaResponseDTO criar(TarefaRequestDTO dados) {
        Tarefa novaTarefa = new Tarefa();
        novaTarefa.setDescricao(dados.descricao());
        
        Tarefa salva = repositorio.save(novaTarefa);
        return new TarefaResponseDTO(salva);
    }
}

```

---

## 4. Tratamento Centralizado de Erros

Precisamos retornar erros semanticamente corretos (como o **404 Not Found**) sem poluir o código com blocos `try-catch` repetitivos.

### 4.1 Exceção Personalizada

```java
package com.exemplo.api.exception;

public class RecursoNaoEncontradoException extends RuntimeException {
    public RecursoNaoEncontradoException(String mensagem) {
        super(mensagem);
    }
}

```

### 4.2 Handler Global (@ControllerAdvice)

O Spring intercepta as exceções e as transforma em um JSON padronizado.

```java
package com.exemplo.api.infra;

import com.exemplo.api.exception.RecursoNaoEncontradoException;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.*;

import java.time.LocalDateTime;
import java.util.Map;

@ControllerAdvice // Interceptador global
public class TratadorDeErros {

    @ExceptionHandler(RecursoNaoEncontradoException.class)
    public ResponseEntity<Object> tratarErro404(RecursoNaoEncontradoException ex) {
        Map<String, Object> corpoErro = Map.of(
            "timestamp", LocalDateTime.now(),
            "status", HttpStatus.NOT_FOUND.value(),
            "erro", "Recurso não encontrado",
            "mensagem", ex.getMessage()
        );
        return ResponseEntity.status(HttpStatus.NOT_FOUND).body(corpoErro);
    }
}

```

---

## 5. Prática: Refatoração Completa da API

Com as camadas separadas, o Controller torna-se extremamente conciso.

```java
package com.exemplo.api.controller;

import com.exemplo.api.dto.*;
import com.exemplo.api.service.TarefaService;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.*;

import java.util.List;

@RestController
@RequestMapping("/api/tarefas")
public class TarefaController {

    private final TarefaService service;

    public TarefaController(TarefaService service) {
        this.service = service;
    }

    @GetMapping
    public ResponseEntity<List<TarefaResponseDTO>> listar() {
        return ResponseEntity.ok(service.listarTodas());
    }

    @GetMapping("/{id}")
    public ResponseEntity<TarefaResponseDTO> buscar(@PathVariable Long id) {
        return ResponseEntity.ok(service.buscarPorId(id));
    }

    @PostMapping
    public ResponseEntity<TarefaResponseDTO> criar(@RequestBody TarefaRequestDTO dados) {
        TarefaResponseDTO novaTarefa = service.criar(dados);
        return ResponseEntity.status(HttpStatus.CREATED).body(novaTarefa);
    }
}

```

### 📊 Resumo das Mudanças Arquiteturais

| Característica | Antes (Capítulo 2) | Depois (Capítulo 3) | Benefício |
| --- | --- | --- | --- |
| **Retorno da API** | Entidade JPA (`@Entity`) | Record DTO | Segurança e Desacoplamento |
| **Lógica de Negócio** | No Controller | No Service | Organização e Reuso |
| **Tratamento de Erros** | Erro 500 ou nulo | 404 Customizado | Semântica HTTP Correta |
| **Persistência** | Conexão Direta | Intermediação via Service | Facilidade em Testes Unitários |

---

## 6. Conclusão

Neste capítulo, profissionalizamos nossa aplicação. Deixamos de ter um protótipo funcional para ter uma **arquitetura em camadas robusta**. Isolamos o domínio do mundo externo, centralizamos a inteligência do negócio e implementamos um tratamento de erros declarativo.

No entanto, ainda há uma falha crítica: o usuário pode tentar criar uma tarefa com descrição vazia ou nula. No próximo capítulo, exploraremos a **Bean Validation** para garantir a integridade dos dados antes mesmo que eles cheguem ao nosso Service.
