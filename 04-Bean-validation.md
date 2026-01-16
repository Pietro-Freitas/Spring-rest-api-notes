# 📚 Capítulo 4: Integridade de Dados e Bean Validation

### 📋 Tópicos deste Capítulo

1. [A Necessidade da Validação: O Princípio GIGO](https://www.google.com/search?q=%231-a-necessidade-da-valida%C3%A7%C3%A3o-o-princ%C3%ADpio-gigo)
2. [O que é Bean Validation (JSR 380)](https://www.google.com/search?q=%232-o-que-%C3%A9-bean-validation-jsr-380)
3. [Anotações de Restrição e sua Semântica](https://www.google.com/search?q=%233-anota%C3%A7%C3%B5es-de-restri%C3%A7%C3%A3o-e-sua-sem%C3%A2ntica)
4. [Validação na Prática: A Anotação @Valid](https://www.google.com/search?q=%234-valida%C3%A7%C3%A3o-na-pr%C3%A1tica-a-anota%C3%A7%C3%A3o-valid)
5. [Tratamento de Erros de Validação (400 Bad Request)](https://www.google.com/search?q=%235-tratamento-de-erros-de-valida%C3%A7%C3%A3o-400-bad-request)
6. [Diferença entre Validação Estrutural e Regra de Negócio](https://www.google.com/search?q=%236-diferen%C3%A7a-entre-valida%C3%A7%C3%A3o-estrutural-e-regra-de-neg%C3%B3cio)
7. [Conclusão](https://www.google.com/search?q=%237-conclus%C3%A3o)

---

### 🎯 Objetivos do Capítulo

* Compreender a importância da integridade de dados na entrada do sistema.
* Aplicar as especificações do **Jakarta Bean Validation** em DTOs.
* Configurar o Spring Boot para interceptar e rejeitar requisições inválidas automaticamente.
* Refinar o `@ControllerAdvice` para fornecer feedback detalhado ao cliente.
* Distinguir onde termina a validação de formato e onde começa a lógica de serviço.

---

## 1. A Necessidade da Validação: O Princípio GIGO

Em computação e análise de sistemas, existe um conceito fundamental conhecido como **GIGO** (*Garbage In, Garbage Out* — "Lixo entra, lixo sai"). Se permitirmos que dados inconsistentes, incompletos ou malformados entrem em nossa camada de serviço, o resultado será um estado de banco de dados corrompido ou erros inesperados em tempo de execução.

Até o momento, nossa API aceita qualquer string como descrição de uma tarefa, incluindo textos vazios ou nulos.

> **Definição 4.1 (Integridade de Dados):** Refere-se à manutenção e garantia da precisão e consistência dos dados durante todo o seu ciclo de vida. No contexto de APIs, a primeira linha de defesa da integridade ocorre na **Validação de Entrada**.

---

## 2. O que é Bean Validation (JSR 380)

Para não termos que escrever dezenas de blocos `if (campo == null)` manualmente, o ecossistema Java padronizou a validação através do **Bean Validation**.

Assim como o JPA (visto no Cap. 2) é uma especificação para banco de dados, o Bean Validation é uma especificação para validação de dados via anotações. A implementação padrão utilizada pelo Spring Boot é o **Hibernate Validator**.

---

## 3. Anotações de Restrição e sua Semântica

As anotações são aplicadas diretamente nos campos dos nossos **DTOs**. É crucial entender a semântica de cada uma para evitar redundâncias.

### 3.1 Principais Anotações

| Anotação | Descrição Semântica | Uso Comum |
| --- | --- | --- |
| `@NotNull` | O campo não pode ser nulo, mas pode ser uma String vazia `""`. | IDs, Objetos aninhados. |
| `@NotEmpty` | O campo não pode ser nulo e seu tamanho deve ser maior que zero. | Listas e Coleções. |
| `@NotBlank` | O campo não pode ser nulo e deve conter ao menos um caractere que não seja espaço. | Nomes, Descrições, E-mails. |
| `@Size(min=x, max=y)` | O tamanho da string ou coleção deve estar entre x e y. | Senhas, Biografias. |
| `@Min` / `@Max` | Restringe valores numéricos. | Idade, Preço, Quantidade. |
| `@Email` | Valida se a string segue o padrão de um endereço de e-mail. | Campos de contato. |

---

## 4. Validação na Prática: A Anotação @Valid

Vamos aplicar essas restrições ao nosso `TarefaRequestDTO`. Observe que a validação deve ocorrer no **DTO de entrada**, pois é ele que recebe os dados "crus" do cliente.

### 4.1 Atualizando o DTO

```java
package com.exemplo.api.dto;

import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Size;

public record TarefaRequestDTO(
    @NotBlank(message = "A descrição não pode estar em branco")
    @Size(min = 5, max = 100, message = "A descrição deve ter entre 5 e 100 caracteres")
    String descricao
) {}

```

### 4.2 Ativando a Validação no Controller

Não basta anotar o DTO; precisamos instruir o Spring a validar o objeto assim que ele chega no Controller através da anotação `@Valid`.

```java
@PostMapping
public ResponseEntity<TarefaResponseDTO> criar(@RequestBody @Valid TarefaRequestDTO dados) {
    // Se os dados forem inválidos, o código abaixo NEM SEQUER É EXECUTADO.
    // O Spring interrompe a requisição e lança uma exceção.
    TarefaResponseDTO novaTarefa = service.criar(dados);
    return ResponseEntity.status(HttpStatus.CREATED).body(novaTarefa);
}

```

---

## 5. Tratamento de Erros de Validação (400 Bad Request)

Quando a validação falha, o Spring lança uma `MethodArgumentNotValidException`. Por padrão, a resposta é um erro 400 genérico. Para uma API profissional, precisamos informar ao cliente **qual campo falhou** e **por que**.

### 5.1 Refinando o Tratador de Erros

Adicionaremos um novo método ao nosso `@ControllerAdvice` (criado no Cap. 3).

```java
@ExceptionHandler(MethodArgumentNotValidException.class)
public ResponseEntity<List<DadosErroValidacao>> tratarErro400(MethodArgumentNotValidException ex) {
    // Extraímos a lista de erros da exceção
    var erros = ex.getFieldErrors().stream()
        .map(DadosErroValidacao::new)
        .toList();
    
    return ResponseEntity.badRequest().body(erros);
}

// Record auxiliar para formatar o JSON de erro
public record DadosErroValidacao(String campo, String mensagem) {
    public DadosErroValidacao(FieldError erro) {
        this(erro.getField(), erro.getDefaultMessage());
    }
}

```

---

## 6. Diferença entre Validação Estrutural e Regra de Negócio

Este é um ponto de confusão comum para iniciantes. É vital estabelecer uma distinção rigorosa:

1. **Validação Estrutural (Bean Validation):** Verifica a "forma" do dado. Ex: "O e-mail tem um @?", "A descrição está vazia?". Isso acontece **antes** do Service.
2. **Regra de Negócio (Service Layer):** Verifica o "contexto" ou o "estado" do sistema. Ex: "Este usuário já possui 10 tarefas e não pode criar mais?", "Este e-mail já está cadastrado no banco?". Isso acontece **dentro** do Service.

> **Regra de Ouro:** Se você precisa consultar o banco de dados para validar algo, essa lógica pertence à **Camada de Serviço**, não às anotações do DTO.

---

## 7. Conclusão

Neste capítulo, implementamos a primeira camada de defesa da nossa aplicação. Através do **Bean Validation**, garantimos que apenas dados estruturalmente corretos cheguem à nossa lógica de negócio.

Aprendemos a utilizar anotações como `@NotBlank` e `@Size`, e como capturar erros de validação de forma centralizada para oferecer uma experiência clara ao desenvolvedor que consome nossa API.

Nossa arquitetura agora está assim:
`Client -> Controller (@Valid) -> Handler (Erro 400 se inválido) -> Service -> Repository -> DB`

Com os dados validados e a arquitetura em camadas sólida, estamos prontos para um passo crucial: **Relacionamentos entre Recursos**. No próximo capítulo, aprenderemos como modelar tarefas que pertencem a usuários, introduzindo chaves estrangeiras e a semântica REST para recursos aninhados.
