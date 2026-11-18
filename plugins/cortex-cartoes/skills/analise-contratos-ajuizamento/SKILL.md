---
name: analise-contratos-ajuizamento
description: "Analisar contratos e documentos bancários (CCB, CDC PJ, leasing, cheque, nota comercial, CPR, CCE, garantias, planilhas de débito, extratos) e recomendar a ação de ajuizamento (busca e apreensão, execução ou monitória), com o relatório de extração que instrui a inicial: requisitos do art. 798 do CPC, polo passivo, cláusulas literais, lacunas, documentos pendentes e indícios para IDPJ. Acionar quando o usuário pedir 'analisar os contratos', 'estratégia de ajuizamento', 'o que dá para ajuizar', 'cabe execução, monitória ou busca?', 'instruir a inicial' ou 'qualificar as partes'. Não redige a peça nem aprofunda fraude."
---

# analise-contratos-ajuizamento (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "analise-contratos-ajuizamento"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
