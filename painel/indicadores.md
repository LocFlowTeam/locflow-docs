---
icon: gauge
description: Os números do painel — contratado x recebido, negócios ganhos, conversão, perda e cancelamento. O que cada um significa, o período e de onde vem.
---

# Indicadores do painel

Na **Visão geral** (o painel inicial), o bloco de **Indicadores** resume a saúde comercial da sua operação em quatro cartões de números. Cada um responde a uma pergunta direta: *Quanto fechei? Quanto entrou no caixa? Estou ganhando ou perdendo negócio? E o que cai depois de fechado?*

{% hint style="info" %}
O cabeçalho do painel diz tudo: **"Um resumo de como está fluindo a sua operação."** Os indicadores são esse termômetro — não substituem o [funil](../orcamentos/acompanhando-e-fechando.md) (que mostra *onde* o negócio trava), mas dizem *o resultado* do que já foi decidido.
{% endhint %}

Cada cartão tem um **botão de ajuda (i)** no canto, com a explicação curta e — para quem quiser — o cálculo recolhido em **"Para quem quer os números"**.

## Os quatro cartões, um por um

### Faturamento do mês {#faturamento-do-mes}

Dois valores empilhados: **Contratado** e **Recebido**. A ajuda do cartão resume assim, quase com estas palavras:

> Dois números: **Contratado** é o valor dos **negócios fechados** no mês (orçamentos que entraram em **reservado/vendido**) — o que está comprometido. **Recebido** é o **dinheiro que entrou no caixa** de verdade (pagamentos confirmados). A diferença é o que você fechou mas ainda vai receber.

#### Contratado x Recebido {#contratado-vs-recebido}

| Número | O que é | Pergunta que responde |
| --- | --- | --- |
| **Contratado** | A soma do valor dos orçamentos que viraram **reservado** (locação) ou **vendido** (venda) no período. | *Quanto eu fechei?* |
| **Recebido** | A soma dos **pagamentos confirmados** que entraram no caixa no período. | *Quanto realmente entrou?* |

A **distância entre os dois** é o que você fechou mas ainda vai receber. Os dois costumam ser diferentes — você fecha um aluguel hoje, mas a parcela cai só na semana que vem.

{% hint style="info" %}
Este cartão só aparece se o seu acesso enxerga **cobrança**. Sem acesso a faturas, você vê os indicadores comerciais (ganhos, conversão, perda, cancelamento), mas não os valores em dinheiro.
{% endhint %}

### Negócios ganhos {#negocios-ganhos}

Um número grande em destaque — quantos negócios você **fechou** no período — quebrado em duas linhas: **Locação** e **Venda**, cada uma com seu ícone de natureza. A ajuda diz:

> Quantos negócios você **fechou** no mês, separados em **Aluguel** e **Venda** — assim você vê de onde veio cada ganho. (O que foi cancelado depois também conta aqui.)

{% hint style="warning" %}
**O que cancelou depois também conta aqui.** "Negócios ganhos" mede o que você **conquistou** no funil, não o que sobreviveu. Um aluguel que você fechou e o cliente cancelou na semana seguinte **continua** somando em Negócios ganhos — o cancelamento aparece no cartão próprio (abaixo). Isso é proposital: cancelar não apaga o fato de que você ganhou a disputa.
{% endhint %}

### Conversão e Perda {#conversao-e-perda}

Um par complementar, lado a lado, com uma barrinha verde/vermelha embaixo. A ajuda explica:

> De tudo que **já foi decidido**: **Conversão** é a fatia que você ganhou; **Perda** é a que escapou (juntas dão 100%). Mostramos também o **maior motivo de perda** — onde você mais deixa negócio escapar.

A palavra-chave é **decidido**. Conversão e Perda olham só para os orçamentos que **já tiveram um desfecho** — fecharam ou foram perdidos. Os que ainda estão em negociação **não entram na conta** (eles aparecem no [funil](../orcamentos/acompanhando-e-fechando.md), que inclui o pipeline aberto e por isso oscila mais).

* **Convertido** — a fatia que virou negócio.
* **Perdido** — a fatia que escapou (proposta que não fechou).

Como são complementares sobre a mesma base, **somam 100%**. Se metade dos seus orçamentos decididos vira negócio, você vê 50% / 50%.

Quando há perdas, o cartão mostra também o **maior motivo de perda** — veja [Maior motivo](#maior-motivo).

### Cancelamento {#cancelamento}

A taxa de negócios que você **chegou a fechar** e que **caíram depois**. É um alerta de pós-venda, separado da conversão e da perda. A ajuda diz:

> De tudo que você **chegou a fechar**, quanto **caiu depois** — um alerta de pós-venda. Quando há cancelamentos, mostramos o **maior motivo**, para você atacar a causa.

{% hint style="info" %}
**Cancelamento não é o mesmo que perda.** **Perda** é o negócio que não fechou (antes do ganho, no funil). **Cancelamento** é o negócio que fechou e depois caiu — quando já havia fatura e logística para desfazer. Por isso eles têm cartões e bases de cálculo diferentes. Veja a distinção completa em [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md#perda-e-cancelamento-com-motivo).
{% endhint %}

Sem cancelamentos no período, o cartão mostra **0%** com a nota *"Sem cancelamentos no período"* — o que é uma boa notícia.

### O maior motivo {#maior-motivo}

Tanto **Perda** quanto **Cancelamento** mostram, quando houve, o **maior motivo** e a fração que ele representa — por exemplo, *"Maior perda: Preço (40%)"* ou *"Maior motivo: Mudança de data (50%)"*.

Esses motivos vêm direto do que você registra ao **perder** ou **cancelar** um orçamento (a lista de motivos do fechamento). Quanto mais você registrar o motivo na hora de encerrar, mais útil fica esse resumo.

{% hint style="success" %}
**Por que isso vira decisão:** se "Preço" lidera as perdas, talvez sua tabela esteja fora do mercado; se é "Não respondeu", o problema é o *follow-up*. O painel transforma cada fechamento perdido num dado — e o conjunto deles, num mapa de onde você escorrega.
{% endhint %}

## Período e recorte {#periodo-e-recorte}

Por padrão, os indicadores olham o **mês atual**. É a foto do mês corrente: quanto você fechou, recebeu, converteu, perdeu e cancelou **neste mês**.

* **Negócios ganhos, Conversão, Perda e Cancelamento** contam os **fatos do período** — o que foi ganho, perdido ou cancelado dentro do mês.
* **Faturamento do mês** soma o **Contratado** (negócios fechados no mês) e o **Recebido** (pagamentos confirmados no mês).

{% hint style="info" %}
Os indicadores são contados pela **data do fato** (quando o negócio foi ganho, perdido, cancelado, ou quando o pagamento entrou). O gráfico maior de **Faturamento**, mais abaixo no painel, deixa você trocar essa base temporal e o intervalo — mas os **cartões de indicador** ficam sempre no mês corrente, para serem um termômetro rápido.
{% endhint %}

## De onde vem cada número {#de-onde-vem-cada-numero}

Estes números são **reais** — saem da sua operação, não são exemplos.

* **Negócios ganhos, Conversão, Perda, Cancelamento e os motivos** vêm de **contar os fechamentos** dos seus orçamentos no funil: cada vez que um orçamento é ganho (reservado/vendido), perdido ou cancelado, isso entra na conta do período.
* **Contratado** vem do **valor dos orçamentos ganhos**; **Recebido**, dos **pagamentos confirmados** na cobrança.

{% hint style="warning" %}
**Os números seguem o que você registra.** Se a equipe esquece de marcar um orçamento como perdido (deixa "parado" em negociação), ele **não** entra na Perda — fica no pipeline aberto do funil. Da mesma forma, a Conversão só é confiável quando os desfechos são lançados. O painel é tão honesto quanto o seu hábito de fechar os orçamentos no sistema.
{% endhint %}

Se um indicador não puder ser calculado (por exemplo, nenhum negócio decidido ainda no mês), o cartão mostra **"—"** em vez de um número inventado.

## Por porte: o que olhar primeiro {#por-porte}

| Porte | O indicador que mais importa |
| --- | --- |
| **Pequeno** | **Faturamento do mês** — Contratado x Recebido responde "quanto fechei e quanto entrou", que é o que tira o sono. Os demais viram úteis quando o volume cresce. |
| **Médio** | **Conversão e Perda** + o **maior motivo**: começa a dar para agir em cima do que faz o negócio escapar (preço, follow-up, área de entrega). |
| **Grande** | **Cancelamento** e os **motivos** viram rotina de gestão — pós-venda, inadimplência e mudança de data deixam de ser surpresa e viram processo. |

## Situações reais {#situacoes-reais}

- **"Fechei muito mas o caixa está magro":** Contratado bem acima de Recebido. Normal se você fecha hoje e recebe depois — mas se a distância só cresce, é sinal de cobrança atrasada. Veja [Recebendo pagamentos](../cobranca/recebendo-pagamentos.md).
- **"Estou perdendo metade":** Conversão em 50%, e o cartão aponta *Maior perda: Preço*. Hora de revisar a tabela ou a forma de apresentar o orçamento.
- **"Fechei 12 negócios, mas 3 caíram":** Negócios ganhos mostra 12 (inclui os que cancelaram); o cartão de Cancelamento mostra a taxa e o motivo — se for *Mudança de data*, talvez valha oferecer remarcação em vez de cancelar.
- **"O mês está zerado":** começo de mês, nada decidido ainda — Conversão e Perda aparecem como **"—"**. Não é erro; é só que ainda não houve desfecho para medir.

## Para quem quer os números {#para-quem-quer-os-numeros}

Os cartões escondem o cálculo atrás de **"Para quem quer os números"** — aqui está, de uma vez. As taxas usam duas siglas: **G** = ganhos (fechados), **C** = cancelados (que foram ganhos e depois caíram), **P** = perdidos.

| Indicador | Fórmula | Base |
| --- | --- | --- |
| **Negócios ganhos** | G + C | Fechados no período (cancelados ainda contam) |
| **Conversão** | (G + C) ÷ (G + C + P) | Só os **decididos** |
| **Perda** | P ÷ (G + C + P) | Só os **decididos** (Conversão + Perda = 100%) |
| **Cancelamento** | C ÷ (G + C) | Só os que **chegaram a fechar** |
| **Contratado** | Σ valor dos negócios ganhos | Período |
| **Recebido** | Σ pagamentos confirmados | Período |

Repare que **Conversão/Perda** e **Cancelamento** têm bases diferentes: a primeira inclui as perdas (todos os decididos), a segunda não (só o que fechou). São perguntas diferentes — "quanto do que decidi eu ganhei" versus "quanto do que ganhei eu mantive" — por isso vivem em cartões separados.

## Próximo passo

Para entender *onde* o negócio trava (e não só o resultado), veja o [funil de vendas](../orcamentos/acompanhando-e-fechando.md). Para o caixa, siga para [Recebendo pagamentos](../cobranca/recebendo-pagamentos.md). E para a operação física que cada negócio ganho dispara, veja a [visão geral da logística](../logistica/visao-geral.md).
