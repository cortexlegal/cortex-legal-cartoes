---
name: confirmacao-prazos
description: "Fechar o ciclo de um prazo processual com acesso real aos autos: lê a auditoria anterior e a pesquisa de bens, decide entre aproveitar, auditar só o que mudou ou fazer a primeira auditoria completa, consulta os autos só no que falta e confirma o prazo. Quando a redação da peça estiver disponível, redige, revisa pela triagem e confere antes de entregar; senão, entrega o prazo confirmado e o diagnóstico. Acionar quando o usuário apontar um prazo, pedir a confirmação dos prazos do dia ou da semana, revisar uma minuta existente ou organizar peças pendentes. Exige o usuário presente."
---

# confirmacao-prazos (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "confirmacao-prazos"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
