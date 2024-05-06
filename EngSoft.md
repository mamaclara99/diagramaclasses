Vc colocou no começo:
```mermaid
classDiagram
 class JanelaInicial {
        + abrirJanela(): void
        + fecharJanela(): void
    }

    class Administracao {
        + adicionarUsuario(): void
        + removerUsuario(): void
    }

    class GerenciadorDados {
        + adicionarDados(): void
        + removerDados(): void
        + buscarDados(): void
    }

    class ControleAluno {
        + adicionarAluno(): void
        + removerAluno(): void
        + atualizarAluno(): void
    }

    class Aluno {
        - nome: string
        - matricula: int
        - dataNascimento: datetime
        - endereco: string
        - telefone: string
        + visualizarInformacoes(): void
        + atualizarInformacoes(): void
    }

    class Disciplina {
        - nome: string
        - codigo: string
        - cargaHoraria: int
        - professorResponsavel: string
        + adicionarDisciplina(): void
        + removerDisciplina(): void
        + atualizarDisciplina(): void
    }

    class Atividade {
        - nome: string
        - tipo: string
        - dataEntrega: datetime
        + adicionarAtividade(): void
        + removerAtividade(): void
        + atualizarAtividade(): void
    }

    class Turma {
        - codigo: string
        - periodo: string
        - horario: string
        - alunosMatriculados: list
        + criarTurma(): void
        + removerTurma(): void
        + matricularAluno(): void
    }
    class GeradorRelatorio {
        +criarRelatorio
        +editarRelatorio
    }
    JanelaInicial o-- Administracao
    JanelaAlunos o-- JanelaInicial
    JanelaDisciplinas o-- JanelaInicial
    JanelaTurmas o-- JanelaInicial
    JanelaAulas o-- JanelaInicial
    JanelaAtividades o--JanelaInicial
    Executar o-- JanelaInicial
    JanelaInicial --o JanelaRelatorios
    GeradorRelatorios --> JanelaRelatorios

    Administracao o-- GerenciadorDados
    GerenciadorDados <-- DadosAluno    
    GerenciadorDados <-- DadosDisciplina
    GerenciadorDados <-- DadosTurma
    GerenciadorDados <-- DadosAula
    GerenciadorDados <-- DadosAtividade

    Administracao o-- GeradorRelatorios
    Administracao o-- ControleAluno    
    Administracao o-- ControleDisciplina
    Administracao o-- ControleTurma
    Administracao o-- ControleAula
    Administracao o-- ControleAtividade
    
    ControleAluno o-- Aluno   
    ControleDisciplina o-- Disciplina
    ControleTurma o-- Turma
    ControleAula o-- Aula
    ControleAtividade o-- Atividade 

    Atividade <-- Disciplina
    Aluno <-- Turma
    Disciplina <-- Aula
```
