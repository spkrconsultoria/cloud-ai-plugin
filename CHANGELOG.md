# Changelog

## 0.2.0

- Skill `novo-projeto`: conduz no chat a criação de projeto (perguntas do formulário da empresa, com sugestões baseadas na pasta e confirmação antes de criar) ou o registro de um workspace rápido, só com uma descrição, que pode ser convertido em projeto depois.
- Servidor MCP: `spkr_project_form`, `spkr_project_create`, `spkr_workspace_register` e `spkr_workspace_promote`. Criar projeto e registrar workspace exigem um token com a opção "criar projetos e workspaces", emitida no portal.
- Pasta sem projeto: o contexto da sessão passa a oferecer projeto existente, projeto novo ou workspace.

## 0.1.1

- Instruções de instalação: depois de instalar, sair e voltar com `claude --continue` em vez de `/clear`, para não perder a conversa.
- Corrige o texto de atualização do guia no README.

## 0.1.0

- Esqueleto do marketplace e do plugin `spkr`.
- Hooks `SessionStart` (contexto e `.spkr-cloudai/INSTRUCOES.md`) e `SessionEnd`.
- Skills `guia` e `conformidade`.
- Endereço da API fixo no plugin (`cloudai.spkr.com.br`, caminho base `/api/v1/plugin/`); só o token é solicitado.
- Servidor MCP `spkr` (`spkr_tick`, `spkr_whoami`, `spkr_list_projects`, `spkr_bind`, `spkr_policy`) para escolher o projeto de uma pasta e consultar as políticas por tema.
- Guia em duas camadas: introdução e índice sempre no contexto e gravados em `.spkr-cloudai/INSTRUCOES.md`; políticas por tema sob demanda.
- Licença proprietária.
