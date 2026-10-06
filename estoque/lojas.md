---
icon: store
description: A loja é o ponto onde o cliente retira e devolve — vinculada a um galpão, no mesmo endereço ou em outro, usando o estoque do galpão ou um estoque próprio.
---

# Lojas: onde o cliente retira e devolve

No LocFlow, **galpão** e **loja** são coisas diferentes:

| | **Galpão** | **Loja** |
| --- | --- | --- |
| **O que é** | Onde o material fica **guardado** | Onde o cliente é **atendido** — vem ver, retirar ou devolver os itens pessoalmente |
| **Onde fica no menu** | **Estoque › Galpões** | **Estoque › Lojas** |
| **Para que o sistema usa** | Origem das entregas, alcance do frete e base da disponibilidade | Ponto de retirada e devolução que o cliente combina no pedido |

**Toda loja é vinculada a um galpão**: é dele que sai o material das retiradas daquela loja. Os dois podem estar **no mesmo endereço** — o caso mais comum — ou em **endereços diferentes**.

{% hint style="info" %}
**Você já tem uma loja.** Ao cadastrar o primeiro galpão, o LocFlow cria a primeira loja sozinho, no mesmo endereço. Quem opera de um endereço só não precisa fazer nada — e nem precisa pensar que são dois cadastros.
{% endhint %}

## Cadastrar uma loja

Em **Estoque › Lojas**, toque em **+**. O cadastro tem três partes:

1. **Identificação** — o **Nome** da loja (ex.: *Loja Centro*). *É este nome que o cliente vê ao combinar a retirada presencial.*
2. **Galpão vinculado** — *o material das retiradas desta loja sai deste galpão.*
3. **Endereço** — informe o CEP e confira o pino no mapa. Se a loja fica no mesmo lugar do galpão, use **Usar o endereço do galpão vinculado**.

## O estoque da loja

Depois de salva, a loja ganha, na edição, a seção **Estoque da loja** — *"onde vive o estoque das retiradas e devoluções feitas nesta loja"*. A mudança **vale na hora**.

| Opção | Quando usar | O que acontece |
| --- | --- | --- |
| **Usar o estoque do galpão** | A loja é só o balcão de atendimento | Disponibilidade, reserva e baixa acontecem no galpão vinculado |
| **Estoque próprio no balcão** *(recomendado quando o endereço é o mesmo)* | Loja e galpão dividem o endereço, mas você quer separar o que fica no balcão | Abastecer é imediato — o material só muda de conta — e o balcão conta na disponibilidade |
| **Estoque próprio em outro endereço** | A loja fica longe do galpão e guarda material | Abastecer é uma transferência em duas fases: sai do galpão e alguém confirma a chegada |

A opção **Estoque próprio no balcão** só pode ser escolhida quando a loja tem o **mesmo endereço** do galpão vinculado.

{% hint style="warning" %}
**Reintegre o estoque antes de desligar.** Uma loja com estoque próprio que ainda tem saldo ou reserva não pode voltar a usar o estoque do galpão. A tela avisa quantos itens estão lá: transfira o material de volta ao galpão vinculado (a transferência é imediata quando é o mesmo endereço) e tente de novo.
{% endhint %}

## A loja com estoque próprio no dia a dia

* Ela aparece como um **local** no [Painel de Estoque](painel.md), com o ícone de loja ao lado do nome.
* No estoque da loja só existem duas operações — **Conferir contagem** e **Transferir entre locais**. As demais (entrada, reparo, baixa…) são do galpão.
* Abastecer e recolher o balcão é uma [transferência](transferencias.md).

## Loja em outro endereço: o material precisa chegar antes

Quando a loja fica longe do galpão, o material que o cliente vai buscar precisa **chegar à loja antes do atendimento**. O LocFlow mostra a transferência pendente e só libera a retirada quando o material está lá. Veja [Transferências](transferencias.md#transferencia-ligada-a-um-pedido).

O atendimento do cliente na loja — retirada e devolução — acontece em **Logística › Minha Loja**. Veja [Loja: retirada e devolução pelo cliente](../logistica/balcao.md).

{% hint style="success" %}
**Por que isso te faz faturar mais:** separar onde o material fica de onde o cliente é atendido deixa você abrir um ponto de retirada mais perto do cliente sem mudar o galpão de lugar — e sem prometer na loja um item que ainda está do outro lado da cidade.
{% endhint %}

## Próximo passo

Cadastre e ajuste o galpão em [Galpões e disponibilidade](galpoes-e-disponibilidade.md), veja como abastecer a loja em [Transferências](transferencias.md) e acompanhe o estoque de cada local no [Painel de Estoque](painel.md).
