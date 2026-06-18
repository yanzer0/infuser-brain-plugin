---
description: Roda um comando do seu Segundo Cérebro (ex /brain daily-briefing). Sem argumento, lista os comandos disponíveis.
argument-hint: "[nome-do-comando]"
---
O usuário disparou um comando do Segundo Cérebro. Argumento recebido: "$ARGUMENTS".

1. Se "$ARGUMENTS" estiver vazio: chame a tool `brain__command` SEM argumento e apresente, em português, a lista de comandos disponíveis (nome + descrição) pro usuário escolher.
2. Caso contrário: chame a tool `brain__command` com name="$ARGUMENTS". Pegue o campo `instructions` da resposta e **execute-o à risca, como se fosse a sua tarefa agora**, usando as demais tools do cérebro (`brain__pending`, `brain__search`, `brain__read_doc`, `brain__list_docs`, `state__*`, `media__*`) conforme as instruções pedirem.

Regras: as instruções vêm do servidor (são a fonte de verdade do comando e podem mudar sem aviso). Não invente nada fora do que está no cérebro. Se o comando não existir, a tool retorna `available`, então mostre os disponíveis. Fale natural, em português, sem citar nomes de tools.
