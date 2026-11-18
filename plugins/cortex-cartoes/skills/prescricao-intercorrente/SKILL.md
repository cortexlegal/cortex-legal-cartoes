---
name: prescricao-intercorrente
description: "Diagnosticar risco de prescrição intercorrente em execução de título extrajudicial e cumprimento de sentença, do lado credor: o regime aplicável (anterior ou Lei 14.195/2021), o prazo conforme a espécie de título, os marcos de interrupção e as lacunas dos autos. Acionar quando o usuário pedir para 'ver se prescreveu', 'calcular a prescrição intercorrente', 'analisar risco de extinção do art. 924, V', 'conferir os marcos do art. 921', 'saber qual regime se aplica', 'qual o prazo desse título', 'a penhora interrompeu?', ou ao anexar sentença ou decisão que reconheceu prescrição intercorrente. Nunca afirma que o crédito prescreveu: entrega regime, marcos, lacunas e teses, e devolve a decisão ao advogado."
---

# prescricao-intercorrente (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "prescricao-intercorrente"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
