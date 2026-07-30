---
icon: money-check-dollar
description: As duas filas de vencimento — o que você deve e o que esperam te pagar — organizadas por urgência, com confirmação em um toque.
---

# Contas a pagar e a receber

Esta é a tela da pergunta mais urgente do financeiro: **o que dói agora?** Ela lista os lançamentos **previstos** — o que ainda não aconteceu — agrupados por **janela de vencimento**, do que já venceu ao que está longe.

Você chega nela pelo menu do financeiro, em **Contas a pagar**. O botão no topo alterna os dois lados.

{% hint style="success" %}
**Por que ela vale a primeira visita do dia:** aqui a leitura é visual, não textual. Você não precisa ler linha por linha para descobrir o que atrasou — a cor, o grupo e o total dizem antes. Em cinco segundos você sabe quanto está vencido e quanto vence hoje.
{% endhint %}

## Os dois lados

| | **A pagar** | **A receber** |
| --- | --- | --- |
| O que lista | **Saídas previstas** — o que você deve | **Entradas previstas** do razão |
| Vem de onde | Despesas que você agendou, contas fixas e o custo de frete de terceiro provisionado | Receitas que você agendou e receitas fixas |
| A confirmação | *Marcar como paga* | *Marcar como recebida* |

{% hint style="warning" %}
**Recebível de cliente não vive aqui — vive em Cobranças.** Quando você ganha um pedido, o valor a receber do cliente nasce como **fatura e parcelas** na tela de [Cobranças](../cobranca/lista-de-cobrancas.md), que é onde você emite, acompanha e dá baixa. O lado **A receber** desta tela é para as **outras** entradas previstas: um reembolso combinado, a venda de um ativo, um recebimento avulso que você mesmo agendou. Se o dinheiro é de cliente, o caminho é Cobranças — e quando a parcela é quitada, a entrada aparece **sozinha** no seu razão.
{% endhint %}

## As janelas de vencimento

Todo previsto cai em uma janela, e a ordem na tela é a da urgência:

| Janela | A pagar | A receber |
| --- | --- | --- |
| Já passou do vencimento | **Vencidas** | **Atrasados** |
| Vence no dia de hoje | **Vence hoje** | **Previsto hoje** |
| Cai nos próximos 7 dias | **Próximos 7 dias** | **Próximos 7 dias** |
| Depois disso | **Mais adiante** | **Mais adiante** |
| Sem data definida | **Sem vencimento** | **Sem vencimento** |

Cada grupo traz a **quantidade** e o **total** dele. As três primeiras janelas também são **chips de filtro** no topo — toque em *Vencidas* para ver só o que atrasou, toque de novo para voltar a ver tudo.

No topo, como protagonista, fica o **total do lado inteiro**: o quanto você deve, ou o quanto espera receber, somando todas as janelas.

{% hint style="info" %}
**"Sem vencimento" tem grupo próprio de propósito.** Um previsto sem data não é uma conta vencida — mas, misturado, ele parecia uma. Agora ele fica no fim da lista, visível, esperando você definir a data quando souber.
{% endhint %}

Dentro de cada grupo, o vencimento **mais antigo vem primeiro**: o que dói mais fica no topo.

## Marcar como paga (ou recebida)

Toque na linha e a folha de confirmação abre. Ela pergunta o **valor realmente pago**, o **dia** em que o dinheiro se moveu e a **conta** por onde ele passou — o passo a passo completo, com a regra da justificativa, está em [Lançamentos](lancamentos.md#confirmar).

Confirmado, o lançamento sai desta tela e passa a compor o **saldo**.

{% hint style="info" %}
**Nem toda linha é confirmável aqui.** Você confirma o que o financeiro gerencia — despesas e receitas **manuais**, **contas fixas** e o **custo de frete de terceiro** provisionado por um pedido. O que espelha um fato de outro módulo (o recebimento de uma fatura, por exemplo) é resolvido na origem. E confirmar exige a permissão de editar lançamentos: se a opção não aparece, é acesso — fale com quem administra as permissões.
{% endhint %}

## Criar uma conta a pagar ou a receber

O botão **+** abre o lançamento já do lado certo e já como **previsto**: você informa valor, descrição, categoria e **vencimento**. No passo *Quando* dá para transformá-lo numa **conta fixa** (mensal, semanal ou anual) — e os próximos vencimentos já nascem nesta lista.

## Quando a lista está vazia

A tela explica o vazio em vez de mostrar só um espaço em branco:

* **Nenhuma conta a pagar** — *"Crie despesas previstas no botão + ou uma conta fixa que se repete sozinha."*
* **Nada a receber previsto** — *"Recebíveis de clientes ficam na tela de Cobranças."*
* **Nada nesta janela** — quando é o filtro que está estreito, e não a fila que está vazia; um toque em **Ver todas** desfaz.

## Por porte

| Porte | Como usar |
| --- | --- |
| **Autônomo / MEI** | Cadastre as contas fixas (aluguel, internet, telefone) uma vez. Abra a tela de manhã e olhe só os chips **Vencidas** e **Hoje**. |
| **Médio** | Use **Próximos 7 dias** para programar a semana e confirmar os pagamentos pelo valor real, com a conta certa. |
| **Grande** | Trate a tela como fila da tesouraria: zerar **Vencidas** todo dia, e o total do lado como o número que vai para a reunião. |

## Situações reais

* **"O que eu tenho que pagar hoje?"** Abra a tela, toque no chip **Hoje**. O total do grupo é o quanto sai hoje.
* **"Paguei a conta de água ontem, mas com desconto."** Toque na linha, troque o valor para o real, ajuste a data para ontem e confirme. O previsto fica guardado como estimativa.
* **"Fechei um pedido e não vejo o valor do cliente aqui."** Ele está em [Cobranças](../cobranca/lista-de-cobrancas.md), como fatura. Quando a parcela for quitada, a entrada aparece sozinha no razão.
* **"Desisti de uma despesa que eu tinha agendado."** Abra a linha em [Lançamentos](lancamentos.md) e use **Cancelar conta**: ela sai da fila e continua no histórico.

## Próximo passo

* Para entender o que é previsto e o que é realizado: [Lançamentos](lancamentos.md#previsto-x-realizado).
* Para o dinheiro que os clientes te devem: [Cobranças: a lista e o que mostra](../cobranca/lista-de-cobrancas.md).
* Para conferir o que já foi pago contra o extrato do banco: [Conciliação e fechamento](conciliacao-e-fechamento.md).
