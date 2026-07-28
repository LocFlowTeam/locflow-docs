---
icon: receipt
description: Toda taxa do pagamento online (transação, antecipação e saque) entra sozinha como despesa no seu financeiro, com o valor real do extrato. Seu saldo bate com o banco.
---

# Taxas do pagamento online

Receber online tem um custo: o **processador de pagamentos** (o serviço que move o dinheiro entre o cliente e você — também chamado de _gateway_) cobra uma taxa por operação. O LocFlow registra **todas essas taxas automaticamente** como despesa na sua Gestão Financeira, com o **valor real** — o mesmo que aparece no extrato do processador. Assim, o saldo que você vê no LocFlow **bate com a sua conta no banco**, sem diferença no fim do mês.

{% hint style="success" %}
**Por que isso importa:** taxa que você não enxerga vira surpresa. Ao lançar cada taxa sozinha, com o valor exato, o LocFlow mostra o **resultado real** de cada recebimento — quanto entrou, quanto o processador levou, e o que **de fato sobrou** para você.
{% endhint %}

## Quais taxas existem

São três tipos de taxa, todas registradas para você:

| Taxa | Quando acontece | Sobre o quê |
| --- | --- | --- |
| **Taxa de transação** | Toda vez que um cliente **paga** uma cobrança online (PIX, cartão ou boleto). | Um valor por pagamento recebido — o custo de processar aquela cobrança. |
| **Taxa de antecipação** | Quando você **antecipa** recebíveis (recebe antes do prazo de liquidação). | O custo de adiantar o dinheiro que ainda não liberou. Veja [Saldo e antecipação](saldo-e-antecipacao.md). |
| **Taxa de saque** | Quando o dinheiro **sai do recebedor para a sua conta bancária** — no saque manual **e** no automático. | O custo da transferência (tipo uma TED/crédito em conta). |

{% hint style="info" %}
**O saque automático também tem taxa.** Se você deixou a transferência automática ligada, cada envio para o seu banco também paga a taxa de saque — e o LocFlow registra essa taxa do mesmo jeito, mesmo você não tendo clicado em nada. Nada de custo escondido.
{% endhint %}

### Não confunda com a taxa da Rede de Parceiros {#taxa-de-plataforma}

Se você usa a [Rede de Parceiros](../parcerias/visao-geral.md), existe uma **quarta** taxa — e ela **não** é do processador:

| | **Taxa de gateway** | **Taxa de plataforma** |
| --- | --- | --- |
| Quem cobra | O processador de pagamentos | O LocFlow, pela Rede de Parceiros |
| Quando incide | Em todo pagamento online, com ou sem parceria | Só em operação **repassada a um parceiro** |
| Sobre o quê | Cada operação processada | **8% do total da operação**, uma vez por orçamento |
| No seu financeiro | Categoria **Taxa de Gateway** | Categoria **Taxa de Plataforma** — linha própria |

{% hint style="warning" %}
**Elas podem aparecer juntas no mesmo pagamento.** Quando o cliente paga online um pedido repassado, os 8% da Rede saem **retidos naquele pagamento** — então o valor que entra para você já vem menor que o total da fatura, além do desconto da tarifa do processador. Isso não é cobrança em dobro: quando você for quitar o repasse ao parceiro, o LocFlow desconta o que já foi retido e cobra só a diferença. A conta inteira está em [O dinheiro da parceria](../parcerias/dinheiro-da-parceria.md#taxa-de-plataforma).
{% endhint %}

Quem arca com a **taxa de gateway** numa operação repassada é um termo do próprio acordo de parceria (o padrão é o vendedor) — veja [Quem paga a maquininha](../parcerias/dinheiro-da-parceria.md#encargos).

## Como aparecem no seu financeiro

A forma de mostrar depende do tipo de taxa:

- **Taxa de transação — junto do recebimento.** Na lista de lançamentos, o **recebimento** e a **taxa** da mesma cobrança aparecem como **uma operação só**, já com o **resultado líquido** (o que entrou, menos a taxa). Toque na operação para ver a **composição**: entrou `+X`, saiu a taxa `−T`, sobrou `X − T`.
- **Taxa de antecipação e taxa de saque — como despesa avulsa.** Elas não pertencem a uma cobrança específica (são da operação de antecipar ou de sacar), então entram como uma **despesa própria** no razão, identificando a operação que a gerou.

Todas caem na categoria **Taxa de Gateway** do seu plano de contas, para você ver o total gasto em taxas nos relatórios.

{% hint style="success" %}
**Exemplo:** o cliente paga R$ 500 no PIX e quita a última parcela. O processador cobra, digamos, R$ 5 de taxa. No seu financeiro entra **+R$ 500** e sai **−R$ 5**, agrupados na mesma operação: o realizado final é **R$ 495**. Você vê de relance o que aquele recebimento rendeu de verdade.
{% endhint %}

## De onde vem o valor (e por que às vezes demora um pouco)

O LocFlow **não estima** a taxa: ele usa o **valor real**, lido do extrato de movimentações do processador. Por isso a taxa pode aparecer com um **pequeno atraso** depois do pagamento — o processador informa o valor exato quando **processa** a operação, e o LocFlow busca essa informação de tempos em tempos e lança a despesa.

{% hint style="info" %}
**Um pequeno atraso é normal e proposital.** Preferimos esperar o **valor exato** do extrato a mostrar um "chute" que depois não bate. Quando a taxa entra, ela já é o número certo — o mesmo do seu banco.
{% endhint %}

## Por porte

| Porte | O que observar nas taxas |
| --- | --- |
| **Autônomo / MEI** | Deixe o LocFlow trabalhar: as taxas entram sozinhas. De vez em quando, olhe o total em **Taxa de Gateway** nos relatórios para saber quanto o PIX está custando. |
| **Médio** | Compare o custo por método (PIX costuma ser o mais barato). Se usa antecipação, acompanhe a **taxa de antecipação** para saber o preço de receber antes. |
| **Grande** | Concentre saques (transferência manual) para diluir a **taxa de saque**, e use os relatórios de despesa por categoria para negociar melhores condições. |

## Situações reais

- **"Recebi R$ 500 mas no banco veio menos":** é a taxa de transação. No LocFlow ela aparece agrupada ao recebimento — abra a operação e veja o `+500 −5 = 495`. O que veio no banco bate com o líquido.
- **"Antecipei meu saldo":** além do recebimento, entra uma despesa de **taxa de antecipação** — o custo de receber antes do prazo.
- **"Deixei o saque automático ligado":** a cada transferência para o seu banco, entra uma pequena despesa de **taxa de saque**. Você não fez nada, mas o custo real fica registrado.

## Próximo passo

- Para acompanhar o dinheiro entrar e os saldos, veja [Pagamento online](pagamento-online.md) e [Saldo e antecipação](saldo-e-antecipacao.md).
- Para ver receitas e despesas do dia a dia (e o total em taxas), abra a sua **Gestão Financeira**.
