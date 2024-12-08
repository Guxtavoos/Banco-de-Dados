

# Pacotes PL/SQL para Gestão Acadêmica

## Estrutura dos Pacotes

1. PKG_ALUNO
Descrição: Gerencia operações relacionadas aos alunos.
Funcionalidades:
delete_aluno(p_id_aluno IN NUMBER): Exclui um aluno e seus registros associados na tabela matriculas.
Cursor c_alunos_maiores_18: Retorna os alunos com mais de 18 anos.
Cursor c_alunos_por_curso(p_id_curso IN NUMBER): Retorna os alunos matriculados em um curso específico.

2. PKG_DISCIPLINA
Descrição: Gerencia disciplinas e matrículas de alunos em disciplinas.
Funcionalidades:
insert_disciplina(p_nome IN VARCHAR2, p_descricao IN VARCHAR2, p_carga_horaria IN NUMBER): Insere uma nova disciplina.
Cursor c_total_alunos_por_disciplina: Lista disciplinas com mais de 10 alunos matriculados.
Cursor c_media_idade_por_disciplina(p_id_disciplina IN NUMBER): Calcula a idade média dos alunos em uma disciplina específica.
list_alunos_disciplina(p_id_disciplina IN NUMBER): Lista os nomes dos alunos matriculados em uma determinada disciplina.

3. PKG_PROFESSOR
Descrição: Gerencia dados relacionados aos professores.
Funcionalidades:
Cursor c_total_turmas_por_professor: Lista professores que lecionam mais de uma turma.
get_total_turmas_professor(p_id_professor IN NUMBER): Retorna o total de turmas que um professor leciona.
get_professor_disciplina(p_id_disciplina IN NUMBER): Retorna o nome do professor que leciona uma disciplina específica.

## Execução
Prepare o Ambiente Oracle:
Certifique-se de ter acesso a uma instância do banco de dados Oracle. Utilize ferramentas como SQL*Plus ou Oracle SQL Developer para conexão ao banco de dados.

Verifique os Pré-requisitos do Banco de Dados:
Certifique-se de que as seguintes tabelas existem no esquema:

alunos: Deve conter as colunas id_aluno, nome e data_nascimento.
matriculas: Deve conter as colunas id_aluno, id_curso e id_disciplina.
disciplinas: Deve conter as colunas id_disciplina, nome, descricao e carga_horaria.
professores: Deve conter as colunas id_professor e nome.
turmas: Deve conter as colunas id_turma, id_professor e id_disciplina.
Execute o Script:
Abra o arquivo SQL contendo o script e execute-o em sua ferramenta cliente. Cada pacote e seu corpo serão criados no esquema.
