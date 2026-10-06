---
icon: money-check-dollar
description: As duas filas de vencimento — o que você deve e o que esperam te pagar — organizadas por urgência, com confirmação em um toque, e o que você já pagou ou recebeu no mês.
---

# Contas a pagar e a receber

Esta é a tela da pergunta mais urgente do financeiro: **o que dói agora?** Ela abre nos lançamentos **previstos** — o que ainda não aconteceu — agrupados por **janela de vencimento**, do que já venceu ao que está longe. E responde também a pergunta que vem junto no fim do mês: **e o que eu já paguei?**

Você chega nela pelo menu do financeiro, em **Contas** (*o que vence e o que já venceu*). O botão no topo alterna os dois lados: **A pagar** e **A receber**.

{% hint style="success" %}
**Por que ela vale a primeira visita do dia:** aqui a leitura é visual, não textual. Você não precisa ler linha por linha para descobrir o que atrasou — a cor, o grupo e o total dizem antes. Em cinco segundos você sabe quanto está vencido e quanto vence hoje.
{% endhint %}

## Os dois lados

| | **A pagar** | **A receber** |
| --- | --- | --- |
| O que lista | **Saídas previstas** — o que você deve | **Entradas previstas** do razão |
| Vem de onde | Despesas que você agendou, contas fixas, o custo de frete de terceiro provisionado e as faturas de cartão de crédito | Receitas que você agendou, receitas fixas e o faturado das notas fiscais avulsas |
| A confirmação | *Marcar como paga* | *Marcar como recebida* |

{% hint style="warning" %}
**Recebível de cliente não vive aqui — vive em Cobranças.** Quando você [gera a cobrança](../cobranca/emitindo-a-cobranca.md) do pedido, o valor a receber do cliente nasce como **fatura e parcelas** na tela de [Cobranças](../cobranca/lista-de-cobrancas.md), que é onde você emite, acompanha e dá baixa. O lado **A receber** desta tela é para as **outras** entradas previstas: um reembolso combinado, a venda de um ativo, um recebimento avulso que você mesmo agendou. Se o dinheiro é de cliente, o caminho é Cobranças — e quando a parcela é quitada, a entrada aparece **sozinha** no seu razão.
{% endhint %}

## Em aberto, pagas ou tudo {#leituras}

Logo abaixo do botão de lado, três leituras:

| Leitura | O que mostra |
| --- | --- |
| **Em aberto** | O previsto, por janela de vencimento — a fila de sempre, e o padrão ao abrir |
| **Pagas** (no lado a receber, **Recebidas**) | O que já foi quitado no período |
| **Tudo** | As duas juntas |

Elas não são o mesmo dado peneirado. **Em aberto** não corta pelo começo do período: uma conta vencida em julho e ainda não paga continua aparecendo em agosto — escondê-la seria esconder justamente o que você abriu a tela para pagar. (Com um período escolhido, ele só limita até quando a lista olha para a frente.) Já **Pagas** e **Tudo** precisam de um período: ao escolher uma delas, o recorte de período liga sozinho (no período do módulo) e aparece no filtro, à vista.

{% hint style="info" %}
**O total do topo é uma dívida, não um movimento.** O **total a pagar** soma só o que está em aberto — o que já foi quitado não entra nele, mesmo na leitura **Tudo**. E o que já foi pago sai da escada de urgência: uma conta quitada com três dias de atraso não aparece como "vencida".
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

{% hint style="info" %}
**A fatura do cartão é uma linha só.** As compras feitas no cartão de crédito não aparecem uma a uma: a fatura que vence aparece como **uma linha**, com o nome do cartão, a quantidade de compras e o total. Toque nela para abrir as compras daquela fatura. Veja [Cartões](cartoes.md).
{% endhint %}

## Marcar como paga (ou recebida)

Toque na linha e a folha de confirmação abre. Ela pergunta o **valor realmente pago**, o **dia** em que o dinheiro se moveu e a **conta** por onde ele passou — o passo a passo completo, com a regra da justificativa, está em [Lançamentos](lancamentos.md#confirmar).

Confirmado, o lançamento sai desta tela e passa a compor o **saldo**.

{% hint style="info" %}
**Nem toda linha é confirmável aqui.** Você confirma o que o financeiro gerencia — despesas e receitas **manuais**, **contas fixas** e o **custo de frete de terceiro** provisionado por um pedido. O que espelha um fato de outro módulo (o recebimento de uma fatura, por exemplo) é resolvido na origem. E confirmar exige a permissão de editar lançamentos: se a opção não aparece, é acesso — fale com quem administra as permissões.
{% endhint %}

## Criar uma conta a pagar ou a receber

O botão **+** abre o lançamento já do lado certo e já como **previsto**: você informa a categoria, quem recebe (ou quem paga), o valor e o **vencimento**. Em *Quanto e quando?* dá para ligar **Repetir automaticamente** e transformá-lo numa **conta fixa** (todo mês, toda semana ou todo ano) ou num **parcelamento** — e os próximos vencimentos já nascem nesta lista. Veja [Contas fixas e parcelamentos](lancamentos.md#conta-fixa).

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
* **"Fechei um pedido e não vejo o valor do cliente aqui."** Ele aparece em [Cobranças](../cobranca/lista-de-cobrancas.md), como fatura, quando você gera a cobrança. Quando a parcela for quitada, a entrada aparece sozinha no razão.
* **"Quanto eu já paguei este mês?"** Troque para **Pagas**: o recorte do mês liga sozinho, e a lista mostra o que foi quitado.
* **"Desisti de uma despesa que eu tinha agendado."** Abra a linha em [Lançamentos](lancamentos.md) e use **Cancelar conta**: ela sai da fila e continua no histórico.

## Próximo passo

* Para entender o que é previsto e o que é realizado: [Lançamentos](lancamentos.md#previsto-x-realizado).
* Para o dinheiro que os clientes te devem: [Cobranças: a lista e o que mostra](../cobranca/lista-de-cobrancas.md).
* Para conferir o que já foi pago contra o extrato do banco: [Conciliação e fechamento](conciliacao-e-fechamento.md).
