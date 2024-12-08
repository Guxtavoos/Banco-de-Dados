

# Pacotes PL/SQL para Gestão Acadêmica

## Estrutura dos Pacotes

### PKG_ALUNO
- **ExcluirAluno**: Exclui um aluno e suas matrículas associadas.
- **ListarAlunos18Anos**: Lista alunos com idade superior a 18 anos.
- **ListarAlunosPorCurso**: Lista alunos matriculados em um curso.

### PKG_DISCIPLINA
- **CadastrarDisciplina**: Cadastra uma nova disciplina.
- **TotalAlunosPorDisciplina**: Lista disciplinas com mais de 10 alunos.
- **MediaIdadePorDisciplina**: Calcula a média de idade dos alunos de uma disciplina.
- **ListarAlunosDisciplina**: Lista alunos matriculados em uma disciplina.

### PKG_PROFESSOR
- **TotalTurmasProfessor**: Retorna o total de turmas de um professor.
- **ProfessorDisciplina**: Retorna o professor de uma disciplina.
- **TotalTurmasPorProfessor**: Lista professores com mais de uma turma.

## Execução
1. Conecte-se ao Oracle utilizando o `SQL*Plus`.
2. Execute o script `pacotes.sql`.
3. Ative o `DBMS_OUTPUT` para visualizar saídas de cursores e procedures:
   ```sql
   SET SERVEROUTPUT ON;
