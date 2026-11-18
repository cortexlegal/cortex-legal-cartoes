---
name: averbacao-premonitoria
description: "Preparar os requerimentos de averbação da certidão de admissão da execução (art. 828 do CPC) nos registros de imóveis, um por cartório, e nos DETRAN, um por UF de domicílio dos executados, depois de conferir o titular de cada bem. Acionar quando o usuário pedir 'averbação premonitória', 'averbar a certidão no cartório', 'averbar no DETRAN' ou 'art. 828'. Não cobre cotas sociais, a comunicação ao juízo nem o cancelamento."
---

# averbacao-premonitoria (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "averbacao-premonitoria"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
