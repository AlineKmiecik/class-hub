# Modelagem M1 - Usuários

## Objetivo
Definir a identidade dos usuários e o vínculo com as matrículas.

## Entidade principal
### Usuário
- id
- nome
- email
- senha
- perfil
- matricula

## Regras
- Cada matrícula pertence a um único aluno.
- O professor também terá matrícula, com perfil específico.
- O administrador terá perfil independente.

## Dependências
- Base para autenticação e acesso
- Vinculada a turma, projeto e entrega

## Regras de integridade
- matricula deve ser única no sistema
- email deve ser único por usuário
- perfil deve ser obrigatório
