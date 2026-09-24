# Modelagem M3 - Entregas e feedback

## Objetivo
Registrar a entrega do aluno, manter o histórico de versões e armazenar a avaliação do professor.

## Entidades principais
### Entrega
- id
- titulo
- arquivo
- dataEnvio
- versao
- dataCriacao
- dataManutencao

### Feedback
- id
- comentario
- data

## Relacionamentos
- Projeto 1:N Entrega
- Entrega 1:N Feedback

## Regras
- A entrega pode ser repostada até a data limite da tarefa.
- A regra de overwriting deve manter a data de criação e a data de manutenção.
- Em tarefa em grupo, a entrega pode conter participantes vinculados por matrícula.

## Dependências
- depende de M1 e M2
- integra com avaliação do professor

## Observação
A regra de retenção histórica completa da entrega deve ser confirmada em próxima etapa.
