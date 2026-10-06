---
icon: building-columns
description: Onde o dinheiro da sua locadora vive — caixa, banco, carteira, a conta do pagamento online e as contas de recebimento — com conta padrão, dados bancários, transferência, mesclagem e inativação.
---

# Contas

Uma **conta** é um lugar onde o seu dinheiro fica: a gaveta do balcão, a conta do banco, a carteira digital. Todo lançamento acontece **em uma conta** — é isso que permite o LocFlow responder *"quanto eu tenho no Banco Azul?"* e não só *"quanto eu tenho, no total?"*.

Você as encontra em **Gestão Financeira → engrenagem (Ajustes) → Contas**.

{% hint style="success" %}
**Por que vale separar as contas:** um saldo único esconde o problema mais comum de locadora pequena — ter dinheiro no total e não ter **naquela** conta onde o boleto vai ser debitado amanhã. Com as contas separadas, o LocFlow mostra os dois números.
{% endhint %}

## Os tipos de conta

| Tipo | Para que serve | Você cria? |
| --- | --- | --- |
| **Caixa** | Dinheiro em espécie que fica com você — a gaveta do balcão, o troco da rua. | Sim |
| **Banco** | Uma conta bancária de verdade. É o tipo que aceita [dados bancários](#dados-bancarios) e extrato. | Sim |
| **Carteira** | Dinheiro guardado fora do banco tradicional: carteira digital, aplicativo de pagamento. | Sim |
| **Gateway** | A conta-espelho do **pagamento online**, com o nome **Stone**. Reflete o dinheiro que está no processador de pagamentos, antes de cair no seu banco. | Não — o LocFlow a mantém |
| **Cartão de crédito** | A conta da **fatura** de um cartão: as compras feitas nele nascem aqui, como dívida prevista. | Não — nasce quando você cadastra o cartão em [Cartões](cartoes.md) |

{% hint style="info" %}
**Por que existe uma conta de gateway.** Quando o cliente paga pelo link, o dinheiro entra **no processador**, não no seu banco: ele fica compensando e só depois é sacado. A conta **Stone** mostra esse dinheiro no lugar certo do seu financeiro em vez de fingir que ele já está no banco — o próprio cartão dela diz: *"Conta temporária: os recebíveis caem aqui e os saques vão para as contas de recebimento."* Os detalhes do ciclo estão em [Saldo e antecipação](../cobranca/saldo-e-antecipacao.md).
{% endhint %}

Para criar: **Criar conta**, escolha o nome (ex.: *Banco Azul PJ*) e o tipo — **Caixa**, **Banco** ou **Carteira**. A conta do gateway, as contas de recebimento e as de cartão não se criam aqui: o LocFlow as mantém sozinho.

## O que a tela mostra

No topo, o **Consolidado (todas as contas)**: o saldo somado e, abaixo, o **previsto em aberto** — o que está agendado e ainda não aconteceu.

Cada conta aparece como um cartão com:

* o **ícone e a cor do tipo** (a mesma língua visual em todo o financeiro);
* o **saldo realizado**, sempre **derivado dos lançamentos** — nunca um número digitado;
* o **previsto**, quando existe;
* os selos: ⭐ **Padrão**, ✔ **Conta de recebimento**, **Inativa** e o resumo dos dados bancários;
* para a Stone e para uma conta de recebimento arquivada, uma frase que explica o papel dela.

Saldo negativo aparece em vermelho com um sinal de atenção — não é bloqueado, porque conta no vermelho é um fato que precisa ser visto, não escondido.

## A conta padrão

Uma conta é a **padrão** da organização, marcada com a estrela. É onde cai **tudo que não disser em qual conta aconteceu** — um lançamento rápido, um registro automático sem conta definida.

Regras que valem a pena saber:

1. A organização **nunca fica sem conta padrão**. Se você inativar a padrão, o LocFlow pede para você **eleger a nova** na mesma ação.
2. Conta inativa não pode ser padrão.
3. Trocar a padrão não mexe em nada do passado — só no destino dos próximos lançamentos sem conta.

## O painel de ações de uma conta

Toque no cartão da conta. O painel abre com a **identidade dela no cabeçalho** (tipo, saldo, previsto e selos) e as ações separadas por peso — porque conferir um saldo e mesclar duas contas não podem ter a mesma cara.

### Ação principal: Ver movimentos

Abre o extrato do mês **já filtrado nesta conta**: saldo anterior, cada linha com o valor e o **saldo depois dela**, e o saldo no fim do mês. Dá para navegar entre meses ali mesmo. É a rotina de conferência — e responde *"por que o saldo é este?"* sem trocar de tela.

### Rotina

| Ação | O que faz |
| --- | --- |
| **Transferir** | Move dinheiro desta conta para outra. Veja [Transferir entre contas](#transferir) |
| **Dados bancários** | Cadastra ou corrige banco, agência e conta. Veja [Dados bancários](#dados-bancarios) |
| **Renomear** | Troca o nome. Vale para todo o histórico — é a mesma conta, com outro nome |

### Configuração da conta

| Ação | O que faz | Volta atrás? |
| --- | --- | --- |
| **Definir como padrão** | Torna esta a conta que recebe o que não diz a conta | Sim, elegendo outra |
| **Mesclar em outra conta** | Faz outra conta **absorver** esta | **Não** |
| **Inativar** / **Reativar** | Tira a conta do caminho, preservando o histórico | Sim |

{% hint style="info" %}
**Ação indisponível não desaparece.** Quando algo não pode ser feito, a opção continua na tela, apagada, com o motivo curto no lugar do toque — *"Já é a padrão"*, *"Conta inativa"*, *"Conta do sistema não se mescla"*, *"Edite em Ajustes › Integração de Pagamento"*. Você entende o **porquê** sem ter de adivinhar.
{% endhint %}

## Contas de recebimento {#conta-de-recebimento}

Quando você usa o [pagamento online](../cobranca/pagamento-online.md), o dinheiro fica no processador e depois é **sacado para uma conta bancária sua** — a **conta de recebimento**, cadastrada em **Ajustes › Integração de Pagamento**.

**Toda conta de recebimento vira, sozinha, uma conta Banco do Financeiro**, com o selo **Conta de recebimento** e os dados bancários já preenchidos. Você não precisa criar nem marcar nada: é nela que os saques aparecem quando o dinheiro sai da Stone e chega ao banco.

O que muda numa conta de recebimento — as três ações aparecem apagadas, com o motivo no lugar do toque:

| Ação | O motivo |
| --- | --- |
| **Dados bancários** | *"Edite em Ajustes › Integração de Pagamento"* — o banco dela é o mesmo do cadastro de recebimento, e só se troca lá |
| **Inativar** | Quando o banco muda, o LocFlow **arquiva** a conta antiga sozinho — com todo o histórico — e cria a do banco novo, que passa a ser a vigente. A arquivada diz isso no cartão e não se reativa |
| **Mesclar em outra conta** | *"Conta de recebimento não se mescla em outra; mescle a outra nela"*. Cadastrou à mão a mesma conta do banco? Abra a duplicada e mescle-a na conta de recebimento |

{% hint style="info" %}
**Cada saque é uma transferência, não uma receita.** Quando um saque — manual ou automático — é concluído, ele aparece no Financeiro como uma **transferência da Stone para a conta de recebimento**, com a taxa do saque junto. O dinheiro já tinha entrado como receita quando o cliente pagou; o saque só muda o lugar onde ele está, por isso não mexe no resultado do mês.
{% endhint %}

{% hint style="warning" %}
**Saques antigos podem não estar no Financeiro.** O saque só passou a virar transferência sozinho a partir de um certo momento; os anteriores podem não ter sido lançados. Se você já sacava antes e não lançou essas transferências à mão, o saldo da **Stone** no Financeiro pode ficar maior que o saldo real no processador. O saldo de verdade, disponível para sacar, é o da tela de [Saldo e antecipação](../cobranca/saldo-e-antecipacao.md).
{% endhint %}

## Dados bancários {#dados-bancarios}

A conta **real** do banco por trás da sua conta do LocFlow. (Numa [conta de recebimento](#conta-de-recebimento) eles já vêm preenchidos e são só de leitura.) Preencha:

1. **Banco** — o campo tem **busca**: digite o nome (*Itaú*) ou o código (*341*) e escolha na lista.
2. **Agência** e, se houver, o **dígito**.
3. **Conta** e, se houver, o **dígito**.
4. **Tipo de conta** — corrente ou poupança (opcional).

{% hint style="info" %}
**Banco fora da lista?** A lista é curada, não exaustiva. Digite o **código COMPE de 3 dígitos** do seu banco e siga — o que você escreveu é preservado exatamente como está.
{% endhint %}

Para **remover** os dados bancários, limpe banco, agência e conta e salve: o botão passa a dizer **Remover dados**, e a tela avisa antes.

Cadastrar isso não é burocracia: é o que dá sentido à [conciliação bancária](conciliacao-e-fechamento.md#extrato) — a conta do LocFlow passa a ter um par de verdade no banco.

## Transferir entre contas {#transferir}

Tirou dinheiro do caixa e depositou no banco? Isso **não é receita nem despesa** — é a mesma quantia mudando de lugar. A transferência registra o par de uma vez: sai de uma conta, entra na outra.

Informe a **conta de destino**, o **valor**, a **data** e, se quiser, uma descrição.

| A transferência | Aparece? |
| --- | --- |
| No **saldo de cada conta** | Sim — uma perde, a outra ganha |
| No **resultado do período** (entradas × saídas) | **Não** — nenhum dinheiro entrou ou saiu da empresa |
| Nos **relatórios** de receita e despesa | **Não** — pelo mesmo motivo |

{% hint style="success" %}
**Tocar duas vezes no botão não gera duas transferências.** Cada abertura da folha vale por **uma** transferência: se a internet oscilar e você tentar de novo, o LocFlow reconhece que é a mesma e registra uma só.
{% endhint %}

## Mesclar duas contas

Cadastrou a mesma conta duas vezes? A **mesclagem** resolve: a conta que você escolher **absorve** esta.

1. Todo o **histórico** de lançamentos migra para a conta de destino.
2. O **saldo de abertura** migra também.
3. A conta absorvida fica **inativa, com o rastro** de que foi mesclada — nada é apagado.
4. Se ela era a padrão, a estrela passa para a conta de destino na mesma operação.

{% hint style="danger" %}
**Mesclar não tem volta.** Não existe "desmesclar": o histórico passa a viver na outra conta. Antes de mesclar, confira que é realmente a mesma conta do mundo real — e não duas contas parecidas.
{% endhint %}

O LocFlow recusa a mesclagem nestes casos, para proteger o seu saldo:

* a conta é **do sistema** (a Stone);
* o **destino** é a conta do gateway;
* a conta é uma **conta de recebimento** — mescle a outra **nela**, não o contrário;
* a conta é a **fatura de um cartão** — mesclá-la viraria dívida em caixa;
* uma das contas já tem **saldo de abertura definido** ou **extrato bancário importado** — nesses casos, juntar os históricos faria o saldo mentir.

## Inativar em vez de excluir

Não existe excluir conta: excluir apagaria o passado. **Inativar** faz o trabalho:

* a conta sai das próximas escolhas (seletores, filtros, transferências);
* os lançamentos antigos continuam nela, e os relatórios de meses anteriores não mudam;
* o cartão fica esmaecido com o selo **Inativa**, e **Reativar** a traz de volta.

A **Stone** e a **conta de recebimento** vigente não se inativam à mão: os recebíveis do gateway caem na primeira antes de cada saque, e a segunda é arquivada sozinha quando o banco muda em Ajustes › Integração de Pagamento.

## O que é rotina e o que é estrutural

| Rotina — faça sem medo | Estrutural — pense antes |
| --- | --- |
| Ver movimentos | Definir a conta padrão |
| Transferir entre contas | Inativar uma conta |
| Corrigir dados bancários | **Mesclar** (irreversível) |
| Renomear | Trocar o banco da conta de recebimento (em Ajustes › Integração de Pagamento) |

## Situações reais

* **"Depositei o dinheiro da semana no banco."** Abra a conta **Caixa** → **Transferir** → destino **Banco**, valor e data. O resultado do mês não muda: nada entrou nem saiu, só trocou de lugar.
* **"Fechei a conta no banco antigo."** Inative a conta. Se ela era a padrão, o LocFlow pede a nova padrão na mesma hora. O histórico continua consultável.
* **"Tenho 'Nubank' e 'Nu PJ' cadastrados, é a mesma conta."** Mescle a duplicada na que você usa — mas só se nenhuma das duas já tiver saldo de abertura ou extrato importado.
* **"Recebo por PIX no link de pagamento e quero ver esse dinheiro separado."** Ele já aparece na conta **Stone**, enquanto está no processador. Quando você saca, ele passa para a sua **conta de recebimento** — que aparece sozinha aqui, com o selo, sem você marcar nada.
* **"Troquei o banco que recebe o pagamento online."** Edite em **Ajustes › Integração de Pagamento**. O Financeiro arquiva a conta antiga, com o histórico, e cria a do banco novo.

## Próximo passo

* Para lançar entradas e saídas nessas contas: [Lançamentos](lancamentos.md).
* Para conferir uma conta contra o extrato do banco e selar o mês: [Conciliação e fechamento](conciliacao-e-fechamento.md).
* Para entender o dinheiro que passa pelo processador: [Saldo e antecipação](../cobranca/saldo-e-antecipacao.md).
