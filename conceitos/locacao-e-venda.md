---
icon: arrows-left-right
description: Locação e venda no mesmo sistema — o que muda no ciclo, e por que atender as duas modalidades amplia o que você fatura.
---

# Locação e venda

O LocFlow nasceu para **locadoras de bens móveis**, mas atende, no mesmo lugar, quem também **vende**. Não são dois sistemas: é o **mesmo** orçamento, a **mesma** cobrança e a **mesma** logística — muda só o que acontece com o item no fim.

{% hint style="success" %}
**Por que isso aumenta seu faturamento:** muita locadora vende peças usadas, consumíveis ou itens de mostruário — e perde esse dinheiro por não ter onde registrar. Com locação **e** venda no mesmo fluxo, toda receita passa pelo seu controle.
{% endhint %}

## A diferença em uma imagem

```mermaid
flowchart LR
    O[Orçamento] --> G[Ganho]
    G --> LOC[Locação:<br/>item vai e VOLTA]
    G --> VEN[Venda:<br/>item sai em DEFINITIVO]
    LOC --> ENT1[Entrega] --> RET[Retirada] --> CONF[Conferência] --> FIM1[Finalizado]
    VEN --> ENT2[Entrega] --> FIM2[Finalizado]
```

## O que muda na prática

| Aspecto | Locação | Venda |
| --- | --- | --- |
| **O item** | Vai ao cliente e **retorna** | Sai em **definitivo** |
| **Estado de ganho** | *Reservado* | *Vendido* |
| **Logística** | Entrega **e** retirada (+ conferência opcional) | Só entrega |
| **Estoque** | Bloqueado pelo período e liberado na volta | Baixa definitiva |
| **Datas** | Período (início e fim do uso) | Data de entrega |

## Um orçamento pode ter os dois

No mesmo orçamento você combina itens de **aluguel** e de **venda** (ex.: aluga a estrutura e vende os consumíveis). O LocFlow entende cada item pela sua natureza e organiza a logística certa para cada parte.

{% hint style="info" %}
Para um produto aparecer como vendável, ligue **"Você vai vender este produto?"** no cadastro e informe o preço de venda. Veja [Catálogo: produtos](../cadastros/catalogo-produtos.md).
{% endhint %}

## Próximo passo

Entenda o todo em [O ciclo de um pedido](ciclo-de-um-pedido.md) ou comece a cadastrar em [Catálogo: produtos](../cadastros/catalogo-produtos.md).
