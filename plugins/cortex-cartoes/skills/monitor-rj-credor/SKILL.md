---
name: monitor-rj-credor
description: "Julgar os alertas das recuperações judiciais e falências em que o cliente é credor: conferir a premissa de cada alerta, calcular a data-limite em dias corridos e propor a retomada das execuções no fim do stay. Acionar quando o usuário pedir 'o que mudou nas RJs', 'tem decisão nova que afete o crédito', 'prazos das recuperações', 'monitorar as RJs' ou 'rodar o monitor de RJ'. Não redige peça nem audita um processo isolado."
---

# monitor-rj-credor (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "monitor-rj-credor"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
