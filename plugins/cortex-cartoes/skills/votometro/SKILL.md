---
name: votometro
description: "Medir o peso de voto de cada credor na assembleia geral de credores de uma recuperação judicial e simular a votação do plano: aprovado pelo quórum do art. 45, aprovável por cram down (art. 58, § 1º) ou rejeitado, a partir do quadro geral de credores ou da relação do art. 7º, § 2º. Entrega a planilha por classe, o parecer de quórum e coalizões e o simulador. Acionar quando o usuário pedir 'votômetro', 'peso de voto dos credores', 'quanto o cliente representa na AGC', 'quem aprova o plano', 'coalizão de credores', 'simular a votação' ou 'cram down'. Não redige petição nem parecer sobre o mérito do plano."
---

# votometro (pelo Cortex Legal)

O método desta skill fica no Cortex Legal e só sai para quem está logado. Não faça a tarefa de memória.

1. Chame `abrir_roteiro` do conector Cortex Legal com `skill: "votometro"`. Mande o `processo` (o CNJ) ou o
   `devedor` quando o caso for da carteira; sem caso da carteira, mande o `motivo`.
2. Siga as etapas do roteiro na ordem. Antes de concluir QUALQUER etapa, chame `abrir_modulo` com o
   `handle` que o roteiro devolveu e o nome do módulo dessa etapa, e aplique o texto que vier. A
   descrição dos módulos no roteiro é só um índice, não é o método: nunca analise nem conclua com base
   nela. Etapa sem o módulo aberto não tem conclusão.
3. Se vier `calibracao_pendente`, faça o que o campo `o_que_fazer` manda.
4. Se a ferramenta não existir ou recusar (login, cargo, termo de uso, mensalidade), diga à pessoa o
   motivo como veio e pare: sem o roteiro, não faça a tarefa.

Não reproduza na resposta a etiqueta da entrega que vem no texto.
