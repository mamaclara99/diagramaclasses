⁠```mermaid
classDiagram
    
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

class JanelaInicial {
        - atributo(privado por causa do -): tipo=estado inicial(se existir)
        + metodo(tipo de cada parametro) tipo de retorno [publico por causa do +]
    }
```
