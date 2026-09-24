# Pendências da versão v1

## Status
- Versão: v1
- Data: 2026-09-24
- A pendência permanece explicitamente documentada e não foi convertida em regra definitiva

## Pendências confirmadas como abertas
### P1. Autorização de tarefas por perfil
O escopo tem uma divergência entre:
- alunos podem criar/atualizar tarefas em um bloco de permissões;
- o fluxo principal e a visão geral tendem a atribuir a gestão de tarefas ao professor.

### P2. Cardinalidade entre turma e projeto
A solução usa "turma" e "projeto" em contextos diferentes; a regra de vínculo entre ambos permanece a ser confirmada em design final.

### P3. Recuperação e segurança de autenticação
O escopo confirma matrícula e senha, mas não detalha:
- política de recuperação de senha;
- expiração de sessões;
- controle de acesso por curso, turma ou projeto;
- autenticação multifator, se aplicável.

### P4. Fluxo de notificação
O escopo informa notificações, mas não define canal exato e comportamento de disparo.

### P5. Versionamento e retenção de entregas
A regra de overwriting foi confirmada, mas a política de retenção histórica e limitação de versões ainda precisa ser validada.

## Riscos
- Ambiguidade entre papéis e permissões pode gerar inconsistência na implementação.
- Duplicidade conceitual entre turma e projeto pode afetar modelagem e acesso.
- Falta de regras de autorização bem definidas pode comprometer segurança.

## Ações recomendadas
1. Confirmar a regra final de criação/atualização de tarefas por perfil.
2. Definir se cada tarefa pertence sempre a um projeto associado a uma turma.
3. Especificar canais de notificação e critério de disparo.
4. Definir política de retenção de versões da entrega.

## Status final
As pendências não bloquearam a criação do refinamento inicial, mas continuam como itens de confirmação antes da fase de implementação.
