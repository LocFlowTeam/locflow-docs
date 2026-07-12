---
icon: truck-fast
description: "Convide uma transportadora ou motorista de fora para executar a logística dos pedidos que você repassa — o papel restrito e isolado, o galpão que é a origem do frete dele, e o recebedor que garante o repasse."
---

# Parceiro Logístico Externo

**Onde fica:** menu da organização → **Parcerias**.

Às vezes o pedido está fechado, mas quem faz a entrega (ou a retirada) não é a sua equipe nem a sua frota: é uma transportadora ou um motorista de **fora** da sua operação. Para esses casos existe o **Parceiro Logístico Externo** — alguém de outra operação a quem você **repassa** pedidos para que ele cuide da logística e receba **a parte dele** por isso. Vale para **locação** e para **venda** de bens móveis.

{% hint style="info" %}
**Não confunda com o fornecedor de frete.** O [fornecedor de frete](fornecedores-de-frete.md) é um terceiro **sem login**, que você cadastra e opera por dentro da sua conta. O Parceiro Logístico Externo é o oposto: ele **tem a própria conta**, entra no LocFlow e faz a logística com as próprias mãos — só que enxergando **apenas** o que você repassa. Veja a comparação em [Fornecedor de frete × Parceiro Externo](#fornecedor-x-parceiro).
{% endhint %}

## O que é um Parceiro Logístico Externo {#o-que-e}

Pense no Parceiro Logístico Externo como um **braço logístico terceirizado que trabalha por conta própria**. Ele não faz parte da sua equipe — não é um [colaborador](../configuracoes/colaboradores-e-acessos.md). É alguém de fora, com acesso **restrito e isolado**: ele entra no LocFlow, mas o único pedaço da sua operação que enxerga são os **pedidos que você escolheu repassar a ele**.

Isso o coloca em um lugar próprio dentro das [Parcerias](visao-geral.md):

- Um **colaborador** trabalha **dentro** da sua organização, com papel e permissões que você define.
- Um **fornecedor de frete** é um terceiro **sem login**, que você opera por inteiro.
- Um **Parceiro Logístico Externo** é externo **e** tem conta própria — ele executa a logística sozinho, mas dentro de uma **caixa isolada** que só mostra o que você repassou.

{% hint style="success" %}
**Por que "isolado" é bom para os dois lados.** Você não abre a sua operação inteira para alguém de fora — ele vê só os pedidos repassados. E ele não precisa aprender o seu sistema por completo: entra numa área enxuta, feita para receber pedido, rodar a logística e acompanhar o repasse dele.
{% endhint %}

## O que o parceiro enxerga e faz {#o-que-o-parceiro-faz}

O parceiro entra com um **papel fixo: "Parceiro Logístico"**. Esse papel não é configurável como o de um colaborador — ele já vem pronto e recortado para uma coisa só: **receber pedidos repassados e cuidar da logística deles**. Na prática, o parceiro:

1. **Vê apenas os pedidos repassados a ele** — nada do resto da sua carteira, dos seus clientes ou dos seus números.
2. **Executa a logística** — planeja e roda o [roteiro](../logistica/planejando-o-roteiro.md) das entregas e retiradas daquele pedido, marcando o que foi feito em campo.
3. **Recebe o repasse** — a parte que cabe a ele cai nos **próprios dados bancários** (o recebedor dele).

{% hint style="info" %}
O que o parceiro **não** faz: ele não mexe no seu catálogo, não vê os seus outros pedidos, não altera preços da sua operação e não acessa as suas configurações. O acesso dele começa e termina no pedido repassado.
{% endhint %}

## Fornecedor de frete × Parceiro Externo {#fornecedor-x-parceiro}

Como os dois vivem na área de **Parcerias**, vale deixar a diferença cristalina:

| | Fornecedor de frete | Parceiro Logístico Externo |
| --- | --- | --- |
| **Quem é** | Uma transportadora terceira que **você** cadastra | Uma transportadora/motorista externo, **com conta própria** |
| **Tem login?** | Não — você opera por ele | Sim — ele entra com um papel **restrito e isolado** |
| **O que enxerga** | Nada (não acessa o sistema) | **Só** os pedidos que você repassa a ele |
| **Quem faz a logística** | A sua equipe, usando a [frota-espelho](fornecedores-de-frete.md#frota-espelho) dele | O **próprio parceiro**, com a mão dele |
| **De onde sai o frete** | Da frota que você monta com o detentor dele | Do **galpão do parceiro** (veja abaixo) |
| **Como ele recebe** | Você acerta com ele por fora | Pelo **recebedor** dele, no repasse automático |

Resumindo: o fornecedor de frete é *força de transporte que você controla*; o Parceiro Logístico Externo é *um parceiro que se conecta e opera sozinho*.

## Como convidar um parceiro {#como-convidar}

Convidar é rápido e funciona como qualquer convite do LocFlow — a mecânica de abrir o link e aceitar está em [Aceitando um convite](../primeiros-passos/aceitando-um-convite.md). O que muda é o destino: em vez de entrar na sua equipe, o parceiro cai naquela **área isolada** só dele.

1. Na área de **Parcerias**, inicie o convite do parceiro.
2. Escolha **como enviar**: por **link** (você copia e manda por WhatsApp, mensagem, o que for) ou por **e-mail**.
3. Escolha **onde ele vai usar** — no **aplicativo** ou no **navegador**. O link já leva o parceiro para o lugar certo.
4. O parceiro **abre o link**, entra (com o Google ou com e-mail e senha) e toca em **aceitar**.
5. Pronto: a partir daí, tudo que você **repassar** a ele aparece na área dele.

{% hint style="info" %}
**Convidar é só o começo do preparo.** Para o parceiro conseguir operar e receber de verdade, ainda faltam duas peças: o **galpão** dele (de onde sai o frete) e o **recebedor** dele (para onde vai o repasse). As duas seções seguintes cuidam disso.
{% endhint %}

## O galpão do parceiro: a origem do frete {#galpao-do-parceiro}

Esta é a parte mais importante da página — a que costuma gerar dúvida e a que mais afeta o dinheiro.

### O que significa {#galpao-conceito}

O **galpão do parceiro** é o **endereço de onde o parceiro sai** para atender. E, mais do que um endereço, ele é a **origem do cálculo do frete** que o parceiro repassa. Ou seja: o valor do frete de um pedido repassado é calculado **a partir do galpão dele**, não do seu.

Faz sentido — quem roda a rota é o parceiro, então a conta de distância precisa partir do ponto de partida **dele**. O mesmo princípio de "de onde sai a carga" que você já conhece do orçamento (em [Movimentos, janelas e galpão de origem](../orcamentos/movimentos-e-janelas.md)) vale aqui, só que o ponto de partida é o galpão do parceiro.

{% hint style="warning" %}
**Consequência direta:** se o galpão do parceiro estiver no lugar errado no mapa, **o frete sai errado** — para mais ou para menos. Por isso o ponto exato importa tanto.
{% endhint %}

### O que preencher {#galpao-dados}

O galpão do parceiro se apoia em dois dados que precisam estar certos:

| Dado | O que é | Por que importa |
| --- | --- | --- |
| **Localização no mapa (o pino)** | O ponto exato de onde o parceiro parte | É a origem do cálculo do frete. Um pino fora do lugar deixa o frete impreciso. |
| **Raio de atendimento** | A área que o parceiro cobre, medida em metros/quilômetros a partir do galpão | Define até onde ele alcança. Fora do raio, o parceiro não atende aquele destino. |

Sobre a **localização no mapa**, vale um cuidado especial:

{% hint style="warning" %}
**Confira o pino — não confie só no endereço.** Quando você digita o endereço, o LocFlow tenta achar o ponto no mapa sozinho (a localização automática pelo endereço). Só que, às vezes, esse ponto **cai um pouco fora** — no meio da quadra, na rua errada, a alguns metros de distância. Como esse ponto é a origem do frete, um deslize ali vira frete impreciso. Por isso, **ajuste o pino manualmente** até ele cair exatamente no galpão.
{% endhint %}

### Dá para ajustar depois {#galpao-editar}

O galpão não é uma decisão de uma vez só. Existe uma **tela para editar o galpão** — mudou o endereço de saída, ampliou a área de atendimento, percebeu que o pino estava torto? É só abrir o galpão e corrigir. A partir da correção, os próximos cálculos de frete já partem do ponto novo.

{% hint style="info" %}
O conceito de **raio de atendimento** (a área que um galpão cobre) é o mesmo dos seus próprios galpões. Se quiser entender melhor como o raio define o alcance de uma origem, veja [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md).
{% endhint %}

## O recebedor: para onde vai o repasse {#recebedor}

Para **receber** a parte dele, o parceiro precisa cadastrar os **próprios dados bancários** — o que o LocFlow chama de **recebedor**. É o mesmo tipo de cadastro que você usa para receber pagamentos online (explicado em [Pagamento online](../cobranca/pagamento-online.md)), só que aqui ele é do parceiro.

{% hint style="warning" %}
**Sem recebedor, não há repasse.** O parceiro pode até executar a logística, mas a parte dele **só é paga** quando os dados bancários dele estão cadastrados e aprovados. É o recebedor que diz ao LocFlow **para onde** mandar o repasse. Deixe esse passo pronto cedo, para o dinheiro não ficar parado.
{% endhint %}

## O acordo: como o repasse é combinado {#o-acordo}

Convidar o parceiro, ter o galpão certo e o recebedor pronto é **preparar o acesso**. A outra metade é **combinar quanto ele recebe** — o **acordo**. É o acordo que define a parte do parceiro em cada pedido repassado e como os valores se dividem quando o cliente paga.

Como esse combinado (a proposta, o aceite das duas partes e a divisão automática no pagamento) tem uma página só para ele, não vamos repetir aqui:

{% hint style="info" %}
Entenda a fundo como o repasse é **combinado, aceito e dividido** em [Acordos de parceria](acordos-de-parceria.md). Lá você vê o vai e volta de aceite entre as duas partes e como cada parcela recebida é repartida automaticamente.
{% endhint %}

## Situações reais {#situacoes-reais}

- **"Fechei um aluguel em outra cidade e não tenho frota lá."** Convide um Parceiro Logístico Externo daquela região, repasse o pedido e deixe que ele rode a entrega e a retirada a partir do galpão dele.
- **"O frete que o parceiro cobrou veio estranho."** Quase sempre é o **pino do galpão** dele fora do lugar. Abra o galpão, arraste o pino para o ponto exato e confira o raio de atendimento.
- **"O parceiro executou tudo, mas não recebeu."** Falta o **recebedor**: os dados bancários dele precisam estar cadastrados e aprovados para o repasse acontecer.
- **"Só quero alguém para transportar, sem dividir ganhos."** Então o seu caso é um [fornecedor de frete](fornecedores-de-frete.md), não um parceiro externo — você cadastra e opera por ele, sem convite nem login.

## Próximo passo {#proximo-passo}

- [Acordos de parceria](acordos-de-parceria.md) — como o repasse é combinado, aceito e dividido.
- [Fornecedores de frete](fornecedores-de-frete.md) — a outra forma de parceria: transporte terceirizado que **você** opera.
- [Parcerias: a visão](visao-geral.md) — o panorama de como as parcerias se encaixam.
- [Aceitando um convite](../primeiros-passos/aceitando-um-convite.md) — o passo a passo que o parceiro segue para entrar.
- [Pagamento online](../cobranca/pagamento-online.md) — o cadastro de recebedor, que também vale para o repasse do parceiro.
- [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md) — o conceito de raio de atendimento de uma origem.

{% hint style="info" %}
**Dica de ouro:** antes de repassar o primeiro pedido, **confira o pino do galpão do parceiro no mapa**. É esse ponto — e não o endereço digitado — que define a origem do frete. Um minuto ajustando o pino é o que garante um frete justo para você, para o parceiro e para o cliente.
{% endhint %}
