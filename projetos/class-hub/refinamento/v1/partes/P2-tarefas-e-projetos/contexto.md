# Parte P2 - Gestão de projetos e tarefas

## Objetivo
Organizar tarefas e projetos acadêmicos, vinculando-os à turma e ao professor responsável.

## Escopo
- criação de projetos
- vinculação de integrantes
- criação de tarefas
- atribuição de responsáveis
- prazo e status
- atualização de status

## Dependências
- depende da identidade e do papel do usuário
- precede a parte de entregas

## Entradas
- dados do projeto
- dados da tarefa
- responsáveis
- turma associada

## Saídas
- projeto criado
- tarefa criada
- tarefa atualizada
- status refletido ao projeto

## Regras de negócio
- Projeto acadêmico = trabalho/tarefa.
- Turma é o agrupamento de alunos que compartilham tarefas/projetos.
- O professor é responsável pelo acompanhamento das tarefas vinculadas.

## Critérios de aceite
- Dado que uma turma foi criada, quando o professor vincula tarefas ou projetos a essa turma, então somente os alunos daquela turma devem ter acesso.
- Dado que o aluno está vinculado a uma tarefa aberta, quando ele executa a atividade e atualiza o status, então o projeto deve refletir a mudança.

## Dúvidas e riscos
- A regra final de criação e atualização de tarefas por aluno e professor precisa ser confirmada.
