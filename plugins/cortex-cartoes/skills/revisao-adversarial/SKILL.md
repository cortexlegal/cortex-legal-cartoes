---
name: revisao-adversarial
description: "Atacar uma peça já redigida, antes do protocolo, por três olhares: o advogado do adversário (a manifestação que ele protocolaria), o juízo (a decisão que defere, parando onde não consegue) e a serventia que teria de cumprir a ordem. Acionar quando o usuário pedir 'atacar essa peça', 'ver se tem furo', 'conferir se o juiz decide com isso' ou 'o cartório cumpre isso?'. Rodar em conversa nova, com a peça e os documentos colados ou anexados. Não redige nem corrige: entrega achados."
---

# revisao-adversarial (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "revisao-adversarial"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
