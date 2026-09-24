# Decisões aprovadas

## Status
- Versão: v1
- Data: 2026-09-24
- Situação: decisões confirmadas para uso no refinamento inicial

## Confirmado
### D1. Definição de turma e projeto
- Projeto acadêmico = trabalho/tarefa
- Turma = grupo de alunos que compartilham tarefas/projetos vinculados

### D2. Autenticação por matrícula
- A autenticação da plataforma será baseada em matrícula e senha.
- Cada matrícula será exclusiva para um aluno.
- Professor também terá matrícula, com role diferente.

### D3. Entrega e overwriting
- O aluno pode enviar entrega até a data limite da tarefa.
- O aluno pode alterar a entrega antes do prazo.
- A regra de overwriting será mantida.
- Deve existir data de criação da primeira entrega e data de manutenção da última atualização.

### D4. Entrega em grupo
- Em tarefas em grupo, o aluno pode incluir outros alunos por matrícula na entrega.
- A associação dos participantes deve ser explicitamente registrada.

### D5. Modelo de arquitetura
- A aplicação seguirá arquitetura em camadas: frontend, backend e banco de dados.
- A comunicação será via API REST.

### D6. Modelo de papéis
- Aluno, professor e administrador são os papéis principais.
- Cada perfil possui permissões específicas conforme definido no escopo.

## Proposta do agente
### P1. Regras finais de autorização por projeto e turma
- O agente sugere validar se o acesso a tarefas e entregas será por turma, por projeto ou por ambos.
- Essa decisão é proposta e depende de confirmação antes de ser tratada como regra definitiva.

### P2. Definição da regra de tarefas por perfil
- O escopo menciona criação e atualização de tarefas por aluno em alguns trechos, mas o fluxo principal aponta professor como responsável.
- Sugestão: confirmar se alunos podem apenas responder/participar de tarefas ou também criar/alterá-las.

## Pendente
- Definição final da regra de autorização por contexto.
- Confirmar se a gestão de tarefas é exclusiva do professor ou compartilhada com alunos em certos casos.
- Validar se o fluxo de notificações inclui email, push, banner ou apenas registro interno.

## Rejeitado
- Nenhuma decisão técnica ou de negócio foi registrada como regra sem aprovação do usuário.
