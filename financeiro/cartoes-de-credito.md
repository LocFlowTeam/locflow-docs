---
icon: credit-card
description: A fatura do cartão igual à do banco — pagar quando e quanto quiser, desfazer um pagamento, lançar juros, IOF, multa, crédito e estorno, e mover uma compra para a fatura certa.
---

# Cartões de crédito

No cartão de crédito, a compra e o pagamento acontecem em dias diferentes: você passa o cartão hoje, e o dinheiro só sai do banco quando paga a fatura. O LocFlow acompanha os dois momentos. Cada compra entra na **fatura** do ciclo dela, e a fatura mostra, como a do banco, o que sobrou da fatura passada, o que você comprou, os juros que o banco cobrou, os créditos que ele deu, o que já foi pago e **o que ainda falta**.

Você encontra os cartões em **Gestão Financeira → engrenagem (Ajustes) → Cartões**. A fatura também aparece em [Contas a pagar](contas-a-pagar-e-a-receber.md), numa linha só (**Fatura · nome do cartão**), e um toque nela traz você para cá.

{% hint style="success" %}
**Por que vale registrar a fatura como ela é:** na vida real você antecipa o pagamento para liberar limite, paga uma parte e deixa o resto, às vezes paga a mais. Se o LocFlow só soubesse "pagou tudo" ou "não pagou", a fatura dele nunca bateria com a do banco — e você deixaria de confiar nos dois números. Aqui cada pagamento tem **valor, data e a conta de onde o dinheiro saiu**.
{% endhint %}

## Cadastrar um cartão {#cadastrar}

Na tela de Cartões, toque no **+** (*Cadastrar cartão*). A folha **Novo cartão** pede:

| Campo | O que é |
| --- | --- |
| **Crédito** ou **Débito** | Crédito *"acumula uma fatura e você paga tudo de uma vez"*. Débito *"sai da conta na hora da compra"* — e por isso não tem fatura. |
| **Apelido** e **Final** | Como a equipe reconhece o cartão (*Nubank PJ*) e os 4 últimos dígitos dele. |
| **De qual banco é este cartão?** | No crédito, a conta que paga a fatura. É ela que já vem marcada quando você for pagar. |
| **Bandeira** | Visa, Mastercard, Elo, American Express ou Hipercard. Opcional — tocar de novo desmarca. |
| **Limite** | Opcional, só no crédito. Com ele, a ficha do cartão mostra quanto ainda está **livre**. |
| **Fecha no dia** e **Vence no dia** | O ciclo da fatura. Compra feita depois do dia de fechamento entra na fatura seguinte. |

Para lançar uma compra no cartão, registre a despesa em [Lançamentos](lancamentos.md#registrar-um-lancamento) e escolha a forma de pagamento **Cartão de crédito** e o cartão. A compra entra sozinha na fatura do ciclo dela — e uma compra parcelada põe cada parcela numa fatura.

## Como a fatura é calculada {#como-a-fatura-e-calculada}

A conta é a mesma do banco:

| | O que entra | Quem lança |
| --- | --- | --- |
| **Saldo anterior** | O que a fatura passada deixou sem pagar | O LocFlow, sozinho |
| **+ Compras** | As compras do ciclo, parcelas inclusive | Você, em Lançamentos |
| **+ Juros, IOF e multa** | O que o banco cobrou | Você, [na fatura](#encargos) |
| **− Créditos e estornos** | O que o banco devolveu ou deu | Você, [na fatura](#credito-ou-estorno) |
| **− Pagamentos** | O que você já pagou desta fatura | Você, [ao pagar](#pagar) |
| **= Falta** | O que ainda precisa ser pago | — |

**Um exemplo.** A fatura de novembro venceu com R$ 440,00 sem pagar. No dia 2 de dezembro, a fatura de dezembro mostra:

| Composição | Valor |
| --- | --- |
| Saldo anterior (novembro) | R$ 440,00 |
| Compras · 6 | R$ 860,00 |
| Juros e IOF | R$ 32,40 |
| Estorno Kalunga | − R$ 20,00 |
| Pagamentos | R$ 0,00 |
| **Falta** | **R$ 1.312,40** |

Esse quadro, a **Composição**, aparece na fatura sempre que há saldo anterior, juros ou créditos — quando "compras menos pagamentos" já não explica o número de cima.

{% hint style="info" %}
**A fatura leva o nome do mês em que vence**, como no banco. O ciclo de 21/10 a 20/11, que vence em 27/11, é a *fatura de novembro*. Nas listas, o ciclo aparece com as datas (*Fatura de 21/10 a 20/11*), porque escrever só o mês esconderia onze dias de compras.
{% endhint %}

### Os estados de uma fatura {#estados}

| Selo | Quando | O que você faz |
| --- | --- | --- |
| **Aberta** | Ainda recebe compras: o dia de fechamento não chegou | Pode **antecipar** o pagamento |
| **Fechada — a pagar** | Fechou, tem saldo e o vencimento não passou | **Pagar fatura** |
| **Fechada · parcial** | Fechou e já recebeu parte do pagamento | Pagar o que falta |
| **Vencida** | Passou do vencimento com saldo | O que falta já está na fatura seguinte, como saldo anterior |
| **Paga** | Nada mais a pagar | — |

### O que passa para a fatura seguinte {#saldo-anterior}

* **O que não for pago até o vencimento** passa, no dia seguinte, para a próxima fatura como **saldo anterior**. A fatura vencida avisa: *"R$ 440,00 não foram pagos até 27/11 e já estão na fatura de dezembro, como saldo anterior. O banco costuma cobrar juros sobre eles."* E a fatura de dezembro diz de onde o valor veio.
* **O que você pagar a mais** vira **crédito**. Na fatura aberta, ele abate as próximas compras dela; se sobrar no fechamento, passa para a fatura seguinte.

A dívida que passou de uma fatura para a outra aparece nas duas, mas **conta uma vez só** — nos totais, no limite e em contas a pagar. Você pode pagá-la por qualquer uma das duas: o pagamento abate **primeiro a dívida mais antiga**, como no banco.

## A tela de Cartões e a ficha do cartão {#onde-encontrar}

No topo da tela, **Faturas em aberto** soma o que falta em todos os cartões — *"Isto não sai do seu saldo em caixa até você pagar."* Abaixo, cada cartão mostra:

* as faturas que **pedem pagamento** (fechadas ou vencidas, com saldo), cada uma com o selo, o que **falta** (não o total), o que já foi pago e o vencimento, e os botões **Ver as {N} compras** e **Pagar fatura…**;
* a **fatura em curso** (ou **Próxima fatura**, quando há uma fechada antes dela), com o que entrou até agora, o **disponível no limite** e o link **Antecipar pagamento**.

Toque no nome do cartão para abrir a **ficha do cartão** — no celular, uma folha; em telas largas, ao lado da lista. Ela abre na fatura que pede decisão (a fechada ou vencida com saldo) e, sem nenhuma, na fatura em curso. São três abas:

| Aba | O que mostra |
| --- | --- |
| **Fatura** | Os avisos (vencida, saldo anterior), o quadro da fatura com **Compras · Pagamentos · Falta** e o botão de pagar, a **Composição**, a lista de **Pagamentos** e a lista de **Compras** |
| **Anteriores** | As faturas passadas, com o selo de cada uma. Toque numa para vê-la |
| **Dados** | Apelido, final, bandeira, o ciclo, o limite e a conta que paga a fatura — com **Editar** |

No cabeçalho, o número grande é o que **falta** (*"R$ 740,00 a pagar"*, com *"de R$ 1.240,00 · vence 27/11"* embaixo), e logo abaixo vem o **limite livre** (*"R$ 2.640,00 livres no limite"*). O limite livre desconta as faturas em aberto **e as parcelas que ainda vão cair**, volta na hora quando você paga e aumenta com um crédito. Fica âmbar quando sobra menos de um décimo do limite, e vermelho quando acaba.

## Pagar a fatura {#pagar}

Você pode pagar **a qualquer momento** — com a fatura aberta, fechada ou vencida —, **quanto quiser** e **quantas vezes precisar**. O caminho é o mesmo para tudo isso:

1. Toque em **Pagar fatura…** (na lista) ou **Pagar fatura** (na ficha). Com a fatura ainda aberta, o botão é **Antecipar pagamento**.
2. A folha **Pagar a fatura de {mês}** abre com o saldo **já preenchido** em **Quanto foi pago**. Pagou outro valor? Digite o que realmente saiu. O chip **Usar o saldo todo** volta ao total.
3. Em **Pago em**, confira o dia — hoje vem marcado. Vale uma data passada (o pagamento que ficou sem registrar); não vale data futura nem anterior à abertura da fatura.
4. Em **Saiu da conta**, confira a conta. Vem marcada a que paga este cartão.
5. Leia o **quadro colorido**: ele diz o efeito **antes** de você confirmar.
6. Toque em **Registrar pagamento de R$ …**.

| O quadro diz | Quando |
| --- | --- |
| Azul — **Pagamento antecipado** | Fatura aberta, valor menor que o que entrou até agora. *"…o limite livre sobe R$ 500,00 agora."* |
| Âmbar — **Pagamento parcial** | Fatura fechada ou vencida, valor menor que o que falta. Diz quanto vai faltar e que, se não for pago até o vencimento, o resto passa para a próxima fatura |
| Verde — **Quita a fatura de {mês}** | O valor cobre tudo. *"As 9 compras do ciclo ficam confirmadas como pagas."* Na fatura aberta: **Paga tudo o que entrou até agora** |
| Roxo — **Quita e sobram R$ … de crédito** | O valor passa do que falta. Diz para qual fatura o crédito vai. Na fatura aberta: **R$ … a mais viram crédito** |

{% hint style="info" %}
**Pagar a fatura é uma transferência, não uma despesa.** O dinheiro sai da conta escolhida e vai para o cartão; a despesa é a compra, e ela conta uma vez só. Por isso o pagamento não aparece no resultado nem nos relatórios de despesa — veja [Nos relatórios](#nos-relatorios).
{% endhint %}

Tocar duas vezes em **Registrar** (ou tentar de novo depois de um erro de rede) **não registra dois pagamentos**: cada abertura da folha vale por um pagamento só.

### Antecipar, pagar em partes, pagar a mais {#tipos-de-pagamento}

| Você quer… | Como fica |
| --- | --- |
| **Antecipar** para liberar limite | Pague com a fatura aberta. O limite livre sobe na hora, e as compras até o dia de fechamento continuam entrando nela. Na lista de Pagamentos, ele aparece como *antecipado* |
| **Pagar uma parte** (o mínimo do banco, ou o que deu) | Digite o valor que saiu. A fatura vira **Fechada · parcial** e mostra *"R$ 500,00 pagos de R$ 1.240,00"*. O LocFlow não calcula o mínimo — o valor é o que você pagou |
| **Pagar o resto depois** | Abra a mesma fatura e pague de novo. Não há limite de pagamentos por fatura |
| **Pagar a mais** | O que passar do saldo vira crédito — veja [O que passa para a fatura seguinte](#saldo-anterior) |

Cada pagamento entra na lista **Pagamentos** da fatura, com a conta, o dia e o valor.

### Quando as compras ficam pagas {#compras-pagas}

O banco não diz quais compras você pagou: você paga **a fatura**. O LocFlow segue a mesma regra:

* **Pagamento parcial não confirma compra nenhuma.** Enquanto falta qualquer valor na fatura (inclusive o saldo que veio da anterior), as compras dela continuam **previstas**.
* **Quando a fatura fica coberta** — por um pagamento, um crédito ou um estorno —, **todas as compras dela** passam a **realizadas**, com o selo verde **Confirmada**, na data do pagamento (ou do crédito) que a cobriu.
* Se a fatura **volta a dever** (você desfez um pagamento, ou lançou juros numa fatura já paga), as compras dela **voltam a ficar em aberto**.

Na prática: o dinheiro sai do banco **no dia de cada pagamento**, mas a despesa das compras só entra no resultado do período **no dia em que a fatura fica paga**. Veja [Previsto × realizado](lancamentos.md#previsto-x-realizado).

## Desfazer um pagamento {#desfazer-pagamento}

Registrou na conta errada, com o valor errado, ou o pagamento não aconteceu? Desfaça:

1. Na ficha do cartão, abra a fatura e toque no pagamento em **Pagamentos**.
2. O detalhe mostra **Pago em**, **Saiu da conta**, **Fatura**, **Quando** (*antes* ou *depois do fechamento*) e **Lançado por** — quem registrou e quando.
3. Toque em **Desfazer pagamento** e confirme. A pergunta diz as duas consequências: *"Os R$ 500,00 voltam a faltar na fatura de novembro e voltam ao saldo do Banco do Brasil."*

O que volta:

* o valor **volta a faltar** na fatura;
* o dinheiro **volta ao saldo** da conta de onde tinha saído;
* se aquele pagamento tinha deixado a fatura paga, as compras dela **voltam a ficar em aberto** — *"2 compras voltaram a ficar em aberto"*. Se outro pagamento ainda cobre a fatura, nada muda nas compras.

Depois, registre o pagamento certo pela folha de sempre.

{% hint style="info" %}
**Pagamentos antigos aparecem numa linha só.** Faturas quitadas antes de o LocFlow registrar cada pagamento separadamente mostram *Pago antes do registro de pagamentos* — o valor está certo, mas sem data nem conta, e essa linha não tem detalhe nem Desfazer.
{% endhint %}

## Lançar na fatura: juros, créditos, estornos e compras fora do lugar {#lancar-na-fatura}

A fatura do banco tem mais do que compras e pagamentos. Para ela bater com a sua:

1. Na ficha do cartão, abra a fatura em que o banco cobrou ou devolveu.
2. Toque em **Mais**. No grupo **A FATURA DE {MÊS}**, toque em **Lançar na fatura…**.
3. A folha **Lançar na fatura de {mês}** oferece três escolhas — nenhuma vem marcada:

| Escolha | O que faz |
| --- | --- |
| **Crédito ou estorno** | *Abate da fatura* |
| **Juros, IOF ou multa** | *Soma na fatura, como despesa financeira* |
| **Mover uma compra** | *Para a fatura anterior ou a próxima* |

Como no pagamento, tocar duas vezes não lança duas vezes.

### Juros, IOF ou multa {#encargos}

Informe o **Valor** e, em **O que é**, deixe **Juros** (vem marcado) ou troque para **IOF** ou **Multa**. Toque em **Lançar R$ … na fatura**.

{% hint style="warning" %}
**Use o valor que está na fatura do banco.** O LocFlow não calcula juros: cada banco cobra de um jeito, e um cálculo nosso discordaria da fatura real. Se o banco cobrou juros **e** IOF, lance os dois, um de cada vez.
{% endhint %}

* Na **Composição**, os encargos ficam numa linha só, com o nome do que há nela — *Juros*, *Juros e IOF*, *Juros, IOF e multa*.
* Eles somam no que falta e seguem a mesma regra das compras: ficam **previstos** até a fatura ser paga.
* Juros numa fatura **já paga** fazem ela voltar a dever — e as compras dela voltam a ficar em aberto até você pagar a diferença.

### Crédito ou estorno {#credito-ou-estorno}

Escolha **Crédito ou estorno** e depois o tipo:

* **Estorno de uma compra** — escolha em **De qual compra** (a lista mostra as compras **Nesta fatura** e **Na fatura anterior**, porque o banco costuma devolver uma fatura depois) e informe o **Valor** do estorno que está na fatura do banco.
* **Crédito do banco** — cashback ou ajuste que o banco pôs na fatura. Informe só o **Valor**.

Os dois **abatem a fatura como um pagamento**, mas não tiram dinheiro de conta nenhuma — quem dá é o banco. Na Composição, cada um ganha uma linha verde própria: *Estorno Kalunga − R$ 20,00*, *Crédito do banco − R$ 15,00*.

* O estorno **não passa do valor da compra**. Se tentar, o campo avisa na hora: *"O estorno não passa do valor da compra (R$ 189,90)."* O que passar disso é crédito do banco, não estorno.
* Se o crédito ou o estorno **cobre o que falta**, a fatura fica paga e as compras dela são confirmadas: *"A fatura ficou coberta: as compras dela estão confirmadas como pagas."*

{% hint style="info" %}
**Estorno se lança pela fatura, não como receita em Lançamentos.** Uma receita registrada em Lançamentos não entra na fatura do cartão — o número que falta continuaria o mesmo.
{% endhint %}

### Mover uma compra para a fatura vizinha {#mover-compra}

Às vezes o banco põe a compra numa fatura diferente da que a data dela sugere — a compra do dia do fechamento, processada só no dia seguinte, por exemplo. Em vez de mentir sobre o dia da compra, mova-a:

1. Escolha **Mover uma compra**.
2. Em **Qual compra**, toque na compra. Só aparecem as compras **em aberto** desta fatura: a compra já paga fica na fatura em que foi paga.
3. Em **Para qual fatura**, escolha **A anterior ({mês})** ou **A próxima ({mês})**. Na fatura **em curso** (a que ainda está aberta), só aparece a anterior: *"A próxima fatura ainda não abriu: se o banco pôs a compra nela, mova depois que esta fechar."*
4. Toque em **Mover para a fatura de {mês}**.

*"O dia da compra não muda: muda a fatura que a cobra."*

**Compra parcelada:** a parcela escolhida leva **as seguintes junto**, cada uma para a fatura vizinha da sua — o banco cobra uma parcela por fatura. A folha diz isso antes do toque: *"As parcelas seguintes (da 3ª à 6ª) vão junto, uma por fatura, como no banco."* As parcelas anteriores ficam onde estão.

Na fatura para onde foi, a compra aparece com o selo azul **Movida** e a indicação *"veio da fatura de novembro"*. Tocar nela abre o detalhe do movimento, com **Voltar para a fatura de {mês}** e **Ver a compra**.

{% hint style="warning" %}
**Juros e créditos não mudam de fatura.** Lançou na fatura errada? [Remova](#remover) e lance de novo na fatura certa.
{% endhint %}

### Remover o que foi lançado (ou voltar uma compra) {#remover}

Todo lançamento na fatura tem conserto. Na **Composição**:

| Toque em… | Abre | O botão |
| --- | --- | --- |
| A linha dos juros (*Juros e IOF*) | **Encargos da fatura de {mês}**, com cada encargo, quem lançou e quando | **Remover**, em cada um |
| A linha de um crédito ou estorno | O detalhe: valor, fatura e **Lançado por** | **Remover estorno** / **Remover crédito** |
| Uma compra com o selo **Movida** (na lista de Compras) | De onde ela veio e o dia da compra | **Voltar para a fatura de {mês}** |

Toda remoção pede confirmação e diz a consequência — *"Os R$ 20,00 voltam a faltar na fatura de dezembro."* Depois dela, o LocFlow refaz a conta: se a fatura ficou coberta, as compras são confirmadas; se voltou a dever, elas voltam a ficar em aberto.

Desfazer um movimento de parcela devolve **a parcela e as que foram junto** para as faturas de onde vieram.

## Nos relatórios {#nos-relatorios}

| O quê | Entra no resultado (DRE)? | Onde e quando |
| --- | --- | --- |
| **Pagamento da fatura** | Não | É transferência: muda o saldo da conta de onde saiu, no dia do pagamento |
| **Compra no cartão** | Sim | Na categoria dela, no dia em que a fatura fica paga |
| **Juros, IOF e multa** | Sim, como despesa | Categoria **Juros e Encargos** (dentro de *Taxas*, nos custos de operação), no dia em que a fatura fica paga |
| **Estorno de uma compra** | Sim, como receita | Categoria **Outras Receitas**, no dia em que você o lança |
| **Crédito do banco** | Sim, como receita | Categoria **Receita Financeira**, no dia em que você o lança |

{% hint style="warning" %}
**O estorno aparece como receita, não como desconto na categoria da compra.** O resultado final é o mesmo — R$ 20,00 a mais de receita equivalem a R$ 20,00 a menos de despesa —, mas a categoria da compra estornada continua mostrando o valor cheio. Lembre disso ao ler o relatório por categoria.
{% endhint %}

Em [Lançamentos](lancamentos.md), o que você lançou na fatura aparece com a origem **Lançado na fatura do cartão**. Essas linhas não se editam nem se cancelam por lá: o conserto é sempre pela fatura, em [Remover](#remover) — senão a fatura e o razão passariam a discordar.

## Quem pode {#permissoes}

As permissões são definidas em [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md):

| Permissão | O que libera |
| --- | --- |
| **Listar lançamentos financeiros** | Abrir a tela de Cartões e a ficha do cartão: faturas, compras, pagamentos e composição — só para consulta |
| **Editar/realizar/cancelar lançamento financeiro** | Cadastrar e editar cartão, **pagar** e **antecipar**, **desfazer pagamento**, **lançar na fatura**, **mover** uma compra e **remover** o que foi lançado |

Sem a permissão de editar, os botões de pagar, desfazer e lançar simplesmente não aparecem — a ficha continua aberta para consulta.

Os avisos *"Fatura do {cartão} fechou"* e *"Fatura do {cartão} vence hoje"* (só quando ainda falta pagar) vão para quem tem a competência **Pagar contas** — veja [Central de Notificações](../configuracoes/central-de-notificacoes.md).

## Quando não dá {#quando-nao-da}

| Situação | O que o LocFlow diz | O que fazer |
| --- | --- | --- |
| Data do pagamento no futuro ou antes de a fatura abrir | *"O pagamento não pode estar no futuro nem antes de a fatura abrir."* (o botão não libera) | Use o dia em que o dinheiro saiu |
| O mês do pagamento já foi conferido e selado na conta que pagou | *"O mês 11/2026 da conta "Banco do Brasil" já foi conferido e selado — reabra o fechamento em Financeiro › Conciliação para mexer nele."* | [Reabra o mês](conciliacao-e-fechamento.md#fechamento-mensal) ou use outra data |
| A conta que paga o cartão está inativa | *"A conta "…" está inativa — reative-a ou escolha outra."* | Escolha outra conta em **Saiu da conta** |
| Desfazer um pagamento cuja saída do banco já foi conciliada com o extrato | *"Lançamento conciliado é imutável — desfaça a conciliação (ou reabra o mês) antes de reverter."* | [Desfaça a conciliação](conciliacao-e-fechamento.md#extrato) daquela linha e tente de novo |
| Estorno maior do que a compra | *"O estorno não passa do valor da compra (R$ …)."* — ou, se ela já tem estornos, *"O estorno passa do que falta estornar desta compra."* | Lance só o estorno; o que passar é **Crédito do banco** |
| Estornar de novo uma compra já estornada inteira | *"Esta compra já foi estornada inteira."* | Confira se o estorno já não foi lançado |
| Mover (ou voltar) uma compra que já foi paga | *"Esta compra já foi paga na fatura em que está. Desfaça o pagamento antes de mudá-la de fatura."* | [Desfaça o pagamento](#desfazer-pagamento) que a quitou |
| Mover uma parcela quando uma das seguintes já foi paga | *"Uma parcela seguinte desta compra (a 4ª) já foi paga: a série não pode mudar de fatura pela metade. Desfaça aquele pagamento antes."* | Desfaça o pagamento daquela fatura, ou deixe a série como está |
| Mover para a próxima uma compra da fatura que ainda está aberta | A opção **A próxima** não aparece: *"A próxima fatura ainda não abriu…"* | Espere a fatura fechar — quando o banco mostra a compra na fatura seguinte, ela já abriu |
| Juros ou crédito lançado na fatura errada | Eles não aparecem em **Mover uma compra**: só compras mudam de fatura | [Remova](#remover) e lance de novo na fatura certa |
| Outra pessoa mexeu na mesma fatura ao mesmo tempo | *"A fatura mudou enquanto isto era feito (um pagamento ou outra edição). Abra a fatura de novo."* | Feche e abra a ficha, confira e repita |

## Situações reais {#situacoes-reais}

* **"Quero liberar limite antes de a fatura fechar."** Dia 12/11, a fatura de novembro do Nubank PJ está aberta com R$ 1.240,00. Toque em **Antecipar pagamento**, digite R$ 500,00, escolha o Banco do Brasil e registre. O quadro azul avisa: o limite livre sobe R$ 500,00 na hora, e as compras até 20/11 continuam entrando na fatura.
* **"Paguei só uma parte e o resto venceu."** A fatura fechou em R$ 1.240,00, você já tinha antecipado R$ 500,00 e pagou mais R$ 300,00 no vencimento. Os R$ 440,00 que faltaram passam para a fatura de dezembro como saldo anterior. Quando a fatura do banco chegar, [lance os juros e o IOF](#encargos) que ele cobrou — é o caso do [exemplo](#como-a-fatura-e-calculada) lá em cima.
* **"A Kalunga devolveu R$ 20,00 de uma compra de novembro."** Na fatura de dezembro, **Mais › Lançar na fatura… › Crédito ou estorno › Estorno de uma compra**, escolha a Kalunga em **Na fatura anterior** e lance R$ 20,00. Ele abate a fatura e aparece como linha verde na Composição.
* **"O banco jogou a compra do dia 20 na fatura seguinte."** Abra a fatura onde ela está, **Lançar na fatura… › Mover uma compra**, escolha a compra e **A próxima**. O dia da compra fica como está; na fatura de destino, ela aparece como **Movida**.
* **"Registrei o pagamento na conta errada."** Toque no pagamento, **Desfazer pagamento**, confirme — o valor volta ao saldo daquela conta e a faltar na fatura. Depois, pague de novo escolhendo a conta certa.

## Próximo passo

* Para lançar as compras do cartão e entender previsto e realizado: [Lançamentos](lancamentos.md).
* Para a fila do que vence: [Contas a pagar e a receber](contas-a-pagar-e-a-receber.md).
* Para as contas de onde a fatura é paga: [Contas: caixa, banco e gateway](contas.md).
* Para ler o efeito no resultado: [Relatórios: como ler](relatorios.md).
