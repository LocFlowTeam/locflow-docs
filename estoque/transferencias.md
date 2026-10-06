---
icon: right-left
description: Como mover material entre galpões e lojas — o despacho, o material em trânsito e a confirmação da chegada, que é o que faz o material entrar no destino.
---

# Transferências entre locais

Mover material de um lugar para outro parece simples: sai daqui, chega lá. No meio do caminho, porém, ele **não está em lugar nenhum** — e é aí que estoque costuma sumir das contas. O LocFlow trata a transferência em **duas fases** justamente para que esse intervalo fique visível.

A transferência move [bens móveis](../primeiros-passos/glossario.md) entre **galpões** e **lojas com estoque próprio** (veja [Lojas](lojas.md)). A tela fica em **Estoque › Transferências**.

## As duas fases

```mermaid
flowchart LR
    A["Despachar<br/>sai da origem na hora"] --> B["Em trânsito<br/>não aparece em nenhum dos dois locais"]
    B --> C["Chegou<br/>entra no destino"]
```

1. **Despachar** — o material **sai da origem na hora**.
2. **Em trânsito** — entre a saída e a chegada, ele **não aparece em nenhum dos dois locais**. A lista **Em trânsito** mostra o que ainda falta receber.
3. **Chegou** — alguém confirma a chegada no destino, e é **isso que faz o material entrar lá**.

{% hint style="info" %}
**Mesmo endereço, uma fase só.** Quando a loja tem estoque próprio **no balcão** — no mesmo endereço do galpão vinculado —, nada viaja: a transferência conclui na hora e o material só muda de conta. A mensagem diz *"Mesmo endereço — já entrou no estoque da loja."*
{% endhint %}

## Despachar

Você pode começar por três caminhos:

* **Estoque › Transferências** — a tela completa, com o formulário em cima e a lista **Em trânsito** embaixo;
* a **ficha do item** no [Painel de Estoque](painel.md) › **Operar em …** › **Transferir entre locais**, já com o produto e a origem escolhidos;
* as **caixinhas** da lista de Itens › **Operar** › transferir, para levar vários itens de uma vez (até 25). Veja [Operar vários itens de uma vez](operar-varios-itens.md).

Os passos:

1. Confira o item e a origem (trocar fica a um toque).
2. Escolha **Para onde vai?** — o galpão ou a loja de destino.
3. Informe a quantidade. O teto é o que pode ser despachado daquele local.
4. Toque em **Despachar**.

## Confirmar a chegada

Na lista **Em trânsito**, cada linha mostra o produto, a quantidade e o caminho (*"20 un · Galpão Centro → Loja · Shopping"*). Quando o material chegar:

* **Chegou** — confirma a chegada; o material entra no estoque do destino.
* **Cancelar** — desiste da transferência; *"O material voltou ao local de origem."*

{% hint style="warning" %}
**Sem confirmar a chegada, o material não entra no destino.** Ele continua em trânsito, fora das contas dos dois locais — e quem estiver na loja vai ver um estoque menor do que o da prateleira. Faça da confirmação um hábito de quem recebe.
{% endhint %}

## Transferência ligada a um pedido {#transferencia-ligada-a-um-pedido}

Quando o cliente vai **retirar numa loja que fica em outro endereço** e o material está no galpão, a retirada precisa que o material **chegue à loja antes**. Nesse caso a transferência fica **vinculada ao pedido** — a lista Em trânsito separa as **Deste pedido** das **Outras transferências** —, e o atendimento só libera a retirada depois que o material chega. Veja [Lojas](lojas.md) e [Balcão: retirada e devolução](../logistica/balcao.md).

## Quem pode fazer o quê

* Ver a tela e a lista Em trânsito pede a permissão de **listar transferências** — quem só confirma chegadas também precisa enxergar a fila.
* Despachar pede a permissão de **criar transferência**.

Se o item **Transferências** não aparece no seu menu, ele pode estar guardado porque a sua operação não usa mais de um local. Para mostrá-lo, use **Personalizar** no menu — ou fale com quem administra os [acessos](../configuracoes/colaboradores-e-acessos.md).

## Situações reais

* **"Abasteci a loja do shopping."** Despache do galpão para a loja. Quando o material chegar, quem está na loja toca em **Chegou** — e só então ele aparece no estoque da loja.
* **"Despachei para o galpão errado."** Enquanto ele estiver em trânsito, toque em **Cancelar**: o material volta para a origem.
* **"Loja e galpão dividem o mesmo prédio."** Configure a loja com **Estoque próprio no balcão**: as transferências entre os dois concluem na hora, sem fila.

## Próximo passo

Veja as outras operações em [Operações de estoque](operacoes-de-estoque.md), entenda galpão e loja em [Lojas](lojas.md) e acompanhe o que cada transferência registra em [Cada movimentação, em detalhe](posicao-e-previsao.md#movimentacoes).
