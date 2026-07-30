---
icon: list-ol
description: O razão do seu caixa — previsto e realizado, como confirmar um pagamento pelo valor que realmente saiu, data de caixa e competência, e o que o LocFlow lança sozinho.
---

# Lançamentos

**Lançamento** é cada entrada e cada saída de dinheiro da sua locadora. A tela de **Lançamentos** é o razão: a lista completa, em ordem de dia, de tudo o que aconteceu e de tudo o que está agendado.

Você chega nela pelo menu do financeiro, em **Lançamentos**.

{% hint style="success" %}
**Por que esta tela é a base de todas as outras:** o saldo, o resultado do mês, os relatórios e o DRE não guardam número nenhum — todos são **somas destas linhas**. Uma categoria errada aqui é um relatório errado lá. Cinco segundos a mais no lançamento economizam a conferência do fim do mês.
{% endhint %}

## Previsto × realizado {#previsto-x-realizado}

Todo lançamento vive em um de dois estados. Essa é a distinção mais importante do módulo:

| | **Previsto** | **Realizado** |
| --- | --- | --- |
| O que é | O dinheiro **vai** entrar ou sair | O dinheiro **já** entrou ou saiu |
| Data que importa | **Vencimento** | **Data de caixa** (o dia em que se moveu) |
| Entra no **saldo**? | **Não** | Sim |
| Entra no **resultado** do período? | **Não** | Sim |
| Onde aparece | [Contas a pagar / a receber](contas-a-pagar-e-a-receber.md) | Saldo, extrato, relatórios |
| Selo na lista | Âmbar, **Previsto** | Verde, **Realizado** |

{% hint style="warning" %}
**Por que o previsto não entra no saldo.** Porque ele ainda não é dinheiro. Se o previsto somasse, o seu saldo mostraria um valor que você não tem — e você tomaria decisões (comprar, pagar, investir) contando com dinheiro que só existe no papel. O previsto tem o seu lugar: ele é o **planejamento**, e aparece como *previsto em aberto* nas contas e nas listas de vencimento. O saldo é o **fato**.
{% endhint %}

Quando um previsto se cumpre, você o **confirma** — e é nesse momento que ele entra no saldo, [pelo valor que realmente se moveu](#confirmar).

## Como a lista se organiza

* **Agrupada por dia**, do mais recente para o mais antigo, com os cabeçalhos *Hoje*, *Ontem* e a data nos dias anteriores.
* **Busca** por descrição, cliente, fornecedor, categoria ou código do orçamento (*ORC-1*).
* **Filtros** por tipo (Entradas / Saídas) e por situação (Realizado / Previsto / Cancelado ou revertido).
* **Totais** de Entradas e Saídas do recorte visível — e eles contam **só o realizado**: previsto e revertido não inflam o cabeçalho.
* Em telas largas, a lista vira uma **tabela** com data, descrição, categoria, situação e valor.

Toque em qualquer linha para abrir o **detalhe**: valor, situação, forma de pagamento, data, categoria, descrição, origem, cliente/fornecedor, orçamento, comprovantes anexados e — quando cabe — as ações de gestão.

{% hint style="info" %}
**Uma operação, uma linha.** O recebimento de uma fatura e a **taxa do pagamento online** daquela mesma cobrança aparecem juntos, como **uma operação só**, já com o líquido (`+500 −5 = 495`). Toque para ver a composição. Duas linhas soltas de mesmo peso faziam parecer que houve duas coisas diferentes. Veja [Taxas do pagamento online](../cobranca/taxas-do-gateway.md).
{% endhint %}

## Registrar um lançamento {#registrar-um-lancamento}

O botão **+** abre **Nova despesa** ou **Nova receita**, e o caminho é um passo a passo de quatro etapas.

### Passo 1 — Valor

Escolha **Despesa** ou **Receita**, digite o **valor** e uma **descrição** (*"Gasolina do caminhão"*, *"Aluguel do galpão 2"*). A tela inteira ganha o tom do tipo: vermelho para despesa, verde para receita.

### Passo 2 — Categoria

Em que o dinheiro entrou ou saiu. A escolha vem do seu [plano de contas](categorias-e-plano-de-contas.md), com busca e as subcategorias visíveis sob a categoria-mãe. Se a categoria estiver ligada a um **serviço** (frete, mão de obra, montagem…), aparece um aviso explicando que aquele valor vai ser comparado, no relatório, com o que você **cobra** por aquele serviço.

Não achou a categoria? Dá para **criar** ali mesmo, sem perder o que já foi preenchido.

### Passo 3 — Quando

A pergunta é uma só: **já foi paga?** (ou *já foi recebida?*).

* **Sim** → você informa a **data do pagamento** e o lançamento nasce **realizado**, entrando no caixa naquele dia.
* **Não** → você informa o **vencimento** e ele nasce **previsto**, indo para as [Contas a pagar / a receber](contas-a-pagar-e-a-receber.md).

Ainda no "não", aparece **Repete?** — *Mensal*, *Semanal* ou *Anual*. Escolhendo uma frequência, você cria uma **conta fixa**: o LocFlow já materializa os próximos vencimentos, e uma prévia mostra quais datas vão nascer.

{% hint style="info" %}
**Contas fixas guardam só o essencial** — valor, categoria e vencimento. Fornecedor, veículo, forma de pagamento e comprovante ficam nos lançamentos avulsos, e por isso o passo 4 não aparece quando você marca uma frequência. A tela avisa isso antes de salvar.
{% endhint %}

### Passo 4 — Detalhes

**Tudo opcional**, tudo visível de uma vez. Cada campo aqui é um relatório que passa a existir:

| Campo | Para que serve |
| --- | --- |
| **Isto sustenta qual operação?** | A natureza do gasto: **Aluguel**, **Venda**, **As duas** ou **Não sei**. É o que permite a margem por operação — veja [abaixo](#natureza) |
| **Conta** | Em qual [conta](contas.md) o dinheiro se moveu. Em branco = a conta padrão |
| **Cliente** (em receitas) | De quem veio o dinheiro — alimenta o relatório de receita por cliente |
| **Fornecedor** (em despesas) | A quem você pagou. Veja [Fornecedores](fornecedores.md) |
| **Veículo** | O veículo como centro de custo — responde *"qual caminhão me custa mais?"*. Recomendado nas despesas de frete |
| **Forma de pagamento** | Pix, dinheiro, maquininha, transferência, boleto ou outro |
| **Comprovante** | Foto ou PDF da nota, do cupom, do recibo — anexado ao lançamento |
| **Data de competência** | A que mês o valor pertence, quando diferente da data de caixa. Veja [abaixo](#caixa-x-competencia) |

{% hint style="success" %}
**Escolher o fornecedor pode preencher a categoria por você.** Se aquele fornecedor tem serviços cadastrados e você ainda não escolheu categoria, o LocFlow sugere a categoria do mesmo serviço e avisa que foi sugestão — troque se não for o caso. É o vínculo explicado em [Fornecedores](fornecedores.md).
{% endhint %}

Tocar duas vezes em **Salvar** (ou repetir depois de um erro de rede) **não gera dois lançamentos**: o LocFlow reconhece que é a mesma tentativa.

## Confirmar um pagamento pelo valor real {#confirmar}

Quase nunca a conta chega exatamente pelo valor previsto. A luz vinha R$ 480, veio R$ 512. O frete estimado em R$ 300 saiu por R$ 285.

Ao confirmar um previsto (na lista ou em [Contas a pagar](contas-a-pagar-e-a-receber.md)), o LocFlow pergunta três coisas:

1. **Valor realmente pago** (ou recebido) — já vem preenchido com o previsto, e é **editável**. É **este** valor que entra no saldo.
2. **Dia em que o dinheiro saiu** (ou entrou) — a data de caixa.
3. **Conta** por onde ele se moveu — em branco, a conta padrão.

Se o valor real for diferente do previsto, aparece uma faixa âmbar com a comparação: *"Previsto R$ 480 · +R$ 32 (6,7%)"*. O previsto **não é apagado** — ele fica guardado como a estimativa, e a diferença passa a ser um dado que você pode acompanhar.

{% hint style="warning" %}
**Diferença grande pede justificativa.** Quando a diferença passa do limite da sua organização (o padrão é **10%**), o campo **Justificativa da diferença** aparece e é obrigatório: *"reajuste da operadora"*, *"consumo do mês de pico"*. Não é burocracia — é a única forma de, três meses depois, alguém entender por que aquela conta dobrou. Se o limite da sua organização for mais rígido que 10%, a folha reabre pedindo a justificativa em vez de simplesmente recusar.
{% endhint %}

## Data de caixa × data de competência {#caixa-x-competencia}

Duas datas, duas perguntas diferentes:

| | **Data de caixa** | **Data de competência** |
| --- | --- | --- |
| Responde | *Quando o dinheiro se moveu?* | *A que mês esse valor pertence?* |
| Manda no | **Saldo**, extrato e resultado do período | Leitura por mês de referência |
| Exemplo | Você pagou a energia de junho no dia 8 de julho: **08/07** | O mês da energia: **junho** |

Na prática, para quase todo lançamento as duas são a **mesma data** — e é por isso que a competência é opcional e vem pré-preenchida. Ela existe para os casos em que separar importa:

* **A conta de um mês paga no outro** — energia, água, telefone.
* **O aluguel do galpão pago adiantado** — sai em dezembro, mas é despesa de janeiro.
* **O seguro anual pago de uma vez** — o dinheiro saiu num dia, o mês de referência é aquele.

{% hint style="info" %}
**Qual olhar no dia a dia:** a **data de caixa**. É ela que diz se você tem dinheiro na conta hoje — e é em regime de caixa que o LocFlow calcula saldo, extrato e resultado. A competência serve para conversar com o contador e para entender um mês que "parece" caro só porque duas contas do mês anterior caíram nele.
{% endhint %}

## A natureza: aluguel, venda ou as duas {#natureza}

Toda despesa sustenta alguma parte do seu negócio. O campo **Isto sustenta qual operação?** guarda qual:

| Resposta | Quando usar |
| --- | --- |
| **Aluguel** | Sustenta a locação: manutenção dos bens móveis que você aluga, insumos de limpeza e inspeção do acervo |
| **Venda** | Sustenta a venda: mercadoria para revenda, equipe comercial |
| **As duas** | Serve às duas ao mesmo tempo: galpão, contador, sistema, marketing, administrativo |
| **Não sei** | Você não decidiu — e isso é visível, não some |

A **categoria sugere**, o **lançamento decide**: se a categoria escolhida costuma ser de aluguel, a resposta já vem pré-selecionada com um aviso de que foi sugestão. Você troca quando o caso é outro — o freelancer contratado para a equipe de vendas está na mesma categoria do freelancer da locação, e só quem lançou sabe para qual foi.

{% hint style="info" %}
**"As duas" é uma resposta certa, não uma desistência.** O aluguel do galpão não é 60% locação e 40% venda: ele é indivisível. No relatório de margem ele aparece numa camada própria, **sem ser rateado** — e sem estragar os dois números. O que ficar em **Não sei** aparece como **Não classificado**: visível, fora das colunas de aluguel e de venda, esperando a sua decisão. A leitura completa está em [Entender seus números](../conceitos/entender-seus-numeros.md).
{% endhint %}

## O que o LocFlow lança sozinho

Boa parte do seu razão você **não digita**. Estas linhas nascem de fatos que já aconteceram em outro módulo:

| Lançamento automático | Nasce quando | Categoria |
| --- | --- | --- |
| **Recebimento de cliente** | Uma parcela da fatura é quitada — no link de pagamento, na baixa manual ou na conferência do caixa da rua | Receita de locação/venda |
| **Taxa do pagamento online** | O processador informa o valor real da tarifa daquele pagamento | Taxa de Gateway |
| **Repasse de parceria** | Você deve (ou quita) o valor de um pedido repassado a um parceiro | Repasse de parceria |
| **Custo de frete de terceiro** | Um pedido cujo frete é de uma transportadora contratada é reservado — nasce como **conta a pagar** | A categoria do serviço de frete |

{% hint style="warning" %}
**Essas linhas não se editam à mão — e é de propósito.** Cada uma é o **espelho de um fato** que vive em outro lugar: a parcela da fatura, o extrato do processador, o acordo com o parceiro, o frete daquele pedido. Se você pudesse mudar o valor aqui, o razão passaria a discordar da fatura, e nenhum dos dois números seria confiável. O caminho é sempre corrigir **na origem**: na cobrança, no orçamento, no acordo — e o razão acompanha sozinho.
{% endhint %}

O que você **pode** fazer com elas:

* **Ver o detalhe** e a composição da operação (entrou X, saiu a taxa T).
* **Abrir o orçamento de origem** com um toque, quando houver.
* **Confirmar o pagamento** do custo de frete provisionado, quando ele de fato for pago — ele é uma conta a pagar como qualquer outra, e passa pela [confirmação por valor real](#confirmar).

## Editar, cancelar e reverter

Só os lançamentos **manuais** e os de **conta fixa** são gerenciáveis. No detalhe, você encontra:

| Ação | Quando aparece | O que faz |
| --- | --- | --- |
| **Marcar como paga / recebida** | No previsto | Confirma pelo valor previsto, na data de hoje |
| **Editar** | Sempre | Reabre o lançamento para correção |
| **Cancelar conta** | No previsto | Desiste daquele agendamento — ele sai das contas a pagar/receber |
| **Reverter lançamento** | No realizado | Tira o valor do caixa. A linha continua no histórico, marcada como **Revertido** |

{% hint style="info" %}
**Nada é apagado de verdade.** Cancelar e reverter **encerram** uma linha, mas ela permanece consultável (filtro *Cancelado/revertido*). Financeiro sem rastro é financeiro que ninguém consegue auditar depois — nem você.
{% endhint %}

{% hint style="warning" %}
**Lançamento com nota fiscal autorizada não se edita.** Se aquele valor já foi declarado em uma nota, o LocFlow recusa a edição e explica o caminho: **cancele a nota primeiro**, corrija o lançamento e emita de novo. Editar sem cancelar deixaria você pagando imposto sobre uma receita que o próprio razão passou a negar.
{% endhint %}

E há uma trava de calendário: **mês fechado não aceita lançamento retroativo**. Se você precisa mexer num mês já selado, o caminho é [reabri-lo](conciliacao-e-fechamento.md#fechamento-mensal).

## Situações reais

* **"A conta de luz veio R$ 40 mais caro."** Confirme a conta a pagar, troque o valor para o real, e justifique se passar dos 10%. O previsto fica guardado como estimativa — e no mês seguinte você vê que não foi um caso isolado.
* **"Paguei a energia de junho em julho."** Data de caixa **julho** (é quando o dinheiro saiu), competência **junho**. O saldo de julho cai; a leitura por competência continua honesta.
* **"O aluguel do galpão é do aluguel ou da venda?"** **As duas**. Ele sustenta a operação inteira e aparece numa camada própria no relatório, sem ser dividido por chute.
* **"Apareceu uma despesa de frete que eu não lancei."** É a provisão do frete de uma transportadora contratada: nasce como conta a pagar quando o pedido é reservado. Quando você pagar de verdade, confirme pelo valor real.
* **"Contratei um freelancer para a equipe de vendas."** Categoria de freelancer, natureza **Venda**. Mês que vem, se ele for para a locação, o mesmo tipo de despesa vai para **Aluguel** — a decisão é do lançamento, não da categoria.

## Próximo passo

* Para trabalhar a fila de vencimentos: [Contas a pagar e a receber](contas-a-pagar-e-a-receber.md).
* Para organizar as categorias que dão sentido a tudo isso: [Categorias e plano de contas](categorias-e-plano-de-contas.md).
* Para conferir o razão contra o banco: [Conciliação e fechamento](conciliacao-e-fechamento.md).
* Para transformar essas linhas em decisão: [Relatórios: como ler](relatorios.md).
