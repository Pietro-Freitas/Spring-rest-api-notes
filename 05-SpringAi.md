# 🚀 SPRING AI: DO ZERO AO PROFISSIONAL
## O Guia Definitivo para Desenvolvedores

### Por que este e-book é diferente?

Você está prestes a embarcar em uma jornada que transformará você de curioso sobre IA para um desenvolvedor capaz de criar aplicações inteligentes de nível empresarial usando Spring AI. Este não é mais um tutorial técnico seco - é um roteiro completo, testado em batalha, que combina teoria sólida com prática intensiva.

---

## 📑 SUMÁRIO NAVEGÁVEL

### 🌱 PARTE I: FUNDAMENTOS (Nível Iniciante)

#### [Capítulo 1: A Revolução da IA no Ecossistema Spring](#capítulo-1) ⏱️ 25 min
- 1.1 O que é Spring AI e por que você deveria se importar
- 1.2 A evolução: de JDBC a IA
- 1.3 Casos de uso reais que vão te inspirar
- 1.4 Arquitetura de alto nível

#### [Capítulo 2: Preparando Seu Arsenal de Desenvolvimento](#capítulo-2) ⏱️ 35 min
- 2.1 Checklist de pré-requisitos
- 2.2 Configuração do ambiente passo a passo
- 2.3 Seu primeiro projeto Spring AI
- 2.4 Troubleshooting de instalação

#### [Capítulo 3: Hello World Inteligente](#capítulo-3) ⏱️ 30 min
- 3.1 Anatomia de uma aplicação Spring AI
- 3.2 Seu primeiro chatbot em 15 minutos
- 3.3 Entendendo o que aconteceu nos bastidores
- 3.4 Expandindo o exemplo básico

#### Capítulo 4: Os Pilares Fundamentais ⏱️ 40 min
- 4.1 Models: O cérebro da operação
- 4.2 Prompts: A arte de fazer perguntas
- 4.3 Tokens: A moeda da IA
- 4.4 Responses: Interpretando as respostas

### 🌿 PARTE II: INTERMEDIÁRIO (Construindo Aplicações Reais)

#### Capítulo 5: Orquestrando Múltiplos LLMs ⏱️ 45 min
- 5.1 OpenAI: O padrão-ouro
- 5.2 Anthropic Claude: O rival criativo
- 5.3 Ollama: IA local e privada
- 5.4 Estratégias de fallback e load balancing

#### Capítulo 6: Vector Stores - A Memória da IA ⏱️ 50 min
- 6.1 Embeddings explicados com analogias
- 6.2 Escolhendo seu Vector Database
- 6.3 Implementação prática com PGVector
- 6.4 Busca semântica na prática

#### Capítulo 7: RAG - Turbinando IAs com Seus Dados ⏱️ 55 min
- 7.1 RAG desmistificado
- 7.2 Document Readers e preparação de dados
- 7.3 Implementando RAG completo
- 7.4 Otimizando relevância e precisão

#### Capítulo 8: Prompt Engineering Profissional ⏱️ 45 min
- 8.1 Anatomia de um prompt eficaz
- 8.2 Templates e parametrização
- 8.3 Técnicas avançadas (Few-shot, Chain-of-thought)
- 8.4 Biblioteca de prompts reutilizáveis

#### Capítulo 9: Streaming e Experiência do Usuário ⏱️ 40 min
- 9.1 Por que streaming é crucial
- 9.2 Implementação com Server-Sent Events
- 9.3 Gerenciamento de contexto e memória
- 9.4 UI responsiva com Spring AI

### 🌳 PARTE III: AVANÇADO (Nível Profissional)

#### Capítulo 10: Function Calling - IAs que Agem ⏱️ 60 min
- 10.1 O conceito de Tools e Functions
- 10.2 Criando ferramentas customizadas
- 10.3 Orquestração de múltiplas funções
- 10.4 Casos de uso empresariais

#### Capítulo 11: Fine-tuning e Customização ⏱️ 50 min
- 11.1 Quando fine-tuning faz sentido
- 11.2 Preparação de datasets
- 11.3 Processo de fine-tuning
- 11.4 Avaliação de modelos customizados

#### Capítulo 12: Performance, Custos e Escalabilidade ⏱️ 55 min
- 12.1 Monitoramento e observabilidade
- 12.2 Estratégias de cache inteligente
- 12.3 Otimização de custos de API
- 12.4 Escalando horizontalmente

#### Capítulo 13: Segurança e Produção ⏱️ 50 min
- 13.1 Proteção contra prompt injection
- 13.2 Gerenciamento seguro de API keys
- 13.3 Compliance e governança
- 13.4 Checklist de produção

### 🎯 PARTE IV: MAESTRIA (Projeto Final)

#### Capítulo 14: Projeto Completo - Sistema de Atendimento IA ⏱️ 90 min
- 14.1 Arquitetura do sistema
- 14.2 Implementação passo a passo
- 14.3 Deploy e monitoramento
- 14.4 Melhorias e próximos passos

#### Capítulo 15: Recursos e Comunidade ⏱️ 20 min
- 15.1 Documentação e referências
- 15.2 Comunidades e fóruns
- 15.3 Mantendo-se atualizado
- 15.4 Contribuindo para o ecossistema

### 📚 RECURSOS ADICIONAIS
- Glossário Completo
- Índice Remissivo
- Tabela de Comparação de LLMs
- Troubleshooting Guide
- Snippets de Código Reutilizáveis

---

## 🎓 COMO USAR ESTE E-BOOK

### Para Iniciantes Absolutos
👉 Siga sequencialmente do Capítulo 1 ao 9. Não pule etapas!

### Para Desenvolvedores Spring Experientes
👉 Leia rapidamente os Capítulos 1-3, foque de 4 em diante.

### Para Profissionais Buscando Especialização
👉 Use como referência, focando nos Capítulos 10-13.

### Projeto Unificador
Ao longo do e-book, construiremos **"DocBot"** - um assistente inteligente de documentação que evolui de um chatbot simples para um sistema completo com RAG, function calling e interface profissional.

---

<div style="page-break-after: always;"></div>

<a name="capítulo-1"></a>

# 📘 CAPÍTULO 1: A REVOLUÇÃO DA IA NO ECOSSISTEMA SPRING

⏱️ **Tempo estimado:** 25 minutos

## 🎯 O QUE VOCÊ VAI DOMINAR

Ao final deste capítulo, você será capaz de:

- ✅ Explicar o que é Spring AI e seu propósito no ecossistema Java
- ✅ Identificar casos de uso ideais para Spring AI
- ✅ Compreender a arquitetura de alto nível e componentes principais
- ✅ Situar Spring AI no contexto da evolução do Spring Framework
- ✅ Tomar decisões informadas sobre quando usar Spring AI

## 🧠 CONCEITO EM 30 SEGUNDOS

Spring AI é a ponte que conecta o robusto ecossistema Spring/Java com o mundo dos Large Language Models (LLMs).

**Pense assim:** se Spring Data facilitou drasticamente o trabalho com bancos de dados, Spring AI faz o mesmo com inteligência artificial - abstraindo complexidades, fornecendo padrões e permitindo que você foque na lógica de negócio.

---

<a name="1-1"></a>

## 📖 1.1 O QUE É SPRING AI E POR QUE VOCÊ DEVERIA SE IMPORTAR

### 🎨 A Analogia do Tradutor Universal

Imagine que você precisa conversar com pessoas de 20 países diferentes. Sem um tradutor, você precisaria:

1. Aprender 20 idiomas
2. Entender 20 culturas diferentes
3. Memorizar 20 conjuntos de regras de etiqueta

Um tradutor universal resolve isso, permitindo que você fale sua língua nativa enquanto ele cuida da comunicação.

**Spring AI é exatamente isso para o mundo da IA:**

```
Seu código Java limpo
        ↓
   [Spring AI] ← O tradutor universal
        ↓
OpenAI, Claude, Gemini, Ollama, etc.
```

### 🔬 Definição Técnica Formal

**Spring AI** é um framework de aplicação que fornece abstrações Spring idiomáticas e portáveis para desenvolver aplicações alimentadas por IA Generativa. Ele oferece:

- Abstrações de alto nível sobre modelos de IA (ChatClient, ImageClient, EmbeddingClient)
- Integrações prontas com principais provedores de LLM
- Componentes especializados para RAG, Vector Stores e Function Calling
- Padrões Spring familiares (Dependency Injection, Configuração, etc.)

### 💡 Por Que Isso Importa?

**Sem Spring AI:**

```java
// Código hipotético verboso e acoplado
OkHttpClient client = new OkHttpClient();
Request request = new Request.Builder()
    .url("https://api.openai.com/v1/chat/completions")
    .addHeader("Authorization", "Bearer " + API_KEY)
    .post(RequestBody.create(
        MediaType.parse("application/json"),
        "{\"model\":\"gpt-4\",\"messages\":[{\"role\":\"user\",\"content\":\"Olá\"}]}"
    ))
    .build();

Response response = client.newCall(request).execute();
String json = response.body().string();
// Agora parse manualmente o JSON, trate erros, retry, etc...
```

**Com Spring AI:**

```java
// Código limpo, testável e manutenível
@Service
public class ChatService {
    private final ChatClient chatClient;
    
    public ChatService(ChatClient chatClient) {
        this.chatClient = chatClient;
    }
    
    public String chat(String mensagem) {
        return chatClient.call(mensagem);
    }
}
```

### 📊 Benefícios Mensuráveis

| Aspecto | Sem Spring AI | Com Spring AI |
|---------|---------------|---------------|
| Linhas de código | ~200 linhas | ~20 linhas |
| Tempo de setup | 2-3 dias | 30 minutos |
| Trocar de LLM | Reescrever tudo | Mudar configuração |
| Testabilidade | Complexa | Simples (mocks prontos) |
| Manutenibilidade | Baixa | Alta |

---

<a name="1-2"></a>

## 🔄 1.2 A EVOLUÇÃO: DE JDBC A IA

### 🎭 História com Contexto

Para entender o valor do Spring AI, vamos fazer uma viagem no tempo:

#### 📅 Anos 2000: A Era do JDBC Puro

```java
// O pesadelo que era trabalhar com banco de dados
Connection conn = null;
PreparedStatement stmt = null;
ResultSet rs = null;
try {
    Class.forName("com.mysql.jdbc.Driver");
    conn = DriverManager.getConnection(DB_URL, USER, PASS);
    stmt = conn.prepareStatement("SELECT * FROM users WHERE id = ?");
    stmt.setInt(1, userId);
    rs = stmt.executeQuery();
    while(rs.next()) {
        // processar...
    }
} catch(SQLException e) {
    e.printStackTrace();
} finally {
    try { if(rs != null) rs.close(); } catch(Exception e) {}
    try { if(stmt != null) stmt.close(); } catch(Exception e) {}
    try { if(conn != null) conn.close(); } catch(Exception e) {}
}
```

#### 📅 Anos 2010: Spring Data Revoluciona

```java
// Mesma funcionalidade, código elegante
public interface UserRepository extends JpaRepository<User, Long> {
    Optional<User> findById(Long id);
}

// Uso:
User user = userRepository.findById(userId).orElseThrow();
```

#### 📅 Anos 2020: O Desafio da IA

Desenvolvedores enfrentaram os mesmos problemas com APIs de IA:
- Códigos boilerplate repetitivos
- Acoplamento forte com provedores
- Falta de padronização
- Dificuldade de testes

#### 📅 2023+: Spring AI ao Resgate

```java
// A mesma revolução, agora para IA
@Service
public class AssistenteIA {
    private final ChatClient chatClient;
    
    public String responder(String pergunta) {
        return chatClient.call(pergunta);
    }
}
```

### 📈 O Padrão Spring Aplicado à IA

| Conceito Spring Tradicional | Equivalente Spring AI |
|----------------------------|----------------------|
| JdbcTemplate | ChatClient |
| @Repository | @Component com AI Clients |
| DataSource | Model Configuration |
| JPA Entities | POJOs com AI annotations |
| Transactions | Conversational Memory |

---

<a name="1-3"></a>

## 💼 1.3 CASOS DE USO REAIS QUE VÃO TE INSPIRAR

### 🎯 Mapeamento: Problema → Solução Spring AI

#### 1. Atendimento ao Cliente Inteligente

**Problema Real:** Empresa recebe 10.000 tickets/dia, 70% são perguntas repetitivas.

**Solução Spring AI:**

```java
@Service
public class SupportBot {
    private final ChatClient chatClient;
    private final VectorStore knowledgeBase;
    
    public String responderTicket(String pergunta) {
        // Busca documentação relevante (RAG)
        List<Document> docs = knowledgeBase.similaritySearch(pergunta);
        
        // Gera resposta contextualizada
        String contexto = docs.stream()
            .map(Document::getContent)
            .collect(Collectors.joining("\n"));
        
        return chatClient.call(new Prompt(
            "Baseando-se nesta documentação: " + contexto + 
            "\n\nResponda: " + pergunta
        ));
    }
}
```

**Resultado:** 60% de redução no tempo de resposta.

#### 2. Análise de Sentimento em Tempo Real

**Problema Real:** Monitorar reputação de marca em redes sociais.

**Solução Spring AI:**

```java
@Service
public class SentimentAnalyzer {
    private final ChatClient chatClient;
    
    public Sentiment analisar(String texto) {
        String prompt = """
            Analise o sentimento do texto a seguir.
            Retorne apenas: POSITIVO, NEGATIVO ou NEUTRO
            
            Texto: %s
            """.formatted(texto);
        
        String resultado = chatClient.call(prompt);
        return Sentiment.valueOf(resultado.trim());
    }
}
```

#### 3. Geração de Relatórios Executivos

**Problema Real:** Executivos precisam de resumos de relatórios de 100+ páginas.

**Solução Spring AI:**

```java
@Service
public class ReportSummarizer {
    private final ChatClient chatClient;
    
    public String resumirRelatorio(String relatorioCompleto) {
        return chatClient.call(new Prompt(
            "Resuma este relatório em 3 parágrafos executivos, " +
            "destacando métricas principais e ações recomendadas:\n\n" +
            relatorioCompleto,
            OpenAiChatOptions.builder()
                .withModel("gpt-4")
                .withTemperature(0.3) // Baixa criatividade, alta precisão
                .build()
        ));
    }
}
```

#### 4. Assistente de Código (Code Review Automatizado)

**Problema Real:** Code reviews atrasam deploys.

**Solução Spring AI:**

```java
@Service
public class CodeReviewer {
    private final ChatClient chatClient;
    
    public List<Suggestion> revisar(String codigo) {
        String prompt = """
            Revise este código Java e retorne sugestões em JSON:
            
            %s
            
            Formato esperado:
            [
              {"linha": 10, "severidade": "ALTA", "mensagem": "..."},
              ...
            ]
            """.formatted(codigo);
        
        String json = chatClient.call(prompt);
        return parseToSuggestions(json);
    }
}
```

### 🏆 Casos de Uso Por Vertical

| Indústria | Aplicação Spring AI |
|-----------|---------------------|
| E-commerce | Recomendações personalizadas, chatbots de vendas |
| Financeiro | Análise de risco, detecção de fraudes, robo-advisors |
| Saúde | Triagem de sintomas, análise de exames (com disclaimers) |
| Educação | Tutores personalizados, correção automática |
| Jurídico | Análise de contratos, pesquisa de jurisprudência |
| RH | Triagem de currículos, onboarding inteligente |

---

<a name="1-4"></a>

## 🏗️ 1.4 ARQUITETURA DE ALTO NÍVEL

### 🎨 Visualização Conceitual

```
┌─────────────────────────────────────────────────────────┐
│                  SUA APLICAÇÃO SPRING                    │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐              │
│  │Controllers│  │ Services │  │Repositories│            │
│  └─────┬────┘  └─────┬────┘  └─────┬──────┘            │
│        │             │              │                    │
│        └─────────────┴──────────────┘                    │
│                      │                                    │
│  ════════════════════╪════════════════════════════════  │
│              SPRING AI LAYER                             │
│  ════════════════════╪════════════════════════════════  │
│                      │                                    │
│    ┌─────────────────┴─────────────────┐                │
│    │       AI Clients Abstraction      │                │
│    │  ┌──────────┐  ┌──────────────┐  │                │
│    │  │ChatClient│  │EmbeddingClient│  │                │
│    │  └──────────┘  └──────────────┘  │                │
│    └─────────────────┬─────────────────┘                │
│                      │                                    │
│    ┌─────────────────┴─────────────────┐                │
│    │    Model Provider Adapters        │                │
│    │  ┌────────┐ ┌─────────┐ ┌──────┐ │                │
│    │  │OpenAI  │ │Anthropic│ │Ollama│ │                │
│    │  └────────┘ └─────────┘ └──────┘ │                │
│    └───────────────────────────────────┘                │
└─────────────────────────────────────────────────────────┘
                      │
       ═══════════════╪═══════════════
              INTERNET / LOCAL
       ═══════════════╪═══════════════
                      │
        ┌─────────────┴─────────────┐
        │   LLM APIs / Local Models │
        │  GPT-4 | Claude | Llama   │
        └───────────────────────────┘
```

### 🧩 Componentes Principais Explicados

#### 1. ChatClient (O Coração)

**Analogia:** Pense no ChatClient como um garçom multilíngue em um restaurante internacional.

- Você faz o pedido na sua língua (código Java)
- Ele traduz para a "língua da cozinha" (API do LLM)
- Traz a resposta formatada para você

**Responsabilidades:**
- Gerenciar conversas
- Enviar prompts
- Receber e parsear respostas
- Lidar com erros e retries

#### 2. EmbeddingClient (O Bibliotecário)

**Analogia:** Um bibliotecário que organiza livros por similaridade de conteúdo, não por ordem alfabética.

- Transforma texto em vetores numéricos
- Permite busca semântica ("conceito similar" vs "palavra exata")

**Uso Típico:**

```java
List<Double> vetor = embeddingClient.embed("Spring Boot é incrível");
// Retorna: [0.234, -0.891, 0.456, ...] (1536 dimensões)
```

#### 3. VectorStore (A Memória de Longo Prazo)

**Analogia:** Um arquivo cerebral que lembra de tudo que você já disse e encontra informações relacionadas instantaneamente.

**Componentes:**
- **Armazenamento:** PostgreSQL com PGVector, ChromaDB, Pinecone
- **Busca:** Similaridade por distância coseno/euclidiana
- **Integração:** Alimenta sistemas RAG

#### 4. Document Readers (Os Tradutores de Formato)

**Analogia:** Conversores que transformam qualquer tipo de arquivo em texto compreensível.

**Suporta:**
- PDF, DOCX, TXT
- JSON, CSV
- Páginas web (HTML)
- Imagens (via OCR com integrações)

#### 5. OutputParsers (Os Organizadores)

**Analogia:** Assistentes que pegam resposta bagunçada da IA e organizam em estruturas Java.

**Exemplo:**

```java
// IA retorna: "Nome: João, Idade: 30, Cidade: São Paulo"
// OutputParser converte automaticamente para:
Pessoa pessoa = new Pessoa("João", 30, "São Paulo");
```

### 🔄 Fluxo de Dados Típico

```mermaid
graph LR
    A[Usuário faz pergunta] --> B[Controller recebe]
    B --> C[Service processa]
    C --> D{Precisa de contexto?}
    D -->|Sim| E[VectorStore busca docs relevantes]
    D -->|Não| F[ChatClient envia prompt]
    E --> F
    F --> G[LLM processa]
    G --> H[Resposta retorna]
    H --> I[OutputParser formata]
    I --> J[Controller retorna ao usuário]
```

---

## ⚠️ ARMADILHAS COMUNS

### ❌ Erro 1: Achar que Spring AI é um LLM

**Equívoco:**

```java
// Spring AI NÃO É um modelo de IA!
// É uma abstração sobre modelos existentes
```

**Realidade:**
- Spring AI = Framework
- GPT-4, Claude, etc. = Modelos
- Spring AI conecta você aos modelos

### ❌ Erro 2: Ignorar custos de API

**Problema:**

```java
// Isso pode custar CARO!
for(int i = 0; i < 10000; i++) {
    chatClient.call("Analise este texto: " + textos[i]);
}
```

**Solução:**
- Implemente cache
- Use batch processing
- Monitore gastos

### ❌ Erro 3: Não validar respostas da IA

**Problema:**

```java
String sql = chatClient.call("Gere um SQL para deletar usuários");
jdbcTemplate.execute(sql); // 🔥 PERIGO!
```

**Solução:**

```java
String sql = chatClient.call("Gere um SQL para deletar usuários");
if(SqlValidator.isSafe(sql) && sql.contains("WHERE")) {
    jdbcTemplate.execute(sql);
} else {
    throw new SecurityException("SQL não validado");
}
```

---

## 🚀 BOAS PRÁTICAS PROFISSIONAIS

### ✅ 1. Use Injeção de Dependência

```java
// ✅ BOM: Testável e desacoplado
@Service
public class MeuServico {
    private final ChatClient chatClient;
    
    @Autowired
    public MeuServico(ChatClient chatClient) {
        this.chatClient = chatClient;
    }
}

// ❌ RUIM: Acoplado e difícil de testar
@Service
public class MeuServico {
    private ChatClient chatClient = new OpenAiChatClient();
}
```

### ✅ 2. Centralize Configurações

```yaml
# application.yml
spring:
  ai:
    openai:
      api-key: ${OPENAI_API_KEY}
      model: gpt-4
      temperature: 0.7
```

```java
@Configuration
public class AiConfig {
    @Bean
    public ChatClient chatClient(
        @Value("${spring.ai.openai.api-key}") String apiKey) {
        // Configuração centralizada
    }
}
```

### ✅ 3. Implemente Observabilidade Desde o Início

```java
@Service
public class ChatService {
    private final ChatClient chatClient;
    private final MeterRegistry meterRegistry;
    
    public String chat(String mensagem) {
        Timer.Sample sample = Timer.start(meterRegistry);
        try {
            String resposta = chatClient.call(mensagem);
            meterRegistry.counter("ai.chat.success").increment();
            return resposta;
        } catch(Exception e) {
            meterRegistry.counter("ai.chat.error").increment();
            throw e;
        } finally {
            sample.stop(meterRegistry.timer("ai.chat.duration"));
        }
    }
}
```

---

## ✅ CHECKLIST DE DOMÍNIO

Marque conforme dominar cada conceito:

- [ ] Consigo explicar Spring AI para um desenvolvedor júnior
- [ ] Entendo a diferença entre Spring AI e os LLMs
- [ ] Sei identificar 3 casos de uso adequados para Spring AI
- [ ] Compreendo o papel de cada componente principal (ChatClient, VectorStore, etc.)
- [ ] Reconheço as armadilhas comuns e sei evitá-las
- [ ] Consigo justificar tecnicamente o uso de Spring AI em um projeto

---

## 🔗 CONECTANDO OS PONTOS

**O que vimos neste capítulo:**
- Fundação conceitual do Spring AI
- Contexto histórico e evolução
- Casos de uso práticos reais
- Arquitetura de alto nível

**O que vem a seguir (Capítulo 2):**
- Setup completo do ambiente
- Instalação passo a passo
- Primeiro projeto hands-on

**Como este capítulo se conecta ao projeto DocBot:**
Você agora entende por que vamos construir o DocBot e quais componentes usaremos. No próximo capítulo, prepararemos o ambiente para começar a codificação.

---

## 📝 RESUMO EM BULLETS

- Spring AI = Abstração sobre APIs de LLM, não um modelo próprio
- Benefício principal: Código limpo, testável e provider-agnostic
- Componentes-chave: ChatClient, EmbeddingClient, VectorStore, Document Readers
- Casos de uso: Chatbots, RAG, análise de sentimento, geração de conteúdo
- Armadilha crítica: Sempre validar respostas de IA antes de executar ações
- Próximo passo: Setup do ambiente de desenvolvimento

💡 **DICA PRO:** Salve este capítulo como referência. Volte a ele sempre que estiver decidindo se Spring AI é adequado para um novo projeto.

---

<div style="page-break-after: always;"></div>

<a name="capítulo-2"></a>

# 🛠️ CAPÍTULO 2: PREPARANDO SEU ARSENAL DE DESENVOLVIMENTO

⏱️ **Tempo estimado:** 35 minutos

## 🎯 O QUE VOCÊ VAI DOMINAR

Ao final deste capítulo, você será capaz de:

- ✅ Configurar um ambiente completo de desenvolvimento Spring AI do zero
- ✅ Criar e configurar seu primeiro projeto Spring AI usando Spring Initializr
- ✅ Gerenciar credenciais de API de forma segura
- ✅ Resolver os problemas mais comuns de instalação
- ✅ Validar que tudo está funcionando corretamente antes de codar

## 🧠 CONCEITO EM 30 SEGUNDOS

Preparar o ambiente de desenvolvimento é como montar uma cozinha profissional antes de cozinhar. Você precisa das ferramentas certas, ingredientes frescos (dependências) e tudo organizado. Fazer isso corretamente agora economizará horas de frustração depois.

---

<a name="2-1"></a>

## 📋 2.1 CHECKLIST DE PRÉ-REQUISITOS

### 🎨 Analogia do Kit de Ferramentas

Imagine que você vai construir uma casa. Antes de começar, você precisa:

- ✅ Ferramentas básicas (martelo, serrote)
- ✅ Materiais de construção (madeira, pregos)
- ✅ Planta do projeto
- ✅ Licenças necessárias

Da mesma forma, para Spring AI você precisa:

### 📦 1. Java Development Kit (JDK)

**Por que precisamos?**
Spring AI é construído em Java/Kotlin. É a fundação de tudo.

**Versão Recomendada:**

```
☑ JDK 17 ou superior (LTS recomendado)
☑ JDK 21 para recursos mais recentes
```

**Como verificar se você já tem:**

```bash
# No terminal/cmd
java -version
```

**Saída esperada:**

```
java version "17.0.8" 2023-07-18 LTS
Java(TM) SE Runtime Environment (build 17.0.8+9-LTS-211)
```

**Instalação (se necessário):**

**Windows:**

```bash
# Usando Chocolatey (gerenciador de pacotes)
choco install openjdk17

# OU baixe manualmente de:
# https://adoptium.net/
```

**macOS:**

```bash
# Usando Homebrew
brew install openjdk@17

# Adicione ao PATH (adicione ao ~/.zshrc ou ~/.bash_profile)
echo 'export PATH="/opt/homebrew/opt/openjdk@17/bin:$PATH"' >> ~/.zshrc
```

**Linux (Ubuntu/Debian):**

```bash
sudo apt update
sudo apt install openjdk-17-jdk
```

### 🔨 2. Maven ou Gradle

**Por que precisamos?**
Gerenciadores de dependências - trazem automaticamente todas as bibliotecas que Spring AI precisa.

**Versão Recomendada:**

```
☑ Maven 3.8+ OU Gradle 7.6+
```

**Como verificar:**

```bash
mvn -version
# OU
gradle -version
```

**Instalação:**

**Maven:**

```bash
# Windows (Chocolatey)
choco install maven

# macOS (Homebrew)
brew install maven

# Linux
sudo apt install maven
```

**Gradle:**

```bash
# Windows (Chocolatey)
choco install gradle

# macOS (Homebrew)
brew install gradle

# Linux
sudo apt install gradle
```

💡 **DICA PRO:** Se você usa uma IDE moderna (IntelliJ IDEA, Eclipse, VS Code com extensões), elas geralmente incluem Maven/Gradle embutidos. Você pode usar essas versões.

### 💻 3. IDE (Ambiente de Desenvolvimento)

**Opções Recomendadas:**

| IDE | Prós | Contras | Nível Recomendado |
|-----|------|---------|-------------------|
| IntelliJ IDEA | Melhor suporte Spring, refactoring poderoso | Pago (versão Ultimate) | Todos |
| VS Code | Leve, gratuito, extensível | Requer configuração manual | Intermediário+ |
| Eclipse | Gratuito, tradicional | Interface menos moderna | Iniciante |

**Setup Recomendado: IntelliJ IDEA Community (Gratuito)**

Download: https://www.jetbrains.com/idea/download/

**Plugins essenciais:**
- Spring Boot (geralmente já vem instalado)
- Lombok (para código mais limpo)
- Rainbow Brackets (facilita leitura de código)

**Instalar plugins:**

```
File → Settings → Plugins → Marketplace → Buscar e instalar
```

### 🔑 4. Credenciais de API do LLM

**Por que precisamos?**
Spring AI se conecta a serviços de IA. Você precisa de uma "chave de acesso" (como senha de WiFi).

#### Opções de Provedores:

#### Opção 1: OpenAI (Recomendado para iniciantes)

**Características:**
- ✅ Mais popular e documentado
- ✅ GPT-4 e GPT-3.5 disponíveis
- ⚠️ Pago (mas oferece créditos iniciais)

**Como obter:**

1. Acesse https://platform.openai.com/signup
2. Crie uma conta (com Google/email)
3. Vá para https://platform.openai.com/api-keys
4. Clique em "Create new secret key"
5. **COPIE A CHAVE AGORA** (ela só é mostrada uma vez!)
6. Formato da chave: `sk-proj-xxxxxxxxxxxxxxxxxxxxx`

**Preços (referência 2024):**
- GPT-3.5-turbo: ~$0.002 / 1K tokens
- GPT-4: ~$0.03 / 1K tokens
- Você recebe $5 de crédito inicial

#### Opção 2: Ollama (Totalmente gratuito e local)

**Características:**
- ✅ 100% gratuito
- ✅ Roda localmente (privacidade total)
- ✅ Sem limites de uso
- ⚠️ Requer GPU para performance decente
- ⚠️ Modelos menores (qualidade inferior ao GPT-4)

**Como obter:**

1. Baixe de https://ollama.ai/download
2. Instale (processo simples, next-next-finish)
3. Abra terminal e rode:

```bash
# Baixar modelo Llama 2 (7B)
ollama pull llama2

# Testar
ollama run llama2
>>> Olá, como você está?
```

💡 **DICA PRO:** Use Ollama para desenvolvimento/testes e OpenAI para produção.

#### Opção 3: Anthropic Claude (Alternativa premium)

**Como obter:**
1. Acesse https://console.anthropic.com/
2. Crie conta
3. Gere API key em Settings → API Keys

**Vantagem:** Melhor em tarefas de raciocínio complexo.

### 🌐 5. Conexão com Internet Estável

- Necessária para baixar dependências
- APIs de LLM requerem conexão (exceto Ollama)
- Testes iniciais consomem ~500MB de downloads

### 📊 Checklist Final de Pré-requisitos

Antes de prosseguir, confirme:

```
☐ JDK 17+ instalado e funcionando
☐ Maven/Gradle instalado
☐ IDE configurada com plugins Spring
☐ Pelo menos UMA chave de API de LLM (OpenAI ou outra)
☐ Conexão estável com internet
☐ Pelo menos 2GB de espaço em disco livre
```

---

<a name="2-2"></a>

## 🚀 2.2 CONFIGURAÇÃO DO AMBIENTE PASSO A PASSO

### 🎨 Analogia: Construindo as Fundações

Agora que temos as ferramentas, vamos construir a fundação da casa. Vamos criar um projeto Spring Boot configurado especificamente para IA.

### 📝 Método 1: Spring Initializr (Recomendado para Iniciantes)

#### Passo 1: Acessar o Initializr

Abra no navegador: **https://start.spring.io/**

#### Passo 2: Configuração do Projeto

Preencha exatamente assim (primeira vez):

```
Project: [●] Maven  [ ] Gradle
Language: [●] Java  [ ] Kotlin  [ ] Groovy
Spring Boot: 3.2.0 (ou mais recente estável)

Project Metadata:
├─ Group: com.seudominio
├─ Artifact: docbot-ai
├─ Name: DocBot AI
├─ Description: Sistema inteligente de documentação
├─ Package name: com.seudominio.docbot
└─ Packaging: [●] Jar  [ ] War
   Java: [●] 17  [ ] 21
```

#### Passo 3: Adicionar Dependências

Clique em **"ADD DEPENDENCIES"** e adicione:

```
1. Spring Web
   (Para criar APIs REST)

2. Spring AI OpenAI
   (Cliente OpenAI integrado)

3. Spring Boot DevTools
   (Reinicialização automática durante desenvolvimento)

4. Lombok (Opcional mas recomendado)
   (Reduz boilerplate de código)
```

**Como adicionar:**
1. Clique no botão "ADD DEPENDENCIES..."
2. Digite o nome (ex: "Spring Web")
3. Clique na dependência que aparece

#### Passo 4: Gerar o Projeto

1. Clique em **"GENERATE"** (botão verde inferior)
2. Um arquivo `docbot-ai.zip` será baixado
3. Extraia para uma pasta de projetos (ex: `C:\projetos\` ou `~/projetos/`)

### 💻 Método 2: Via IntelliJ IDEA (Alternativa)

#### Passo 1: Novo Projeto

```
File → New → Project
```

#### Passo 2: Configuração

```
Generators: [Spring Initializr]

Name: docbot-ai
Location: C:\projetos\docbot-ai
Language: Java
Type: Maven
Group: com.seudominio
Artifact: docbot-ai
JDK: 17

[Next]
```

#### Passo 3: Dependências

```
Spring Boot: 3.2.x

Dependencies:
☑ Web → Spring Web
☑ AI → OpenAI
☑ Developer Tools → Spring Boot DevTools
☑ Developer Tools → Lombok

[Create]
```

### 📂 Estrutura do Projeto Gerado

Após abrir o projeto na IDE, você verá:

```
docbot-ai/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/seudominio/docbot/
│   │   │       └── DocBotAiApplication.java  ← Classe principal
│   │   └── resources/
│   │       ├── application.properties  ← Configurações
│   │       └── static/                 ← Arquivos estáticos
│   └── test/
│       └── java/                       ← Testes
├── pom.xml                             ← Dependências Maven
└── README.md
```

### 🔧 Passo 4: Configurar Credenciais de API

#### Onde colocar API keys (NUNCA no código!)

Abra: `src/main/resources/application.properties`

Adicione:

```properties
# Configuração OpenAI
spring.ai.openai.api-key=${OPENAI_API_KEY}
spring.ai.openai.chat.options.model=gpt-3.5-turbo
spring.ai.openai.chat.options.temperature=0.7
```

**Explicação linha por linha:**

```properties
# ${OPENAI_API_KEY} - Busca a chave de uma variável de ambiente
# Isso é MUITO mais seguro do que escrever: spring.ai.openai.api-key=sk-xxxxx

# model=gpt-3.5-turbo - Modelo padrão (mais barato)
# Opções: gpt-3.5-turbo, gpt-4, gpt-4-turbo-preview

# temperature=0.7 - Controla "criatividade"
# 0.0 = Respostas determinísticas e objetivas
# 1.0 = Respostas criativas e variadas
# 0.7 = Equilíbrio (padrão recomendado)
```

### 🔐 Passo 5: Configurar Variável de Ambiente

⚡ **ATENÇÃO:** NUNCA commite chaves de API no Git!

#### Windows:

**Método 1: Temporário (sessão atual)**

```bash
# No CMD
set OPENAI_API_KEY=sk-sua-chave-aqui

# No PowerShell
$env:OPENAI_API_KEY="sk-sua-chave-aqui"
```

**Método 2: Permanente**

```
1. Botão direito em "Este Computador" → Propriedades
2. Configurações Avançadas do Sistema
3. Variáveis de Ambiente
4. Em "Variáveis do usuário", clique [Novo]
   Nome: OPENAI_API_KEY
   Valor: sk-sua-chave-aqui
5. [OK] → Reinicie a IDE
```

#### macOS/Linux:

Adicione ao arquivo de perfil:

```bash
# Abra o arquivo de perfil
nano ~/.zshrc   # macOS com zsh
# OU
nano ~/.bashrc  # Linux com bash

# Adicione no final:
export OPENAI_API_KEY="sk-sua-chave-aqui"

# Salve (Ctrl+O, Enter, Ctrl+X)

# Aplique as mudanças
source ~/.zshrc
# OU
source ~/.bashrc
```

**Verificar:**

```bash
echo $OPENAI_API_KEY
# Deve mostrar sua chave
```

#### IntelliJ IDEA: Configuração de Variáveis

Alternativa prática:

```
1. Run → Edit Configurations
2. Selecione sua aplicação
3. Environment Variables → [...]
4. Adicione:
   Name: OPENAI_API_KEY
   Value: sk-sua-chave-aqui
5. [OK]
```

💡 **VANTAGEM:** Chave fica apenas no projeto, não afeta sistema todo.

### ✅ Passo 6: Validar Configuração

#### Teste 1: Build do Projeto

```bash
# No terminal da IDE (View → Tool Windows → Terminal)
mvn clean install
```

**Saída esperada:**

```
[INFO] BUILD SUCCESS
[INFO] Total time: 15.234 s
```

❌ Se der erro: Veja seção Troubleshooting.

#### Teste 2: Executar Aplicação

**No IntelliJ:**

```
Clique direito em DocBotAiApplication.java → Run 'DocBotAiApplication'
```

**Na linha de comando:**

```bash
mvn spring-boot:run
```

**Saída esperada:**

```
  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::                (v3.2.0)

2024-01-15 10:30:45.123  INFO 12345 --- [main] c.s.d.DocBotAiApplication
: Starting DocBotAiApplication using Java 17
...
2024-01-15 10:30:50.456  INFO 12345 --- [main] o.s.b.w.embedded.tomcat.TomcatWebServer
: Tomcat started on port(s): 8080 (http)
2024-01-15 10:30:50.467  INFO 12345 --- [main] c.s.d.DocBotAiApplication
: Started DocBotAiApplication in 5.821 seconds
```

🎉 **Se você viu isso, SUCESSO!** Pressione Ctrl+C para parar.

---

<a name="2-3"></a>

## 💻 2.3 SEU PRIMEIRO PROJETO SPRING AI

### 🎯 Objetivo

Criar um endpoint REST simples que conversa com ChatGPT e validar que tudo está funcionando.

### 📝 Passo 1: Criar o Controller

**Crie o arquivo:**
`src/main/java/com/seudominio/docbot/controller/ChatController.java`

```java
package com.seudominio.docbot.controller;

import org.springframework.ai.chat.ChatClient;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

/**
 * Controller REST para interações com IA.
 * 
 * Este é nosso primeiro contato com Spring AI!
 * Vamos criar um endpoint simples que recebe uma pergunta
 * e retorna uma resposta do ChatGPT.
 */
@RestController  // Marca esta classe como um controller REST
public class ChatController {

    // ChatClient é injetado automaticamente pelo Spring
    // Ele já vem configurado com as credenciais do application.properties
    private final ChatClient chatClient;

    // Injeção de dependência via construtor (padrão recomendado)
    public ChatController(ChatClient chatClient) {
        this.chatClient = chatClient;
    }

    /**
     * Endpoint GET /chat
     * 
     * Exemplo de uso:
     * http://localhost:8080/chat?mensagem=Olá, como você está?
     * 
     * @param mensagem A pergunta do usuário
     * @return Resposta do ChatGPT
     */
    @GetMapping("/chat")
    public String chat(@RequestParam String mensagem) {
        // Aqui acontece a mágica!
        // chatClient.call() envia a mensagem para o ChatGPT
        // e retorna a resposta como String
        return chatClient.call(mensagem);
    }
}
```

### 🔧 Passo 2: Executar a Aplicação

```bash
mvn spring-boot:run
```

Aguarde até ver:

```
Tomcat started on port(s): 8080 (http)
```

### 🧪 Passo 3: Testar o Endpoint

#### Método 1: Navegador

Abra no navegador:

```
http://localhost:8080/chat?mensagem=Olá, como você está?
```

**Resposta esperada:**

```
Olá! Estou funcionando perfeitamente, obrigado por perguntar. 
Como posso ajudá-lo hoje?
```

#### Método 2: curl (Terminal)

```bash
curl "http://localhost:8080/chat?mensagem=Explique Spring Boot em uma frase"
```

**Resposta esperada:**

```
Spring Boot é um framework Java que simplifica drasticamente 
a criação de aplicações robustas com configuração mínima.
```

#### Método 3: Postman/Insomnia

```
GET http://localhost:8080/chat
Query Params:
  mensagem: Qual é a capital do Brasil?
```

### 🎉 Se Funcionou: PARABÉNS!

Você acabou de:
- ✅ Configurar um projeto Spring AI completo
- ✅ Integrar com ChatGPT
- ✅ Criar e testar seu primeiro endpoint de IA

### 🔍 O Que Aconteceu nos Bastidores?

Vamos dissecar o fluxo:

```
1. Navegador envia: GET /chat?mensagem=Olá

2. Spring recebe e roteia para ChatController.chat()

3. chatClient.call("Olá") executa:
   ├─ Monta requisição HTTP para https://api.openai.com/v1/chat/completions
   ├─ Inclui header Authorization com sua API key
   ├─ Envia JSON:
   │  {
   │    "model": "gpt-3.5-turbo",
   │    "messages": [{"role": "user", "content": "Olá"}],
   │    "temperature": 0.7
   │  }
   └─ Aguarda resposta

4. OpenAI processa e retorna JSON:
   {
     "choices": [
       {"message": {"content": "Olá! Como posso ajudar?"}}
     ]
   }

5. chatClient extrai o texto da resposta

6. Spring retorna ao navegador
```

### 🧩 Melhorando o Código: Versão com Tratamento de Erros

```java
package com.seudominio.docbot.controller;

import org.springframework.ai.chat.ChatClient;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.*;

@RestController
@RequestMapping("/api/chat")  // Prefixo /api para organização
public class ChatController {

    private final ChatClient chatClient;

    public ChatController(ChatClient chatClient) {
        this.chatClient = chatClient;
    }

    /**
     * Versão melhorada com tratamento de erros
     */
    @GetMapping
    public ResponseEntity<String> chat(
            @RequestParam(required = true) String mensagem) {
        
        try {
            // Validação básica
            if (mensagem == null || mensagem.trim().isEmpty()) {
                return ResponseEntity
                    .badRequest()
                    .body("Mensagem não pode ser vazia");
            }

            // Limitação de tamanho (evitar custos excessivos)
            if (mensagem.length() > 500) {
                return ResponseEntity
                    .badRequest()
                    .body("Mensagem muito longa (máximo 500 caracteres)");
            }

            // Chamada à IA
            String resposta = chatClient.call(mensagem);

            return ResponseEntity.ok(resposta);

        } catch (Exception e) {
            // Log do erro (em produção, use um logger apropriado)
            System.err.println("Erro ao processar mensagem: " + e.getMessage());

            return ResponseEntity
                .status(HttpStatus.INTERNAL_SERVER_ERROR)
                .body("Erro ao processar sua mensagem. Tente novamente.");
        }
    }
}
```

**Teste os cenários:**

```bash
# Sucesso
curl "http://localhost:8080/api/chat?mensagem=Teste"

# Erro: mensagem vazia
curl "http://localhost:8080/api/chat?mensagem="

# Erro: mensagem muito longa
curl "http://localhost:8080/api/chat?mensagem=$(python3 -c 'print("A"*501)')"
```

---

<a name="2-4"></a>

## 🔧 2.4 TROUBLESHOOTING DE INSTALAÇÃO

### 🎨 Analogia do Técnico de TI

Pense nesta seção como um manual de primeiros socorros. Problemas acontecem, mas a maioria tem solução rápida.

### ❌ Problema 1: "ChatClient could not be found"

**Erro completo:**

```
Field chatClient in ChatController required a bean of type 
'org.springframework.ai.chat.ChatClient' that could not be found.
```

**Causa:** Dependência Spring AI não foi incluída corretamente.

**Solução:**

1. Abra `pom.xml`
2. Verifique se existe:

```xml
<dependency>
    <groupId>org.springframework.ai</groupId>
    <artifactId>spring-ai-openai-spring-boot-starter</artifactId>
</dependency>
```

3. Se não existir, adicione dentro de `<dependencies>`
4. Clique direito no projeto → Maven → Reload Project
5. Rebuilde: `mvn clean install`

### ❌ Problema 2: "Invalid API Key"

**Erro:**

```
401 Unauthorized: {"error": {"message": "Incorrect API key provided"}}
```

**Causas possíveis:**

1. **API key incorreta**
   - Copie novamente de https://platform.openai.com/api-keys
   - Verifique se não há espaços extras

2. **Variável de ambiente não carregada**

```bash
# Teste:
echo $OPENAI_API_KEY

# Se não mostrar nada, a variável não está configurada
```

3. **IDE não reiniciada após configurar variável**
   - Feche completamente a IDE
   - Reabra
   - Execute novamente

**Solução temporária para debug:**

```properties
# application.properties (APENAS PARA TESTES LOCAIS!)
spring.ai.openai.api-key=sk-sua-chave-aqui
```

⚡ **ATENÇÃO:** Remova isso antes de commitar!

### ❌ Problema 3: Porta 8080 já está em uso

**Erro:**

```
Web server failed to start. Port 8080 was already in use.
```

**Solução 1: Mudar porta**

```properties
# application.properties
server.port=8081
```

**Solução 2: Matar processo na porta 8080**

```bash
# Windows
netstat -ano | findstr :8080
taskkill /PID <número_do_pid> /F

# macOS/Linux
lsof -ti:8080 | xargs kill -9
```

### ❌ Problema 4: Timeout ao chamar API

**Erro:**

```
SocketTimeoutException: Read timed out
```

**Causa:** Conexão lenta ou firewall bloqueando.

**Solução:**

```properties
# application.properties
spring.ai.openai.chat.options.timeout=60s
```

**Testar conectividade:**

```bash
curl https://api.openai.com/v1/models \
  -H "Authorization: Bearer $OPENAI_API_KEY"
```

### ❌ Problema 5: Dependências não baixam

**Erro:**

```
Failed to read artifact descriptor for org.springframework.ai:...
```

**Solução:**

1. Limpar cache Maven:

```bash
mvn dependency:purge-local-repository
```

2. Forçar atualização:

```bash
mvn clean install -U
```

3. Verificar settings.xml do Maven:

```xml
<!-- ~/.m2/settings.xml -->
<settings>
  <mirrors>
    <mirror>
      <id>central</id>
      <url>https://repo.maven.apache.org/maven2</url>
      <mirrorOf>central</mirrorOf>
    </mirror>
  </mirrors>
</settings>
```

### ❌ Problema 6: Lombok não funciona

**Sintoma:** Erros em @Data, @Getter, etc.

**Solução IntelliJ:**

```
1. File → Settings → Plugins
2. Instale "Lombok"
3. File → Settings → Build, Execution, Deployment → Compiler → Annotation Processors
4. Marque "Enable annotation processing"
5. Restart IDE
```

### 🆘 Checklist de Troubleshooting Geral

Quando algo não funcionar, siga esta ordem:

```
1. ☐ Verificar logs completos (não apenas última linha)
2. ☐ Tentar mvn clean install
3. ☐ Verificar variáveis de ambiente (echo $NOME_VAR)
4. ☐ Reiniciar IDE completamente
5. ☐ Verificar internet (ping google.com)
6. ☐ Testar com curl diretamente a API
7. ☐ Verificar versões (java -version, mvn -version)
8. ☐ Procurar erro exato no Google/Stack Overflow
9. ☐ Perguntar na comunidade (links no Cap. 15)
```

---

## ⚠️ ARMADILHAS COMUNS

### ❌ 1. Commitar API Keys no Git

**Problema:**

```bash
git add .
git commit -m "Projeto funcionando"
# 🔥 Sua chave agora está pública no GitHub!
```

**Solução:**

Crie `.gitignore`:

```
# Application properties com secrets
application-*.properties
.env

# IDE
.idea/
*.iml

# Build
target/
```

**Se já commitou:**

```bash
# URGENTE: Invalide a chave em https://platform.openai.com/api-keys
# Depois:
git filter-branch --force --index-filter \
  "git rm --cached --ignore-unmatch application.properties" \
  --prune-empty --tag-name-filter cat -- --all
```

### ❌ 2. Não limitar tamanho de prompts

**Problema:**

```java
// Usuário malicioso pode enviar 100MB de texto
chatClient.call(request.getMensagem());
```

**Solução:**

```java
if (mensagem.length() > 1000) {
    throw new IllegalArgumentException("Mensagem muito longa");
}
```

### ❌ 3. Ignorar custos

**Problema:** Não monitorar gastos com API.

**Solução:**

```java
@Service
public class CostTracker {
    private AtomicInteger requestCount = new AtomicInteger(0);
    
    public void trackRequest() {
        int count = requestCount.incrementAndGet();
        if (count > 100) { // Limite diário
            throw new RuntimeException("Limite diário atingido");
        }
    }
}
```

---

## 🚀 BOAS PRÁTICAS PROFISSIONAIS

### ✅ 1. Profiles do Spring

Separe configurações por ambiente:

**application.properties (base):**

```properties
spring.application.name=docbot-ai
```

**application-dev.properties (desenvolvimento):**

```properties
spring.ai.openai.chat.options.model=gpt-3.5-turbo
logging.level.org.springframework.ai=DEBUG
```

**application-prod.properties (produção):**

```properties
spring.ai.openai.chat.options.model=gpt-4
logging.level.org.springframework.ai=INFO
```

**Ativar:**

```bash
# Dev
java -jar app.jar --spring.profiles.active=dev

# Prod
java -jar app.jar --spring.profiles.active=prod
```

### ✅ 2. Health Checks

**Adicione dependência:**

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

**Configure:**

```properties
management.endpoints.web.exposure.include=health,info
management.endpoint.health.show-details=always
```

**Teste:**

```bash
curl http://localhost:8080/actuator/health
```

### ✅ 3. Logging Estruturado

```java
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

@RestController
public class ChatController {
    private static final Logger log = LoggerFactory.getLogger(ChatController.class);
    
    @GetMapping("/chat")
    public String chat(@RequestParam String mensagem) {
        log.info("Recebida mensagem: {} (tamanho: {})", 
                 mensagem.substring(0, Math.min(50, mensagem.length())),
                 mensagem.length());
        
        try {
            String resposta = chatClient.call(mensagem);
            log.info("Resposta gerada com sucesso (tamanho: {})", resposta.length());
            return resposta;
        } catch (Exception e) {
            log.error("Erro ao processar mensagem", e);
            throw e;
        }
    }
}
```

---

## ✅ CHECKLIST DE DOMÍNIO

- [ ] Instalei e validei JDK 17+
- [ ] Configurei Maven/Gradle funcionando
- [ ] IDE está rodando com plugins Spring
- [ ] Obtive e configurei API key do OpenAI (ou Ollama)
- [ ] Criei projeto Spring AI via Initializr
- [ ] Configurei variáveis de ambiente de forma segura
- [ ] Executei aplicação sem erros
- [ ] Testei endpoint /chat com sucesso
- [ ] Entendo o fluxo completo de uma requisição
- [ ] Sei resolver os 5 problemas mais comuns

---

## 🔗 CONECTANDO OS PONTOS

**O que vimos:**
- Setup completo do ambiente
- Primeiro código funcional
- Troubleshooting essencial

**O que vem a seguir (Capítulo 3):**
- Anatomia detalhada de uma aplicação Spring AI
- Expandir o chatbot básico
- Adicionar contexto e memória

**Projeto DocBot:**
Agora temos a fundação do DocBot. No próximo capítulo, vamos transformá-lo em um chatbot mais inteligente, capaz de lembrar conversas.

---

## 📝 RESUMO EM BULLETS

- Pré-requisitos: JDK 17+, Maven/Gradle, IDE, API key de LLM
- Setup: Spring Initializr com dependência `spring-ai-openai-spring-boot-starter`
- Segurança: SEMPRE usar variáveis de ambiente para API keys
- Primeiro código: Controller com ChatClient injetado
- Testes: curl, navegador ou Postman
- Troubleshooting: 90% dos problemas são API key ou dependências
- Próximo nível: Expandir funcionalidades do chatbot

💡 **DICA PRO:** Salve este capítulo como referência para configurar futuros projetos. Você vai reusar esses passos várias vezes.

---

<div style="page-break-after: always;"></div>

<a name="capítulo-3"></a>

# 🤖 CAPÍTULO 3: HELLO WORLD INTELIGENTE

⏱️ **Tempo estimado:** 30 minutos

## 🎯 O QUE VOCÊ VAI DOMINAR

Ao final deste capítulo, você será capaz de:

- ✅ Compreender a anatomia completa de uma aplicação Spring AI
- ✅ Implementar diferentes tipos de interações com LLMs
- ✅ Personalizar respostas usando parâmetros avançados
- ✅ Criar um chatbot com memória de conversação
- ✅ Estruturar código seguindo melhores práticas profissionais

## 🧠 CONCEITO EM 30 SEGUNDOS

Se o Capítulo 2 foi montar a cozinha, este é aprender as técnicas de cozinha fundamentais. Vamos pegar o código básico e transformá-lo em algo profissional, explorando todos os ingredientes (componentes) que o Spring AI oferece.

---

<a name="3-1"></a>

## 🏗️ 3.1 ANATOMIA DE UMA APLICAÇÃO SPRING AI

### 🎨 Analogia: O Restaurante Completo

Pense em uma aplicação Spring AI como um restaurante:

```
┌─────────────────────────────────────────┐
│         🍽️  RESTAURANTE SPRING AI        │
├─────────────────────────────────────────┤
│                                          │
│  👨‍💼 Garçom (Controller)                  │
│     ↓ "Cliente pediu X"                  │
│                                          │
│  👨‍🍳 Chef (Service Layer)                 │
│     ↓ "Vou preparar usando IA"           │
│                                          │
│  🔪 Ferramentas (ChatClient, Prompts)    │
│     ↓ "Ingredientes processados"         │
│                                          │
│  📦 Despensa (Configuration, Models)     │
│     "Configurações e recursos"           │
│                                          │
│  🌐 Fornecedor (OpenAI API)              │
│     "Matéria-prima (respostas)"          │
└─────────────────────────────────────────┘
```

### 📐 Arquitetura em Camadas

**Estrutura Profissional Completa:**

```
src/main/java/com/seudominio/docbot/
│
├── 📁 controller/          ← Camada de apresentação (REST endpoints)
│   └── ChatController.java
│
├── 📁 service/             ← Lógica de negócio
│   ├── ChatService.java
│   └── PromptService.java
│
├── 📁 config/              ← Configurações do Spring AI
│   └── AiConfig.java
│
├── 📁 model/               ← DTOs e entidades
│   ├── ChatRequest.java
│   └── ChatResponse.java
│
└── 📁 exception/           ← Tratamento de erros
    └── AiExceptionHandler.java
```

### 🔍 Componente por Componente

#### 1. Controller - A Interface com o Mundo

```java
package com.seudominio.docbot.controller;

import com.seudominio.docbot.model.ChatRequest;
import com.seudominio.docbot.model.ChatResponse;
import com.seudominio.docbot.service.ChatService;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.*;

/**
 * RESPONSABILIDADE: Receber requisições HTTP e delegar ao Service.
 * 
 * ❌ NÃO DEVE: Conter lógica de negócio
 * ✅ DEVE: Validar entrada, chamar service, retornar resposta
 */
@RestController
@RequestMapping("/api/v1/chat")  // Versionamento de API (boa prática)
public class ChatController {

    private final ChatService chatService;

    // Injeção por construtor (preferível a @Autowired em campo)
    public ChatController(ChatService chatService) {
        this.chatService = chatService;
    }

    /**
     * Endpoint para chat simples.
     * 
     * POST /api/v1/chat
     * Body: { "message": "Olá" }
     * Response: { "response": "Olá! Como posso ajudar?" }
     */
    @PostMapping
    public ResponseEntity<ChatResponse> chat(@RequestBody ChatRequest request) {
        // Controller apenas delega - não processa
        ChatResponse response = chatService.processMessage(request);
        return ResponseEntity.ok(response);
    }
}
```

#### 2. Service - O Cérebro da Operação

```java
package com.seudominio.docbot.service;

import com.seudominio.docbot.model.ChatRequest;
import com.seudominio.docbot.model.ChatResponse;
import org.springframework.ai.chat.ChatClient;
import org.springframework.ai.chat.messages.Message;
import org.springframework.ai.chat.messages.UserMessage;
import org.springframework.ai.chat.prompt.Prompt;
import org.springframework.stereotype.Service;

import java.util.List;

/**
 * RESPONSABILIDADE: Conter a lógica de negócio.
 * 
 * ✅ DEVE: Orquestrar chamadas à IA, aplicar regras, processar dados
 */
@Service
public class ChatService {

    private final ChatClient chatClient;

    public ChatService(ChatClient chatClient) {
        this.chatClient = chatClient;
    }

    /**
     * Processa uma mensagem do usuário.
     * 
     * @param request Objeto com a mensagem do usuário
     * @return Resposta estruturada da IA
     */
    public ChatResponse processMessage(ChatRequest request) {
        // 1. Validação (pode lançar exceção que será tratada globalmente)
        validateRequest(request);

        // 2. Preparar mensagem para a IA
        Message userMessage = new UserMessage(request.getMessage());
        Prompt prompt = new Prompt(List.of(userMessage));

        // 3. Chamar IA
        String aiResponse = chatClient.call(prompt).getResult().getOutput().getContent();

        // 4. Construir resposta estruturada
        return new ChatResponse(aiResponse, estimateTokens(aiResponse));
    }

    private void validateRequest(ChatRequest request) {
        if (request.getMessage() == null || request.getMessage().isBlank()) {
            throw new IllegalArgumentException("Mensagem não pode ser vazia");
        }
        
        if (request.getMessage().length() > 2000) {
            throw new IllegalArgumentException("Mensagem muito longa (máx: 2000)");
        }
    }

    private int estimateTokens(String text) {
        // Estimativa grosseira: 1 token ≈ 4 caracteres em inglês
        return text.length() / 4;
    }
}
```

#### 3. Model - Estruturas de Dados

```java
package com.seudominio.docbot.model;

import com.fasterxml.jackson.annotation.JsonProperty;

/**
 * DTO para requisição de chat.
 * 
 * Exemplo JSON:
 * {
 *   "message": "Explique Spring AI",
 *   "context": "Sou iniciante em Java"
 * }
 */
public class ChatRequest {
    
    @JsonProperty("message")  // Mapeia campo JSON para atributo Java
    private String message;
    
    @JsonProperty("context")
    private String context;  // Contexto opcional

    // Construtores
    public ChatRequest() {}
    
    public ChatRequest(String message) {
        this.message = message;
    }

    // Getters e Setters (ou use Lombok @Data)
    public String getMessage() {
        return message;
    }

    public void setMessage(String message) {
        this.message = message;
    }

    public String getContext() {
        return context;
    }

    public void setContext(String context) {
        this.context = context;
    }
}
```

```java
package com.seudominio.docbot.model;

import com.fasterxml.jackson.annotation.JsonProperty;
import java.time.LocalDateTime;

/**
 * DTO para resposta de chat.
 * 
 * Exemplo JSON:
 * {
 *   "response": "Spring AI é...",
 *   "tokens_used": 150,
 *   "timestamp": "2024-01-15T10:30:00"
 * }
 */
public class ChatResponse {
    
    @JsonProperty("response")
    private String response;
    
    @JsonProperty("tokens_used")
    private int tokensUsed;
    
    @JsonProperty("timestamp")
    private LocalDateTime timestamp;

    // Construtor
    public ChatResponse(String response, int tokensUsed) {
        this.response = response;
        this.tokensUsed = tokensUsed;
        this.timestamp = LocalDateTime.now();
    }

    // Getters (setters opcionais para objetos de resposta)
    public String getResponse() {
        return response;
    }

    public int getTokensUsed() {
        return tokensUsed;
    }

    public LocalDateTime getTimestamp() {
        return timestamp;
    }
}
```

#### 4. Configuration - Customizações

```java
package com.seudominio.docbot.config;

import org.springframework.ai.chat.ChatClient;
import org.springframework.ai.openai.OpenAiChatClient;
import org.springframework.ai.openai.OpenAiChatOptions;
import org.springframework.ai.openai.api.OpenAiApi;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

/**
 * RESPONSABILIDADE: Configurar beans customizados do Spring AI.
 * 
 * Aqui você pode:
 * - Criar clientes customizados
 * - Definir configurações padrão
 * - Injetar valores de properties
 */
@Configuration
public class AiConfig {

    @Value("${spring.ai.openai.api-key}")
    private String apiKey;

    /**
     * Bean customizado de ChatClient com configurações específicas.
     * 
     * Este bean sobrescreve o autoconfiguration padrão do Spring AI.
     */
    @Bean
    public ChatClient chatClient() {
        // Cria API client da OpenAI
        OpenAiApi openAiApi = new OpenAiApi(apiKey);

        // Configurações customizadas
        OpenAiChatOptions options = OpenAiChatOptions.builder()
            .withModel("gpt-3.5-turbo")      // Modelo a usar
            .withTemperature(0.7)             // Criatividade (0-1)
            .withMaxTokens(500)               // Limite de tokens por resposta
            .withTopP(1.0)                    // Nucleus sampling
            .withFrequencyPenalty(0.0)        // Penalidade por repetição
            .withPresencePenalty(0.0)         // Penalidade por presença
            .build();

        // Retorna cliente configurado
        return new OpenAiChatClient(openAiApi, options);
    }
}
```

**Explicação dos Parâmetros:**

| Parâmetro | Range | Efeito | Quando Usar |
|-----------|-------|--------|-------------|
| temperature | 0.0 - 2.0 | Controla aleatoriedade | 0.3 para fatos, 0.9 para criatividade |
| max_tokens | 1 - 4096 | Limite de tamanho da resposta | Controlar custos e tamanho |
| top_p | 0.0 - 1.0 | Nucleus sampling | Geralmente 1.0 (deixe temperature controlar) |
| frequency_penalty | -2.0 - 2.0 | Reduz repetições | 0.5 para evitar texto repetitivo |
| presence_penalty | -2.0 - 2.0 | Incentiva novos tópicos | 0.5 para respostas mais diversas |

#### 5. Exception Handler - Tratamento Global de Erros

```java
package com.seudominio.docbot.exception;

import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.ExceptionHandler;
import org.springframework.web.bind.annotation.RestControllerAdvice;

import java.time.LocalDateTime;
import java.util.HashMap;
import java.util.Map;

/**
 * RESPONSABILIDADE: Capturar exceções globalmente e retornar respostas HTTP apropriadas.
 * 
 * ✅ Centraliza tratamento de erros
 * ✅ Retorna mensagens user-friendly
 * ✅ Log de erros para debugging
 */
@RestControllerAdvice  // Aplica a todos os @RestController
public class AiExceptionHandler {

    /**
     * Trata erros de validação (400 Bad Request).
     */
    @ExceptionHandler(IllegalArgumentException.class)
    public ResponseEntity<Map<String, Object>> handleValidationError(
            IllegalArgumentException ex) {
        
        Map<String, Object> errorResponse = new HashMap<>();
        errorResponse.put("timestamp", LocalDateTime.now());
        errorResponse.put("status", HttpStatus.BAD_REQUEST.value());
        errorResponse.put("error", "Validation Error");
        errorResponse.put("message", ex.getMessage());

        return ResponseEntity
            .status(HttpStatus.BAD_REQUEST)
            .body(errorResponse);
    }

    /**
     * Trata erros internos do servidor (500 Internal Server Error).
     */
    @ExceptionHandler(Exception.class)
    public ResponseEntity<Map<String, Object>> handleGenericError(Exception ex) {
        
        // Log do erro (em produção, use Logger apropriado)
        System.err.println("Erro não tratado: " + ex.getMessage());
        ex.printStackTrace();

        Map<String, Object> errorResponse = new HashMap<>();
        errorResponse.put("timestamp", LocalDateTime.now());
        errorResponse.put("status", HttpStatus.INTERNAL_SERVER_ERROR.value());
        errorResponse.put("error", "Internal Server Error");
        errorResponse.put("message", "Ocorreu um erro ao processar sua solicitação");

        return ResponseEntity
            .status(HttpStatus.INTERNAL_SERVER_ERROR)
            .body(errorResponse);
    }
}
```
# 🤖 CAPÍTULO 3: HELLO WORLD INTELIGENTE (Continuação)

---

<a name="3-2"></a>

## 💻 3.2 SEU PRIMEIRO CHATBOT EM 15 MINUTOS

### 🎯 Objetivo Deste Módulo

Construir um chatbot funcional com interface REST que:
- Aceita mensagens do usuário
- Retorna respostas contextualizadas
- Registra histórico de conversação
- Possui tratamento robusto de erros

### 🎨 Analogia: Montando um LEGO Complexo

Se o capítulo anterior foi construir peças individuais de LEGO, agora vamos montá-las em uma estrutura funcional. Cada peça tem seu lugar exato.

### 📝 Passo 1: Criar o Modelo de Conversação

**Arquivo:** `src/main/java/com/seudominio/docbot/model/Conversation.java`

```java
package com.seudominio.docbot.model;

import java.time.LocalDateTime;
import java.util.ArrayList;
import java.util.List;
import java.util.UUID;

/**
 * Representa uma conversação completa com histórico de mensagens.
 * 
 * Uma conversação é como uma "sessão de chat" - mantém o contexto
 * de todas as mensagens trocadas entre usuário e IA.
 */
public class Conversation {
    
    private final String id;  // ID único da conversação
    private final LocalDateTime startedAt;
    private final List<MessagePair> messages;  // Histórico completo
    
    /**
     * Construtor - inicializa nova conversação
     */
    public Conversation() {
        this.id = UUID.randomUUID().toString();
        this.startedAt = LocalDateTime.now();
        this.messages = new ArrayList<>();
    }
    
    /**
     * Adiciona um par de mensagens (usuário + IA) ao histórico.
     * 
     * @param userMessage Mensagem enviada pelo usuário
     * @param aiResponse Resposta gerada pela IA
     */
    public void addMessage(String userMessage, String aiResponse) {
        MessagePair pair = new MessagePair(
            userMessage, 
            aiResponse, 
            LocalDateTime.now()
        );
        this.messages.add(pair);
    }
    
    /**
     * Retorna todo o histórico formatado como contexto para a IA.
     * 
     * Formato:
     * Usuário: Olá
     * Assistente: Olá! Como posso ajudar?
     * Usuário: Qual é a capital do Brasil?
     * Assistente: A capital do Brasil é Brasília.
     */
    public String getContextHistory() {
        StringBuilder context = new StringBuilder();
        for (MessagePair pair : messages) {
            context.append("Usuário: ").append(pair.getUserMessage()).append("\n");
            context.append("Assistente: ").append(pair.getAiResponse()).append("\n");
        }
        return context.toString();
    }
    
    // Getters
    public String getId() {
        return id;
    }
    
    public LocalDateTime getStartedAt() {
        return startedAt;
    }
    
    public List<MessagePair> getMessages() {
        return new ArrayList<>(messages);  // Retorna cópia para imutabilidade
    }
    
    public int getMessageCount() {
        return messages.size();
    }
    
    /**
     * Classe interna para representar um par mensagem-resposta.
     */
    public static class MessagePair {
        private final String userMessage;
        private final String aiResponse;
        private final LocalDateTime timestamp;
        
        public MessagePair(String userMessage, String aiResponse, LocalDateTime timestamp) {
            this.userMessage = userMessage;
            this.aiResponse = aiResponse;
            this.timestamp = timestamp;
        }
        
        // Getters
        public String getUserMessage() {
            return userMessage;
        }
        
        public String getAiResponse() {
            return aiResponse;
        }
        
        public LocalDateTime getTimestamp() {
            return timestamp;
        }
    }
}
```

### 📝 Passo 2: Criar o Gerenciador de Conversações

**Arquivo:** `src/main/java/com/seudominio/docbot/service/ConversationManager.java`

```java
package com.seudominio.docbot.service;

import com.seudominio.docbot.model.Conversation;
import org.springframework.stereotype.Service;

import java.util.Map;
import java.util.Optional;
import java.util.concurrent.ConcurrentHashMap;

/**
 * Gerenciador de conversações ativas.
 * 
 * RESPONSABILIDADE: Armazenar e recuperar conversações por ID.
 * 
 * ⚠️ NOTA: Esta implementação usa memória (não persiste após restart).
 * Em produção, use Redis, banco de dados, etc.
 */
@Service
public class ConversationManager {
    
    // ConcurrentHashMap garante thread-safety
    private final Map<String, Conversation> conversations = new ConcurrentHashMap<>();
    
    /**
     * Cria uma nova conversação.
     * 
     * @return A conversação criada (com ID único)
     */
    public Conversation createConversation() {
        Conversation conversation = new Conversation();
        conversations.put(conversation.getId(), conversation);
        return conversation;
    }
    
    /**
     * Busca uma conversação existente por ID.
     * 
     * @param conversationId ID da conversação
     * @return Optional com a conversação (vazio se não encontrada)
     */
    public Optional<Conversation> getConversation(String conversationId) {
        return Optional.ofNullable(conversations.get(conversationId));
    }
    
    /**
     * Deleta uma conversação (libera memória).
     * 
     * @param conversationId ID da conversação a deletar
     * @return true se deletada, false se não existia
     */
    public boolean deleteConversation(String conversationId) {
        return conversations.remove(conversationId) != null;
    }
    
    /**
     * Retorna estatísticas do gerenciador.
     */
    public Map<String, Object> getStats() {
        return Map.of(
            "active_conversations", conversations.size(),
            "total_messages", conversations.values().stream()
                .mapToInt(Conversation::getMessageCount)
                .sum()
        );
    }
}
```

### 📝 Passo 3: Atualizar o ChatService com Contexto

**Arquivo:** `src/main/java/com/seudominio/docbot/service/ChatService.java` (versão melhorada)

```java
package com.seudominio.docbot.service;

import com.seudominio.docbot.model.ChatRequest;
import com.seudominio.docbot.model.ChatResponse;
import com.seudominio.docbot.model.Conversation;
import org.springframework.ai.chat.ChatClient;
import org.springframework.ai.chat.messages.Message;
import org.springframework.ai.chat.messages.SystemMessage;
import org.springframework.ai.chat.messages.UserMessage;
import org.springframework.ai.chat.prompt.Prompt;
import org.springframework.stereotype.Service;

import java.util.ArrayList;
import java.util.List;

/**
 * Serviço de chat com suporte a contexto conversacional.
 */
@Service
public class ChatService {

    private final ChatClient chatClient;
    private final ConversationManager conversationManager;
    
    // Prompt de sistema que define o comportamento da IA
    private static final String SYSTEM_PROMPT = """
        Você é DocBot, um assistente especializado em documentação técnica.
        
        Características:
        - Sempre responda em português brasileiro
        - Seja conciso mas completo
        - Use exemplos de código quando apropriado
        - Se não souber algo, admita honestamente
        - Mantenha um tom profissional mas amigável
        """;

    public ChatService(ChatClient chatClient, ConversationManager conversationManager) {
        this.chatClient = chatClient;
        this.conversationManager = conversationManager;
    }

    /**
     * Processa mensagem com contexto de conversação.
     * 
     * @param request Requisição com mensagem e ID de conversação (opcional)
     * @return Resposta da IA com metadata
     */
    public ChatResponse processMessage(ChatRequest request) {
        // 1. Validação
        validateRequest(request);
        
        // 2. Obter ou criar conversação
        Conversation conversation = getOrCreateConversation(request.getConversationId());
        
        // 3. Construir prompt com contexto
        Prompt prompt = buildPromptWithContext(request.getMessage(), conversation);
        
        // 4. Chamar IA
        String aiResponse = chatClient.call(prompt)
            .getResult()
            .getOutput()
            .getContent();
        
        // 5. Atualizar histórico
        conversation.addMessage(request.getMessage(), aiResponse);
        
        // 6. Construir resposta
        return new ChatResponse(
            aiResponse, 
            estimateTokens(request.getMessage() + aiResponse),
            conversation.getId()
        );
    }

    /**
     * Constrói prompt incluindo:
     * - System message (personalidade da IA)
     * - Histórico de conversação
     * - Mensagem atual do usuário
     */
    private Prompt buildPromptWithContext(String userMessage, Conversation conversation) {
        List<Message> messages = new ArrayList<>();
        
        // 1. System message (sempre primeiro)
        messages.add(new SystemMessage(SYSTEM_PROMPT));
        
        // 2. Histórico de conversação (se existir)
        String history = conversation.getContextHistory();
        if (!history.isEmpty()) {
            messages.add(new SystemMessage("Histórico da conversação:\n" + history));
        }
        
        // 3. Mensagem atual do usuário
        messages.add(new UserMessage(userMessage));
        
        return new Prompt(messages);
    }

    /**
     * Obtém conversação existente ou cria nova.
     */
    private Conversation getOrCreateConversation(String conversationId) {
        if (conversationId != null && !conversationId.isBlank()) {
            return conversationManager.getConversation(conversationId)
                .orElseThrow(() -> new IllegalArgumentException(
                    "Conversação não encontrada: " + conversationId
                ));
        }
        return conversationManager.createConversation();
    }

    private void validateRequest(ChatRequest request) {
        if (request.getMessage() == null || request.getMessage().isBlank()) {
            throw new IllegalArgumentException("Mensagem não pode ser vazia");
        }
        
        if (request.getMessage().length() > 2000) {
            throw new IllegalArgumentException("Mensagem muito longa (máx: 2000 caracteres)");
        }
    }

    private int estimateTokens(String text) {
        // Estimativa: 1 token ≈ 4 caracteres
        return text.length() / 4;
    }
}
```

### 📝 Passo 4: Atualizar os Modelos de Request/Response

**Arquivo:** `src/main/java/com/seudominio/docbot/model/ChatRequest.java` (atualizado)

```java
package com.seudominio.docbot.model;

import com.fasterxml.jackson.annotation.JsonProperty;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Size;

/**
 * Request de chat com suporte a conversação contextual.
 */
public class ChatRequest {
    
    @NotBlank(message = "Mensagem é obrigatória")
    @Size(max = 2000, message = "Mensagem muito longa (máximo 2000 caracteres)")
    @JsonProperty("message")
    private String message;
    
    @JsonProperty("conversation_id")
    private String conversationId;  // Opcional - para continuar conversação existente
    
    // Construtores
    public ChatRequest() {}
    
    public ChatRequest(String message) {
        this.message = message;
    }
    
    public ChatRequest(String message, String conversationId) {
        this.message = message;
        this.conversationId = conversationId;
    }

    // Getters e Setters
    public String getMessage() {
        return message;
    }

    public void setMessage(String message) {
        this.message = message;
    }

    public String getConversationId() {
        return conversationId;
    }

    public void setConversationId(String conversationId) {
        this.conversationId = conversationId;
    }
}
```

**Arquivo:** `src/main/java/com/seudominio/docbot/model/ChatResponse.java` (atualizado)

```java
package com.seudominio.docbot.model;

import com.fasterxml.jackson.annotation.JsonProperty;
import java.time.LocalDateTime;

/**
 * Response de chat com metadata enriquecida.
 */
public class ChatResponse {
    
    @JsonProperty("response")
    private String response;
    
    @JsonProperty("tokens_used")
    private int tokensUsed;
    
    @JsonProperty("timestamp")
    private LocalDateTime timestamp;
    
    @JsonProperty("conversation_id")
    private String conversationId;  // ID para continuar a conversação

    // Construtor
    public ChatResponse(String response, int tokensUsed, String conversationId) {
        this.response = response;
        this.tokensUsed = tokensUsed;
        this.conversationId = conversationId;
        this.timestamp = LocalDateTime.now();
    }

    // Getters
    public String getResponse() {
        return response;
    }

    public int getTokensUsed() {
        return tokensUsed;
    }

    public LocalDateTime getTimestamp() {
        return timestamp;
    }

    public String getConversationId() {
        return conversationId;
    }
}
```

### 📝 Passo 5: Controller Completo com Endpoints Adicionais

**Arquivo:** `src/main/java/com/seudominio/docbot/controller/ChatController.java` (versão final)

```java
package com.seudominio.docbot.controller;

import com.seudominio.docbot.model.ChatRequest;
import com.seudominio.docbot.model.ChatResponse;
import com.seudominio.docbot.model.Conversation;
import com.seudominio.docbot.service.ChatService;
import com.seudominio.docbot.service.ConversationManager;
import jakarta.validation.Valid;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.*;

import java.util.Map;

/**
 * API REST para chatbot com gerenciamento de conversações.
 */
@RestController
@RequestMapping("/api/v1/chat")
public class ChatController {

    private final ChatService chatService;
    private final ConversationManager conversationManager;

    public ChatController(ChatService chatService, ConversationManager conversationManager) {
        this.chatService = chatService;
        this.conversationManager = conversationManager;
    }

    /**
     * Endpoint principal de chat.
     * 
     * POST /api/v1/chat
     * 
     * Body:
     * {
     *   "message": "Olá, como você está?",
     *   "conversation_id": "uuid-opcional"  // Omita para nova conversação
     * }
     * 
     * Response:
     * {
     *   "response": "Olá! Estou bem, obrigado. Como posso ajudar?",
     *   "tokens_used": 25,
     *   "timestamp": "2024-01-15T10:30:00",
     *   "conversation_id": "123e4567-e89b-12d3-a456-426614174000"
     * }
     */
    @PostMapping
    public ResponseEntity<ChatResponse> chat(@Valid @RequestBody ChatRequest request) {
        ChatResponse response = chatService.processMessage(request);
        return ResponseEntity.ok(response);
    }

    /**
     * Cria uma nova conversação.
     * 
     * POST /api/v1/chat/conversations
     * 
     * Response:
     * {
     *   "conversation_id": "uuid",
     *   "started_at": "2024-01-15T10:30:00",
     *   "message_count": 0
     * }
     */
    @PostMapping("/conversations")
    public ResponseEntity<Map<String, Object>> createConversation() {
        Conversation conversation = conversationManager.createConversation();
        
        return ResponseEntity.ok(Map.of(
            "conversation_id", conversation.getId(),
            "started_at", conversation.getStartedAt(),
            "message_count", conversation.getMessageCount()
        ));
    }

    /**
     * Busca histórico de uma conversação.
     * 
     * GET /api/v1/chat/conversations/{id}
     */
    @GetMapping("/conversations/{id}")
    public ResponseEntity<Map<String, Object>> getConversation(@PathVariable String id) {
        Conversation conversation = conversationManager.getConversation(id)
            .orElseThrow(() -> new IllegalArgumentException("Conversação não encontrada"));
        
        return ResponseEntity.ok(Map.of(
            "conversation_id", conversation.getId(),
            "started_at", conversation.getStartedAt(),
            "message_count", conversation.getMessageCount(),
            "messages", conversation.getMessages()
        ));
    }

    /**
     * Deleta uma conversação.
     * 
     * DELETE /api/v1/chat/conversations/{id}
     */
    @DeleteMapping("/conversations/{id}")
    public ResponseEntity<Void> deleteConversation(@PathVariable String id) {
        boolean deleted = conversationManager.deleteConversation(id);
        
        if (!deleted) {
            return ResponseEntity.notFound().build();
        }
        
        return ResponseEntity.noContent().build();
    }

    /**
     * Estatísticas do sistema.
     * 
     * GET /api/v1/chat/stats
     */
    @GetMapping("/stats")
    public ResponseEntity<Map<String, Object>> getStats() {
        return ResponseEntity.ok(conversationManager.getStats());
    }
}
```

### 🧪 Passo 6: Testando o Chatbot Completo

#### Teste 1: Nova Conversação

```bash
# Criar nova conversação
curl -X POST http://localhost:8080/api/v1/chat/conversations

# Response:
{
  "conversation_id": "a1b2c3d4-e5f6-7g8h-9i0j-k1l2m3n4o5p6",
  "started_at": "2024-01-15T10:30:00",
  "message_count": 0
}
```

#### Teste 2: Primeira Mensagem

```bash
curl -X POST http://localhost:8080/api/v1/chat \
  -H "Content-Type: application/json" \
  -d '{
    "message": "Olá! O que é Spring AI?"
  }'

# Response:
{
  "response": "Olá! Spring AI é um framework que facilita a integração...",
  "tokens_used": 75,
  "timestamp": "2024-01-15T10:31:00",
  "conversation_id": "a1b2c3d4-e5f6-7g8h-9i0j-k1l2m3n4o5p6"
}
```

#### Teste 3: Continuando a Conversação (com Contexto)

```bash
# Use o conversation_id recebido anteriormente
curl -X POST http://localhost:8080/api/v1/chat \
  -H "Content-Type: application/json" \
  -d '{
    "message": "Pode dar um exemplo de código?",
    "conversation_id": "a1b2c3d4-e5f6-7g8h-9i0j-k1l2m3n4o5p6"
  }'

# A IA lembrará que você perguntou sobre Spring AI!
# Response:
{
  "response": "Claro! Aqui está um exemplo de uso do Spring AI:\n\n```java\n@Service\npublic class ChatService {\n    private final ChatClient chatClient;\n    ...",
  "tokens_used": 120,
  "timestamp": "2024-01-15T10:32:00",
  "conversation_id": "a1b2c3d4-e5f6-7g8h-9i0j-k1l2m3n4o5p6"
}
```

#### Teste 4: Verificar Histórico

```bash
curl http://localhost:8080/api/v1/chat/conversations/a1b2c3d4-e5f6-7g8h-9i0j-k1l2m3n4o5p6

# Response:
{
  "conversation_id": "a1b2c3d4-e5f6-7g8h-9i0j-k1l2m3n4o5p6",
  "started_at": "2024-01-15T10:30:00",
  "message_count": 2,
  "messages": [
    {
      "userMessage": "Olá! O que é Spring AI?",
      "aiResponse": "Olá! Spring AI é...",
      "timestamp": "2024-01-15T10:31:00"
    },
    {
      "userMessage": "Pode dar um exemplo de código?",
      "aiResponse": "Claro! Aqui está...",
      "timestamp": "2024-01-15T10:32:00"
    }
  ]
}
```

#### Teste 5: Estatísticas

```bash
curl http://localhost:8080/api/v1/chat/stats

# Response:
{
  "active_conversations": 3,
  "total_messages": 7
}
```

### 🎉 Parabéns! Você Construiu um Chatbot Real!

**O que você acabou de criar:**

✅ **API REST completa** com múltiplos endpoints
✅ **Gerenciamento de conversações** com memória contextual
✅ **Validação de entrada** automática
✅ **Tratamento de erros** robusto
✅ **Metadata enriquecida** em respostas
✅ **Código profissional** seguindo melhores práticas

---

<a name="3-3"></a>

## 🔍 3.3 ENTENDENDO O QUE ACONTECEU NOS BASTIDORES

### 🎨 Analogia: Raio-X da Aplicação

Agora que o chatbot está funcionando, vamos fazer um "raio-X" para entender exatamente o que acontece em cada camada quando você envia uma mensagem.

### 📊 Fluxo Completo de Uma Requisição

```
┌─────────────────────────────────────────────────────────────┐
│                    JORNADA DE UMA MENSAGEM                   │
└─────────────────────────────────────────────────────────────┘

1. Cliente HTTP (Postman/curl)
   │
   │ POST /api/v1/chat
   │ { "message": "Olá", "conversation_id": "abc123" }
   │
   ▼
2. Spring DispatcherServlet
   │  ├─ Identifica o controller (ChatController)
   │  ├─ Identifica o método (@PostMapping)
   │  └─ Deserializa JSON → ChatRequest object
   │
   ▼
3. Jakarta Validation
   │  ├─ Valida @NotBlank
   │  ├─ Valida @Size(max=2000)
   │  └─ Se falhar → Retorna 400 Bad Request
   │
   ▼
4. ChatController.chat()
   │  └─ Delega para chatService.processMessage(request)
   │
   ▼
5. ChatService.processMessage()
   │
   ├─ 5.1 validateRequest()
   │  └─ Regras de negócio adicionais
   │
   ├─ 5.2 getOrCreateConversation()
   │  ├─ Se conversation_id fornecido:
   │  │  └─ conversationManager.getConversation(id)
   │  └─ Senão:
   │     └─ conversationManager.createConversation()
   │
   ├─ 5.3 buildPromptWithContext()
   │  ├─ Cria SystemMessage (personalidade da IA)
   │  ├─ Adiciona histórico (conversation.getContextHistory())
   │  └─ Adiciona UserMessage (mensagem atual)
   │
   ├─ 5.4 chatClient.call(prompt)
   │  │
   │  ├─ OpenAiChatClient prepara requisição HTTP
   │  │  ├─ URL: https://api.openai.com/v1/chat/completions
   │  │  ├─ Headers:
   │  │  │  ├─ Authorization: Bearer sk-xxxxx
   │  │  │  └─ Content-Type: application/json
   │  │  └─ Body (JSON):
   │  │     {
   │  │       "model": "gpt-3.5-turbo",
   │  │       "messages": [
   │  │         {"role": "system", "content": "Você é DocBot..."},
   │  │         {"role": "user", "content": "Histórico..."},
   │  │         {"role": "user", "content": "Olá"}
   │  │       ],
   │  │       "temperature": 0.7,
   │  │       "max_tokens": 500
   │  │     }
   │  │
   │  ├─ Envia HTTP POST para OpenAI
   │  │
   │  ├─ OpenAI processa (pode demorar 1-5 segundos)
   │  │
   │  ├─ Recebe response JSON:
   │  │  {
   │  │    "id": "chatcmpl-xyz",
   │  │    "choices": [{
   │  │      "message": {
   │  │        "role": "assistant",
   │  │        "content": "Olá! Como posso ajudar?"
   │  │      },
   │  │      "finish_reason": "stop"
   │  │    }],
   │  │    "usage": {
   │  │      "prompt_tokens": 50,
   │  │      "completion_tokens": 10,
   │  │      "total_tokens": 60
   │  │    }
   │  │  }
   │  │
   │  └─ Extrai content da resposta
   │     └─ Retorna "Olá! Como posso ajudar?"
   │
   ├─ 5.5 conversation.addMessage()
   │  └─ Adiciona par (pergunta, resposta) ao histórico
   │
   └─ 5.6 Cria ChatResponse
      └─ Inclui resposta, tokens, conversationId
   
   ▼
6. ChatController
   │  └─ Envelopa em ResponseEntity.ok()
   │
   ▼
7. Spring DispatcherServlet
   │  ├─ Serializa ChatResponse → JSON
   │  └─ Define headers HTTP (Content-Type: application/json)
   │
   ▼
8. Cliente HTTP recebe response
   Status: 200 OK
   Body: {"response": "Olá! Como posso ajudar?", ...}
```

### 🔬 Análise Profunda: O Que Acontece na Chamada da API OpenAI

#### Requisição HTTP Real Enviada

```http
POST https://api.openai.com/v1/chat/completions HTTP/1.1
Host: api.openai.com
Authorization: Bearer sk-proj-xxxxxxxxxxxxxxxxxxxx
Content-Type: application/json
Content-Length: 456

{
  "model": "gpt-3.5-turbo",
  "messages": [
    {
      "role": "system",
      "content": "Você é DocBot, um assistente especializado em documentação técnica.\n\nCaracterísticas:\n- Sempre responda em português brasileiro\n- Seja conciso mas completo\n- Use exemplos de código quando apropriado\n- Se não souber algo, admita honestamente\n- Mantenha um tom profissional mas amigável"
    },
    {
      "role": "system",
      "content": "Histórico da conversação:\nUsuário: Olá! O que é Spring AI?\nAssistente: Olá! Spring AI é um framework...\n"
    },
    {
      "role": "user",
      "content": "Pode dar um exemplo de código?"
    }
  ],
  "temperature": 0.7,
  "max_tokens": 500,
  "top_p": 1.0,
  "frequency_penalty": 0.0,
  "presence_penalty": 0.0
}
```

#### Processamento no Servidor OpenAI

```
┌────────────────────────────────────────────┐
│        DENTRO DO SERVIDOR OPENAI           │
├────────────────────────────────────────────┤
│                                            │
│ 1. Recebe requisição                       │
│    └─ Valida API key                       │
│    └─ Verifica quota/limites               │
│                                            │
│ 2. Tokenização                             │
│    └─ Converte texto em tokens numéricos  │
│       "Pode" → [47799]                    │
│       "dar" → [29271]                     │
│       "um" → [1234]                       │
│       ...                                  │
│    └─ Total: ~150 tokens (prompt)         │
│                                            │
│ 3. Modelo GPT-3.5-turbo processa          │
│    ├─ Contexto: system + histórico        │
│    ├─ Atenção multi-head                  │
│    ├─ Transformers (12 camadas)           │
│    └─ Geração autoregressiva              │
│       (palavra por palavra)                │
│                                            │
│ 4. Sampling                                │
│    └─ temperature=0.7 adiciona            │
│       aleatoriedade controlada            │
│                                            │
│ 5. Detokenização                           │
│    └─ Tokens → texto legível              │
│                                            │
│ 6. Retorna JSON                            │
└────────────────────────────────────────────┘
```

#### Response HTTP Real Recebida

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 892
x-ratelimit-limit-requests: 3500
x-ratelimit-remaining-requests: 3499
x-ratelimit-limit-tokens: 90000
x-ratelimit-remaining-tokens: 89850

{
  "id": "chatcmpl-8g7xYz123456789",
  "object": "chat.completion",
  "created": 1705320600,
  "model": "gpt-3.5-turbo-0613",
  "choices": [
    {
      "index": 0,
      "message": {
        "role": "assistant",
        "content": "Claro! Aqui está um exemplo básico de uso do Spring AI:\n\n```java\n@Service\npublic class ChatService {\n    private final ChatClient chatClient;\n    \n    public ChatService(ChatClient chatClient) {\n        this.chatClient = chatClient;\n    }\n    \n    public String chat(String mensagem) {\n        return chatClient.call(mensagem);\n    }\n}\n```\n\nEste código cria um serviço simples que injeta o ChatClient e o usa para enviar mensagens à IA."
      },
      "finish_reason": "stop"
    }
  ],
  "usage": {
    "prompt_tokens": 156,
    "completion_tokens": 94,
    "total_tokens": 250
  }
}
```

### 💰 Anatomia dos Custos

```
┌──────────────────────────────────────────────────────────┐
│              CÁLCULO DE CUSTOS (GPT-3.5-turbo)           │
├──────────────────────────────────────────────────────────┤
│                                                          │
│ Entrada (Prompt): 156 tokens                            │
│ ├─ System message: 80 tokens                            │
│ ├─ Histórico: 60 tokens                                 │
│ └─ Pergunta atual: 16 tokens                            │
│                                                          │
│ Saída (Completion): 94 tokens                           │
│                                                          │
│ Total: 250 tokens                                        │
│                                                          │
│ Preço GPT-3.5-turbo (jan/2024):                         │
│ ├─ Input: $0.0015 / 1K tokens                           │
│ └─ Output: $0.002 / 1K tokens                           │
│                                                          │
│ Custo desta requisição:                                 │
│ ├─ Input: 156 × 0.0015 / 1000 = $0.000234              │
│ ├─ Output: 94 × 0.002 / 1000 = $0.000188               │
│ └─ TOTAL: $0.000422 (~R$ 0.002 centavos)               │
│                                                          │
│ ⚠️ Com histórico de 10 mensagens:                       │
│    Cada nova pergunta custará ~3x mais                  │
│    (devido ao contexto acumulado)                        │
└──────────────────────────────────────────────────────────┘
```

### 🧠 Decisões de Design Importantes

#### Por Que Usar SystemMessage?

```java
// ❌ SEM SystemMessage:
messages.add(new UserMessage("Você é um assistente. Responda: " + pergunta));
// Problema: Usuário pode sobrescrever personalidade

// ✅ COM SystemMessage:
messages.add(new SystemMessage("Você é DocBot..."));
messages.add(new UserMessage(pergunta));
// Vantagem: Personalidade protegida, não conta para histórico do usuário
```

#### Por Que ConcurrentHashMap para Conversações?

```java
// ❌ HashMap normal:
private final Map<String, Conversation> conversations = new HashMap<>();
// Problema: Não é thread-safe. Múltiplos usuários simultâneos = DESASTRE

// ✅ ConcurrentHashMap:
private final Map<String, Conversation> conversations = new ConcurrentHashMap<>();
// Vantagem: Thread-safe, perfeito para ambientes multi-thread (web)
```

#### Por Que Validar DUAS Vezes?

```java
// Validação 1: Jakarta Validation (automática)
@NotBlank(message = "Mensagem é obrigatória")
private String message;

// Validação 2: No Service (manual)
if (request.getMessage().length() > 2000) {
    throw new IllegalArgumentException("Mensagem muito longa");
}
```

**Motivo:**
- **Validação 1:** Garante formato básico (não nulo, não vazio)
- **Validação 2:** Regras de negócio complexas (limites de custo, contexto específico)

### 🎭 Cenários de Fluxo Especiais

#### Cenário 1: Erro de Rede com OpenAI

```
Usuario envia mensagem
    ↓
ChatService.processMessage()
    ↓
chatClient.call(prompt)
    ↓
HTTP POST para OpenAI
    ↓
❌ Timeout (30 segundos)
    ↓
Spring AI lança ResourceAccessException
    ↓
AiExceptionHandler.handleGenericError()
    ↓
Response 500 para usuário:
{
  "error": "Internal Server Error",
  "message": "Erro ao processar sua mensagem. Tente novamente."
}
```

#### Cenário 2: Conversação Não Encontrada

```
Usuario envia mensagem com conversation_id inexistente
    ↓
ChatService.getOrCreateConversation()
    ↓
conversationManager.getConversation(id)
    ↓
Returns Optional.empty()
    ↓
.orElseThrow(() -> new IllegalArgumentException(...))
    ↓
AiExceptionHandler.handleValidationError()
    ↓
Response 400 para usuário:
{
  "error": "Validation Error",
  "message": "Conversação não encontrada: abc123"
}
```

### 🔐 Segurança: O Que Protege Sua API Key

```
┌────────────────────────────────────────────────────┐
│          CAMADAS DE PROTEÇÃO DA API KEY            │
├────────────────────────────────────────────────────┤
│                                                    │
│ 1. Variável de Ambiente                           │
│    ├─ Nunca no código-fonte                       │
│    └─ Não commitada no Git                        │
│                                                    │
│ 2. application.properties                         │
│    ├─ ${OPENAI_API_KEY} placeholder               │
│    └─ Resolvido em runtime                        │
│                                                    │
│ 3. Spring @Value injection                        │
│    ├─ Injetada no AiConfig                        │
│    └─ Não exposta em logs                         │
│                                                    │
│ 4. OpenAiApi (classe interna Spring AI)          │
│    ├─ Armazena key em campo privado              │
│    └─ Apenas usa em headers HTTP                  │
│                                                    │
│ 5. HTTPS                                           │
│    └─ Comunicação criptografada com OpenAI       │
│                                                    │
│ ⚠️ NUNCA FAÇA:                                    │
│    String apiKey = "sk-xxxxx";  // ❌ PERIGO!    │
│    System.out.println(apiKey);  // ❌ NUNCA!     │
│    logger.info("Key: " + key);  // ❌ NÃO!       │
└────────────────────────────────────────────────────┘
```

---

<a name="3-4"></a>

## 🚀 3.4 EXPANDINDO O EXEMPLO BÁSICO

### 🎯 Objetivo

Adicionar funcionalidades profissionais que transformam nosso chatbot de "demo" para "production-ready":

1. **Streaming de Respostas** (respostas em tempo real)
2. **Rate Limiting** (proteção contra abuso)
3. **Métricas e Monitoramento**
4. **Cache Inteligente**
5. **Múltiplos Modelos** (fallback strategy)

---

### 📡 FEATURE 1: Streaming de Respostas

#### 🎨 Analogia

**Sem streaming:** É como esperar um arquivo de 1GB baixar 100% para depois abrir.

**Com streaming:** É como Netflix - começa a assistir enquanto ainda está baixando.

#### 💻 Implementação

**1. Criar DTO para Streaming**

`src/main/java/com/seudominio/docbot/model/StreamChunk.java`

```java
package com.seudominio.docbot.model;

import com.fasterxml.jackson.annotation.JsonProperty;

/**
 * Representa um "pedaço" de resposta em streaming.
 */
public class StreamChunk {
    
    @JsonProperty("content")
    private String content;  // Parte do texto
    
    @JsonProperty("is_final")
    private boolean isFinal;  // true se for o último chunk
    
    @JsonProperty("conversation_id")
    private String conversationId;
    
    public StreamChunk(String content, boolean isFinal, String conversationId) {
        this.content = content;
        this.isFinal = isFinal;
        this.conversationId = conversationId;
    }
    
    // Getters
    public String getContent() { return content; }
    public boolean isFinal() { return isFinal; }
    public String getConversationId() { return conversationId; }
}
```

**2. Service com Suporte a Streaming**

`ChatService.java` (adicionar método)

```java
import org.springframework.ai.chat.StreamingChatClient;
import reactor.core.publisher.Flux;

@Service
public class ChatService {
    
    private final ChatClient chatClient;
    private final StreamingChatClient streamingChatClient;  // NOVO
    private final ConversationManager conversationManager;
    
    // Construtor atualizado
    public ChatService(
            ChatClient chatClient, 
            StreamingChatClient streamingChatClient,
            ConversationManager conversationManager) {
        this.chatClient = chatClient;
        this.streamingChatClient = streamingChatClient;
        this.conversationManager = conversationManager;
    }
    
    // Método existente: processMessage()...
    
    /**
     * NOVO: Processa mensagem com streaming (retorna Flux reativo).
     * 
     * @param request Requisição de chat
     * @return Flux de chunks de texto (enviados conforme gerados)
     */
    public Flux<StreamChunk> processMessageStreaming(ChatRequest request) {
        validateRequest(request);
        
        Conversation conversation = getOrCreateConversation(request.getConversationId());
        Prompt prompt = buildPromptWithContext(request.getMessage(), conversation);
        
        // StringBuilder para acumular resposta completa
        StringBuilder fullResponse = new StringBuilder();
        
        return streamingChatClient.stream(prompt)
            .map(chatResponse -> {
                // Extrai conteúdo de cada chunk
                String content = chatResponse.getResult().getOutput().getContent();
                fullResponse.append(content);
                
                return new StreamChunk(
                    content, 
                    false,  // Não é final ainda
                    conversation.getId()
                );
            })
            .concatWith(Flux.defer(() -> {
                // Após todos os chunks, adiciona ao histórico
                conversation.addMessage(request.getMessage(), fullResponse.toString());
                
                // Envia chunk final (vazio, apenas sinaliza fim)
                return Flux.just(new StreamChunk(
                    "", 
                    true,  // É o chunk final
                    conversation.getId()
                ));
            }));
    }
}
```

**3. Controller com Endpoint de Streaming**

`ChatController.java` (adicionar método)

```java
import org.springframework.http.MediaType;
import reactor.core.publisher.Flux;

@RestController
@RequestMapping("/api/v1/chat")
public class ChatController {
    
    // Campos e métodos existentes...
    
    /**
     * NOVO: Endpoint de streaming.
     * 
     * POST /api/v1/chat/stream
     * 
     * Retorna Server-Sent Events (text/event-stream).
     * Cliente recebe chunks conforme gerados.
     */
    @PostMapping(
        value = "/stream",
        produces = MediaType.TEXT_EVENT_STREAM_VALUE
    )
    public Flux<StreamChunk> chatStream(@Valid @RequestBody ChatRequest request) {
        return chatService.processMessageStreaming(request);
    }
}
```

**4. Testando Streaming**

```bash
# Com curl (mostra chunks conforme chegam)
curl -N -X POST http://localhost:8080/api/v1/chat/stream \
  -H "Content-Type: application/json" \
  -d '{"message":"Escreva um poema sobre Spring AI"}' 

# Output (em tempo real):
data:{"content":"Primavera","is_final":false,"conversation_id":"..."}

data:{"content":" do","is_final":false,"conversation_id":"..."}

data:{"content":" código","is_final":false,"conversation_id":"..."}

data:{"content":",","is_final":false,"conversation_id":"..."}
...
data:{"content":"","is_final":true,"conversation_id":"..."}
```

**Cliente JavaScript para Streaming:**

```javascript
const eventSource = new EventSource('/api/v1/chat/stream');

eventSource.onmessage = (event) => {
    const chunk = JSON.parse(event.data);
    
    if (chunk.is_final) {
        console.log('Streaming concluído!');
        eventSource.close();
    } else {
        // Adiciona chunk ao DOM
        document.getElementById('chat').innerHTML += chunk.content;
    }
};
```

---

### 🛡️ FEATURE 2: Rate Limiting (Proteção Contra Abuso)

#### 🎨 Analogia

Rate limiting é como um segurança de boate: permite X pessoas por hora. Se exceder, você espera na fila.

#### 💻 Implementação

**1. Adicionar Dependência**

`pom.xml`

```xml
<dependency>
    <groupId>com.github.vladimir-bukhtoyarov</groupId>
    <artifactId>bucket4j-core</artifactId>
    <version>8.7.0</version>
</dependency>
```

**2. Configurar Rate Limiter**

`src/main/java/com/seudominio/docbot/config/RateLimitConfig.java`

```java
package com.seudominio.docbot.config;

import io.github.bucket4j.Bandwidth;
import io.github.bucket4j.Bucket;
import io.github.bucket4j.Refill;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

import java.time.Duration;
import java.util.Map;
import java.util.concurrent.ConcurrentHashMap;

/**
 * Configuração de rate limiting.
 * 
 * Limite: 10 requisições por minuto por IP.
 */
@Configuration
public class RateLimitConfig {
    
    private final Map<String, Bucket> buckets = new ConcurrentHashMap<>();
    
    /**
     * Cria ou retorna bucket para um IP.
     */
    public Bucket resolveBucket(String ip) {
        return buckets.computeIfAbsent(ip, k -> createNewBucket());
    }
    
    private Bucket createNewBucket() {
        // Capacidade: 10 tokens
        // Refill: 10 tokens a cada 1 minuto
        Bandwidth limit = Bandwidth.classic(
            10, 
            Refill.intervally(10, Duration.ofMinutes(1))
        );
        
        return Bucket.builder()
            .addLimit(limit)
            .build();
    }
}
```

**3. Interceptor para Rate Limiting**

`src/main/java/com/seudominio/docbot/interceptor/RateLimitInterceptor.java`

```java
package com.seudominio.docbot.interceptor;

import com.seudominio.docbot.config.RateLimitConfig;
import io.github.bucket4j.Bucket;
import io.github.bucket4j.ConsumptionProbe;
import jakarta.servlet.http.HttpServletRequest;
import jakarta.servlet.http.HttpServletResponse;
import org.springframework.stereotype.Component;
import org.springframework.web.servlet.HandlerInterceptor;

/**
 * Interceptor que aplica rate limiting em todas as requisições.
 */
@Component
public class RateLimitInterceptor implements HandlerInterceptor {
    
    private final RateLimitConfig rateLimitConfig;
    
    public RateLimitInterceptor(RateLimitConfig rateLimitConfig) {
        this.rateLimitConfig = rateLimitConfig;
    }
    
    @Override
    public boolean preHandle(
            HttpServletRequest request, 
            HttpServletResponse response, 
            Object handler) throws Exception {
        
        String ip = getClientIP(request);
        Bucket bucket = rateLimitConfig.resolveBucket(ip);
        
        // Tenta consumir 1 token
        ConsumptionProbe probe = bucket.tryConsumeAndReturnRemaining(1);
        
        if (probe.isConsumed()) {
            // Adiciona headers informativos
            response.addHeader("X-Rate-Limit-Remaining", 
                String.valueOf(probe.getRemainingTokens()));
            return true;  // Permite requisição
        } else {
            // Limite excedido
            long waitForRefill = probe.getNanosToWaitForRefill() / 1_000_000_000;
            
            response.setStatus(429);  // Too Many Requests
            response.addHeader("X-Rate-Limit-Retry-After-Seconds", 
                String.valueOf(waitForRefill));
            response.getWriter().write(
                "{\"error\":\"Rate limit exceeded. Retry in " + waitForRefill + " seconds\"}"
            );
            
            return false;  // Bloqueia requisição
        }
    }
    
    private String getClientIP(HttpServletRequest request) {
        String xfHeader = request.getHeader("X-Forwarded-For");
        if (xfHeader == null) {
            return request.getRemoteAddr();
        }
        return xfHeader.split(",")[0];
    }
}
```

**4. Registrar Interceptor**

`src/main/java/com/seudominio/docbot/config/WebConfig.java`

```java
package com.seudominio.docbot.config;

import com.seudominio.docbot.interceptor.RateLimitInterceptor;
import org.springframework.context.annotation.Configuration;
import org.springframework.web.servlet.config.annotation.InterceptorRegistry;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;

@Configuration
public class WebConfig implements WebMvcConfigurer {
    
    private final RateLimitInterceptor rateLimitInterceptor;
    
    public WebConfig(RateLimitInterceptor rateLimitInterceptor) {
        this.rateLimitInterceptor = rateLimitInterceptor;
    }
    
    @Override
    public void addInterceptors(InterceptorRegistry registry) {
        registry.addInterceptor(rateLimitInterceptor)
                .addPathPatterns("/api/**");  // Aplica em todos os endpoints /api
    }
}
```

**5. Testando Rate Limiting**

```bash
# Faça 11 requisições rápidas
for i in {1..11}; do
  curl -X POST http://localhost:8080/api/v1/chat \
    -H "Content-Type: application/json" \
    -d '{"message":"teste"}' \
    -w "\nStatus: %{http_code}\n"
done

# Primeiras 10: Status 200
# 11ª requisição: Status 429
# Response:
# {"error":"Rate limit exceeded. Retry in 60 seconds"}
```

---

### 📊 FEATURE 3: Métricas e Monitoramento

#### 💻 Implementação

**1. Adicionar Dependência Micrometer**

`pom.xml`

```xml
<dependency>
    <groupId>io.micrometer</groupId>
    <artifactId>micrometer-registry-prometheus</artifactId>
</dependency>
```

**2. Habilitar Endpoints Actuator**

`application.properties`

```properties
management.endpoints.web.exposure.include=health,info,prometheus,metrics
management.metrics.export.prometheus.enabled=true
```

**3. Service com Métricas**

`ChatService.java` (atualizar)

```java
import io.micrometer.core.instrument.MeterRegistry;
import io.micrometer.core.instrument.Timer;

@Service
public class ChatService {
    
    private final ChatClient chatClient;
    private final ConversationManager conversationManager;
    private final MeterRegistry meterRegistry;  // NOVO
    
    public ChatService(
            ChatClient chatClient,
            ConversationManager conversationManager,
            MeterRegistry meterRegistry) {
        this.chatClient = chatClient;
        this.conversationManager = conversationManager;
        this.meterRegistry = meterRegistry;
    }
    
    public ChatResponse processMessage(ChatRequest request) {
        // Inicia timer
        Timer.Sample sample = Timer.start(meterRegistry);
        
        try {
            validateRequest(request);
            Conversation conversation = getOrCreateConversation(request.getConversationId());
            Prompt prompt = buildPromptWithContext(request.getMessage(), conversation);
            
            String aiResponse = chatClient.call(prompt)
                .getResult()
                .getOutput()
                .getContent();
            
            conversation.addMessage(request.getMessage(), aiResponse);
            
            // Incrementa contador de sucesso
            meterRegistry.counter("docbot.chat.requests", 
                "status", "success").increment();
            
            // Registra tokens usados
            int tokens = estimateTokens(request.getMessage() + aiResponse);
            meterRegistry.counter("docbot.chat.tokens.used").increment(tokens);
            
            return new ChatResponse(aiResponse, tokens, conversation.getId());
            
        } catch (Exception e) {
            // Incrementa contador de erro
            meterRegistry.counter("docbot.chat.requests", 
                "status", "error").increment();
            throw e;
            
        } finally {
            // Para timer e registra duração
            sample.stop(meterRegistry.timer("docbot.chat.duration"));
        }
    }
    
    // Outros métodos...
}
```

**4. Acessar Métricas**

```bash
# Formato Prometheus
curl http://localhost:8080/actuator/prometheus

# Output:
# docbot_chat_requests_total{status="success",} 127.0
# docbot_chat_requests_total{status="error",} 3.0
# docbot_chat_tokens_used_total 45890.0
# docbot_chat_duration_seconds_sum 234.5
# docbot_chat_duration_seconds_max 5.2
```

**5. Dashboard Grafana (Query Exemplo)**

```promql
# Taxa de requisições por segundo
rate(docbot_chat_requests_total[1m])

# Duração média das requisições
rate(docbot_chat_duration_seconds_sum[5m]) 
/ 
rate(docbot_chat_duration_seconds_count[5m])

# Tokens usados por hora
increase(docbot_chat_tokens_used_total[1h])
```

---

### 💾 FEATURE 4: Cache Inteligente

#### 🎨 Analogia

Cache é como ter um "caderno de cola" com respostas frequentes. Se a pergunta é igual, não precisa "pensar" de novo - só copia a resposta anterior.

#### 💻 Implementação

**1. Adicionar Dependência**

`pom.xml`

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-cache</artifactId>
</dependency>

<dependency>
    <groupId>com.github.ben-manes.caffeine</groupId>
    <artifactId>caffeine</artifactId>
</dependency>
```

**2. Configurar Cache**

`src/main/java/com/seudominio/docbot/config/CacheConfig.java`

```java
package com.seudominio.docbot.config;

import com.github.benmanes.caffeine.cache.Caffeine;
import org.springframework.cache.CacheManager;
import org.springframework.cache.annotation.EnableCaching;
import org.springframework.cache.caffeine.CaffeineCacheManager;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

import java.util.concurrent.TimeUnit;

@Configuration
@EnableCaching
public class CacheConfig {
    
    @Bean
    public CacheManager cacheManager() {
        CaffeineCacheManager cacheManager = new CaffeineCacheManager("chatResponses");
        
        cacheManager.setCaffeine(Caffeine.newBuilder()
            .maximumSize(1000)  // Máximo 1000 entradas
            .expireAfterWrite(1, TimeUnit.HOURS)  // Expira após 1 hora
            .recordStats());  // Habilita estatísticas
        
        return cacheManager;
    }
}
```

**3. Service com Cache**

`ChatService.java` (adicionar método)

```java
import org.springframework.cache.annotation.Cacheable;

@Service
public class ChatService {
    
    // Métodos existentes...
    
    /**
     * NOVO: Método com cache para perguntas simples (sem contexto).
     * 
     * Se a mesma pergunta for feita, retorna resposta cacheada
     * (economiza chamada à API e reduz latência).
     */
    @Cacheable(value = "chatResponses", key = "#message")
    public String chatSimpleWithCache(String message) {
        validateSimpleMessage(message);
        
        // Esta chamada só acontece se não estiver em cache
        return chatClient.call(message);
    }
    
    private void validateSimpleMessage(String message) {
        if (message == null || message.isBlank()) {
            throw new IllegalArgumentException("Mensagem não pode ser vazia");
        }
    }
}
```

**4. Controller com Endpoint Cacheado**

`ChatController.java` (adicionar)

```java
/**
 * NOVO: Endpoint simples com cache.
 * 
 * GET /api/v1/chat/simple?message=Olá
 * 
 * Ideal para FAQs que não precisam de contexto.
 */
@GetMapping("/simple")
public ResponseEntity<String> chatSimple(@RequestParam String message) {
    String response = chatService.chatSimpleWithCache(message);
    return ResponseEntity.ok(response);
}
```

**5. Testando Cache**

```bash
# Primeira chamada (vai à API OpenAI - ~2 segundos)
time curl "http://localhost:8080/api/v1/chat/simple?message=Qual%20a%20capital%20do%20Brasil"
# Response: "A capital do Brasil é Brasília."
# real  0m2.134s

# Segunda chamada (resposta do cache - ~10ms)
time curl "http://localhost:8080/api/v1/chat/simple?message=Qual%20a%20capital%20do%20Brasil"
# Response: "A capital do Brasil é Brasília." (mesma resposta)
# real  0m0.012s  ← 200x mais rápido!
```

**6. Métricas de Cache**

```bash
curl http://localhost:8080/actuator/metrics/cache.gets

# Output:
{
  "name": "cache.gets",
  "measurements": [
    {"statistic": "HIT", "value": 45.0},
    {"statistic": "MISS", "value": 12.0}
  ]
}

# Hit Rate: 45 / (45 + 12) = 78.9%
```

---

### 🔄 FEATURE 5: Múltiplos Modelos (Fallback Strategy)

#### 🎨 Analogia

É como ter 3 chefs na cozinha: se o chef principal está ocupado, o segundo assume. Se ambos estão indisponíveis, o terceiro entra em ação.

#### 💻 Implementação

**1. Configurar Múltiplos Clientes**

`AiConfig.java` (expandir)

```java
package com.seudominio.docbot.config;

import org.springframework.ai.chat.ChatClient;
import org.springframework.ai.openai.OpenAiChatClient;
import org.springframework.ai.anthropic.AnthropicChatClient;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.context.annotation.Primary;

@Configuration
public class AiConfig {
    
    @Value("${spring.ai.openai.api-key}")
    private String openaiKey;
    
    @Value("${spring.ai.anthropic.api-key}")
    private String anthropicKey;
    
    /**
     * Cliente primário: OpenAI GPT-3.5-turbo
     */
    @Bean
    @Primary
    public ChatClient primaryChatClient() {
        // Configuração OpenAI...
        return new OpenAiChatClient(/* ... */);
    }
    
    /**
     * Cliente fallback: Anthropic Claude
     */
    @Bean("fallbackChatClient")
    public ChatClient fallbackChatClient() {
        // Configuração Anthropic...
        return new AnthropicChatClient(/* ... */);
    }
}
```

**2. Service com Fallback**

`src/main/java/com/seudominio/docbot/service/ResilientChatService.java`

```java
package com.seudominio.docbot.service;

import org.springframework.ai.chat.ChatClient;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.stereotype.Service;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

/**
 * Service com estratégia de fallback entre modelos.
 */
@Service
public class ResilientChatService {
    
    private static final Logger log = LoggerFactory.getLogger(ResilientChatService.class);
    
    private final ChatClient primaryClient;
    private final ChatClient fallbackClient;
    
    public ResilientChatService(
            ChatClient primaryClient,
            @Qualifier("fallbackChatClient") ChatClient fallbackClient) {
        this.primaryClient = primaryClient;
        this.fallbackClient = fallbackClient;
    }
    
    /**
     * Tenta primary, se falhar usa fallback.
     */
    public String chat(String message) {
        try {
            log.info("Tentando primary client (OpenAI)...");
            return primaryClient.call(message);
            
        } catch (Exception e) {
            log.warn("Primary client falhou: {}. Usando fallback...", e.getMessage());
            
            try {
                return fallbackClient.call(message);
            } catch (Exception fallbackError) {
                log.error("Fallback também falhou!", fallbackError);
                throw new RuntimeException("Todos os modelos estão indisponíveis");
            }
        }
    }
}
```

**3. Testando Fallback**

```bash
# Simular falha da OpenAI (API key inválida temporariamente)
curl -X POST http://localhost:8080/api/v1/chat/resilient \
  -H "Content-Type: application/json" \
  -d '{"message":"Teste de fallback"}'

# Logs:
# INFO  - Tentando primary client (OpenAI)...
# WARN  - Primary client falhou: 401 Unauthorized. Usando fallback...
# INFO  - Fallback (Anthropic) processou com sucesso

# Response (vem do Claude):
{
  "response": "Teste de fallback bem-sucedido!",
  "model_used": "claude-2"
}
```

---

## ⚠️ ARMADILHAS COMUNS

### ❌ 1. Não Limitar Histórico de Conversação

**Problema:**

```java
// Conversação com 100 mensagens
// Prompt final: 10.000 tokens
// Custo: $0.15 POR MENSAGEM! 💸
```

**Solução:**

```java
public String getContextHistory() {
    // Limita aos últimos 10 pares de mensagens
    int start = Math.max(0, messages.size() - 10);
    List<MessagePair> recentMessages = messages.subList(start, messages.size());
    
    StringBuilder context = new StringBuilder();
    for (MessagePair pair : recentMessages) {
        context.append("Usuário: ").append(pair.getUserMessage()).append("\n");
        context.append("Assistente: ").append(pair.getAiResponse()).append("\n");
    }
    return context.toString();
}
```

### ❌ 2. Não Tratar Timeouts

**Problema:**

```java
// Usuário espera 60 segundos, nada acontece
String response = chatClient.call(prompt);  // Timeout sem tratamento
```

**Solução:**

```java
@Bean
public ChatClient chatClient() {
    // ...
    RestTemplate restTemplate = new RestTemplate();
    restTemplate.setRequestFactory(new HttpComponentsClientHttpRequestFactory() {{
        setConnectTimeout(10_000);  // 10 segundos
        setReadTimeout(30_000);     // 30 segundos
    }});
    // ...
}
```

### ❌ 3. Expor Informações Sensíveis em Logs

**Problema:**

```java
log.info("Processando mensagem: {}", request.getMessage());
// Usuário enviou: "Meu CPF é 123.456.789-00"
// Agora está no log! 🚨
```

**Solução:**

```java
log.info("Processando mensagem (tamanho: {})", request.getMessage().length());
// Log seguro, não expõe conteúdo
```

---

## 🚀 BOAS PRÁTICAS PROFISSIONAIS

### ✅ 1. Versionamento de API

```java
@RestController
@RequestMapping("/api/v1/chat")  // v1 explícito
public class ChatController {
    // Quando mudar breaking changes, crie v2
}

// Futuro: /api/v2/chat com mudanças incompatíveis
```

### ✅ 2. Health Checks Customizados

```java
package com.seudominio.docbot.health;

import org.springframework.ai.chat.ChatClient;
import org.springframework.boot.actuate.health.Health;
import org.springframework.boot.actuate.health.HealthIndicator;
import org.springframework.stereotype.Component;

@Component
public class AiHealthIndicator implements HealthIndicator {
    
    private final ChatClient chatClient;
    
    public AiHealthIndicator(ChatClient chatClient) {
        this.chatClient = chatClient;
    }
    
    @Override
    public Health health() {
        try {
            // Testa com prompt simples
            chatClient.call("ping");
            return Health.up()
                .withDetail("model", "gpt-3.5-turbo")
                .withDetail("status", "operational")
                .build();
        } catch (Exception e) {
            return Health.down()
                .withDetail("error", e.getMessage())
                .build();
        }
    }
}
```

```bash
curl http://localhost:8080/actuator/health

# Response:
{
  "status": "UP",
  "components": {
    "ai": {
      "status": "UP",
      "details": {
        "model": "gpt-3.5-turbo",
        "status": "operational"
      }
    }
  }
}
```

### ✅ 3. Documentação com OpenAPI/Swagger

`pom.xml`

```xml
<dependency>
    <groupId>org.springdoc</groupId>
    <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
    <version>2.3.0</version>
</dependency>
```

`ChatController.java` (adicionar anotações)

```java
import io.swagger.v3.oas.annotations.Operation;
import io.swagger.v3.oas.annotations.tags.Tag;

@RestController
@RequestMapping("/api/v1/chat")
@Tag(name = "Chat", description = "API de conversação com IA")
public class ChatController {
    
    @PostMapping
    @Operation(
        summary = "Envia mensagem para o chatbot",
        description = "Processa mensagem do usuário e retorna resposta da IA"
    )
    public ResponseEntity<ChatResponse> chat(@Valid @RequestBody ChatRequest request) {
        // ...
    }
}
```

Acesse: http://localhost:8080/swagger-ui.html

---

## ✅ CHECKLIST DE DOMÍNIO DO CAPÍTULO 3

- [ ] Compreendo a arquitetura em camadas (Controller → Service → ChatClient)
- [ ] Sei criar conversações com histórico contextual
- [ ] Implementei streaming de respostas em tempo real
- [ ] Configurei rate limiting para proteção da API
- [ ] Adicionei métricas e monitoramento
- [ ] Implementei cache para otimização de performance
- [ ] Criei estratégia de fallback entre modelos
- [ ] Entendo o fluxo completo de uma requisição
- [ ] Sei calcular custos aproximados de tokens
- [ ] Aplico boas práticas de segurança (API keys, validação, logs)

---

## 🔗 CONECTANDO OS PONTOS

**O que vimos neste capítulo:**
- Anatomia completa de uma aplicação Spring AI profissional
- Chatbot funcional com conversações contextuais
- Features avançadas (streaming, rate limiting, cache, fallback)
- Fluxo detalhado de requisições e custos

**O que vem a seguir (Capítulo 4):**
- Fundamentos profundos: Models, Prompts, Tokens, Responses
- Como escolher o modelo certo para cada caso de uso
- Prompt engineering: transformar perguntas ruins em excelentes
- Otimização de tokens para reduzir custos

**Projeto DocBot - Estado Atual:**
Agora temos um chatbot robusto com:
- ✅ API REST completa
- ✅ Gerenciamento de conversações
- ✅ Streaming em tempo real
- ✅ Proteções de produção
- ✅ Observabilidade completa

No próximo capítulo, vamos aprofundar nos **conceitos fundamentais** que tornarão você um expert em controlar o comportamento da IA.

---

## 📝 RESUMO EM BULLETS

- **Arquitetura:** Controller → Service → ChatClient (separação clara)
- **Conversações:** Use ConversationManager para manter contexto
- **Streaming:** Flux reativo com Server-Sent Events
- **Rate Limiting:** Bucket4j protege contra abuso (10 req/min default)
- **Métricas:** Micrometer + Prometheus para observabilidade
- **Cache:** Caffeine reduz latência e custos em 200x
- **Fallback:** Múltiplos modelos garantem resiliência
- **Custos:** Limite histórico de conversações (max 10 mensagens)
- **Segurança:** Nunca logue conteúdo sensível de usuários
- **Próximo nível:** Dominar prompts e tokens

💡 **DICA PRO:** Em produção, substitua ConcurrentHashMap por Redis para conversações persistentes e distribuídas.

---

<div style="page-break-after: always;"></div>
