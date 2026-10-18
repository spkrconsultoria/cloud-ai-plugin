# Changelog

## 0.1.0 (em desenvolvimento)

- Esqueleto do marketplace e do plugin `spkr`.
- Hooks `SessionStart` (contexto e `.spkr-cloudai/INSTRUCOES.md`) e `SessionEnd`.
- Skills `guia` e `conformidade`.
- Endereço da API fixo no plugin (`cloudai.spkr.com.br`, caminho base `/api/v1/plugin/`); só o token é solicitado.
- Servidor MCP `spkr` (`spkr_tick`, `spkr_whoami`, `spkr_list_projects`, `spkr_bind`, `spkr_policy`) para escolher o projeto de uma pasta e consultar as políticas por tema.
- Guia em duas camadas: introdução e índice sempre no contexto e gravados em `.spkr-cloudai/INSTRUCOES.md`; políticas por tema sob demanda.
- Licença proprietária.
