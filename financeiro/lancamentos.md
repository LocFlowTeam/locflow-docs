---
icon: list-ol
description: O razão do seu caixa — previsto e realizado, como registrar uma despesa ou receita (e o lançamento rápido), contas fixas e parcelamentos, como confirmar um pagamento pelo valor que realmente saiu, data de caixa e competência, e o que o LocFlow lança sozinho.
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
* **Filtros** por tipo (Entradas / Saídas) e por situação (Realizado / Previsto / Cancelado ou revertido). Nos filtros avançados, você também escolhe **qual data o período recorta** — vencimento, competência, pagamento ou registro (sem escolher, cada conta usa a data que responde por ela: o vencimento no que está previsto, o pagamento no que já saiu) — e **se a conta se repete**: **Fixas** (as que têm repetição por trás, mesmo com valor que varia, como a energia) ou **Variáveis**.
* **Totais** de Entradas e Saídas do recorte visível — e eles contam **só o realizado**: previsto e revertido não inflam o cabeçalho.
* Em telas largas, a lista vira uma **tabela** com data, descrição, categoria, situação e valor.

Toque em qualquer linha para abrir o **detalhe**: valor, situação, forma de pagamento, data, categoria, descrição, origem, cliente/fornecedor, orçamento, comprovantes anexados e — quando cabe — as ações de gestão.

{% hint style="info" %}
**Uma operação, uma linha.** O recebimento de uma fatura e a **taxa do pagamento online** daquela mesma cobrança aparecem juntos, como **uma operação só**, já com o líquido (`+500 −5 = 495`). Toque para ver a composição. Duas linhas soltas de mesmo peso faziam parecer que houve duas coisas diferentes. Veja [Taxas do pagamento online](../cobranca/taxas-do-gateway.md).
{% endhint %}

## Registrar um lançamento {#registrar-um-lancamento}

O botão **+** (ou **Novo lançamento**, em telas largas) abre **Novo lançamento**, com três caminhos:

| Caminho | Para quê |
| --- | --- |
| **Nova despesa** | Dinheiro que sai: aluguel do galpão, combustível, conserto, salário |
| **Nova receita** | Dinheiro que entra fora das cobranças: a venda de um ativo, um reembolso combinado |
| **Lançamento rápido** | O atalho de quem lança muitas contas por dia — veja [abaixo](#lancamento-rapido) |

Despesas e receitas manuais entram no caixa junto com o que o sistema já registra sozinho — recebimentos de clientes e repasses você **não** precisa lançar.

### No celular: três passos

Uma barra no topo mostra onde você está: **O que foi?**, **Quanto e quando?** e **Confirmar**. A tela ganha a cor do tipo — vermelho para o dinheiro que sai, verde para o que entra.

#### 1. O que foi?

1. Confirme o tipo: **Dinheiro que saiu** ou **Dinheiro que entrou**.
2. **Do que foi esse gasto?** (ou *De onde veio esse dinheiro?*) — escolha a **categoria**. As mais usadas aparecem numa grade; a busca abre o [plano de contas](categorias-e-plano-de-contas.md) inteiro, com as subcategorias, e ali também dá para **criar** uma categoria sem perder o que já foi preenchido. *A categoria define o resto do formulário.*
3. Escolhida a categoria, um cartão mostra o que **já vem resolvido por ela**: como o valor **entra na margem** — aluguel, venda ou estrutura do negócio — e se é preciso dizer de qual **veículo**, **funcionário** ou **galpão** é a despesa. Discordou? Toque em **Trocar**. Se a categoria não decide a margem, o cartão fica âmbar — *"Escolha como isto entra na margem"* — e pede um toque em **Escolher**. Veja [A natureza](#natureza).
4. **Para quem você paga?** (ou *De quem você recebe?*) — o fornecedor ou o cliente. Os mais recentes aparecem em chips; **Outro** busca os demais ou cadastra um novo.
5. **Na lista vai aparecer como** — a descrição se monta sozinha a partir da categoria e de quem recebe. Se o padrão não servir, toque em **Apelido** e dê outro nome (*"Aluguel do galpão 2"*).

{% hint style="success" %}
**Escolher o fornecedor pode preencher a categoria por você.** Se você escolhe o fornecedor antes da categoria e ele tem serviços cadastrados, o LocFlow sugere a categoria do mesmo serviço e avisa que foi sugestão — troque se não for o caso. É o vínculo explicado em [Fornecedores](fornecedores.md).
{% endhint %}

#### 2. Quanto e quando?

1. Digite o **valor**.
2. **Esse dinheiro já saiu da conta?** (ou *já entrou na conta?*):
   * **Sim, já paguei** (ou *já recebi*) — *entra no caixa*: o lançamento nasce **realizado**;
   * **Ainda vou pagar** (ou *receber*) — *vira conta a pagar* (ou a receber): o lançamento nasce **previsto** e vai para as [Contas a pagar e a receber](contas-a-pagar-e-a-receber.md).
3. A data: **Quando saiu?** (ou *Quando entrou?*) se já foi pago; **Vence quando?** se ainda vai ser. Os atalhos **Hoje** e **Em 7 dias** — e, quando o histórico daquela categoria com aquele fornecedor (ou cliente) mostra um dia de sempre, *Dia 10 · como sempre* — resolvem o caso comum; o calendário fica logo abaixo.
4. Só no que ainda vai acontecer aparece **Repetir automaticamente** — veja [Contas fixas e parcelamentos](#conta-fixa).

#### 3. Confirmar

1. Um **resumo** do lançamento, em que cada linha se toca para trocar — categoria, quem recebe, a margem, a recorrência.
2. **Quer melhorar o registro?** — tudo opcional, e cada campo é um relatório que passa a existir:

| Campo | Para que serve |
| --- | --- |
| **Comprovante** | *Fotografar o recibo* — foto ou PDF da nota, do cupom, do recibo, anexado ao lançamento |
| **Como você paga** | Boleto, Pix, transferência, cartão de crédito, cartão de débito, dinheiro, maquininha… Com cartão, a tela pergunta **qual cartão** — opcional no crédito; no débito, havendo cartão de débito cadastrado, a escolha é obrigatória. Veja [Cartões](cartoes.md) |
| **Sai de** / **Entra em** | Em qual [conta](contas.md) o dinheiro se moveu. Em branco = a conta padrão |
| **Observações** | Uma anotação sobre a conta |
| **Em que isto foi gasto?** | O **veículo**, o **funcionário** ou o **galpão** da despesa — é o que responde *"qual caminhão me custa mais?"*. Toque para vincular; quando a categoria exige um deles, ele já aparece aberto e é obrigatório |

Tocar duas vezes em **Salvar** (ou repetir depois de um erro de rede) **não gera dois lançamentos**: o LocFlow reconhece que é a mesma tentativa.

### No computador: um formulário só

Em telas largas não há passos: é um formulário único, com **O essencial** (tipo, categoria, para quem, valor, se já foi pago, data e repetição) e **Comprovação** (conta, forma de pagamento, cartão e comprovante). À direita, uma coluna mostra **como vai aparecer na lista** e o **efeito no relatório de margem** — quanto cada coluna (aluguel, venda, estrutura) muda com este lançamento.

### Contas fixas e parcelamentos {#conta-fixa}

Em **Quanto e quando?**, para o que ainda vai ser pago, ligue **Repetir automaticamente** e escolha **Todo mês**, **Toda semana** ou **Todo ano**. O LocFlow já cria os próximos vencimentos nas Contas a pagar (ou a receber), e uma prévia mostra as próximas datas.

Escolha também **quantas vezes**:

* **sem fim** — a **conta fixa** de sempre: aluguel, internet, contador;
* **3x, 6x, 10x ou 12x** — um **parcelamento**: o valor digitado é **dividido** entre as parcelas (a prévia mostra, por exemplo, *"12x de R$ 250,00"*), a tela diz em que dia cai a última e a série se encerra sozinha.

{% hint style="info" %}
**A conta fixa repete tudo o que você preencheu.** Fornecedor, veículo, funcionário, conta, forma de pagamento, a margem e o comprovante continuam em **cada** mês gerado — você não perde nada por marcar *todo mês*. Uma despesa **já paga** não vira conta fixa: a repetição só aparece para o que ainda vai vencer.
{% endhint %}

### Lançamento rápido {#lancamento-rapido}

Para quem lança dezenas de contas por dia, a tela é uma **frase pronta**: *"Paguei R$ 4.500,00 de aluguel para Cíntia hoje"*. Cada parte da frase é um botão:

* o **valor** é a única coisa digitada, no teclado da própria tela;
* toque na **categoria**, em **para quem**, na **data** ou na **forma de pagamento** para trocar cada uma;
* atalhos para **Recibo** (fotografar o comprovante) e para **repetir todo mês**.

Toque em **Lançar** — ou **Lançar e repetir**, que grava e já deixa a tela pronta para o próximo, com a mesma categoria e o mesmo fornecedor (ou cliente).

{% hint style="warning" %}
**É atalho, não substituto.** Se a categoria exige dizer de qual **veículo** ou de qual **funcionário** é a despesa, a frase não tem esse campo: a tela avisa e oferece **Abrir formulário completo**, levando o tipo, o valor, a data e a categoria que você já escolheu.
{% endhint %}

## Confirmar um pagamento pelo valor real {#confirmar}

Quase nunca a conta chega exatamente pelo valor previsto. A luz vinha R$ 480, veio R$ 512. O frete estimado em R$ 300 saiu por R$ 285.

Ao confirmar um previsto (na lista ou na tela [Contas](contas-a-pagar-e-a-receber.md)), o LocFlow pergunta três coisas:

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
| Manda no | **Saldo**, extrato e os relatórios no modo **Caixa** | Os relatórios no modo **Competência** |
| Exemplo | Você pagou a energia de junho no dia 8 de julho: **08/07** | O mês da energia: **junho** |

Na prática, para quase todo lançamento as duas são a **mesma data** — e é por isso que, ao criar o lançamento, a competência nasce igual à data do movimento. Para mudar, abra o lançamento depois e use **Contabilidade · competência, apelido e observações**. Separar existe para os casos em que importa:

* **A conta de um mês paga no outro** — energia, água, telefone.
* **O aluguel do galpão pago adiantado** — sai em dezembro, mas é despesa de janeiro.
* **O seguro anual pago de uma vez** — o dinheiro saiu num dia, o mês de referência é aquele.

{% hint style="info" %}
**Qual olhar no dia a dia:** a **data de caixa**. É ela que diz se você tem dinheiro na conta hoje — saldo e extrato são sempre de caixa. A competência serve para conversar com o contador e para entender um mês que "parece" caro só porque duas contas do mês anterior caíram nele: nos [Relatórios](relatorios.md), troque para **Competência** e cada valor volta para o mês a que pertence.
{% endhint %}

## A natureza: aluguel, venda ou as duas {#natureza}

Toda despesa sustenta alguma parte do seu negócio. No lançamento, isso aparece como **como o valor entra na margem** — no cartão *Já resolvido pela categoria*, no primeiro passo:

| Resposta | Quando usar |
| --- | --- |
| **Aluguel** | Sustenta a locação: manutenção dos bens móveis que você aluga, insumos de limpeza e inspeção do acervo |
| **Venda** | Sustenta a venda: mercadoria para revenda, equipe comercial |
| **Estrutura do negócio** ("as duas") | Serve às duas ao mesmo tempo: galpão, contador, sistema, marketing, administrativo |

A **categoria sugere**, o **lançamento decide**: cada categoria diz que operação costuma sustentar (o campo **Sustenta qual operação?** do [plano de contas](categorias-e-plano-de-contas.md)), e o lançamento já nasce com essa resposta — *"Entra na margem como aluguel"*. Você toca em **Trocar** quando o caso é outro: o freelancer contratado para a equipe de vendas está na mesma categoria do freelancer da locação, e só quem lançou sabe para qual foi. Se a categoria não decide, o cartão fica âmbar e pede a sua escolha.

{% hint style="info" %}
**"As duas" é uma resposta certa, não uma desistência.** O aluguel do galpão não é 60% locação e 40% venda: ele é indivisível. No relatório de margem ele aparece numa camada própria, **sem ser rateado** — e sem estragar os dois números. O lançamento que ficar sem resposta aparece como **Não classificado**: visível, fora das colunas de aluguel e de venda, esperando a sua decisão. A leitura completa está em [Entender seus números](../conceitos/entender-seus-numeros.md).
{% endhint %}

## O que o LocFlow lança sozinho

Boa parte do seu razão você **não digita**. Estas linhas nascem de fatos que já aconteceram em outro módulo:

{% hint style="success" %}
**A regra da casa:** todo dinheiro que passa pelo LocFlow entra na sua Gestão Financeira — dos dois lados, quando os dois lados são do LocFlow. Se você pagou, tem a saída; se você recebeu, tem a entrada. Nenhum valor fica só numa tela de outro módulo, porque número fora do razão não entra no saldo, no fluxo de caixa nem no DRE — e o que não entra no DRE não sustenta decisão.
{% endhint %}

| Lançamento automático | Nasce quando | Categoria |
| --- | --- | --- |
| **Recebimento de cliente** | Uma parcela da fatura é quitada — no link de pagamento, na baixa manual ou na conferência do caixa da rua | Receita de locação/venda |
| **Taxa do pagamento online** | O processador informa o valor real da tarifa daquele pagamento | Taxa de Gateway |
| **Repasse de parceria** | Você deve (ou quita) o valor de um pedido repassado a um parceiro | Repasse de parceria |
| **Recebimento da rede** | Um repasse que **você** tinha a receber da rede é pago — pelo split na fonte, pela quitação do saldo ou por fora | Rede de Parcerias |
| **Custo de frete de terceiro** | Um pedido cujo frete é de uma transportadora contratada é reservado — nasce como **conta a pagar** | A categoria do serviço de frete |

Além dessas, o detalhe de um lançamento pode dizer que ele veio de outros fatos — todos automáticos:

| Aparece como | De onde vem |
| --- | --- |
| **Reembolso ao cliente** | Um pedido já pago foi cancelado e o dinheiro voltou ao cliente |
| **Recebimento de parceiro** | O parceiro logístico cobrou o cliente na rua e acertou com você a parte que era sua. Se esse pagamento for estornado, nasce a **Devolução de recebimento de parceiro**. Veja [Cobrança na rua](../parcerias/cobranca-na-rua.md) |
| **Taxa da plataforma** | A taxa da plataforma numa operação de parceria. Volta como **Estorno de taxa da plataforma** quando o pagamento é revertido |
| **Estorno de repasse ao logístico** | O repasse que você pagou ao parceiro voltou, porque o pagamento foi revertido |
| **Estorno de taxa do gateway** | O processador devolveu a tarifa depois de um estorno ou contestação |
| **Devolução de recebimento da rede** | Um valor que você tinha recebido da rede foi estornado |
| **Saque do gateway** | Um saque concluído do pagamento online — uma transferência da Stone para a sua conta de recebimento. Veja [Contas](contas.md#conta-de-recebimento) |
| **Documento fiscal** | Uma nota fiscal **avulsa** autorizada cria uma **entrada prevista** — o faturado que ainda vai entrar. A nota de um pedido ou de um lançamento não cria nada novo: aquela receita já está no razão |
| **Conta recorrente** | Um mês gerado por uma [conta fixa](#conta-fixa) |
| **Importado do extrato** | Um lançamento criado a partir de uma linha do extrato do banco, na [conciliação](conciliacao-e-fechamento.md#extrato) |
| **Ajuste de conciliação** | A diferença entre o razão e o extrato, registrada ao [fechar o mês](conciliacao-e-fechamento.md#fechamento-mensal) |
| **Transferência entre contas** | As duas pernas de uma [transferência](contas.md#transferir) — fora do resultado |

{% hint style="warning" %}
**Essas linhas não se editam à mão — e é de propósito.** Cada uma é o **espelho de um fato** que vive em outro lugar: a parcela da fatura, o extrato do processador, o acordo com o parceiro, o frete daquele pedido, a nota fiscal. Se você pudesse mudar o valor aqui, o razão passaria a discordar da fatura, e nenhum dos dois números seria confiável. O caminho é sempre corrigir **na origem**: na cobrança, no orçamento, no acordo — e o razão acompanha sozinho.
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
