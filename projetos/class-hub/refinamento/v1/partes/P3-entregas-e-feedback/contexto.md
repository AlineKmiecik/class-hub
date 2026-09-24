# Parte P3 - Entregas e feedback

## Objetivo
Registrar entregas, permitir atualização antes do prazo, acompanhar histórico e avaliar o resultado com nota e feedback.

## Escopo
- envio de documentos
- comentário e anexos
- versionamento da entrega
- histórico de entregas
- avaliação
- feedback
- aprovação ou ajuste

## Dependências
- depende da parte de autenticação
- depende da parte de tarefas e projetos

## Entradas
- tarefa vinculada
- arquivos anexados
- comentários
- participantes da entrega
- nota e feedback do professor

## Saídas
- entrega registrada
- versão atualizada
- notificação enviada
- avaliação registrada

## Regras de negócio
- O aluno pode realizar entregas para tarefas do professor.
- O aluno pode incluir anexos e comentários em uma entrega.
- O aluno pode atualizar a entrega enquanto a tarefa estiver em aberto.
- A data de criação da primeira entrega e a data de manutenção da atualização devem ser preservadas.
- Em tarefas em grupo, o aluno pode incluir outros alunos por matrícula.

## Critérios de aceite
- Dado que o aluno está vinculado a uma tarefa aberta, quando ele envia uma entrega com anexo e comentário, então a entrega deve ser registrada com sucesso.
- Dado que a tarefa ainda está em aberto, quando o aluno altera a entrega, então a nova versão deve substituir a anterior e registrar a data de manutenção.
- Dado que a tarefa passou da data limite, quando o aluno tentar reenviar a entrega, então o sistema deve bloquear a ação e exibir mensagem de prazo encerrado.
- Dado que a entrega foi submetida, quando o professor acessa a tarefa, então ele deve visualizar o conteúdo, anexos, comentários e participantes.
- Dado que a entrega foi analisada, quando o professor registra nota e feedback, então o aluno deve receber a avaliação.

## Dúvidas e riscos
- Política de retenção histórica da entrega ainda precisa ser confirmada.
