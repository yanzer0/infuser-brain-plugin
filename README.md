# Infuser Brain (plugin de comandos)

Plugin do Claude Code que traz os comandos do seu **Segundo Cérebro Infuser** como slash commands (`/council`, `/criar-ui`, `/proposta`, `/contrato`, `/carrossel`...).

## Como funciona

Cada comando aqui é uma **casca fina**. Ele não contém a lógica do comando: só chama a tool `brain__command` do MCP da Infuser, recebe a instrução do servidor e executa. Quer dizer:

- O **conteúdo dos comandos mora no servidor** (no seu tenant). A gente melhora ou cria comando do nosso lado e você recebe no próximo startup, **sem reinstalar nada**.
- Sem o **token do seu tenant** (`INFUSER_MCP_TOKEN`), o plugin é uma casca morta: toda chamada volta 401. Por isso este repo é público sem risco. Ele não carrega segredo, dado nem método.

## Instalação

1. Adicione o marketplace:
   ```
   /plugin marketplace add yanzer0/infuser-brain
   ```
2. Instale o plugin:
   ```
   /plugin install infuser-brain@infuser
   ```
3. Defina o token do seu tenant (fornecido pela Infuser) na variável de ambiente `INFUSER_MCP_TOKEN`.
4. Reinicie a sessão. Os comandos aparecem no menu `/`.

Sem argumento, `/brain` lista todos os comandos disponíveis no seu tenant.

## O que NÃO está aqui

O harness (surface de aprendizados, gate de risco, rotina de encerramento) é entregue à parte. Este plugin é só a camada de comandos.

---
Infuser · https://useinfuser.com
