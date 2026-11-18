---
name: analise-matricula-imovel
description: "Ler matrículas de imóveis (uma ou um lote) e montar a análise patrimonial: titular atual e cadeia dominial, ônus real, constrições, averbação do art. 828, avaliação, credor de primeiro grau, penhorabilidade (bem de família, direitos do fiduciante, fração ideal) e ordem de preferência. Acionar quando o usuário pedir 'análise de matrícula', 'verificar ônus', 'quem é o dono', 'há penhora', 'dá para penhorar', 'é bem de família' ou 'ordem de preferência'. Não redige petição nem conclui fraude."
---

# analise-matricula-imovel (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "analise-matricula-imovel"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
