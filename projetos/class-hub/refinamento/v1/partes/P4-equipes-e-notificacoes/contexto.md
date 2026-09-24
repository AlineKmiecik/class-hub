# Parte P4 - Equipes e notificações

## Objetivo
Permitir organização de equipes dentro das turmas e comunicar eventos relevantes aos usuários.

## Escopo
- criação de equipes
- entrada de alunos em equipes
- gerenciamento de equipe pelo professor
- notificações de tarefa, feedback, prazo e aprovação/reprovação

## Dependências
- depende das partes anteriores
- depende da modelagem de usuários e tarefas

## Entradas
- dados da equipe
- matrícula dos participantes
- evento de tarefa, feedback ou prazo

## Saídas
- equipe registrada
- participante associado
- notificação disparada

## Regras de negócio
- Alunos podem criar e entrar em equipes.
- Professor pode gerenciar as equipes.
- Notificações devem ser disparadas com base em eventos relevantes.

## Critérios de aceite
- Dado que a tarefa é de grupo, quando o aluno incluir participantes com matrícula válida, então os alunos vinculados devem ser associados à entrega.
- Dado que há atualização relevante na tarefa, quando a entrega for avaliada ou houver prazo próximo, então a notificação deve ser enviada ao destinatário correto.

## Dúvidas e riscos
- Canal e critério de disparo das notificações ainda precisam ser confirmados.
