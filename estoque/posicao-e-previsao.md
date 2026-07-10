---
icon: boxes-stacked
description: Veja o estoque real que você tem agora no galpão — e preveja quanto vai sobrar numa data futura, com os orçamentos que seguram cada item.
---

# Posição e previsão de estoque

Duas perguntas diferentes rondam a cabeça de quem aluga [bens móveis](../primeiros-passos/glossario.md): **"quanto eu tenho AGORA no galpão?"** e **"quanto vai sobrar no dia do evento do cliente?"**. O LocFlow responde as duas — e é importante não confundi-las.

- **Posição** = o estoque **REAL de agora**. A foto do que está fisicamente no galpão neste momento.
- **Estoque planejado** = o que aparece **quando você monta um orçamento**. Já desconta as reservas de outros pedidos na janela daquele evento.

{% hint style="info" %}
Regra de ouro: a **Posição** conta o que existe hoje; o **orçamento** projeta o que estará livre na data. Um item pode estar "no galpão agora" e mesmo assim **não** estar disponível para o sábado que vem, porque já foi prometido a outro cliente.
{% endhint %}

## Posição

Na Posição você vê, por galpão, um **card de cada produto** com a **foto** e, em destaque, **quantos itens estão disponíveis ali agora**. É a conferência rápida do físico: quanto entrou, quanto saiu, o que sobrou.

- **Locação** — quanto de cada item você tem para alugar.
- **Venda** — o saldo destinado à venda, separado por condição (novo, seminovo, usado).

{% hint style="warning" %}
**Produto "sem estoque cadastrado".** Se um item nunca teve uma entrada registrada, o número que aparece não é confiável — o sistema não sabe quantos você realmente tem. O card fica em âmbar e leva você direto a **cadastrar a entrada** daquele produto. Enquanto não cadastrar, trate o valor como indefinido.
{% endhint %}

A Posição **não** é o mesmo que a disponibilidade avaliada na criação do orçamento. Lá, o LocFlow olha a **janela de bloqueio** do evento e desconta o que outros pedidos já reservaram — veja [Galpões e disponibilidade](galpoes-e-disponibilidade.md).

## Prever

Quer saber **quanto de um item vai sobrar num período futuro** sem abrir um orçamento? Use o alternador **"Agora | Prever"**.

Ao escolher uma **janela** (a data de entrega até a de retorno), o LocFlow mostra, por produto:

- **quantos estarão previstos** para aquele período; e
- **quais orçamentos seguram** o item — cada reserva com o **código do orçamento**, a quantidade e a janela em que ele ocupa o estoque.

Toque no código de um orçamento para abri-lo na hora e entender por que o item está reservado.

{% hint style="info" %}
A previsão considera a **Data de Liberação** de cada pedido: um item volta a contar como disponível quando retorna **e** conclui a manutenção (se você configurou um tempo de giro para o produto). Por isso a previsão pode ser mais conservadora que a simples data de devolução — ela protege você de prometer um item que ainda estará sendo revisado.
{% endhint %}

{% hint style="success" %}
**Por que isso te faz faturar mais:** com a previsão, você responde "consigo atender o dia 20?" em segundos, olhando exatamente **quais pedidos** disputam o item — sem planilha, sem achismo e sem prometer o que não tem.
{% endhint %}

## Próximo passo

Entenda a regra que protege contra reserva dupla em [Galpões e disponibilidade](galpoes-e-disponibilidade.md) e como o pedido caminha em [O ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md). Em dúvida sobre um termo? Consulte o [Glossário](../primeiros-passos/glossario.md).
