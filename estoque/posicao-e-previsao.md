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

### Produto "sem estoque cadastrado" {#sem-cadastro}

{% hint style="warning" %}
Se um item nunca teve uma entrada registrada, o número que aparece não é confiável — o sistema não sabe quantos você realmente tem. O card fica em âmbar e leva você direto a **cadastrar a entrada** daquele produto. Enquanto não cadastrar, trate o valor como indefinido.
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

## Cada movimentação, em detalhe {#movimentacoes}

A Posição responde **"quanto"**. Para responder **"o que aconteceu e por quê"**, o LocFlow guarda toda entrada e toda saída num histórico de movimentações — na aba Movimentações do painel, ou no histórico dentro da ficha de cada item. Toque em qualquer linha para abrir o registro completo:

- **o que mudou** — quanto entrou ou saiu, e em qual estoque (aluguel, ou venda numa condição);
- **em qual galpão** aconteceu;
- **quando aconteceu** de fato e, se o lançamento foi feito depois (um registro retroativo), **quando foi registrado**;
- **o motivo**;
- **quem registrou**;
- o **custo de aquisição** do lote (nas entradas) ou a **receita da venda** (nas vendas), quando existem;
- **de onde ela veio** — avaria, conferência de retorno, descarte na manutenção, logística, ajuste de contagem, entre outras origens;
- um atalho para abrir o **orçamento envolvido**, quando a movimentação pertence a um.

{% hint style="info" %}
**Movimentações antigas mostram "—".** Motivo e responsável só existem a partir do momento em que o LocFlow passou a registrá-los. Uma movimentação anterior a isso mostra um travessão nesses dois campos — o sistema prefere admitir que não sabe a inventar um nome.
{% endhint %}

Direto no **item selecionado**, o menu "Operar este item" já oferece **dar baixa**, **reclassificar** e **registrar saída** — cada ação abre com o galpão e o tipo de estoque daquele item já preenchidos, prontos para confirmar.

{% hint style="info" %}
Uma movimentação de descarte ou reclassificação vinda do reparo de um item aparece aqui do mesmo jeito que qualquer outra. Veja o ciclo completo em [Manutenção: o desfecho do reparo](manutencao.md).
{% endhint %}

## Próximo passo

Entenda a regra que protege contra reserva dupla em [Galpões e disponibilidade](galpoes-e-disponibilidade.md), o que acontece quando um item volta do conserto em [Manutenção: o desfecho do reparo](manutencao.md) e como o pedido caminha em [O ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md). Em dúvida sobre um termo? Consulte o [Glossário](../primeiros-passos/glossario.md).
