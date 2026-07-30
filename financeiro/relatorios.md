---
icon: chart-pie
description: As quatro abas do relatório, a pergunta que cada uma responde, como ler cada número — e a armadilha de interpretação de cada uma.
---

# Relatórios: como ler

Você encontra os relatórios em **Gestão Financeira → Relatórios**.

Este não é um extrato bonito. São **quatro perguntas diferentes** sobre o mesmo dinheiro, e cada aba responde uma:

| Aba | A pergunta que ela responde |
| --- | --- |
| **Categorias** | Onde meu dinheiro foi? |
| **Insights** | Com quem, em quê e por qual caminho ele foi? |
| **DRE** | No fim do ano, sobrou ou faltou? |
| **Serviços** | Eu ganho no aluguel? na venda? em cada serviço que eu cobro? |

{% hint style="success" %}
**Por que vale aprender a ler:** relatório que você não entende vira decoração. Depois destas quatro leituras você consegue responder "vale mais fazer com a minha frota ou repassar?" e "aluguel e venda: qual dos dois sustenta a casa?" — com número, não com sensação.
{% endhint %}

A tabela acima está na ordem em que as abas aparecem na tela; as seções abaixo seguem uma ordem de **aprendizado** — cada uma usa o que a anterior explicou.

Se você quer primeiro o **raciocínio** por trás dos números (competência e caixa, margem de contribuição, estrutura), comece por [Entender seus números](../conceitos/entender-seus-numeros.md) e volte para cá.

## Dois controles no topo, valendo para tudo

1. **Período** — abre com o **mês corrente** e tem cinco modos: intervalo livre, semana, mês, últimos 30/60/90 dias e ano.
2. **Olho de privacidade** — esconde os valores (viram `••••`) para você abrir o relatório na frente de alguém sem mostrar faturamento.

A aba **DRE** é a exceção: ela é sempre de um **ano inteiro**, e você troca de ano nas setinhas.

{% hint style="info" %}
**Todas as abas são regime de caixa.** Um valor entra no relatório no dia em que o dinheiro **realmente se moveu** — não no dia em que você faturou. O que está previsto (a receber ou a pagar) **não aparece** aqui; ele vive em [Contas a pagar e a receber](contas-a-pagar-e-a-receber.md). Isso é deliberado: relatório de caixa não mente sobre dinheiro que ainda pode não vir.
{% endhint %}

## Aba Categorias — "onde meu dinheiro foi?"

Um botão alterna entre **Despesas** e **Receitas**. Você vê uma rosca com o total no centro e, ao lado, o ranking: nome, valor, participação em % e uma barra proporcional. Toque numa linha para destacá-la na rosca.

**Como ler:**

* As **subcategorias** aparecem recuadas sob a categoria-mãe. O total da mãe **já inclui** as filhas — não some as duas.
* Quando há muitas categorias, as menores são agrupadas numa fatia **"Outras"**. Se ela ficou gorda, é sinal de que vale criar categoria para algo que está escondido ali.
* O **%** é a participação dentro do recorte que está na tela. Trocou o período, muda a base do percentual.

{% hint style="warning" %}
**A armadilha: comparar meses de volume diferente.** Em janeiro parado, o aluguel do galpão pode aparecer como 40% das despesas; em novembro cheio, como 12%. **O galpão não mudou** — mudou o tamanho do bolo. Para comparar meses, olhe o **valor em reais** das despesas fixas e o **percentual** das variáveis (frete, mão de obra, insumos). O percentual só é comparável entre meses de volume parecido.
{% endhint %}

Para criar, renomear ou agrupar categorias, veja [Categorias e plano de contas](categorias-e-plano-de-contas.md).

## Aba DRE — "no fim do ano, sobrou ou faltou?"

DRE é o apelido de *Demonstração do Resultado* — o nome que o seu contador usa para "quanto sobrou depois de tudo". A aba mostra o ano inteiro em três blocos:

```
  (+) Receita total
  (−) Custos de operação          ← frete/transporte e taxas
  (−) Despesas administrativas    ← todo o resto
  (=) Resultado do ano
```

Abaixo você tem o detalhe categoria por categoria, o gráfico de **Evolução mensal** (receitas × despesas × resultado) e a tabela **Mês a mês**, para ver a sazonalidade da sua temporada.

**Como ler:** comece pela linha **Resultado** de cada mês na tabela. Um ano fechando positivo com quatro meses negativos é um negócio sazonal saudável; um ano positivo apenas por causa de **um** mês excepcional é um negócio frágil.

{% hint style="warning" %}
**A armadilha: é regime de caixa, e caixa distorce compras grandes.** No mês em que você paga 200 cadeiras novas, o DRE mostra um mês terrível — e nos meses seguintes, em que essas cadeiras estão faturando sem custo nenhum aparecendo, ele mostra meses ótimos. Nenhum dos dois é a verdade da operação. Da mesma forma, uma fatura emitida e **não paga** não aparece aqui: para você o pedido "aconteceu", para o relatório de caixa ainda não. Veja [Competência e caixa](../conceitos/entender-seus-numeros.md#1-competencia-e-caixa-faturei-nao-e-recebi).
{% endhint %}

## Aba Serviços — o coração da análise

É a aba que responde **"eu ganho ou perco no aluguel? e na venda? e em cada serviço que eu cobro?"**. São três cartões, de cima para baixo — e o primeiro, *Ganho por natureza*, tem quatro partes que valem uma por uma.

### Ganho por natureza: as duas colunas

Duas colunas, **Aluguel** e **Venda**, com a mesma conta em cada uma: receita, menos os custos que existem **por causa daquela operação**, resultando na **margem de contribuição**.

| | Aluguel | Venda |
| --- | --- | --- |
| **(+) Receita** | R$ 92.000 | R$ 18.000 |
| **(−) Custos diretos** | R$ 52.000 | R$ 14.800 |
| **(=) Margem de contribuição** | **R$ 40.000** | **R$ 3.200** |
| *da receita* | 43,5% | 17,8% |
| *cobre a estrutura* | 1,41x | 0,11x |

Leitura: cada R$ 100 que entram de aluguel deixam R$ 43,50 depois dos custos daquela locação. Na venda, deixam R$ 17,80 — o que é normal, porque na venda a mercadoria em si é custo direto.

As **duas colunas aparecem sempre**, mesmo zeradas. Uma coluna vazia é informação: significa "não vendi nada neste período".

### Estrutura (as duas) e Não classificado

Abaixo de um filete, em **largura cheia**, dois blocos que **não se dividem entre as colunas**:

| Bloco | O exemplo | No mês do exemplo |
| --- | --- | --- |
| **Estrutura (as duas)** | Galpão, contador, sistema, administrativo, marketing, energia | − R$ 28.400 · 14 lançamentos |
| **Não classificado** | Lançamentos em que ninguém respondeu "isto sustenta qual operação?" | − R$ 1.900 · 3 lançamentos |

**A estrutura fica inteira, sem ser dividida — e isso é decisão consciente, não uma conta que faltou.** O galpão serve ao aluguel e à venda ao mesmo tempo, e qualquer régua para fatiá-lo entre os dois inventaria número e estragaria as duas colunas. O porquê completo, com exemplo, está em [Por que a estrutura não é dividida](../conceitos/entender-seus-numeros.md#3-estrutura-o-que-e-e-por-que-nao-dividimos).

**Não classificado é uma pendência sua**, não um erro do sistema. Toque no bloco: o LocFlow abre a lista de [Lançamentos](lancamentos.md), onde você abre cada um e responde a pergunta. Enquanto não responder, aquele valor **não entra em nenhuma das colunas** — ele fica visível, de fora, cobrando resposta.

### O resultado, com a conta impressa na tela

```
Margem do aluguel + margem da venda − estrutura − não classificado = resultado
    R$ 40.000     +    R$ 3.200     −  R$ 28.400  −    R$ 1.900     = R$ 12.900
```

A identidade aparece escrita embaixo do resultado justamente para você poder conferir a linha com o dedo. Nada foi rateado dentro das colunas: some as quatro partes e você chega no resultado do período.

### A linha de cobertura da estrutura

Sob cada coluna aparece algo como *"43,5% da receita · cobre 1,41x da estrutura"*. Essa é a resposta à pergunta "quem paga o galpão?" **sem dividir o galpão**:

* **1,41x** — a margem do aluguel paga a estrutura inteira e ainda sobra 41% dela.
* **0,11x** — a venda, sozinha, pagaria 11% da estrutura. Não é "a venda dá prejuízo": é "a venda ainda é pequena para carregar a casa".
* **Some as duas.** Aluguel 1,41 + venda 0,11 = **1,52** — a operação como um todo cobre a estrutura uma vez e meia. Abaixo de 1,00 somando as duas, o mês fecha no vermelho.

{% hint style="info" %}
**O que fazer com a cobertura:** ela é a régua de crescimento. Se você quer contratar mais uma pessoa no administrativo (R$ 3.000/mês na estrutura), a pergunta deixa de ser "eu tenho R$ 3.000?" e passa a ser "a minha margem de contribuição aguenta R$ 31.400 de estrutura?". Com R$ 43.200 de margem somada, aguenta. Com R$ 30.000, não.
{% endhint %}

### Ganho por serviço prestado

O **segundo cartão** põe cada serviço que você **cobra** (frete, mão de obra, montagem, desmontagem, layout, outros) contra o que ele **custa**. **Pior margem primeiro** — a lista abre pelo problema, não pelo troféu.

| Serviço | Margem | % | Detalhe |
| --- | --- | --- | --- |
| **Frete** | − R$ 1.400 | −12,7% | Cobrou R$ 11.000 · gastou R$ 12.400 |
| **Mão de obra** | R$ 2.400 | 40,0% | Cobrou R$ 6.000 · gastou R$ 3.600 |
| **Montagem** | R$ 2.700 | 30,0% | Cobrou R$ 9.000 · gastou R$ 6.300 |

Repare que **mão de obra** aparece antes de **montagem** mesmo tendo margem percentual maior: a ordem é pelo valor em reais. Os dois números dizem coisas diferentes — o **%** diz se o preço está certo, o **R$** diz se aquilo é grande o bastante para merecer sua atenção esta semana.

De onde vem cada lado:

* **A receita** sai da composição do pedido: cada acréscimo que você cobrou entra no serviço dele, e o frete entra pelo valor **cobrado do cliente**.
* **O custo** sai da categoria do lançamento. Uma categoria só entra num serviço se você marcou o **serviço associado** dela — é isso que faz "quanto gastei de frete" encontrar "quanto cobrei de frete". As subcategorias herdam a marcação da mãe.

A última linha, **"Locação/venda e estrutura"**, é o que não é serviço cobrado: o bem alugado ou vendido (já com o desconto que você deu) mais tudo que a categoria não liga a nenhum serviço.

{% hint style="warning" %}
**A armadilha: serviço sem categoria marcada aparece como lucro puro.** Se você cobra montagem mas lança o pagamento dos montadores numa categoria sem serviço associado, a montagem vai mostrar margem de 100%. Margem redonda demais é quase sempre custo faltando, não eficiência.
{% endhint %}

### Frete em detalhe

O **terceiro cartão** é dedicado ao frete — é onde mais locadora perde dinheiro sem saber:

```
  (+) Frete cobrado do cliente        R$ 11.000
  (−) Repasse a parceiros            R$  4.200
  (−) Combustível                    R$  5.100
  (−) Pedágio                        R$    900
  (−) Manutenção de veículos         R$  2.200
  (=) Margem de frete              − R$  1.400
```

Embaixo, uma frase de veredito: *"O frete que você cobra está se pagando"* ou *"Atenção: o frete cobrado NÃO cobre o frete pago — você está subsidiando as entregas."*

E, quando existe frete de terceiro no período, **Custo por transportadora** — quanto foi para cada uma. É detalhamento de para onde o dinheiro foi, não uma subtração nova.

{% hint style="info" %}
Frete subsidiado não é necessariamente erro: tem locadora que entrega "de graça" de propósito para fechar o aluguel. O relatório não decide isso por você — ele só garante que a decisão seja **consciente e medida**, e não uma surpresa no fim do ano.
{% endhint %}

## Aba Insights — seis cortes do mesmo dinheiro

| Corte | O que mostra |
| --- | --- |
| **Fazer × repassar** | Margem do frete por quem executou: sua frota, fornecedor ou parceiro |
| **Fornecedor** | Com quem você mais gasta |
| **Funcionário** | Quanto custa cada funcionário (salário, benefícios, diárias atribuídos a ele) |
| **Veículo** | Qual veículo custa mais |
| **Método** | Como você paga (Pix, boleto, cartão, dinheiro…) |
| **Cliente** | De quem vem o dinheiro |

Os cinco últimos são rankings com rosca e barra — leitura direta. O primeiro merece parágrafo próprio.

### Fazer × repassar: a decisão da frota

Compara a margem do frete em três modalidades — **com a sua frota**, **repassado a fornecedor** e **repassado a parceiro** — e devolve **uma frase de decisão**:

> *Frete repassado a fornecedor rende 29,0% contra 13,2% com a sua frota — priorize repassado a fornecedor enquanto a diferença durar.*

| Modalidade | Cobrou | Custou | Margem | % | Amostra |
| --- | --- | --- | --- | --- | --- |
| Repassado a fornecedor | R$ 3.100 | R$ 2.200 | R$ 900 | 29,0% | 5 pedidos |
| Com a sua frota | R$ 6.800 | R$ 5.900 | R$ 900 | 13,2% | 9 pedidos |
| Repassado a parceiro | R$ 1.100 | R$ 900 | R$ 200 | 18,2% | 2 pedidos |

**Por que este corte usa só custo evitável.** O custo de cada viagem aqui é o que você **deixa de gastar se a viagem não acontecer**: no terceiro, o que ele cobra; na sua frota, o que o cálculo de frete estima para aquela viagem (combustível, motorista, manutenção variável). **Galpão e contador ficam de fora de propósito** — eles não mudam se você terceirizar. Se entrassem, a sua frota apareceria artificialmente caríssima, você terceirizaria tudo, o relatório melhoraria e o seu lucro cairia. Esse é o erro clássico, e o LocFlow não o comete.

{% hint style="info" %}
**Por que um insight às vezes cala.** Com um ou dois pedidos, "repassar rende mais" é sorte, não tendência. Só há veredito quando **pelo menos duas modalidades têm 3 pedidos ou mais**; abaixo disso a tela explica o silêncio ("precisa de 3 pedidos em pelo menos duas modalidades para comparar") e marca a modalidade curta como **amostra pequena**. No exemplo acima, "repassado a parceiro" aparece com os números, mas fica fora da comparação. Preferimos calar a te empurrar uma conclusão frágil.
{% endhint %}

{% hint style="warning" %}
**A armadilha: margem não é a única variável.** Quando as duas modalidades rendem parecido, a própria frase diz para decidir por **prazo e risco**, não por margem. Terceiro barato que atrasa entrega de casamento custa mais caro que qualquer ponto percentual.
{% endhint %}

## A primeira leitura do mês, em ordem

Faça nesta sequência — cada passo prepara o próximo. Leva uns dez minutos.

1. **Concilie antes de ler.** Relatório sobre razão incompleto é ficção. Confira o extrato do banco contra o seu razão em [Conciliação e fechamento](conciliacao-e-fechamento.md).
2. **Serviços → Não classificado.** Se tiver pendência, classifique agora. Enquanto houver valor aí, as colunas de aluguel e venda estão incompletas.
3. **Serviços → Resultado do período.** O número do mês. Positivo ou negativo, é daqui que tudo parte.
4. **Serviços → cobertura da estrutura.** Some as duas coberturas. Acima de 1,00, a operação paga a casa. Abaixo, você já sabe o assunto do mês.
5. **Serviços → ganho por serviço prestado.** Olhe a **primeira linha** (a pior). Se estiver negativa, você tem um preço a corrigir ou um custo a cortar — e sabe exatamente em quê.
6. **Insights → Fazer × repassar.** Só se você tem frota. Confirme se a modalidade que você usa mais é a que rende mais.
7. **Categorias → Despesas.** Passe o olho no top 5. Alguma subiu sem motivo? É agora que se pergunta, não em dezembro.
8. **DRE, uma vez por trimestre.** Olhe a linha **Resultado** mês a mês e compare com o mesmo trimestre do ano passado.

{% hint style="success" %}
**Faça no mesmo dia todo mês.** Relatório lido de forma irregular só mostra sustos. Lido sempre no dia 5, mostra **tendência** — e tendência é o que permite decidir antes de doer.
{% endhint %}

## Antes de confiar nos números, leia isto

O resultado é **regime de caixa**, e isso tem uma consequência importante na comparação entre aluguel e venda: o **desgaste dos seus itens locáveis não aparece como custo**, enquanto na venda o custo da mercadoria aparece inteiro. Ou seja, **a comparação de hoje favorece o aluguel**. Não é bug e não é opinião — é como o caixa funciona, e você precisa saber disso para ajustar a leitura na sua cabeça. O ajuste, com exemplo, está em [O aviso honesto](../conceitos/entender-seus-numeros.md#6-o-aviso-honesto-o-desgaste-do-seu-acervo-nao-aparece).

## Próximo passo

* [Entender seus números](../conceitos/entender-seus-numeros.md) — o raciocínio por trás de cada aba.
* [Categorias e plano de contas](categorias-e-plano-de-contas.md) — onde você marca serviço e natureza, que é o que faz o relatório funcionar.
* [Lançamentos](lancamentos.md) — onde você classifica o que ficou pendente.
