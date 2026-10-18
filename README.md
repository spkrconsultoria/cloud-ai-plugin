# SPKR Cloud for AI: plugin para Claude Code

Marketplace e plugin da SPKR que levam o guia de conformidade de infraestrutura da sua empresa para dentro do Claude Code.

## O que o plugin faz

- Ao abrir uma sessão (também depois de `/clear` e de compactar a conversa), baixa o guia do seu projeto e o grava em `.spkr-cloudai/INSTRUCOES.md`.
- Entrega à IA, no contexto da sessão, a introdução do guia (regras principais) e o índice por temas. O detalhe de cada tema a IA consulta sob demanda.
- Registra o início e o fim da sessão (identificador da sessão, motivo do fim e horário). **Não envia o texto dos seus prompts nem das respostas.**
- Se a pasta ainda não tem projeto e você tem acesso a mais de um, a IA pergunta qual usar e guarda a escolha; o guia do projeto escolhido já vale na mesma conversa.
- Skills: `/spkr:guia` (mostra o guia e confere o `CLAUDE.md`) e `conformidade` (a IA consulta o guia antes de decidir Docker, banco, portas, variáveis e segredos).

O plugin é cooperativo: ele ajuda a seguir o padrão da empresa, mas não garante bloqueio.

## Instalação

O portal SPKR, na tela **Começar com Claude Code**, gera o seu token pessoal. Depois:

```text
/plugin marketplace add spkrconsultoria/spkr-cloud-ai-plugin
/plugin install spkr@spkr-cloud-ai
```

O Claude Code pede o token pessoal. O token fica no cofre do sistema, não em arquivo.

Depois de instalar, **saia e volte à mesma conversa** para o plugin carregar o guia: digite `/exit` e rode `claude --continue` (no Desktop e nas IDEs, feche e reabra a sessão). Assim você não perde o trabalho da conversa. Evite o `/clear` para isso, porque ele limpa o histórico.

Na primeira vez em uma pasta, se você tiver acesso a mais de um projeto, a IA pergunta qual usar. O guia do projeto escolhido já vale na mesma conversa; o arquivo `.spkr-cloudai/INSTRUCOES.md` é gravado quando a próxima sessão começa (`/exit` e `claude --continue`, `/compact` ou nova sessão).

Este repositório não contém tokens nem dados de clientes. Licença: ver `LICENSE`.

## Requisitos

Claude Code com suporte a plugins. No Windows 10 (1803 ou mais novo) e no Windows 11, o `curl.exe` já vem com o sistema. Não é preciso instalar Node nem outras bibliotecas.

## Atualizar o guia

O plugin baixa a versão mais recente sempre que uma sessão começa, é retomada (`claude --continue`) ou é compactada (`/compact`). Para atualizar sem perder a conversa, saia com `/exit` e volte com `claude --continue`. Se a API estiver fora do ar, vale a última versão gravada em `.spkr-cloudai/INSTRUCOES.md`.

## Segurança

- O token é enviado só ao endereço da SPKR (`cloudai.spkr.com.br`), em cabeçalho `Authorization`.
- O token pode ser revogado no portal SPKR a qualquer momento.
