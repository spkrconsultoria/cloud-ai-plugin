# Changelog

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
