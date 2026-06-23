---
icon: filter
description: O funil de vendas do painel — quanto avança de uma etapa para a outra, a taxa de passagem e onde os orçamentos travam (o gargalo).
---

# O funil de vendas no painel

O **funil de vendas** do painel responde a uma pergunta só: **onde estão os seus negócios e onde eles travam** — do primeiro contato até fechar. É o mesmo caminho que você acompanha em [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md), só que visto de cima, em volume: quantos orçamentos estão em cada etapa agora.

{% hint style="info" %}
Texto de ajuda dentro do app: *"O funil mostra onde seus negócios estão e onde eles travam — do primeiro contato até fechar."* Toque no **(i)** no canto do card para abrir essa ajuda a qualquer momento.
{% endhint %}

## O que o funil mostra <a id="o-que-o-funil-mostra"></a>

O funil é um empilhado de etapas, do **topo** (mais orçamentos, primeiro contato) ao **fundo** (o fechamento). Cada etapa é um **estado do orçamento**:

* **Em aberto** — pedidos recebidos, ainda sem negociação iniciada.
* **Em negociação** — em conversa com o cliente, ajustando itens e valores.
* **Fechamento** — onde o negócio vira ganho. No **aluguel** isso acontece por dois caminhos (veja [Aluguel e venda](#aluguel-e-venda)); na **venda**, fecha direto em **vendido**.

Ao passar o mouse (ou tocar) numa etapa, abre um **detalhe** com a quantidade de orçamentos, o nome da etapa, o valor em **pipeline** e — quando faz sentido — a taxa de passagem e o aviso de gargalo. Veja [O detalhe de cada etapa](#detalhe-da-etapa).

### A forma é fixa — o volume está no número <a id="forma-fixa"></a>

Um detalhe importante de leitura: **a forma do funil não muda com os seus dados**. São sempre as mesmas etapas, na mesma ordem, com o mesmo afunilamento desenhado. O **volume está no número** (e no detalhe ao tocar), **não na largura** da faixa.

{% hint style="info" %}
Texto de ajuda do app: *"A forma do funil é fixa: são sempre as mesmas etapas, na mesma ordem. O volume está no número (e no detalhe ao tocar), não na largura — etapa sem nenhum orçamento aparece em cinza, para você nunca se perder no formato."*
{% endhint %}

Ou seja: uma etapa **sem nenhum orçamento** aparece em **cinza** (um espaço reservado), em vez de sumir. Assim o funil nunca "deforma" e você sempre reconhece o mesmo desenho.

### Aluguel e venda são separados <a id="aluguel-e-venda"></a>

O caminho do **aluguel** é diferente do caminho da **venda**, então o funil é **de uma natureza por vez**. Use o seletor no topo do card para alternar entre **Aluguel** e **Venda**.

A diferença mais importante está no **fechamento**:

| Natureza | Como fecha |
| --- | --- |
| **Venda** | Fecha direto em **vendido** — um único degrau de fechamento. |
| **Aluguel** | Fecha por **dois caminhos**: **pré-reserva** (com sinal, estoque pré-travado) **ou** **reserva direta**. |

No aluguel, a **pré-reserva** é opcional — um jeito de "segurar" o aluguel antes de confirmar de vez (veja [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md)). Como o cliente pode fechar por qualquer um dos dois, o funil **soma os dois caminhos** ao medir quem saiu da negociação. Isso evita subestimar o avanço (e o gargalo) só porque parte das reservas passou pela pré-reserva.

{% hint style="info" %}
**Estados terminais ficam de fora.** **Perdido**, **Cancelado** e **Finalizado** não entram no funil de conversão — ele é só o caminho de quem ainda pode (ou já conseguiu) fechar. Para olhar perdas e cancelamentos, use os **Indicadores** do painel e os motivos registrados em [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md).
{% endhint %}

## A taxa de passagem: quanto avança <a id="taxa-de-passagem"></a>

A **taxa de passagem** é o coração da leitura do funil. Ela responde: **de quem chegou até uma etapa, quantos avançaram para a próxima?**

> Passa **X%** para a próxima · retém **Y%**

Ela é calculada sobre o **acumulado** — quem está na etapa **ou já passou por ela**. Por isso a taxa fica **sempre entre 0% e 100%**: nunca passa de 100%, nunca fica negativa. Se 100 orçamentos chegaram à negociação e 60 já viraram reserva, a passagem da negociação é **60%** — e **40%** continuam "retidos" ali, ainda negociando.

{% hint style="info" %}
Texto de ajuda do app: *"A taxa de passagem é quantos avançaram de uma etapa, sobre quantos chegaram até ela (o acumulado — quem está ali ou já passou). Por isso fica sempre entre 0 e 100%."*
{% endhint %}

No **aluguel**, a passagem da negociação **conta os dois caminhos de fechamento juntos** — quem virou pré-reserva e quem virou reserva direta — como explicado em [Aluguel e venda](#aluguel-e-venda).

## O gargalo: onde os orçamentos travam <a id="gargalo"></a>

O **gargalo** é a etapa que **menos deixa passar** — a de **menor taxa de passagem**. É onde os orçamentos mais acumulam e escorrem. O painel marca essa etapa com um selo:

> **Gargalo · é aqui que mais acumula**

{% hint style="success" %}
Texto de ajuda do app: *"O gargalo é a etapa que MENOS deixa passar — a de menor taxa de passagem. O painel marca com 'Gargalo': é onde mexer rende mais."* Atacar o gargalo é o jeito mais barato de fechar mais: você não precisa de mais orçamentos no topo, só de **destravar onde já estão**.
{% endhint %}

Na prática: se o gargalo está em **negociação**, o problema é follow-up — propostas enviadas que ficam sem resposta. Se está em **em aberto**, é o **primeiro contato** que não acontece a tempo. O selo te diz onde olhar; o que fazer você decide com o resto do painel (motivos de perda, chance de fechar de cada orçamento).

## A conversão do funil <a id="conversao-do-funil"></a>

No resumo do card (quando nenhuma etapa está em foco) aparece a **conversão do funil**: quantos saíram do **topo** e chegaram ao **fechamento** (reserva ou venda).

{% hint style="warning" %}
**A conversão do funil oscila — e tudo bem.** Ela **inclui o pipeline ainda aberto** (orçamentos que ainda podem fechar ou cair), então sobe e desce conforme negócios entram e saem. Para a taxa de conversão "limpa" — só dos negócios **já decididos** —, olhe os **Indicadores** do painel.
{% endhint %}

Texto de ajuda do app: *"A conversão do funil é quantos saíram do topo e chegaram ao fechamento. Ela inclui o pipeline ainda aberto, então oscila — para a taxa 'limpa' (só dos já decididos), olhe os Indicadores."*

## O detalhe de cada etapa <a id="detalhe-da-etapa"></a>

Passe o mouse ou toque numa faixa para abrir o detalhe daquela etapa:

* **Quantidade** de orçamentos na etapa e o **valor em pipeline** (a soma dos valores dos orçamentos ali).
* A **taxa de passagem** e quantos ficam **retidos** (`Passa X% para a próxima · retém Y%`).
* O selo **Gargalo**, se for o caso.
* Uma descrição curta e dicas (ex.: *"Aguardando 1º contato · Priorize os mais antigos"*, *"Proposta enviada · Acompanhe os sem resposta"*).

O resumo (sem etapa em foco) mostra o total **no topo**, a **conversão do funil** e o **pipeline** total. A dica do card lembra: *"Passe o mouse ou toque numa etapa para ver os detalhes."*

## Esses números são reais ou de exemplo? <a id="numeros-reais-ou-ilustrativos"></a>

{% hint style="success" %}
**O funil de vendas usa os seus dados reais.** As quantidades e valores de cada etapa vêm dos **seus orçamentos**, agregados por natureza e estado. Não são números de exemplo: se você fechou uma reserva hoje, ela conta no funil.
{% endhint %}

Vale uma ressalva honesta: outros blocos do painel ainda podem mostrar **valores ilustrativos** enquanto ganham os dados reais (isso aparece sinalizado em cada bloco). O **funil de vendas**, porém, já lê os seus orçamentos de verdade.

## Por porte: o que olhar primeiro <a id="por-porte"></a>

| Porte | Como usar o funil |
| --- | --- |
| **Pequeno** | Olhe o **topo** e a **conversão** de vez em quando — confirma que não tem pedido esquecido entrando. Sem complicação. |
| **Médio** | Use o **gargalo** como rotina semanal: a etapa que menos deixa passar diz onde investir o follow-up. |
| **Grande** | Cruze o gargalo com os **motivos de perda** e a **chance de fechar** de cada orçamento: o funil aponta *onde*, os outros blocos dizem *por quê* — e isso vira decisão de preço, de equipe e de área de atendimento. |

## Para quem quer os números <a id="para-quem-quer-os-numeros"></a>

Esta parte é opcional — o funil se lê sem nenhuma fórmula. Mas se você gosta de saber a conta por trás, aqui está (é exatamente o que o app calcula).

### Volume acumulado <a id="volume-acumulado"></a>

O funil trabalha com **volume acumulado**: para cada etapa $i$, $V_i$ é **quantos chegaram até ali** — estão na etapa **ou já passaram** dela. Como quem avança continua sendo contado, vale sempre:

$$V_0 \ge V_1 \ge \dots \ge V_n$$

No **aluguel**, o fechamento $V_n$ **soma os dois caminhos**: pré-reserva + reserva.

### Taxa de passagem e parados <a id="formula-passagem"></a>

A taxa de passagem de uma etapa é o acumulado da etapa seguinte sobre o acumulado da etapa atual:

$$\text{passagem}_i = \frac{V_{i+1}}{V_i}$$

Como o numerador nunca é maior que o denominador, a taxa fica **sempre em [0, 1]** (0% a 100%) — nunca passa de 100% nem fica negativa. Quem ficou **retido** (parado) na etapa é a diferença:

$$\text{parados}_i = V_i - V_{i+1}$$

### Gargalo e conversão do funil <a id="formula-gargalo"></a>

O **gargalo** é a etapa de menor passagem:

$$\text{gargalo} = \min_i \; \text{passagem}_i$$

E a **conversão do funil** é o fechamento sobre o topo:

$$\text{conversão} = \frac{V_n}{V_0}$$

Como $V_0$ inclui o **pipeline ainda aberto** (orçamentos que ainda podem fechar ou cair), essa conversão **oscila** com o tempo. Para a conversão "limpa" — só dos negócios já decididos (ganhos sobre ganhos + perdidos) —, use os **Indicadores** do painel.

> **Base dos números:** os valores vêm dos seus orçamentos reais, agregados por natureza e estado atual. O funil é um retrato do **agora** — o estado em que cada orçamento está neste momento —, não um histórico de transições.

## Situações reais <a id="situacoes-reais"></a>

- **"Entra muito, fecha pouco":** o topo está cheio, mas a conversão do funil é baixa. Você abre o detalhe de cada etapa e o selo **Gargalo** está em **negociação** — propostas enviadas sem resposta. O problema não é falta de orçamento, é **follow-up**.
- **"Some no aluguel?":** você acha que a passagem da negociação está baixa, mas lembra que metade fecha por **pré-reserva**. Tranquilo: o funil já **soma pré-reserva + reserva** — o número que você vê é o avanço real.
- **"Uma etapa em cinza":** a etapa de pré-reserva aparece **cinza** porque você não usa pré-reserva — vai direto para reserva. Não é erro: é a etapa **sem orçamento**, desenhada como espaço reservado para o funil não deformar.

## Próximo passo <a id="proximo-passo"></a>

O funil mostra **onde** os negócios travam; para agir em cada orçamento, vá para [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md) — lá você arrasta o card, registra o **motivo** de perda e fecha (reserva/venda). Para entender o que cada estado significa, veja também o [ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md). Pedido ganho? Siga para a [cobrança](../cobranca/faturas-e-parcelas.md) e a [logística](../logistica/visao-geral.md).
