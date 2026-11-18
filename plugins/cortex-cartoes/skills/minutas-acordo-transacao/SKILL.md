---
name: minutas-acordo-transacao
description: "Gerar a petição conjunta de homologação de acordo no contencioso cível bancário: acordo em execução ou cumprimento de sentença (suspensão até a quitação pelo art. 922 do CPC, com ou sem garantia reforçada), acordo em busca e apreensão (negócio processual atípico, garantia fiduciária mantida) e acordo de honorários de sucumbência. Confirma o escopo (contratos, processos e fluxos) e confere a soma do fluxo antes de redigir. Acionar quando o usuário mandar um fluxo de pagamento e pedir minuta de acordo, transação, composição ou negócio processual, mesmo sem citar a peça."
---

# minutas-acordo-transacao (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "minutas-acordo-transacao"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
