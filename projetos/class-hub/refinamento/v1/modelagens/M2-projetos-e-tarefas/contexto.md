# Modelagem M2 - Projetos e tarefas

## Objetivo
Representar a estrutura de trabalho acadêmico e os vínculos a turmas e alunos.

## Entidades principais
### Projeto
- id
- titulo
- descricao
- dataInicio
- dataFim

### Tarefa
- id
- titulo
- descricao
- prazo
- status
- prioridade

## Relacionamentos
- Projeto 1:N Tarefa
- Usuário N:N Projeto
- Projeto 1:1 Equipe

## Regras
- Projeto acadêmico = trabalho/tarefa.
- Turma agrupa os alunos e projetos vinculados.
- Tarefa é a unidade de execução e avaliação.

## Dependências
- depende de M1
- sustenta entrega e feedback
