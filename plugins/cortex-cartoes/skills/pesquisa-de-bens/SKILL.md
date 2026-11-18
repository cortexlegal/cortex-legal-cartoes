---
name: pesquisa-de-bens
description: "Consolidar as pesquisas patrimoniais de um caso (todas as pessoas físicas e jurídicas ligadas ao mesmo devedor ou grupo) num documento único e vivo: lê o que o Cortex já tem e cada retorno novo (ONR, CNIB, JUCESP, SISBAJUD, RENAJUD, INFOJUD, matrículas, teia societária), carimba a origem de cada achado, registra as contradições com as duas versões e grava no Cortex os bens, as averbações e as medidas. Acionar quando o usuário pedir 'pesquisa de bens', 'consolidar as pesquisas', 'atualizar a pesquisa patrimonial', 'o que achamos do devedor' ou trouxer retornos de pesquisa. Não pede a pesquisa à equipe nem redige petição."
---

# pesquisa-de-bens (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "pesquisa-de-bens"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
