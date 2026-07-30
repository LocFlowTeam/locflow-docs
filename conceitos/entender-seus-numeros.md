---
icon: lightbulb
description: Seis ideias que transformam o relatório em decisão — competência e caixa, margem de contribuição, por que a estrutura não é dividida, cobertura, natureza e o aviso honesto sobre o desgaste do seu acervo.
---

# Entender seus números

Você entende do seu negócio. Você sabe quantas cadeiras cabem no caminhão, quanto tempo leva para montar uma tenda de 10×10 e qual cliente atrasa. O que quase nenhum dono de locadora aprendeu — porque ninguém ensina — é **como transformar o movimento do caixa em decisão**.

Esta página é isso. Seis ideias, com números de locadora de verdade. Nenhuma delas exige que você seja contador.

| | A ideia | O que ela te dá |
| --- | --- | --- |
| 1 | **Competência e caixa** | Parar de confundir "faturei" com "recebi" |
| 2 | **Margem de contribuição** | O número que decide se um trabalho vale a pena |
| 3 | **Estrutura** | Por que galpão e contador ficam fora da conta de cada trabalho |
| 4 | **Cobertura da estrutura** | Saber se a operação paga a casa — e quanto pode crescer |
| 5 | **Natureza e serviço** | Fazer o relatório separar aluguel de venda sozinho |
| 6 | **O aviso honesto** | O que os números de hoje **ainda não** mostram |

## 1. Competência e caixa: faturei não é recebi

São duas datas diferentes para o mesmo negócio, e confundi-las é a causa número um de "o relatório diz que eu tenho dinheiro, mas a conta está vazia".

* **Competência** — quando o negócio **aconteceu**.
* **Caixa** — quando o dinheiro **se moveu**.

**Exemplo.** Dia 20 de setembro você fecha um casamento de R$ 30.000: metade na assinatura (paga em 22/set), metade em 10 de outubro.

| | Setembro | Outubro |
| --- | --- | --- |
| **Por competência** (quando o negócio aconteceu) | R$ 30.000 | — |
| **Por caixa** (quando o dinheiro entrou) | R$ 15.000 | R$ 15.000 |

Os relatórios do LocFlow são **regime de caixa**: eles contam o dinheiro no dia em que ele se moveu. Então esse pedido aparece em setembro com R$ 15.000, e os outros R$ 15.000 aparecem em outubro.

E o que ainda não entrou? Fica registrado como **previsto** — visível em [Contas a pagar e a receber](../financeiro/contas-a-pagar-e-a-receber.md), somado ali como "a receber", mas **fora do saldo** que você vê na [Visão geral](../financeiro/visao-geral.md).

{% hint style="success" %}
**Por que previsto fora do saldo te protege.** Se os R$ 15.000 de outubro já entrassem no saldo em setembro, você abriria o app, veria dinheiro que não existe e decidiria em cima dele — compraria lona, pagaria um freela, adiantaria fornecedor. Aí o cliente atrasa 40 dias, ou não paga. **Saldo é dinheiro que você pode gastar hoje.** Promessa de pagamento é outra coisa, e por isso mora em outra tela.
{% endhint %}

{% hint style="info" %}
O lançamento tem um campo opcional **Data de competência** (no passo *Detalhes*). Ele serve para você registrar a qual mês aquele gasto pertence de verdade — a conta de energia de junho paga em julho, por exemplo. Os relatórios continuam lendo o **dia do caixa**; a competência fica como memória sua, para quando você conversar com o contador.
{% endhint %}

## 2. Margem de contribuição: o número de decisão

Definição em uma linha: **é o que sobra de um trabalho depois de pagar os custos que só existiram por causa dele.**

**Exemplo.** Locação para um casamento: 1 tenda de 6×6 e 100 cadeiras, R$ 4.800.

| | |
| --- | --- |
| **(+) Receita** | R$ 4.800 |
| (−) Frete de ida e volta | R$ 600 |
| (−) Dois freelancers na montagem | R$ 700 |
| (−) Lavagem e reparo de 4 cadeiras que voltaram sujas | R$ 120 |
| **(=) Margem de contribuição** | **R$ 3.380** (70% da receita) |

Repare no que **não** entrou: o aluguel do galpão, o contador, o salário do administrativo, o sistema. E não entrou por um motivo simples e verificável — **se este casamento não acontecesse, você pagaria exatamente o mesmo galpão**.

É isso que faz a margem de contribuição ser **o número de decisão**:

* **"Aceito este trabalho?"** Se a margem de contribuição é positiva e você tem os itens livres, aceitar é melhor que não aceitar. O trabalho ajuda a pagar a casa.
* **"Dou desconto até quanto?"** No exemplo, o piso do preço é **R$ 1.420** — exatamente o que os custos diretos consomem. Abaixo disso você paga para trabalhar: o cliente não cobre nem o frete e os freelancers.
* **"Que serviço eu corto?"** O que tem margem negativa — e a aba Serviços te mostra ordenado pela pior.

{% hint style="warning" %}
**Margem de contribuição não é lucro.** Ela ainda precisa pagar a estrutura. Um mês com R$ 43.000 de margem e R$ 50.000 de estrutura fecha no vermelho, mesmo com todos os trabalhos "lucrativos". A ideia 4 trata exatamente disso.
{% endhint %}

## 3. Estrutura: o que é e por que não dividimos

**Estrutura** é tudo que você paga para a locadora **existir**, independentemente de quantos pedidos entraram no mês:

| Exemplo | Muda se você fizer 10 pedidos em vez de 100? |
| --- | --- |
| Aluguel do galpão | Não |
| Contador | Não |
| Sistema / internet / telefone | Não |
| Salário do administrativo | Não |
| Marketing | Não (é decisão sua, não do pedido) |
| Energia da parte administrativa | Quase nada |

No LocFlow, esses lançamentos recebem a natureza **"As duas"** e aparecem no relatório num bloco de **largura cheia, indivisível**: `Estrutura (as duas)`. Eles **não são divididos entre aluguel e venda**.

Isso costuma soar estranho na primeira leitura — "mas parte do galpão é do aluguel e parte é da venda, não é?". Na intuição, sim. Na prática, **qualquer régua para fazer essa divisão produz um número pior do que não dividir**.

Vamos provar com um mês de exemplo — o mesmo usado em [Relatórios: como ler](../financeiro/relatorios.md):

| | |
| --- | --- |
| Aluguel | R$ 92.000 de receita · **R$ 40.000** de margem de contribuição |
| Venda | R$ 18.000 de receita · **R$ 3.200** de margem de contribuição |
| Estrutura (as duas) | R$ 28.400 |
| Não classificado | R$ 1.900 |
| **Resultado do mês** | **R$ 12.900** |

### Dividir por faturamento pune quem cresce

Receita total: R$ 92.000 de aluguel + R$ 18.000 de venda = R$ 110.000. O aluguel é 83,6% disso, então absorveria R$ 23.750 da estrutura, e a venda R$ 4.650.

Resultado: a venda passa a mostrar **prejuízo de R$ 1.450** (R$ 3.200 − R$ 4.650). Aí você corta a venda — e:

| | Antes | Depois de cortar a venda |
| --- | --- | --- |
| Margem do aluguel | R$ 40.000 | R$ 40.000 |
| Margem da venda | R$ 3.200 | R$ 0 |
| (−) Estrutura | R$ 28.400 | **R$ 28.400** |
| (−) Não classificado | R$ 1.900 | R$ 1.900 |
| **Resultado** | **R$ 12.900** | **R$ 9.700** |

**O galpão não caiu um centavo, e você ficou R$ 3.200 mais pobre** por causa de um número inventado por uma régua. Isso tem nome no mercado: espiral da morte. A linha "no vermelho" é cortada, a estrutura é redistribuída nas que sobraram, mais uma aparece no vermelho, e assim vai.

E tem o outro lado: se no mês seguinte a venda crescer para R$ 40.000 de receita, a fatia do aluguel na estrutura cai para R$ 19.800 e o "lucro do aluguel" **salta quase R$ 4.000** — por um motivo que não tem nada a ver com o aluguel. Número que se move sozinho não serve para decidir.

### Dividir por lucro quebra em mês de prejuízo

Janeiro parado: aluguel fecha em −R$ 2.000 de margem, venda em +R$ 1.000. Soma: −R$ 1.000. Divida a estrutura "por lucro" e os pesos viram **200%** e **−100%**: uma natureza absorve R$ 56.800 de galpão e a outra recebe um **crédito** de R$ 28.400 — como se o galpão tivesse pagado dinheiro para você. Troque os sinais e o absurdo troca de lado: quem perdeu dinheiro é que recebe o crédito. Não é impreciso; é inválido.

### E o pior: a conta que mais importa fica errada

A pergunta que mais mexe no seu bolso é **"faço com a minha frota ou terceirizo?"**. Nessa conta, só entra o que **muda com a escolha**:

> **Custo evitável** é o que você **deixa de gastar** se aquilo não acontecer.

Se você terceirizar todo o frete amanhã: o combustível, o motorista extra e a manutenção variável desaparecem — são **evitáveis**. O galpão, o contador e o sistema continuam chegando na mesma data e no mesmo valor — **não são evitáveis**.

Se você embutir uma fatia do galpão no custo do frete próprio, a sua frota parece caríssima, você terceiriza, o relatório do frete melhora — e o **lucro total cai**, porque o galpão continua lá e agora você também paga o terceiro. É o erro mais caro que uma planilha de locadora comete, e é por isso que o insight **Fazer × repassar** usa **somente custo evitável**.

{% hint style="info" %}
**O que o LocFlow faz em vez de dividir:** empilha em camadas. Primeiro a margem de contribuição de cada natureza (limpa, sem nada rateado). Depois, embaixo e inteira, a estrutura. E uma linha que responde "quem paga o galpão?" sem dividir o galpão: a **cobertura**. É a ideia 4.

**Não existe botão de rateio no LocFlow, e isso é decisão consciente** — não é recurso faltando. Se um dia existir, será uma lente opcional, desligada por padrão, e nunca alterará o seu razão.
{% endhint %}

{% hint style="success" %}
**Como usar "custo evitável" no dia a dia.** Diante de qualquer decisão, faça duas perguntas: *o que aparece na minha conta se eu fizer isso?* e *o que desaparece da minha conta se eu não fizer?* Só o que muda entre as duas respostas entra na comparação. Vale para frete, para contratar freelancer em vez de fixo, para comprar o segundo caminhão.
{% endhint %}

## 4. Cobertura da estrutura

Na aba **Serviços**, sob cada coluna, aparece algo como *"cobre 1,41x da estrutura"*. Leia assim:

| Cobertura | Significa |
| --- | --- |
| **1,41x** (aluguel) | A margem do aluguel paga a estrutura inteira e sobra 41% dela |
| **0,11x** (venda) | A venda, sozinha, pagaria 11% da estrutura |
| **1,52x** (soma das duas) | A operação inteira cobre a casa uma vez e meia |

Três coisas que a cobertura resolve:

1. **Some sempre as duas.** É a soma que diz se o mês fecha no azul. Acima de 1,00, sim. Abaixo, não — e quanto falta está na diferença.
2. **Cobertura baixa não é veredito de corte.** "A venda cobre 0,11x" quer dizer "a venda ainda é pequena", não "a venda dá prejuízo". Enquanto a margem de contribuição dela for **positiva**, ela está ajudando a pagar o galpão. Cortar essa linha deixa você com R$ 28.400 de estrutura e menos margem para pagá-la.
3. **É a régua de crescimento.** Contratar mais uma pessoa no administrativo por R$ 3.000/mês muda a pergunta de "eu tenho R$ 3.000?" para "a minha margem aguenta R$ 31.400 de estrutura?". Com R$ 43.200 de margem somada, aguenta com folga. Com R$ 30.000, você estaria contratando para dentro do prejuízo.

**E quando nenhuma das duas cobre?** Some: se a soma ficar abaixo de 1,00, você tem três caminhos reais e um caminho falso.

| Caminho | O que fazer |
| --- | --- |
| **Aumentar a margem** | Subir preço, cortar desconto ou reduzir custo direto (frete, freela, insumo) — a aba Serviços mostra em qual serviço primeiro |
| **Diminuir a estrutura** | É a única coisa que realmente derruba os R$ 28.400: renegociar galpão, rever assinaturas, revisar o administrativo |
| **Crescer volume** | Só funciona se a margem de contribuição for positiva — mais pedidos com margem negativa aprofundam o buraco |
| **~~Cortar a natureza de menor cobertura~~** | **Não funciona.** A estrutura não cai, e você perde a margem que ela trazia |

## 5. Natureza e serviço: a categoria sugere, o lançamento decide

Para o relatório separar aluguel de venda, cada movimento de dinheiro precisa responder a uma pergunta: **"isto sustenta qual operação?"**. São quatro respostas possíveis:

| Resposta | Quando usar | No relatório |
| --- | --- | --- |
| **Aluguel** | Sustenta a locação: manutenção do acervo, freela da equipe de montagem, frete de entrega | Entra na coluna Aluguel |
| **Venda** | Sustenta a venda: mercadoria comprada para revender, comissão do vendedor | Entra na coluna Venda |
| **As duas** | Galpão, contador, sistema, administrativo, marketing | Bloco `Estrutura (as duas)`, inteiro |
| **Não sei** | Ninguém decidiu ainda | Bloco `Não classificado`, fora das colunas |

### Por que a categoria sugere e o lançamento decide

A **categoria** carrega uma sugestão (em **Gestão Financeira → Categorias**, campo *Sustenta qual operação?*). Ela pré-seleciona a resposta quando você registra um lançamento naquela categoria — e resolve 90% dos casos sem você pensar.

Mas ela não pode ser a palavra final, e o exemplo é o **freelancer**. Você tem uma categoria "Freelancers". No sábado você contrata dois para montar uma tenda — isso é **aluguel**. Na terça, contrata um para o mutirão de venda de itens de mostruário — isso é **venda**. **Mesma categoria, naturezas diferentes.** Se a categoria decidisse, um dos dois estaria no lugar errado, para sempre.

Por isso a decisão fica **no lançamento**: no passo **Detalhes** do novo lançamento (e direto no formulário, quando você edita), o campo *"Isto sustenta qual operação?"* já vem com a sugestão da categoria marcada — e você troca quando o caso for diferente.

{% hint style="success" %}
**O que o LocFlow responde sozinho, sem te perguntar:**

* **Recebimento de um pedido** — herda a natureza do pedido: pedido de locação vira Aluguel, pedido de venda vira Venda.
* **Nota fiscal emitida** — a nota já diz o que foi faturado: nota de venda vira Venda, nota do serviço de locação vira Aluguel.
* **Frete de terceiro provisionado** — nasce com a natureza do pedido que o gerou.

Sobra para você **o caso ambíguo** — que é exatamente o caso em que só você sabe a resposta.
{% endhint %}

### "Não classificado" é uma pendência sua, não um erro nosso

O LocFlow **não chuta**. Sem resposta, o valor vai para o bloco `Não classificado`: visível, contado no resultado do período, e **fora** das colunas de aluguel e venda. Preferimos te mostrar uma pendência de R$ 1.900 a te entregar uma margem de aluguel silenciosamente errada.

Para zerar a fila:

1. Abra **Gestão Financeira → Relatórios → Serviços**.
2. Toque no bloco **Não classificado** — o LocFlow leva você para a lista de [Lançamentos](../financeiro/lancamentos.md).
3. Abra cada lançamento. Na edição, o campo *"Isto sustenta qual operação?"* aparece direto no formulário.
4. Responda e salve. Se aquela categoria vai sempre para o mesmo lado, aproveite e marque a sugestão **na categoria** — assim os próximos já nascem certos.

### O serviço: o outro lado da mesma moeda

A **natureza** diz *qual operação* aquele dinheiro sustenta. O **serviço associado** diz *a qual serviço prestado* ele pertence — frete, mão de obra, montagem, desmontagem, layout ou outros.

É o que permite ao relatório colocar lado a lado **o que você cobra** de frete e **o que você gasta** com frete. Sem essa marcação, os dois números existem em telas separadas e ninguém junta. As subcategorias herdam a marcação da mãe: marque "Frete/Transporte" e "Pedágio" já entra no frete. Detalhes em [Categorias e plano de contas](../financeiro/categorias-e-plano-de-contas.md).

## 6. O aviso honesto: o desgaste do seu acervo não aparece

Este é o ponto em que a maioria dos sistemas fica calada. Nós não vamos ficar, porque a leitura errada aqui custa dinheiro de verdade.

Os relatórios são **regime de caixa** — contam o dinheiro no dia em que ele se moveu. Consequência direta:

| | Como o custo aparece hoje |
| --- | --- |
| **Aluguel** | O **desgaste e a reposição** dos seus itens locáveis **não aparecem**. Você comprou as cadeiras há dois anos; elas se desgastam a cada temporada, mas nenhum custo é registrado quando isso acontece |
| **Venda** | O custo da mercadoria aparece **inteiro**, no mês em que você pagou o fornecedor |

**Ou seja: a comparação entre aluguel e venda, hoje, favorece o aluguel.** Não porque o aluguel seja necessariamente melhor, mas porque um dos lados está mostrando um custo que o outro esconde.

{% hint style="warning" %}
**Como compensar isso na sua cabeça** — três passos, uma vez por temporada:

1. **Some o que você pagou pelo acervo que está em uso.** Exemplo: 400 cadeiras a R$ 80 = R$ 32.000.
2. **Divida pelas temporadas que ele aguenta.** Se as cadeiras sobrevivem a 4 temporadas, o desgaste é de **R$ 8.000 por temporada**.
3. **Subtraia esse valor da margem do aluguel antes de comparar com a venda.** No mês do exemplo, a margem do aluguel cai de R$ 40.000 para R$ 32.000 — e a cobertura da estrutura cai de **1,41x para 1,13x**.

R$ 32.000 contra R$ 3.200 continua sendo uma vitória folgada do aluguel. O ponto não é inverter a conclusão: é você **saber de quanto é a folga de verdade** antes de decidir comprar mais acervo ou empurrar mais venda.
{% endhint %}

Duas consequências práticas do mesmo efeito, para você não se enganar em nenhuma das duas direções:

* **O mês em que você compra acervo parece um desastre.** Você paga R$ 20.000 em tendas novas e o resultado do mês afunda. Não afundou: você trocou dinheiro por um bem que vai faturar por anos. Os meses seguintes, por sua vez, parecem melhores do que são.
* **Mês sem compra de mercadoria faz a venda parecer melhor.** Se você vendeu do estoque comprado no mês anterior, a receita aparece agora e o custo apareceu antes.

{% hint style="info" %}
**O que fazer enquanto isso.** Registre a **compra de acervo** com a natureza **Aluguel** — assim, quando ela aparecer, aparece no lado certo. E mantenha a reserva mental de reposição por temporada: é ela que impede a decisão "vou parar de vender porque o aluguel rende mais" de nascer de um número incompleto.

O LocFlow ainda **não** faz essa conta por você. É por isso que ela está escrita aqui, em vez de escondida.
{% endhint %}

## Três perguntas que você passa a conseguir responder

| A pergunta | Onde clicar | O que olhar |
| --- | --- | --- |
| **Aluguel e venda: qual dos dois sustenta a casa?** | Relatórios → **Serviços** | As duas margens de contribuição e a **cobertura** de cada uma. Some as coberturas para saber se o mês fecha no azul — e desconte a reserva de reposição do aluguel antes de comparar (ideia 6) |
| **Cada serviço que eu cobro se paga?** | Relatórios → **Serviços** → *Ganho por serviço prestado* | A **primeira linha** (pior margem). Depois, *Frete em detalhe*, para ver se o frete cobrado cobre o frete pago |
| **Vale mais fazer com a minha frota ou repassar?** | Relatórios → **Insights** → *Fazer × repassar* | A frase de veredito e o tamanho da **amostra**. Se estiver em silêncio, é porque ainda não há pedidos suficientes para concluir |

## Próximo passo

* [Relatórios: como ler](../financeiro/relatorios.md) — aba por aba, com as armadilhas de interpretação.
* [Locação e venda](locacao-e-venda.md) — como as duas modalidades convivem no mesmo pedido.
* [Categorias e plano de contas](../financeiro/categorias-e-plano-de-contas.md) — onde você marca natureza e serviço.
* [Conciliação e fechamento](../financeiro/conciliacao-e-fechamento.md) — como garantir que o número que você está lendo está completo.
