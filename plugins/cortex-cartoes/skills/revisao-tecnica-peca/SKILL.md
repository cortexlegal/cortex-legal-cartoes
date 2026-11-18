---
name: revisao-tecnica-peca
description: "Revisar tecnicamente uma peça pronta, própria ou de colega: conferir os fatos contra os documentos, as contas, a tese, os dispositivos legais e os precedentes citados, e apontar cada correção com o trecho atual e o trecho proposto. Acionar quando o usuário pedir 'revisar a peça', 'conferir os fatos', 'conferir a tese', 'vê se está certo' ou 'conferir os precedentes'. Pedido de 'atacar a peça' ou 'ver se tem furo' é da revisão adversarial. Não redige a peça do zero."
---

# revisao-tecnica-peca (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "revisao-tecnica-peca"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
