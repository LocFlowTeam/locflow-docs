---
icon: file-invoice-dollar
description: Como transformar o valor de um orçamento em parcelas reais — à vista, sinal + restante ou parcelado, com vencimentos.
---

# Emitindo a cobrança

A [fatura](faturas-e-parcelas.md) nasce quando você **gera a cobrança** do orçamento. Nessa hora, você diz **como o cliente vai pagar**: tudo de uma vez, com uma entrada, ou parcelado — e em **quais datas**. É o passo que tira o valor do papel e o transforma em parcelas reais, com vencimentos que a sua operação vai acompanhar.

{% hint style="success" %}
**Por que isso importa:** o jeito de cobrar é uma decisão de negócio, não um detalhe técnico. Pedir um sinal segura o compromisso; parcelar ajuda o cliente a fechar; o pagamento a prazo é o que o cliente PJ espera. Emitir a cobrança certa é o que faz o dinheiro entrar do jeito que combina com você.
{% endhint %}

## O que significa emitir a cobrança

Emitir a cobrança é pegar o **total do orçamento** e reparti-lo em **parcelas** com **datas de vencimento**. Você não digita o valor — ele vem do orçamento, que é a fonte da verdade. Você escolhe **o formato** e o LocFlow calcula o resto.

{% hint style="info" %}
A tela diz, com todas as letras: *"O valor é o total do orçamento. Escolha como o cliente vai pagar — as parcelas são calculadas automaticamente."*
{% endhint %}

Vale tanto para **locação** quanto para **venda** — o que muda é a sua escolha de formato, não a mecânica.

## Onde emitir

Abra as **Ações rápidas** do orçamento e toque em **Gerar cobrança**. A ação fica disponível enquanto o pedido ainda pode avançar no funil — inclusive **Em aberto** e **Em negociação**.

O LocFlow recomenda gerar a cobrança em **Pré-reserva** ou **Reservado**, quando há mais certeza de faturamento. Essa é uma recomendação, não uma obrigação: se você gerar antes, a tela avisa e pede sua confirmação.

```mermaid
flowchart LR
    G[Orcamento no funil] --> AC[Acoes rapidas]
    AC --> GC[Gerar cobranca]
    GC --> P[Parcelas com<br/>valores e datas]
```

{% hint style="info" %}
**A sua operação define a trava da reserva.** Se o Motor Operacional exigir cobrança para reservar, ao tocar em **Reservar** o LocFlow abre a geração automaticamente e conclui as duas ações juntas. Se o Motor não exigir, a tela não força essa etapa: você pode reservar sem cobrança e gerar depois.
{% endhint %}

{% hint style="info" %}
**Pré-reserva é opcional.** Algumas organizações não usam essa etapa. Isso não impede reservar nem cobrar: a recomendação também vale diretamente para **Reservado**.
{% endhint %}

## Escolha como o cliente vai pagar

São três formatos. Você toca em um cartão no topo da folha e o restante da tela se ajusta ao que aquele formato precisa.

| Formato | Para que serve | Resultado |
| --- | --- | --- |
| **À vista** | Pagamento único. | Uma parcela só, com o total. |
| **Sinal + restante** | Entrada agora, o resto depois. | Duas parcelas: o sinal e o restante. |
| **Parcelado** | Dividir em várias vezes. | Tantas parcelas quantas você definir. |

### À vista

O caminho mais simples: **uma parcela** com o valor cheio do orçamento, vencendo na data que você escolher. É o padrão para quem recebe tudo de uma vez — comum na **venda** e em locações de curta duração.

### Sinal + restante

Para "segurar" o compromisso. Você define **só o sinal** (a entrada) de duas formas:

* **Percentual** — uma fatia do total (ex.: 50%). Precisa ser maior que zero e menor que 100%.
* **Valor fixo** — um valor em reais (ex.: R$ 300,00).

O **restante é deduzido automaticamente** — você não calcula nada. O LocFlow garante que **sinal + restante = total**.

{% hint style="info" %}
**O sinal vence na hora.** A entrada é para confirmar agora, então ela já nasce vencendo hoje. Só o **restante** usa a data de vencimento que você escolher (e o prazo, se você ativar o "a prazo"). É o típico "entrada na reserva, restante na entrega".
{% endhint %}

### Parcelado

Para dividir em várias vezes. Aqui você define:

* **Número de parcelas** — quantas vezes.
* **Intervalo** — de quanto em quanto tempo elas vencem: **Mensal** (a cada 30 dias) ou **Quinzenal** (a cada 15 dias).

A partir da **data de vencimento** da primeira, o LocFlow espaça as demais pelo intervalo escolhido. Por padrão, ele **divide o total igualmente** entre as parcelas (qualquer sobra de centavos vai para a última). Se você quiser controlar o valor de cada uma, dá — veja [Definir o valor exato de cada parcela](#definir-o-valor-exato-de-cada-parcela).

## Data de vencimento

Todo formato pede uma **data de vencimento** base. O LocFlow já chega com uma **sugestão** para você não começar do zero: ele propõe a data em que **o uso do item começa** (a entrega, na prática). Você confirma ou troca — não pode ser uma data no passado.

* **À vista:** é a data em que a parcela única vence.
* **Sinal + restante:** é a data do **restante** (o sinal vence hoje).
* **Parcelado:** é a data da **primeira** parcela; as outras vão se espaçando a partir dela.

## Pagamento a prazo (D+X)

Quer dar um **prazo** ao cliente — pagar 30 dias depois, por exemplo? Ative **Pagamento a prazo** e escolha **D+X**: D+15, D+30, D+45, ou um número livre de dias.

O que o prazo desloca depende do formato:

| Formato | O que o "a prazo" desloca |
| --- | --- |
| **À vista** | O vencimento da parcela única. |
| **Sinal + restante** | Só o **restante** (o sinal continua vencendo hoje). |
| **Parcelado** | O vencimento de **todas** as parcelas. |

{% hint style="info" %}
**A prazo mexe nas DATAS, não nos valores.** D+30 adia o vencimento; não muda quanto se cobra em cada parcela. É o "pagamento faturado" que o cliente PJ costuma pedir — entrega agora, pagamento daqui a X dias.
{% endhint %}

## Como o cliente vai pagar (indicativo) {#pagamento-combinado}

Logo abaixo do "a prazo", pouco antes do resumo das parcelas, há uma seção — **"Como o cliente vai pagar (indicativo)"** —, **fechada por padrão**, com o resumo **"Nada combinado"** enquanto você não mexe nela. É onde você anota **o que o cliente falou**: "no Pix", "metade na entrega", "dinheiro na retirada".

Até aqui esse acerto morria na conversa entre o vendedor e o cliente. Quem ia receber — o operador no balcão, o motorista na porta — chegava sem saber.

{% hint style="warning" %}
**Combinado é recado, não regra.** O que você marca aqui **não cria parcela, não muda vencimento, não escolhe o meio de pagamento e não impede receber por outro**. O método que vale continua sendo o que for registrado **no ato do recebimento** — a [baixa manual](recebendo-pagamentos.md) ou o [pagamento online](pagamento-online.md). Por isso a tela escreve "indicativo" com todas as letras.
{% endhint %}

**Não confunda com o formato da cobrança.** *À vista*, *sinal + restante* e *parcelado* são a **regra** que cria as parcelas — é o que você escolheu lá em cima, e é o que move dinheiro. O combinado é o acerto de balcão: muda a qualquer momento e não move um centavo.

### O que você informa

**As formas** — uma ou várias — entre as mesmas opções do lançamento manual do financeiro, na ordem em que aparecem: **Boleto**, **Pix**, **Transferência**, **Cartão de crédito**, **Cartão de débito**, **Dinheiro**, **Maquininha** e **Outra**. O cliente que disse "Pix ou dinheiro na entrega" combinou as duas coisas: marque as duas. A tela mostra o combinado como uma frase — *"Pix ou Dinheiro"* —, e o filtro da lista enxerga cada uma delas.

{% hint style="info" %}
**O cartão de débito existe aqui e não existe na baixa.** Ele faz parte do vocabulário do combinado (e do [lançamento manual](../financeiro/lancamentos.md)), mas **não** é uma das formas da [baixa de parcela](recebendo-pagamentos.md#os-metodos-de-recebimento). Faz sentido: "combinei receber no débito" é uma informação; um recebimento "no débito" não é algo que a cobrança saiba registrar.
{% endhint %}

**A observação**, opcional, que só aparece **depois** de você escolher a forma. É a frase curta que dá o contexto — o próprio campo sugere *"ex.: metade na entrega"* —, com até **140 caracteres** e um contador ao lado.

Para desfazer uma forma, **toque de novo no chip marcado**: só ela desmarca. Desmarcando a última, a cobrança volta a "nada combinado". Nada disso é obrigatório — a maioria das emissões não usa, e é por isso que a seção nasce fechada. Fechada, ela ainda mostra no cabeçalho o que você combinou.

{% hint style="info" %}
**O link de pagamento também escreve aqui.** Quando você gera o [link de pagamento](pagamento-online.md#o-link-e-o-combinado) ou liga uma forma nele, o combinado da cobrança passa a **acompanhar o link** — sem você digitar de novo. Isso dura até alguém mexer no combinado à mão: a partir daí, o link não sobrescreve mais. Veja o detalhe na página do pagamento online.
{% endhint %}

### Os outros dois lugares onde se informa

* **Na cobrança avulsa** — o botão **Cobrança avulsa**, na lista de Cobranças, abre **"Nova cobrança avulsa"** (cliente, valor, motivo, vencimento). Ali o mesmo campo fica **sempre visível**, no fim do formulário.
* **Depois, a qualquer momento** — pelo lápis na ficha da cobrança. Veja [Faturas e parcelas](faturas-e-parcelas.md#pagamento-combinado).

## O resumo das parcelas

Enquanto você mexe nas opções, a folha mostra um **Resumo das parcelas** ao vivo: cada linha com o rótulo (Sinal, Restante, Parcela 1, 2…), a **data em que vence** e o **valor**, mais o **total** no rodapé. É a sua conferência antes de confirmar — o que você vê ali é exatamente o que será gerado.

Quando o resumo estiver do seu jeito, toque em **Gerar cobrança**. Pronto: o orçamento vira parcelas reais, com datas, prontas para receber.

## Gerar a fatura de locação junto

Na folha de emissão há o bloco **Gerar fatura de locação**: *"Ao gerar a cobrança, cria também o PDF da fatura de locação nos Documentos."* É o documento de cobrança para mandar ao cliente, com parcelas e vencimentos reais.

Marcando a caixa, a emissão **não fica mais lenta por causa disso**. A cobrança é confirmada na hora, a folha fecha e o aviso diz para onde olhar: *"A fatura de locação está sendo gerada em Documentos."* Lá, o documento aparece como **"Gerando…"** e vira **"Gerado"** sozinho, sem você precisar ficar na tela.

{% hint style="info" %}
Se o nome do arquivo do seu modelo tiver campos para preencher, a folha os pede **antes** de emitir. Se ainda assim faltar alguma informação, o documento fica em **"Falta preencher"** na lista — e a cobrança, que é o que importa, já está feita.
{% endhint %}

A fatura de locação só existe em **aluguel**; na venda a caixa não aparece.

## Definir o valor exato de cada parcela

No **Parcelado**, o padrão é dividir o total por igual. Mas às vezes você quer uma **primeira parcela maior**, ou valores combinados caso a caso. Para isso, ative a opção de definir o valor de cada parcela.

{% hint style="info" %}
O texto na tela: *"Padrão: dividido igualmente. Ative para definir o valor exato de cada parcela."*
{% endhint %}

Ao ativar, cada parcela ganha um campo de valor. Uma regra te protege de errar: a **soma das parcelas precisa fechar o total** do orçamento. Se passar ou faltar, o LocFlow avisa quanto sobra ou falta — e só libera a emissão quando a conta bate. Assim a cobrança nunca sai cobrando a mais nem a menos do que o pedido.

## Editar vencimento de uma parcela

Combinou uma data e depois precisou empurrar? Você pode **reagendar o vencimento** de uma parcela **ainda não paga** — pelo ícone de lápis na linha da parcela (com a permissão certa). Escolha a nova data e salve.

{% hint style="warning" %}
**Se a parcela já tem um boleto em aberto**, mudar a data atualiza o próprio boleto — e o LocFlow avisa: *"O boleto em aberto terá o vencimento atualizado — a linha digitável continua a mesma."* Ou seja: o cliente continua usando o mesmo boleto, só com o novo vencimento. Não é preciso gerar outro.
{% endhint %}

Reagendar muda **a data**. Para mudar **valores** depois de emitida, o caminho é o orçamento: como a fatura deriva dele, editar o orçamento (valor, itens, frete) reflete na cobrança. Veja [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md).

## Casos em que a cobrança não é gerada

Dois pontos para não tropeçar:

* **Orçamento de valor zero** (por exemplo, um desconto que zera o total): nenhuma cobrança é gerada — não há o que receber.
* **Já existe cobrança para este orçamento:** o LocFlow não emite uma segunda. Cada orçamento tem **uma** fatura quando a cobrança é gerada. Para ajustar o que já foi emitido, você reagenda parcelas ou edita o orçamento — não emite de novo.

## Por porte

| Porte | Como costuma emitir |
| --- | --- |
| **Pequeno** | Quase sempre **À vista**, na data da entrega. Um toque e a cobrança está pronta — sem pensar em parcela. |
| **Médio** | **Sinal + restante** para segurar reservas e **Parcelado** para fechar negócios maiores; começa a usar o **a prazo** para clientes recorrentes. |
| **Grande** | Controla **o valor de cada parcela**, usa **D+X** como política de faturamento PJ e reagenda vencimentos conforme o combinado com cada cliente. |

A ideia é a mesma de todo o LocFlow: **simples para quem quer simples, flexível para quem precisa de controle**.

## Situações reais

* **Festa do fim de semana, venda à vista:** orçamento em negociação, você abre Gerar cobrança, confirma o aviso, deixa em **À vista** com vencimento na entrega e confirma. Uma parcela, pronto.
* **Reserva de um mês com entrada:** você escolhe **Sinal + restante**, define 30% de sinal — vence hoje — e o restante para a data da entrega. O cliente confirma pagando a entrada.
* **Cliente PJ que paga faturado:** **À vista**, mas com **a prazo D+30**: você entrega agora e a cobrança vence daqui a 30 dias.
* **Locação grande dividida:** **Parcelado** em 3x mensais. Você ativa o valor por parcela, deixa a primeira maior (a "entrada") e ajusta as outras até a soma fechar o total.
* **Precisou empurrar uma parcela:** o cliente pediu mais uma semana. Você abre a parcela em aberto, troca a data no lápis e salva — se havia boleto, ele continua o mesmo, só com o novo vencimento.
* **"Ele disse que paga metade na entrega":** você emite normalmente (o formato e as datas não mudam) e, na seção **Como o cliente vai pagar (indicativo)**, marca **Pix** e escreve *metade na entrega*. Quem for receber lê o recado na lista e na ficha — e continua livre para registrar o que de fato entrar.

## Para quem quer os números

Só para os curiosos — o LocFlow faz isso por você.

* **À vista:** 1 parcela = total, vencendo na data escolhida (mais o D+X, se ativo).
* **Sinal + restante:**
  * Sinal por **percentual**: `sinal = total × percentual ÷ 100`.
  * Sinal por **valor fixo**: exatamente o valor que você digitou.
  * **Restante** = `total − sinal` (sempre, para fechar o total).
  * O sinal vence **hoje**; o restante na data escolhida + D+X.
* **Parcelado (divisão igual):** cada parcela = `total ÷ nº de parcelas`, arredondado; **a sobra de centavos vai para a última** parcela — então a soma fecha o total ao centavo.
* **Parcelado (valor por parcela):** você define cada valor; o LocFlow exige que a **soma seja igual ao total** antes de emitir.
* **A prazo (D+X):** soma X dias corridos à data de vencimento (e a todas as parcelas, no parcelado) — **sem** tocar nos valores.

## Próximo passo

* Para entender a fatura, as parcelas e o que cada status significa: [Faturas e parcelas](faturas-e-parcelas.md).
* Para registrar o dinheiro que entrou (na mão ou pelo motorista): [Recebendo pagamentos](recebendo-pagamentos.md).
* Para cobrar com link de PIX, cartão ou boleto: [Pagamento online](pagamento-online.md).
* Para entender como o orçamento avança no funil: [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md).
