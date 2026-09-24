# Contexto geral - Class Hub

## Status
- Versão: v1
- Data: 2026-09-24
- Status geral: confirmado para refinamento inicial

## Objetivo
A plataforma Class Hub tem como objetivo apoiar o gerenciamento de projetos acadêmicos em contexto de ensino, permitindo a organização de turmas, tarefas, entregas, avaliações e comunicação entre professores, alunos e administradores.

## Problema a resolver
A solução deve centralizar a gestão de atividades acadêmicas em uma aplicação web, com controle de acesso por perfil, organização de tarefas e projetos, registro de entregas, avaliação, feedback e acompanhamento de desempenho.

## Escopo confirmado
- Gestão de turmas
- Gestão de projetos acadêmicos / tarefas
- Autenticação com matrícula e senha
- Entrega de atividades por alunos
- Avaliação e feedback do professor
- Dashboard por perfil
- Notificações de tarefas, prazos e avaliações
- Controle de acesso por tipo de usuário
- Arquitetura em camadas: frontend, backend, banco de dados

## Usuários e perfis
### Aluno
- Possui matrícula única
- Pode entrar em turmas
- Pode consultar tarefas e projetos vinculados
- Pode enviar entregas com anexos e comentários
- Pode atualizar a entrega enquanto a tarefa estiver em aberto
- Pode incluir outros alunos em entregas de grupo por matrícula
- Pode consultar notas e feedbacks

### Professor
- Possui matrícula única com role específica
- Pode gerir tarefas e projetos vinculados a turmas
- Pode acompanhar entregas
- Pode registrar nota e feedback
- Pode aprovar ou reprovar etapas
- Pode acompanhar evolução dos alunos

### Administrador
- Pode gerenciar usuários
- Pode gerenciar acessos
- Pode gerenciar cursos
- Pode consultar todos os projetos
- Pode gerar relatórios institucionais

## Relação entre turma e projeto
Informação confirmada pelo usuário:
- Projeto acadêmico = trabalho/tarefa
- Turma = grupo de alunos que compartilham tarefas/projetos vinculados

## Fluxos principais confirmados
### Fluxo 1 - Criação de projeto
Aluno cria projeto -> Convida integrantes -> Professor é vinculado -> Projeto criado

### Fluxo 2 - Execução de atividade
Líder cria tarefa -> Aluno recebe tarefa -> Executa atividade -> Atualiza status -> Projeto é atualizado

### Fluxo 3 - Entrega
Aluno envia entrega -> Professor recebe notificação -> Professor analisa -> Aprova ou solicita ajuste

### Fluxo 4 - Encerramento
Todas as etapas concluídas -> Professor aprova projeto -> Projeto finalizado -> Histórico arquivado

## Arquitetura confirmada
### Frontend
- Interface web para alunos, professores e administradores
- Dashboards e telas de projetos, tarefas, entregas e avaliações
- Comunicação via API REST

### Backend
- Regras de negócio
- Autenticação e segurança
- Controle do fluxo das atividades
- Notificações
- Acesso aos dados

### Banco de Dados
- Usuários
- Projetos
- Tarefas
- Entregas
- Feedbacks

Fluxo: Frontend -> API REST -> Backend -> Banco de Dados

## Entidades principais e relacionamentos confirmados
### Usuário
- id
- nome
- email
- senha
- perfil
- matricula

### Projeto
- id
- titulo
- descricao
- dataInicio
- dataFim

### Equipe
- id
- nome
- lider

### Tarefa
- id
- titulo
- descricao
- prazo
- status
- prioridade

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

### Relacionamentos confirmados
- Usuário N:N Projeto
- Projeto 1:N Tarefa
- Projeto 1:N Entrega
- Entrega 1:N Feedback
- Equipe 1:N Usuário
- Projeto 1:1 Equipe

## Endpoints principais confirmados
### Autenticação
- POST /auth/login
- POST /auth/register

### Projetos
- GET /projetos
- POST /projetos
- GET /projetos/{id}
- PUT /projetos/{id}
- DELETE /projetos/{id}

### Tarefas
- GET /tarefas
- POST /tarefas
- PUT /tarefas/{id}
- DELETE /tarefas/{id}

### Entregas
- POST /entregas
- GET /entregas/{id}

### Feedbacks
- POST /feedbacks
- GET /feedbacks

## Tecnologias sugeridas confirmadas
### Frontend
- HTML
- CSS
- JavaScript

### Backend
- Java Spring Boot
- Framework REST

### Banco
- Banco relacional

### Infraestrutura
- Docker
- Git
- CI/CD

## Regras confirmadas para entregas
- O aluno pode incluir anexos e comentários em uma entrega.
- O aluno pode atualizar a entrega enquanto a data limite da tarefa estiver em aberto.
- A entrega pode ser repostada até a data limite, sem ultrapassá-la.
- A regra de overwriting será mantida.
- Deve existir data de criação da primeira entrega e data de manutenção da última atualização.
- Em tarefa em grupo, o aluno pode incluir outros alunos vinculando suas matrículas à entrega.

## Critérios de aceite baseados no escopo confirmado
1. Dado que o aluno possui matrícula e senha válidas, quando ele acessa a plataforma, então deve conseguir entrar no sistema e visualizar seu painel.
2. Dado que o aluno está vinculado a uma tarefa aberta, quando ele envia uma entrega com anexo e comentário, então a entrega deve ser registrada com sucesso.
3. Dado que a tarefa ainda está em aberto, quando o aluno altera a entrega, então a nova versão deve substituir a anterior e registrar a data de manutenção.
4. Dado que a tarefa passou da data limite, quando o aluno tentar reenviar a entrega, então o sistema deve bloquear a ação e exibir mensagem de prazo encerrado.
5. Dado que a tarefa é de grupo, quando o aluno incluir participantes com matrícula válida, então os alunos vinculados devem ser associados à entrega.
6. Dado que a entrega foi submetida, quando o professor acessa a tarefa, então ele deve visualizar o conteúdo, anexos, comentários e participantes.
7. Dado que a entrega foi analisada, quando o professor registra nota e feedback, então o aluno deve receber a avaliação.
8. Dado que há atualização relevante na tarefa, quando a entrega for avaliada ou houver prazo próximo, então a notificação deve ser enviada ao destinatário correto.
9. Dado que uma turma foi criada, quando o professor vincula projetos ou tarefas a essa turma, então somente os alunos daquela turma devem ter acesso.
10. Dado que uma matrícula já está vinculada a um aluno, quando outra pessoa tentar usar a mesma matrícula, então o cadastro deve ser rejeitado.

## Pendências explícitas
- Permissão de alunos para criar e atualizar tarefas ainda precisa ser revisada em conjunto com o fluxo de professor e a regra de negócio final.
- A diferenciação entre “projeto acadêmico”, “tarefa” e “turma” foi esclarecida como conceito, mas ainda pode ser validada em conjunto com a modelagem final.
- Autenticação detalhada com matrícula e senha foi confirmada, mas a política específica de recuperação de senha e autorização por contexto ainda está pendente.

## Documentos de referência
- README da solução: ../README.md
- Contexto direto do refinamento: presente neste diretório

## Status final do contexto geral
- Confirmado: escopo, papéis, autenticação, entrega, arquitetura e endpoints fundamentais
- Pendente: regras específicas finais de autorização e refinamento do fluxo de tarefas por perfil
