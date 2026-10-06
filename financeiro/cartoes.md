---
icon: credit-card
description: Os cartões de crédito e débito da empresa — cadastro, a fatura de cada ciclo, as compras de cada fatura e como pagar a fatura sem lançar a despesa duas vezes.
---

# Cartões

Muita despesa de locadora passa pelo cartão da empresa: o combustível, a peça da oficina, a assinatura do sistema. No crédito, o dinheiro não sai no dia da compra — sai no dia em que a **fatura** é paga, somando um mês inteiro de compras. Sem o cartão cadastrado, essa dívida fica invisível até o vencimento.

Você cadastra os cartões em **Gestão Financeira → engrenagem (Ajustes) → Cartões** — *"Crédito e débito, com a fatura de cada ciclo"*.

{% hint style="success" %}
**Por que vale cadastrar:** com o cartão no LocFlow, cada compra entra no razão no dia em que aconteceu, na categoria certa — e a fatura aparece nas contas a pagar como uma linha só, com o total e a data. Você sabe quanto deve no cartão **antes** de a fatura chegar.
{% endhint %}

## Crédito ou débito

| | **Crédito** | **Débito** |
| --- | --- | --- |
| Como funciona | *Acumula uma fatura e você paga tudo de uma vez* | *Sai da conta na hora da compra* |
| Onde a compra aparece | Na **fatura** do cartão, como dívida prevista | Direto na conta do banco, como uma despesa qualquer |
| Tem ciclo? | Sim — fecha e vence num dia do mês | Não |

## Cadastrar um cartão

Em **Cartões**, use **Novo cartão**:

1. **Crédito** ou **Débito**.
2. **Apelido** — como a equipe chama o cartão (*Nubank PJ*) — e o **Final**, os 4 últimos dígitos.
3. **De qual banco é este cartão?** — a [conta](contas.md) Banco a que ele pertence. No crédito, *a fatura é paga por esta conta — é o banco do cartão que debita, mesmo que você transfira dinheiro de outro para cobrir*. No débito, cada compra sai dessa conta na hora. (Cadastre uma conta bancária antes, se ainda não tiver.)
4. No crédito, **O ciclo da fatura**: **Fecha no dia** e **Vence no dia**.
5. **Salvar cartão**.

Para mudar o apelido, o final, os dias do ciclo ou — no crédito — o banco que paga a fatura, abra o cartão e use **Editar cartão**. A função (crédito ou débito) não muda depois do cadastro; no cartão de débito, o banco também não.

## A tela de cartões

No topo, **Faturas em aberto**: quanto você deve somando todos os cartões. Embaixo, um cartão por cartão, com:

* o apelido, a função e o final (*Crédito · final 1234*) e o ciclo;
* cada **fatura a pagar** — *"Fatura de 05/08 a 04/09"* —, com a situação (**Aberta**, **Fechada — a pagar**, **Vencida** ou **Paga**), o valor em aberto, quantas compras e o vencimento;
* a **fatura em curso** (ou a **próxima fatura**), com as compras até agora, o dia em que fecha e, quando houver, o **disponível no limite**.

Toque em **Ver as N compras desta fatura** (ou **Ver as compras deste ciclo**) para abrir o extrato.

### O extrato da fatura

O extrato mostra uma fatura por vez — o **total da fatura**, o que **já foi pago** e o que está **em aberto** — e a lista de compras daquele ciclo. As setas do topo andam entre os ciclos.

* Ele abre no ciclo que **pede decisão**: entre o fechamento e o vencimento existem duas faturas ao mesmo tempo, e a mais recente costuma ser a errada para pagar.
* Compras que vieram de uma **assinatura** ou de um **parcelamento** aparecem com o ícone de série — é a resposta para *"por que a fatura subiu?"*.

## Lançar uma compra no cartão

Ao [registrar uma despesa](lancamentos.md#registrar-um-lancamento), escolha a forma de pagamento **Cartão de crédito** ou **Cartão de débito**, e a tela pergunta **qual cartão**:

* no **crédito**, a compra entra na fatura daquele cartão — e no ciclo certo, pelo dia da compra;
* no **débito**, a despesa sai da conta do banco do cartão, e o cartão fica registrado para você saber quanto passou em cada um.

Comprou parcelado? Em *Quanto e quando?*, escolha **Ainda vou pagar**, ligue **Repetir automaticamente** e escolha **3x**, **6x**, **10x** ou **12x**: o valor é dividido, e cada parcela cai na fatura do seu mês. Veja [Contas fixas e parcelamentos](lancamentos.md#conta-fixa).

## Pagar a fatura

Na fatura fechada (ou vencida), toque em **Pagar fatura pela** *(conta do banco do cartão)* — o botão já diz de qual conta o dinheiro sai. A mensagem confirma quantas compras foram quitadas e o valor pago. No extrato da fatura, o mesmo pagamento está em **Pagar pela** *(conta do banco do cartão)*.

{% hint style="warning" %}
**Pagar a fatura é uma transferência, não uma despesa.** O dinheiro sai da conta do banco e quita o cartão — a despesa foi cada **compra**, que já está no razão desde o dia em que aconteceu. Não lance o pagamento da fatura como despesa: você contaria o mesmo gasto duas vezes.
{% endhint %}

## Onde o cartão aparece no resto do financeiro

* **No saldo, não.** O que você deve no cartão é **previsto**: não entra no saldo em caixa até a fatura ser paga.
* **Em Contas**, a fatura que vence aparece como **uma linha só**, com o nome do cartão e o total — não uma linha por compra. Veja [Contas a pagar e a receber](contas-a-pagar-e-a-receber.md).
* **Nos Relatórios**, o corte **Cartão** dos Insights responde *"quanto passou em cada cartão"* — crédito e débito juntos. Veja [Relatórios: como ler](relatorios.md).
* **Em Contas (Ajustes)**, cada cartão de crédito tem a sua conta da fatura, que o LocFlow mantém sozinho. Veja [Contas](contas.md).

## Inativar um cartão

Cartão cancelado? Abra-o e use **Inativar**: ele sai da rotina, mas o histórico das faturas permanece — e, se ainda houver valor em aberto, ele continua a pagar. **Reativar** traz o cartão de volta.

## Próximo passo

* Para lançar as compras: [Lançamentos](lancamentos.md).
* Para acompanhar o vencimento da fatura: [Contas a pagar e a receber](contas-a-pagar-e-a-receber.md).
* Para ver quanto passou em cada cartão: [Relatórios: como ler](relatorios.md).
