# Parte P1 - Autenticação e identidade

## Objetivo
Garantir que alunos, professores e administradores tenham acesso seguro à plataforma com base em matrícula e senha, além de perfil específico.

## Escopo
- cadastro de usuários
- login
- logout
- recuperação de senha
- controle de acesso por perfil
- matrícula única por aluno

## Dependências
- Base para todas as operações da plataforma
- Dependente de modelagem de usuário

## Entradas
- matrícula
- senha
- perfil do usuário

## Saídas
- token ou sessão autenticada
- resposta de login/logout
- erro de credenciais

## Regras de negócio
- Cada matrícula corresponde a um único aluno.
- O professor também terá matrícula com role específica.
- O acesso será controlado pela role do perfil.

## Critérios de aceite
- Dado que o aluno possui matrícula e senha válidas, quando acessa a plataforma, então deve conseguir entrar no sistema.
- Dado que uma matrícula já está vinculada a um aluno, quando outra pessoa tentar usar a mesma matrícula, então o cadastro deve ser rejeitado.

## Dúvidas e riscos
- Recuperação de senha e política de sessão ainda precisam ser confirmadas.
