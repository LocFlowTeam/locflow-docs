---
icon: list-check
description: As oito operações que mudam o estoque — registrar entrada, conferir contagem, enviar para reparo, registrar avaria, dar baixa, transferir, reclassificar e registrar saída — e a janela que todas usam.
---

# Operações de estoque

Todo número do estoque muda por uma de **oito operações**. Elas não são telas soltas que você precisa procurar: são **ações** que nascem do [Painel de Estoque](painel.md) ou da ficha de um item.

| Por onde começar | O que acontece |
| --- | --- |
| **Operar** no topo do painel (no celular, o botão **+**) | Abre **Nova operação**, com as oito. Você escolhe a operação e depois o item |
| A **ficha do item** › **Operar em …** | A operação já abre com o produto, o local e o tipo de estoque escolhidos |
| As **caixinhas** da lista de Itens › **Operar** | Conferir contagem, enviar para reparo ou transferir vários itens de uma vez. Veja [Operar vários itens de uma vez](operar-varios-itens.md) |

Cada operação só aparece para quem tem a permissão dela — e quando o seu plano a inclui: a **saída avulsa** (venda de estoque sem orçamento) é de plano superior. E numa **loja com estoque próprio** só existem duas — **Conferir contagem** e **Transferir entre locais**: as demais são operações do galpão.

## A mesma janela para as oito

Toda operação abre na mesma janela, com as coisas sempre no mesmo lugar:

1. **O cabeçalho** — o ícone e a cor da operação, o verbo (*Dar baixa*, *Reclassificar*) e uma frase do que vai acontecer.
2. **O item, numa linha só** — o produto, o local e o tipo de estoque já escolhidos. Trocar fica a um toque.
3. **A pergunta essencial** — quase sempre *quantas unidades?*, com o **teto à vista** (*de 40 disponíveis*, ou *de 40 na prateleira*) e o atalho **Todas (40)** para preencher o máximo.
4. **A prévia do efeito**, antes de confirmar — por exemplo, *"Ficarão 37 na prateleira"*.
5. **Um botão só**, na cor da operação, que diz o que vai fazer (*Dar baixa em 3*). Enquanto falta alguma coisa, ele diz **por escrito o que falta**, em vez de ficar apagado sem explicação.

A cor já avisa o peso do gesto: **neutra** para o movimento comum, **âmbar** para o que tira material do disponível, **vermelha** para o que tira material do seu patrimônio.

## As oito, lado a lado

| Operação | Quando usar | O que acontece | Até quanto |
| --- | --- | --- | --- |
| **Registrar entrada** | Chegou material: uma compra, ou o estoque inicial | O material passa a existir no estoque, com o valor de compra | Sem limite |
| **Conferir contagem** | A prateleira não bate com o sistema | O saldo passa a valer o que você contou | Sem limite: vale o que você contou |
| **Enviar para reparo** | O item precisa de conserto ou lavagem | Sai do disponível e vai para a bancada | O disponível |
| **Registrar avaria** | O material chegou danificado ou quebrou | Sai do estoque e do patrimônio — e pode virar cobrança do cliente | O que está na prateleira |
| **Dar baixa** | Quebra sem conserto, roubo, perda | Sai do estoque e do patrimônio, de vez | O que está na prateleira |
| **Transferir entre locais** | O material precisa ir para outro galpão ou loja | Sai daqui e entra lá | O que pode ser despachado |
| **Reclassificar** | O item vai mudar de uso | Passa de um tipo de estoque para outro, no mesmo local | O disponível |
| **Registrar saída** | Venda avulsa, sem orçamento | Sai do patrimônio; o valor vira receita da venda | O disponível |

## Registrar entrada {#registrar-entrada}

A entrada é o que faz um produto **existir no estoque**: o recebimento de uma compra ou o material que já estava no galpão quando você começou a usar o LocFlow. A janela pergunta:

1. **Produto** — busque pelo nome ou pelo SKU.
2. **Onde vai ficar?** — o galpão.
3. **É de aluguel ou venda?** — o cadastro do produto já sugere a resposta, e a outra fica a um toque. Aluguel e venda são **dois estoques**: o de aluguel sai e volta; o de venda sai de vez. Na venda, a janela pergunta também **Novo, seminovo ou usado?**.
4. **Quantas unidades?**
5. **Data da compra** — opcional, e não pode ser no futuro.
6. **Valor de compra** — **Por unidade** ou **Total da nota**. Ele já vem preenchido com o valor de reposição do produto; use como está ou ajuste. Se o preço mudou desde a última compra, ligue **Atualizar o valor de reposição do produto**.
7. **Depreciação** (recolhida, opcional) — a **vida útil** em meses e o **valor residual** por unidade. É o que faz o valor do material cair com o tempo no [Patrimônio](patrimonio.md).

Confirme com **Registrar entrada** — ou **Registrar e adicionar outra**, para seguir lançando a nota inteira sem fechar a janela.

{% hint style="info" %}
**Atalho no catálogo.** No cadastro de um produto já salvo, o botão **Registrar entrada** abre esta janela com o produto escolhido, e **Ver no estoque** abre a ficha dele no painel. Não é preciso sair do produto e procurá-lo de novo.
{% endhint %}

{% hint style="info" %}
**Produto sem preço avulso também tem estoque.** Se o produto não tem preço de aluguel (ou de venda) no cadastro, a janela explica: tudo bem — o estoque pode existir para os kits que usam aquela peça.
{% endhint %}

## Conferir contagem

Contar é comparar o que existe **na prateleira** com o que o sistema diz. Você informa **quantas contou** e, se der diferente, o LocFlow registra a **diferença** e o saldo passa a valer o que você contou.

{% hint style="warning" %}
**Conte só o que está na prateleira.** O material em reparo ou em quarentena está separado e não entra na contagem. Se você contar a bancada junto, vai "achar" sobra que não existe — e o ajuste inflaria o estoque. Na contagem de vários itens, cada linha avisa quantas unidades estão separadas.
{% endhint %}

Use a contagem quando a prateleira está diferente do sistema **sem um motivo conhecido**. Se você sabe o motivo — quebrou, sumiu, foi roubado —, o caminho é **avaria** ou **baixa**, que guardam o porquê.

## Enviar para reparo

Manda unidades para a bancada de manutenção. Elas **saem do disponível** — ninguém consegue prometê-las enquanto estão no conserto —, mas continuam suas e continuam no patrimônio. Só o que está **disponível** pode ir: material reservado para um pedido fica onde está. E se um pedido confirmado precisar daquele material enquanto ele estiver no conserto, o envio é recusado.

O que acontece quando o item volta — voltar ao estoque, descartar, reclassificar ou separar em quarentena — está em [Manutenção: o desfecho do reparo](manutencao.md).

## Registrar avaria

Para o material que **chegou danificado de um evento** ou **quebrou no galpão**. A janela pergunta **Quantas avariaram?** e **O que aconteceu?** (*"vidro trincado no transporte"*) — é esse texto que aparece no histórico quando alguém perguntar por que o saldo caiu.

Se o dano foi do cliente, ligue **Cobrar do cliente?**, escolha o **cliente a cobrar** e o **valor da cobrança**: o LocFlow gera uma cobrança avulsa pelo dano no mesmo gesto.

{% hint style="warning" %}
**A baixa vale mesmo se a cobrança falhar.** A avaria tira o material do estoque assim que você confirma. Se a cobrança não puder ser gerada, o app avisa que a avaria foi registrada e a cobrança falhou — gere-a manualmente em [Cobranças](../cobranca/lista-de-cobrancas.md).
{% endhint %}

A avaria é sempre **item a item**: cada uma tem o seu motivo e pode virar cobrança — decisões que pedem atenção individual.

## Dar baixa

A baixa é **definitiva**: o material sai do estoque e do patrimônio. Use para o que quebrou sem conserto, foi roubado ou se perdeu.

* Se o dano foi do cliente e pode ser cobrado, prefira **avaria** — ela faz a mesma baixa e ainda gera a cobrança.
* Se a prateleira está diferente do sistema sem um motivo assim, o caminho é **conferir a contagem**, não dar baixa.

## Transferir entre locais

Move material entre **galpões e lojas com estoque próprio**. Escolha **para onde vai?**, a quantidade e toque em **Despachar**. O material sai da origem na hora e entra no destino quando alguém confirma a chegada — a não ser que a loja e o galpão fiquem no mesmo endereço, quando a transferência conclui na hora. O passo a passo, com a fila do que está em trânsito, está em [Transferências](transferencias.md).

## Reclassificar

Muda o **uso** do material sem tirar nem pôr nada: o mesmo produto sai de um tipo de estoque e entra em outro, no mesmo local. O caso clássico são as cadeiras aposentadas do aluguel que vão para a venda como usadas.

* **Para onde vai?** — Aluguel ou Venda; na venda, também **Novo, seminovo ou usado?**.
* Só o que está **disponível** pode mudar de uso: material reservado para um pedido continua onde está.
* O destino **não precisa ter preço** no catálogo: onde o material fica separado é um fato do galpão, não do que o cliente vê.

## Registrar saída

A saída avulsa é uma **venda sem orçamento**: o material deixa de ser seu. A janela pergunta **quantas vender?** e o **valor total da venda**, que entra como receita da venda.

* Só o que está **disponível** pode sair: unidades reservadas para um aluguel ficam de fora, porque já têm dono naquela data.
* Vendas feitas por um **orçamento de venda** já saem do estoque sozinhas, na entrega — esta operação é só para a venda avulsa.

## Se a internet cair no meio

Pode tentar de novo sem medo: o LocFlow reconhece o reenvio e **não registra duas vezes** o que já tinha entrado.

{% hint style="success" %}
**Por que isso te faz faturar mais:** quando toda mudança de estoque passa por uma operação com nome e motivo, o número da tela volta a ser confiável — e é ele que decide se você aceita ou recusa o próximo pedido.
{% endhint %}

## Próximo passo

Opere vários itens de uma vez em [Operar vários itens de uma vez](operar-varios-itens.md), acompanhe o material em trânsito em [Transferências](transferencias.md) e veja o que cada movimentação registra em [Cada movimentação, em detalhe](posicao-e-previsao.md#movimentacoes).
