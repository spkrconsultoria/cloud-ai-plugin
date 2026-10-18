---
name: guia
description: Mostra o guia de conformidade SPKR do projeto (.spkr-cloudai/INSTRUCOES.md), confere se o CLAUDE.md o importa e explica como atualizá-lo. Use quando o usuário pedir o guia, as regras de infraestrutura da empresa ou o motivo de o contexto SPKR não ter sido carregado.
disable-model-invocation: true
---

# Guia de conformidade SPKR

O guia fica em `.spkr-cloudai/INSTRUCOES.md`, na raiz do projeto. O plugin o baixa sozinho ao abrir a sessão, depois de `/clear` e depois de compactar a conversa, e injeta a introdução e o índice do guia no contexto. As políticas por tema são consultadas sob demanda pela ferramenta `spkr_policy`. Você não gera nem reescreve o guia: ele vem pronto da SPKR.

## O que fazer

1. Leia `.spkr-cloudai/INSTRUCOES.md`.
   - Se existir, apresente ao usuário um resumo curto: projeto, versão e os temas do índice. O texto completo está no arquivo; não copie o guia inteiro na resposta.
   - Se não existir, diga que o guia não foi carregado e **não invente regras**. Sugira, nesta ordem: abrir `/plugin` e conferir a configuração do plugin `spkr` (endereço da API e token); rodar `/clear` para tentar de novo; pedir ao administrador da empresa um novo token no portal SPKR.
2. Confira se o `CLAUDE.md` do projeto contém a linha `@.spkr-cloudai/INSTRUCOES.md`. Se não contiver, mostre a linha ao usuário e **só a inclua depois de ele confirmar**. Se não houver `CLAUDE.md`, ofereça criar um com essa linha.
3. Para atualizar o guia, oriente o usuário a rodar `/clear`. O plugin baixa a versão mais recente nesse momento.

## Limites

- Se a API da SPKR estiver fora do ar, a versão que já está em `.spkr-cloudai/INSTRUCOES.md` continua valendo. Diga isso ao usuário.
- Não envie o conteúdo do guia, do token ou do projeto para nenhum endereço externo.
