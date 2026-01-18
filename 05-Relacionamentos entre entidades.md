📚 Capítulo 5: Relacionamentos Entre Entidades e Associações
📋 Tópicos deste Capítulo
 * A Teoria Relacional: Cardinalidade e Normalização
 * Associações no JPA: A Questão da Direcionalidade
 * Implementando @ManyToOne (Muitos para Um)
 * O Dilema do Carregamento: Lazy vs. Eager
 * Adaptação dos DTOs e Service
 * Conclusão
🎯 Objetivos do Capítulo
 * Compreender a discrepância entre associações de objetos (referências) e relacionamentos de banco de dados (chaves estrangeiras).
 * Implementar o relacionamento Um-para-Muitos entre Usuários e Tarefas.
 * Dominar o uso das anotações @ManyToOne e @JoinColumn.
 * Analisar o impacto de performance das estratégias de carregamento (FetchType).
 * Refatorar DTOs para manipular relacionamentos via IDs.
1. A Teoria Relacional: Cardinalidade e Normalização
Até este ponto, nossas Tarefas existiam em um vácuo. Em um sistema real, dados raramente são órfãos; eles pertencem a alguém ou a algo. Para modelar isso, precisamos introduzir o conceito de Relacionamento.
Vamos introduzir uma nova Entidade: Usuario. A relação lógica é: "Um Usuário pode possuir muitas Tarefas, mas uma Tarefa pertence a apenas um Usuário".
Na Teoria dos Conjuntos e Modelagem de Dados, chamamos isso de Cardinalidade 1:N (Um-para-Muitos).
1.1 O Abismo Estrutural
Aqui, a Impedância Objeto-Relacional (discutida no Cap. 2) se manifesta novamente com força:
 * No Banco de Dados (SQL): A relação é definida pela Chave Estrangeira (Foreign Key). A tabela tb_tarefas terá uma coluna usuario_id. O banco "não sabe" que o usuário tem uma lista; ele só sabe que a tarefa aponta para um usuário.
 * Na Memória (Java): Objetos se relacionam através de Referências. O objeto Tarefa pode ter um campo Usuario, e o objeto Usuario pode ter uma List<Tarefa>.
2. Associações no JPA: A Questão da Direcionalidade
No JPA, podemos modelar esse relacionamento de duas formas:
 * Unidirecional: Apenas um lado "conhece" o outro (ex: A Tarefa sabe quem é seu dono, mas o Usuário não tem uma lista de tarefas).
 * Bidirecional: Ambos os lados possuem referências um para o outro.
Para manter a integridade do sistema e seguir o princípio do Owning Side (Lado Proprietário), focaremos na relação física real: A Tarefa aponta para o Usuário.
> Conceito Fundamental (Lado Proprietário): Em um relacionamento de banco de dados, o "dono" da relação é sempre a tabela que segura a Chave Estrangeira (neste caso, a Tarefa).
> 
3. Implementando @ManyToOne (Muitos para Um)
Primeiro, vamos criar a entidade Usuario (simplificada para focar no relacionamento).
3.1 A Entidade Usuario
package com.exemplo.api.model;

import jakarta.persistence.*;

@Entity
@Table(name = "tb_usuarios")
public class Usuario {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(unique = true, nullable = false)
    private String email;

    // Construtores, Getters e Setters omitidos por brevidade
    public Usuario() {}
    public Usuario(Long id) { this.id = id; } // Útil para criar referências apenas com ID
}

3.2 Atualizando a Entidade Tarefa
Agora, alteramos a Tarefa para incluir a referência ao Usuario.
package com.exemplo.api.model;

import jakarta.persistence.*;

@Entity
@Table(name = "tb_tarefas")
public class Tarefa {
    
    // ... atributos anteriores (id, descricao, etc)

    // A ANOTAÇÃO CRUCIAL DO CAPÍTULO:
    @ManyToOne(fetch = FetchType.LAZY) // Explicaremos o LAZY na seção 4
    @JoinColumn(name = "usuario_id")   // Define o nome da coluna no banco (Foreign Key)
    private Usuario usuario;

    // Getter e Setter para o usuario
    public Usuario getUsuario() { return usuario; }
    public void setUsuario(Usuario usuario) { this.usuario = usuario; }
}

Ao rodar o projeto, o Hibernate executará:
ALTER TABLE tb_tarefas ADD COLUMN usuario_id BIGINT;
ALTER TABLE tb_tarefas ADD CONSTRAINT fk_usuario FOREIGN KEY (usuario_id) REFERENCES tb_usuarios(id);
4. O Dilema do Carregamento: Lazy vs. Eager
Note que utilizamos fetch = FetchType.LAZY na anotação @ManyToOne. Esta é, possivelmente, a decisão de design mais importante em termos de performance.
O JPA oferece duas estratégias para carregar dados relacionados:
 * Eager (Ansioso): Quando você busca uma Tarefa, o JPA imediatamente faz outro SELECT (ou um JOIN) para buscar o Usuário.
   * Problema: Se você buscar 1.000 tarefas, pode acabar trazendo 1.000 usuários desnecessariamente.
 * Lazy (Preguiçoso): Quando você busca uma Tarefa, o campo usuario vem como um Proxy (um objeto fantasma). O SELECT do usuário só é executado se (e somente se) você chamar tarefa.getUsuario().getEmail().
> Regra de Ouro da Performance: Por padrão, relacionamentos @ManyToOne são EAGER no JPA. Sempre altere para LAZY explicitamente, a menos que você tenha uma prova concreta de que precisa dos dados sempre.
> 
5. Adaptação dos DTOs e Service
Agora temos um problema de arquitetura: nosso TarefaRequestDTO (criado no Cap. 3) não sabe nada sobre usuários. O cliente da API não envia o objeto Usuário completo; ele envia apenas o ID do usuário.
Precisamos refatorar o fluxo de criação.
5.1 Atualizando o Request DTO
package com.exemplo.api.dto;

import jakarta.validation.constraints.NotNull;

public record TarefaRequestDTO(
    String descricao,
    
    @NotNull(message = "O ID do usuário é obrigatório")
    Long usuarioId
) {}

5.2 Refatorando o Service
O TarefaService agora tem uma nova responsabilidade: validar se o usuário existe antes de salvar a tarefa. Para isso, precisaremos injetar o UsuarioRepository (supondo que já o criamos de forma análoga ao TarefaRepository).
@Service
public class TarefaService {

    private final TarefaRepository tarefaRepository;
    private final UsuarioRepository usuarioRepository; // Nova dependência

    public TarefaService(TarefaRepository tr, UsuarioRepository ur) {
        this.tarefaRepository = tr;
        this.usuarioRepository = ur;
    }

    @Transactional
    public TarefaResponseDTO criar(TarefaRequestDTO dados) {
        // 1. Buscamos o usuário no banco (Validação de Integridade Referencial)
        Usuario usuario = usuarioRepository.findById(dados.usuarioId())
                .orElseThrow(() -> new RecursoNaoEncontradoException("Usuário não encontrado"));

        // 2. Criamos a tarefa e associamos ao usuário recuperado
        Tarefa novaTarefa = new Tarefa();
        novaTarefa.setDescricao(dados.descricao());
        novaTarefa.setUsuario(usuario); // Associação do Objeto

        // 3. Salvamos
        Tarefa salva = tarefaRepository.save(novaTarefa);
        
        return new TarefaResponseDTO(salva);
    }
}

5.3 O Problema da Serialização (Loop Infinito)
Se retornássemos a Entidade Tarefa no Controller, o Jackson (serializador JSON) tentaria serializar a Tarefa, que tem um Usuário, que poderia ter uma lista de Tarefas... gerando um StackOverflowError.
Como estamos usando o padrão DTO (TarefaResponseDTO), estamos protegidos! Só precisamos garantir que o DTO retorne apenas o que interessa (ex: o ID ou o email do usuário, não o objeto inteiro).
// Atualizando o Response DTO para incluir info básica do dono
public record TarefaResponseDTO(
    Long id,
    String descricao,
    Long usuarioId // Retornamos apenas o ID para manter a resposta leve
) {
    public TarefaResponseDTO(Tarefa t) {
        this(t.getId(), t.getDescricao(), t.getUsuario().getId());
    }
}

6. Conclusão
Neste capítulo, elevamos a complexidade do nosso modelo de dados. Saímos de entidades isoladas para um grafo de objetos conectados.
Aprendemos que:
 * Chaves Estrangeiras são representadas por composições de objetos em Java.
 * A anotação @ManyToOne com @JoinColumn materializa essa relação.
 * O carregamento LAZY é vital para evitar que nossa aplicação "sufoque" o banco de dados carregando dados desnecessários.
 * O Service atua como o orquestrador que une duas entidades distintas (Usuario e Tarefa) para realizar uma operação de negócio.
Agora que nosso sistema possui relacionamentos, surge uma nova necessidade: Como buscar tarefas apenas de um usuário específico? Ou Como buscar tarefas que contenham a palavra 'Urgente'?
No próximo capítulo, exploraremos o poder das Query Methods do Spring Data e JPQL para realizar consultas avançadas.