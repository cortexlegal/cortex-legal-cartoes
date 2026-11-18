---
name: auditoria-cronologica-processo
description: "Auditar a cronologia dos autos evento a evento para achar contradições, omissões, atos travados e vulnerabilidades antes de qualquer peça. Opera em duas trilhas: (A) execução e cumprimento de sentença, com os pressupostos de citação, o fluxo expropriatório das penhoras, o aproveitamento das pesquisas patrimoniais e a prescrição intercorrente; (B) recuperação judicial e falência, com o status do crédito (classe, habilitação, impugnação, garantia) e o mérito do plano. Acionar quando o usuário enviar autos, íntegra, incidente ou trecho de processo e pedir para analisar a cronologia, auditar o processo, entender por que o processo não anda, verificar se uma decisão ignorou algo, ou questionar a validade de citação, intimação, procuração ou substabelecimento. Acionar também antes de redigir manifestação, embargos ou recurso. Não redige a peça nem conduz o leilão: entrega o diagnóstico que os alimenta."
---

# auditoria-cronologica-processo (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "auditoria-cronologica-processo"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
