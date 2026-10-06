---
icon: boxes-stacked
description: O que cada número do estoque quer dizer — disponível, reservado, no local, com o cliente e ao todo —, o estoque sem cadastro e como prever quanto vai sobrar numa data futura.
---

# O estoque de agora e a previsão

Duas perguntas diferentes rondam a cabeça de quem aluga [bens móveis](../primeiros-passos/glossario.md): **"quanto eu tenho AGORA no galpão?"** e **"quanto vai sobrar no dia do evento do cliente?"**. O LocFlow responde as duas — e é importante não confundi-las.

- **Agora** = o estoque **real deste momento**: o que está na prateleira, pronto para sair. É assim que o [Painel de Estoque](painel.md) abre.
- **Previsão** = quanto vai sobrar **num período futuro**, já descontando o que outros pedidos seguram. É o mesmo painel, com um período escolhido.
- **Estoque planejado** = o que aparece **quando você monta um orçamento**. Ele olha só a janela daquele evento e desconta as reservas de outros pedidos nela.

{% hint style="info" %}
Regra de ouro: o **agora** conta o que existe hoje; a **previsão** e o **orçamento** projetam o que estará livre na data. Um item pode estar "no galpão agora" e mesmo assim **não** estar disponível para o sábado que vem, porque já foi prometido a outro cliente.
{% endhint %}

## O estoque de agora {#agora}

O estoque de agora aparece em três lugares do [Painel de Estoque](painel.md): no número grande da **Visão geral** (*Na prateleira agora*) e na linha de fatos logo abaixo dele; nas colunas da lista de **Itens**; e nos números da **ficha** de cada item.

{% hint style="info" %}
**Procurando a antiga tela "Posição"?** Ela virou a seção **Itens** do Painel de Estoque — com aluguel e venda na mesma lista, separados pelo filtro **Aluguel ou venda**.
{% endhint %}

### O que cada número quer dizer

| Número | O que é |
| --- | --- |
| **Disponível** | O que você pode **prometer agora**: está no galpão, não tem dono, não está na bancada e não está em observação. |
| **Reservado** | O que **já tem dono**: pedidos ganhos seguram o material para a data deles. Continua no galpão — por isso conta no local. |
| **Em reparo** | O que saiu para manutenção ou lavagem e volta quando o reparo for concluído. A bancada quase sempre fica no próprio galpão, então conta no local. |
| **Em quarentena** | O que saiu da bancada avaliado, mas ainda espera alguém decidir o destino. Está separado, não removido. Veja [Quarentena](quarentena.md). |
| **No local** | O que você encontraria **contando o galpão a pé, agora**: o disponível, o reservado, o que está na bancada e o que está em quarentena. |
| **Com o cliente** | O que saiu para um aluguel e **ainda não voltou**. Continua sendo seu, mas não está aqui. |
| **Físico** (o "ao todo") | O **parque inteiro**: o que está no local mais o que está na rua. Ele não muda quando o material sai para uma entrega — só quando entra ou sai do seu patrimônio. |

As contas, do jeito que o app mostra na ajuda:

```
no local   = disponível + reservado + em reparo + em quarentena
físico     = no local + com o cliente
disponível = no local − reservado − em reparo − em quarentena
```

{% hint style="success" %}
**Situação real.** A Maria tem **2.054** cadeiras no parque e **1.217** estão em eventos. A linha de fatos do painel diz *"… 837 no local · 1.217 com o cliente · 2.054 ao todo"* — os 837 são exatamente o que ela encontraria se fosse contar o galpão agora. O número grande, o **disponível**, é um pouco menor: dos 837, ainda saem as reservadas e o que está na bancada.
{% endhint %}

"Em reparo" e "Em quarentena" só aparecem para quem tem acesso a manutenção e quarentena. Sem esse acesso, a tela não mostra um zero que ninguém saberia interpretar.

### Aluguel e venda são dois estoques {#aluguel-e-venda}

O mesmo galpão guarda duas coisas diferentes:

- O material de **aluguel** sai e **volta** — por isso tem reserva, data de retorno e previsão de sobra.
- O de **venda** sai e **não volta**: quando a entrega acontece, aquelas unidades saem do estoque para sempre. Na venda, o material ainda se separa por **condição** — **novo**, **seminovo** e **usado** são estoques distintos do mesmo produto.

Por isso o gráfico de disponibilidade fala só de aluguel. Para a venda, a pergunta é outra — *quanto tenho e quanto já saiu* — e ela se responde na lista de **Itens** (filtrando por venda e pela condição) e nas **Movimentações** (filtro **Vendas**). Veja também [Locação e venda](../conceitos/locacao-e-venda.md).

Ter estoque de aluguel **não exige** preço de aluguel no cadastro: a ficha da peça que só acompanha kits explica em qual kit ela é usada — e, quando a ficha pergunta em qual estoque você quer operar, aquele estoque aparece com o selo **sem preço avulso**.

## Estoque sem cadastro {#sem-cadastro}

Um estoque fica **sem cadastro** quando está **zerado e nunca teve uma entrada registrada** — o produto existe no catálogo, mas o sistema não tem como saber quantos você tem. Nesse caso o painel não inventa um número:

* o cartão **Sem estoque cadastrado**, na Visão geral, diz quantos produtos estão assim, com o lembrete *"Registre a entrada"*;
* na lista de Itens, a linha ganha o selo **sem cadastro** (âmbar), e o filtro **Sem cadastro** mostra só esses;
* **Disponível** e **Físico** aparecem como **?**, e o produto fica de fora dos totais.

**Ter material já basta para o estoque contar.** Uma conferência de contagem ou uma reclassificação que põe unidades naquele estoque também o tornam "cadastrado" — mesmo sem uma entrada registrada. O aviso existe só para o estoque realmente vazio.

**Para resolver**, registre a entrada do produto: em **Operar › Registrar entrada** ou pelo atalho **Registrar entrada** do cadastro do produto. Veja [Registrar entrada](operacoes-de-estoque.md#registrar-entrada).

{% hint style="warning" %}
**Contagem não forma patrimônio.** O estoque que nasceu de uma contagem passa a valer em unidades, mas fica sem **valor de compra** — e o [Patrimônio](patrimonio.md) só soma o que entrou com custo. Para o seu material aparecer com valor, registre a entrada.
{% endhint %}

{% hint style="info" %}
**No orçamento, a mesma régua.** O carrinho só diz que o estoque de um kit não está cadastrado quando algum item do kit realmente não está. E, quando o app não consegue ler o estoque — sem internet, ou para quem vende sem permissão de ver estoque —, a linha diz **Estoque não lido**, sem acusar falta de cadastro e sem impedir o salvar: quem decide se falta material é o sistema, na hora de gravar.
{% endhint %}

## Prever {#prever}

Quer saber **quanto de um item vai sobrar num período futuro** sem abrir um orçamento? No topo do Painel de Estoque, toque no recorte de tempo — ele mostra **Agora**. A folha **"De quando estamos falando?"** oferece:

| Opção | O que mostra |
| --- | --- |
| **Agora** | O que está na prateleira neste momento, pronto para sair — o padrão |
| **Próximos 14 dias** | Previsão: desconta o que já está prometido nas duas semanas seguintes |
| **Previsão para um período** | A data de entrega até a de retorno, com a **hora da entrega** e a **hora do retorno** — depois, toque em **Usar …** |

{% hint style="info" %}
**A hora conta.** Uma locação ocupa das 8h de um dia às 18h de outro. Informar os horários evita conflito entre dois pedidos que só se cruzam no papel.
{% endhint %}

Com o período escolhido, o painel entra em modo previsão e **avisa isso**: a faixa *"Previsão para …"* com **Ver agora**, o selo **PREVISÃO** no número grande (que passa a ser **Livre no período**) e a coluna **Livre na janela** no lugar de Disponível. O recorte **Prometido a mais**, na lista de Itens, mostra o que já foi prometido além do que existe naquela janela — é o caso em que alguém vai ficar sem material.

### A curva de disponibilidade

Na Visão geral, o bloco **Disponibilidade na janela · aluguel** desenha quanto sobra **em cada dia** do período escolhido (no **Agora**, só o dia de hoje):

- Por padrão a curva soma **todos os itens** do galpão. Escolha **um produto** para ver só a linha dele.
- Cada dia mostra quanto está **livre**, quanto já tem **dono** e o **total** do parque.
- A linha tracejada é o **apto** — o disponível mais o reservado, o teto do que dá para prometer naquele dia. Ela não conta a bancada nem a quarentena.
- Escolhendo **dois ou mais produtos**, o gráfico vira uma **grade**: um item por linha, um dia por coluna, cada item com a sua própria régua. Quanto mais escura a célula, mais daquele item já está comprometido; a célula com um **traço** no meio é o extremo — não sobra nenhuma unidade. O gargalo fica no topo.

**O dia mais apertado da janela é o que manda.** A curva é desenhada por dia: um dia ocupado por poucas horas aparece como ocupado — melhor sobrar cautela do que prometer demais.

### Quem está segurando {#quem-esta-segurando}

A curva diz **quanto** sobra; ela não diz **de quem** é o compromisso. Para isso, toque em **Quem está segurando**, ao lado do gráfico. A mesma folha aparece no orçamento, quando você confere a disponibilidade de um item do carrinho.

Cada produto vem num cartão com:

- o veredito — **Tem folga**, **Apertado**, **No limite** ou **Descoberto**;
- a barra de ocupação e o número — *"280 comprometidas de 300"*, com *"faltam N"* quando passa do que existe;
- o dia do aperto — *"Aperto em 12/10"*, o dia em que mais material está ocupado ao mesmo tempo;
- a lista de quem segura, cada um com a quantidade e o período (*14/09 → 18/09*). Toque no código de um orçamento para abri-lo na hora. **Manutenção programada** é material na bancada; **Reserva de parceria** é material reservado para uma operação de parceria.

{% hint style="info" %}
**O período vai da entrega até a liberação** — o retorno **mais** o preparo. O preparo é o que você definiu no cadastro do produto, no cartão **Manutenção e giro** (*Precisa de preparo no retorno?* e o tempo de preparo), ou, para produtos sem tempo próprio, o **Tempo mínimo de preparo** do Motor de Estoque. Por isso a previsão pode ser mais conservadora que a simples data de devolução: ela protege você de prometer um item que ainda estará sendo revisado.
{% endhint %}

A previsão **não** é o mesmo número que aparece ao montar um orçamento: lá o cálculo olha a **janela de bloqueio** daquele evento — veja [Galpões e disponibilidade](galpoes-e-disponibilidade.md).

{% hint style="success" %}
**Por que isso te faz faturar mais:** com a previsão, você responde "consigo atender o dia 20?" em segundos, olhando exatamente **quais pedidos** disputam o item — sem planilha, sem achismo e sem prometer o que não tem.
{% endhint %}

## Cada movimentação, em detalhe {#movimentacoes}

O número responde **"quanto"**. Para responder **"o que aconteceu e por quê"**, o LocFlow guarda toda entrada e toda saída num histórico de movimentações — na seção **Movimentações** do painel, ou no histórico dentro da ficha de cada item. Toque em qualquer linha para abrir o registro completo:

- **o que mudou** — quanto entrou ou saiu, e em qual estoque (aluguel, ou venda numa condição);
- **em qual galpão** aconteceu;
- **quando aconteceu** de fato e, se o lançamento foi feito depois (um registro retroativo), **quando foi registrado**;
- **o motivo**;
- **quem registrou**;
- o **custo de aquisição** do lote (nas entradas) ou a **receita da venda** (nas vendas), quando existem;
- **de onde ela veio** — avaria, conferência de retorno, descarte na manutenção, logística, ajuste de contagem, entre outras origens;
- um atalho para abrir o **orçamento envolvido**, quando a movimentação pertence a um.

{% hint style="info" %}
**Movimentações antigas mostram "—".** Motivo e responsável só existem a partir do momento em que o LocFlow passou a registrá-los. Uma movimentação anterior a isso mostra um travessão nesses dois campos — o sistema prefere admitir que não sabe a inventar um nome.
{% endhint %}

Direto na **ficha do item**, o bloco **Operar em …** oferece as operações daquele estoque — entre elas **Dar baixa**, **Reclassificar** e **Registrar saída** —, e cada uma abre com o galpão e o tipo de estoque daquele item já preenchidos. Veja [Operações de estoque](operacoes-de-estoque.md).

{% hint style="info" %}
Uma movimentação de descarte ou reclassificação vinda do reparo de um item aparece aqui do mesmo jeito que qualquer outra. Veja o ciclo completo em [Manutenção: o desfecho do reparo](manutencao.md).
{% endhint %}

## Próximo passo

Conheça o painel inteiro em [Painel de Estoque](painel.md), entenda a regra que protege contra reserva dupla em [Galpões e disponibilidade](galpoes-e-disponibilidade.md), o que acontece quando um item volta do conserto em [Manutenção: o desfecho do reparo](manutencao.md) e como o pedido caminha em [O ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md). Em dúvida sobre um termo? Consulte o [Glossário](../primeiros-passos/glossario.md).
