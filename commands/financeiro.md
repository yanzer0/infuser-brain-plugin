---
description: Mostra o dashboard financeiro do mês - entradas, saídas, líquido, comparação com o mês anterior, MRR e top categorias - lido dos docs financeiros do cérebro
argument-hint: "[contexto opcional]"
---
Comando `/financeiro` do seu Segundo Cérebro (Infuser). Argumento do usuário (se houver): "$ARGUMENTS".

1. Chame a tool `brain__command` com name="financeiro".
2. Pegue o campo `instructions` da resposta e **execute-o à risca, como se fosse a sua tarefa agora** (considerando o argumento acima), usando as demais tools do cérebro (`brain__pending`, `brain__search`, `brain__read_doc`, `brain__list_docs`, `brain__update_doc`, `state__*`, `media__*`) conforme as instruções pedirem.

As instruções vêm do servidor (são a fonte de verdade do comando e podem mudar sem aviso). Não invente nada fora do que está no cérebro. Fale natural, em português, sem citar nomes de tools.
