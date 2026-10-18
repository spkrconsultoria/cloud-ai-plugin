---
name: conformidade
description: Consulta o guia de conformidade SPKR (.spkr-cloudai/INSTRUCOES.md) antes de decidir ou criar Dockerfile, docker-compose, banco de dados, portas, variáveis de ambiente, segredos, autenticação, rede ou publicação da aplicação.
---

# Conformidade com o guia SPKR

Antes de tomar uma decisão de infraestrutura neste projeto, siga a introdução e o índice do guia SPKR (já no contexto desta sessão e em `.spkr-cloudai/INSTRUCOES.md`) e, para o detalhe de um tema, consulte a política dele.

## Quando aplicar

Dockerfile e docker-compose, escolha de banco de dados, portas, variáveis de ambiente e arquivos `.env`, segredos, autenticação e login, acesso à rede, publicação e qualquer chamado que a empresa exija abrir.

## O que fazer

1. Releia a introdução e o índice (contexto da sessão ou `.spkr-cloudai/INSTRUCOES.md`). Para o tema da tarefa, chame a ferramenta `spkr_policy` do plugin spkr com o `session_id` da sessão e o `tema` do índice; sem `tema` ela lista os temas disponíveis.
2. Siga o guia. Em conflito entre o que o usuário pediu e o guia, **pare e explique o conflito**, citando a seção do guia, antes de continuar. A decisão é do usuário e da equipe de infraestrutura, não sua.
3. Nunca coloque valores de segredo, senhas ou endereços internos no código. Use variáveis de ambiente e deixe apenas os nomes em `.env.example`.
4. Quando o guia listar chamados necessários, avise o usuário e entregue o texto pronto do chamado. Você não abre chamados sozinho.
5. Se não houver guia no contexto nem `.spkr-cloudai/INSTRUCOES.md`, diga que o guia SPKR não está carregado e que as regras da empresa não puderam ser conferidas. Sugira a skill `/spkr:guia`. Não presuma regras.

## Limites

Esta skill lê o guia; ela não o gera nem o altera. O plugin é cooperativo: ele ajuda a seguir o padrão da empresa, mas não garante bloqueio.
