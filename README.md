classDiagram
 class JanelaInicial {
    }

    class Administracao {
    }

    class GerenciadorDados {
    }

    class ControleAluno {
    }

    class Aluno {
        - nome: string
        - matricula: int
        - dataNascimento: datetime
        - endereco: string
        - telefone: string
    }

    class Disciplina {
        - nome: string
        - codigo: string
        - cargaHoraria: int
        - professorResponsavel: string
    }

    class Atividade {
        - nome: string
        - tipo: string
        - dataEntrega: datetime
    }

    class Turma {
        - codigo: string
        - periodo: string
        - horario: string
        - alunosMatriculados: list
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

