# Capítulo 1: Fundamentos de Arquitetura Web e o Framework Spring Boot

## Tópicos deste Capítulo
1. [Introdução Conceitual](#1-introdução-conceitual-do-monólito-aos-sistemas-distribuídos)
2. [A Natureza da API](#2-a-natureza-da-api-application-programming-interface)
3. [O Estilo Arquitetural REST](#3-o-estilo-arquitetural-rest)
4. [O Protocolo HTTP](#4-o-protocolo-http-como-substrato)
5. [Introdução ao Spring Boot](#5-introdução-ao-spring-boot)
6. [Prática: Primeira API REST](#6-construindo-a-primeira-api-rest-com-spring-boot)
7. [Boas Práticas Iniciais](#7-boas-práticas-iniciais)

---

### Objetivos do Capítulo
* Compreender a natureza dos sistemas distribuídos e a necessidade de interfaces de comunicação.
* Definir formalmente o conceito de API e o estilo arquitetural REST.
* Analisar o protocolo HTTP como o substrato fundamental para APIs Web.
* Introduzir o Spring Boot através dos princípios de Inversão de Controle e Injeção de Dependência.
* Implementar uma API REST inicial, analisando rigorosamente o fluxo de execução.

---

## 1. Introdução Conceitual: Do Monólito aos Sistemas Distribuídos

Para compreendermos a engenharia de software moderna, devemos primeiramente analisar a evolução da topologia das aplicações. Historicamente, o desenvolvimento de software centrava-se na criação de **aplicações monolíticas**.

> **Definição de Monólito:** Uma aplicação monolítica pode ser definida como um sistema onde a interface de usuário (o que se vê), a lógica de negócios (o processamento) e a camada de acesso a dados (a persistência) residem em um único bloco de código, compilado e implantado como uma unidade indivisível.

![Comparação Monólito vs Distribuído](./images/microservices-soa.jpeg)

Embora o modelo monolítico seja simples inicialmente, ele apresenta um problema fundamental de escalabilidade e manutenção. À medida que a complexidade aumenta, a alteração de um pequeno componente exige a recompilação de todo o sistema. Isso nos leva ao conceito de **Sistemas Distribuídos**.

> **Definição 1.1 (Sistema Distribuído):** Um sistema distribuído é uma coleção de computadores ou processos independentes que se apresentam ao usuário como um sistema único e coerente.

Em um ambiente web moderno, raramente um sistema opera isolado. Uma loja virtual, por exemplo, não é apenas um programa; é uma composição de serviços:
* Um serviço gerencia o catálogo.
* Outro processa pagamentos (frequentemente externo, como PayPal ou Stripe).
* Um terceiro gerencia a logística.

### O Problema da Comunicação
Se separamos o sistema em partes distintas (desacoplamento), surge um novo desafio: *como essas partes conversam entre si?*

Diferente de uma função interna que chama outra na mesma memória do computador, sistemas distribuídos precisam trocar dados através de uma rede, que é inerentemente não confiável e lenta comparada à memória RAM. É para resolver esse problema de comunicação padronizada que surgem as APIs.

---

## 2. A Natureza da API (Application Programming Interface)

O termo **API** é frequentemente utilizado de forma coloquial, mas exige uma definição precisa.

> **Definição 2.1 (API):** Uma Interface de Programação de Aplicações (API) é um conjunto de definições e protocolos que permite a interação entre componentes de software distintos, abstraindo a complexidade da implementação interna desses componentes.

Podemos pensar na API como um **contrato**. Suponha que você possua um componente $A$ (o cliente) e um componente $B$ (o servidor). O componente $A$ não precisa saber como $B$ realiza suas tarefas (se usa Java, Python, ou como armazena dados). $A$ precisa apenas saber:
1.  O que pedir.
2.  Como pedir.
3.  O que esperar como resposta.

### 2.1 API Local vs. API Web
É crucial distinguir dois contextos:

* **API Local:** Ocorre quando usamos uma biblioteca no nosso código. Por exemplo, ao usar a classe `Math` em Java, estamos consumindo a API da biblioteca padrão do Java. A comunicação é feita via chamadas de método na memória.
* **API Web:** Ocorre quando a comunicação atravessa a rede. O contrato não é mais uma assinatura de método em código, mas sim mensagens enviadas via protocolos de rede (geralmente HTTP).

*Neste capítulo, focaremos exclusivamente em APIs Web.*

---

## 3. O Estilo Arquitetural REST

Ao projetar APIs Web, poderíamos inventar qualquer formato de mensagem. Porém, a falta de padronização geraria caos. Para resolver isso, Roy Fielding, em sua dissertação de doutorado (2000), definiu o **REST** (Representational State Transfer).

> **Nota Importante:** REST não é um protocolo e não é um código. REST é um **estilo arquitetural**, um conjunto de restrições e princípios de design.

### 3.1 Os Princípios Fundamentais do REST
Para que um sistema seja considerado RESTful, ele deve aderir a certos princípios. Destacaremos os três mais críticos para o nosso estudo inicial:

1.  **Recursos (Resources):** No REST, tudo é um recurso. Um recurso é qualquer informação que pode ser nomeada: um usuário, um produto, uma imagem. Cada recurso deve possuir um identificador único (URI).
2.  **Representações:** O servidor não envia o objeto do banco de dados diretamente. Ele envia uma representação do estado daquele recurso. A representação mais comum hoje é o **JSON** (JavaScript Object Notation), embora possa ser XML, HTML ou texto puro.
3.  **Statelessness (Ausência de Estado):** Esta é a restrição mais importante.

> **Princípio da Ausência de Estado:** Cada requisição do cliente para o servidor deve conter toda a informação necessária para entender e processar o pedido. O servidor não deve guardar o "contexto" da conversa anterior.

**Por que REST domina?**
A separação entre a interface (o que o cliente vê) e o armazenamento de dados (o que o servidor faz), combinada com a ausência de estado, permite que a aplicação escale. Se o servidor não guarda estado, qualquer servidor pode responder a qualquer requisição, facilitando o balanceamento de carga.

---

## 4. O Protocolo HTTP como Substrato

Embora o REST possa teoricamente ser implementado sobre outros protocolos, na prática, ele é quase sinônimo de **HTTP** (HyperText Transfer Protocol). O HTTP fornece os verbos e a semântica que o REST utiliza para manipular recursos.

### 4.1 Anatomia do HTTP
Uma interação HTTP consiste em dois atos: uma Requisição e uma Resposta.

#### A Requisição (Request)
Contém o Método, a URI, Headers e o Body.

| Método (Verbo) | Descrição da Ação |
| :--- | :--- |
| **GET** | Recuperar uma representação de um recurso (Leitura). |
| **POST** | Criar um novo recurso. |
| **PUT** | Atualizar/Substituir um recurso existente. |
| **DELETE** | Remover um recurso. |

* **URI:** O endereço do recurso (ex: `/usuarios/1`).
* **Headers:** Metadados (ex: `Content-Type: application/json` indica envio de dados em JSON).
* **Body:** Os dados em si (opcional, GET geralmente não tem corpo).

#### A Resposta (Response)
Contém o Status Code e o Body.

| Código (Status) | Categoria | Exemplo |
| :--- | :--- | :--- |
| **2xx** | Sucesso | `200 OK`, `201 Created` |
| **4xx** | Erro do Cliente | `400 Bad Request`, `404 Not Found` |
| **5xx** | Erro do Servidor | `500 Internal Server Error` |

* **Body:** A representação do recurso solicitado (ex: o JSON do usuário).

---

## 5. Introdução ao Spring Boot

Com a teoria estabelecida, voltamo-nos para a implementação. Java é uma linguagem robusta, mas configurar um servidor web, tratar conexões HTTP e converter JSON em objetos Java manualmente é uma tarefa árdua. Aqui entra o **Spring Framework** e o **Spring Boot**.

### 5.1 O Problema do "Boilerplate"
No passado, configurar uma aplicação Java Web exigia imensos arquivos XML. O Spring Boot adota a filosofia de **Convenção sobre Configuração**. Ele "opina" sobre como a aplicação deve ser estruturada e configura automaticamente o ambiente.

### 5.2 Inversão de Controle (IoC) e Injeção de Dependência (DI)
Para entender o Spring, devemos entender como ele gerencia os objetos. No paradigma tradicional, se o Objeto A precisa do Objeto B, o Objeto A instancia o Objeto B:

```java
// Abordagem Tradicional (Acoplada)
public class PedidoService {
    // O PedidoService cria sua própria dependência
    private Repositorio repositorio = new Repositorio(); 
}
```
Isso cria um **alto acoplamento**. O Spring inverte essa lógica através da **Inversão de Controle (IoC)**.

> **Definição 5.1 (Injeção de Dependência):** É o padrão de projeto onde as dependências de um objeto são fornecidas externamente, em vez de serem construídas pelo próprio objeto.

No Spring, a implementação desacoplada utiliza a injeção via construtor:

```java
// Abordagem Spring (Desacoplada)
@Service
public class PedidoService {
    private final Repositorio repositorio;

    // O Spring "injeta" a instância de Repositorio aqui automaticamente
    public PedidoService(Repositorio repositorio) {
        this.repositorio = repositorio;
    }
}

```

---

## 6. Construindo a Primeira API REST com Spring Boot

Vamos materializar esses conceitos criando uma API simples que gerencia "Tarefas".

### 6.1 Estrutura Básica

Um projeto Spring Boot inicia-se tipicamente com uma classe anotada com `@SpringBootApplication`.

* Esta anotação diz ao Spring: "Escaneie este pacote, encontre meus componentes e inicie o servidor".
* O servidor embutido (**Tomcat**) é configurado automaticamente para ouvir requisições na porta 8080.

### 6.2 O Controller

No padrão **MVC (Model-View-Controller)**, o **Controller** é o componente responsável por receber a requisição HTTP. Veja a implementação:

```java
package com.exemplo.api.controller;

import org.springframework.web.bind.annotation.*;
import java.util.List;
import java.util.ArrayList;

// 1. @RestController: Define que esta classe trata requisições Web 
// e o retorno dos métodos é serializado automaticamente no corpo da resposta (JSON).
@RestController
// 2. @RequestMapping: Define o "caminho base" da URL para este recurso.
@RequestMapping("/api/tarefas")
public class TarefaController {

    // Simulando um banco de dados em memória para fins didáticos
    private List<String> tarefas = new ArrayList<>();

    public TarefaController() {
        tarefas.add("Estudar Spring Boot");
        tarefas.add("Ler sobre REST");
    }

    // 3. @GetMapping: Mapeia requisições HTTP do tipo GET para este método.
    // URL de Acesso: GET /api/tarefas
    @GetMapping
    public List<String> listarTarefas() {
        // O Spring converterá automaticamente esta Lista Java para um Array JSON.
        return tarefas;
    }

    // 4. @PostMapping: Mapeia requisições HTTP do tipo POST.
    // @RequestBody: Captura o JSON do corpo da requisição e o converte em String.
    @PostMapping
    public void adicionarTarefa(@RequestBody String novaTarefa) {
        tarefas.add(novaTarefa);
    }
}

```

### 6.3 Análise do Fluxo de Execução

Ao realizar um `GET /api/tarefas`, o fluxo segue estas etapas:

1. **Chegada:** A requisição atinge o servidor embutido (**Tomcat**).
2. **Roteamento (DispatcherServlet):** O Spring analisa a URL e o verbo HTTP, encontrando o `TarefaController`.
3. **Execução:** O método `listarTarefas()` é invocado logicamente.
4. **Serialização:** O retorno `List<String>` é transformado em **JSON** pela biblioteca interna (**Jackson**).
5. **Resposta:** O JSON é enviado com o **Status Code 200 OK**.

---

## 7. Boas Práticas Iniciais

Hábitos de "higiene de código" essenciais para evitar **dívida técnica**:

### 7.1 Separação de Responsabilidades (Camadas)

No exemplo acima, a lista está dentro do Controller. Em cenários reais, utilizamos camadas distintas:

* **Controller:** Responsável apenas por receber a requisição e devolver a resposta (Interface).
* **Service Layer:** Onde reside a **Lógica de Negócio** e validações pesadas.
* **Repository Layer:** Responsável pela persistência e acesso a dados (**SQL/NoSQL**).

### 7.2 Semântica de URLs

As URLs devem representar **recursos** (substantivos) e não **ações** (verbos).

* ✅ **Correto:** `POST /api/tarefas` (Usa o verbo HTTP para definir a ação de criar).
* ❌ **Incorreto:** `POST /api/criarTarefa` (Expor o verbo na URL viola os princípios REST).

---

## 8. Conclusão

Neste capítulo, estabelecemos as fundações para o desenvolvimento de APIs Web:

* Partimos dos **Sistemas Distribuídos** e da necessidade de comunicação padronizada.
* Definimos **API** como o contrato fundamental e **REST** como o estilo arquitetural.
* Utilizamos o **Spring Boot** e a **Injeção de Dependência** para gerenciar a complexidade do código.

> **Insight:** A compreensão do *porquê* antes do *como* diferencia um "copiador de código" de um engenheiro de software capaz de projetar sistemas resilientes.

Nos próximos capítulos, abandonaremos a lista em memória para integrar um banco de dados real com **Spring Data JPA**.
