# Manifesto da versão v1

## Visão geral
Este diretório consolida o refinamento inicial da solução Class Hub, com base no escopo confirmado pelo usuário.

## Status dos artefatos
- contexto-geral.md: confirmado
- decisoes.md: confirmado
- pendencias.md: confirmado
- historico.md: confirmado
- diagramas/arquitetura-geral.puml: confirmado
- partes/P1-autenticacao/contexto.md: confirmado
- partes/P2-tarefas-e-projetos/contexto.md: confirmado
- partes/P3-entregas-e-feedback/contexto.md: confirmado
- partes/P4-equipes-e-notificacoes/contexto.md: confirmado
- modelagens/M1-usuarios/contexto.md: confirmado
- modelagens/M2-projetos-e-tarefas/contexto.md: confirmado
- modelagens/M3-entregas-feedback/contexto.md: confirmado
- continuacao.md: confirmado

## Ordem sugerida de desenvolvimento
1. P1 - Autenticação e identidade
2. P2 - Gestão de projetos e tarefas
3. P3 - Entregas e feedback
4. P4 - Equipes e notificações

## Dependências
- P1 é base para todos os fluxos autenticados
- P2 precede P3, pois as entregas pertencem a tarefas/projetos
- P3 suporta avaliação e feedback
- P4 depende da existência de turmas, alunos, projetos e entregas

## Arquivos principais
- Contexto geral: [contexto-geral.md](contexto-geral.md)
- Decisões: [decisoes.md](decisoes.md)
- Pendências: [pendencias.md](pendencias.md)
- Histórico: [historico.md](historico.md)
- Continuação: [continuacao.md](continuacao.md)

## Observação
Este manifesto é atualizado sob a regra de que decisões ainda não aprovadas continuam sendo registradas como pendentes e não são convertidas em regras finais.
