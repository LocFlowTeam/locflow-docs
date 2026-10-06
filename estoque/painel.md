---
icon: table-columns
description: O Painel de Estoque por dentro — as quatro seções, o recorte de tempo que abre no agora, a ficha do item e onde ficam as operações.
---

# Painel de Estoque

O **Painel de Estoque** responde, em poucos segundos, a pergunta que todo locador faz antes de prometer um item: **quanto eu tenho e o que está travado?** Ele fica em **Estoque › Painel de Estoque**.

É **um painel, não catorze telas**. Antes, cada pergunta pedia uma tela diferente — disponibilidade numa, reparo em outra, valor numa terceira. Agora o painel responde primeiro, e as operações (registrar entrada, conferir contagem, dar baixa…) viram **ações a partir do item**, não destinos que você precisa procurar.

{% hint style="info" %}
**Quem vê o quê.** O painel aparece para quem tem qualquer permissão de estoque — consulta, operação ou patrimônio. O número principal é sempre em **unidades**; valor em reais só aparece para quem tem acesso ao patrimônio. E o botão **Operar** só existe para quem pode mexer no estoque (quem só consulta não vê um botão apagado: ele simplesmente não aparece).
{% endhint %}

## As quatro seções

| Seção | A pergunta que ela responde |
| --- | --- |
| **Visão geral** | Quanto tenho e o que está travado |
| **Itens** | Busca, lotes e ficha do produto |
| **Movimentações** | Tudo que entrou e saiu |
| **Patrimônio** | Quanto vale o seu material — só para quem tem acesso ao patrimônio. Veja [Patrimônio](patrimonio.md) |

No celular, toque no **título do topo** para trocar de seção. Em telas largas, as seções viram **abas**: as de operação à esquerda e o **Patrimônio**, separado sob o rótulo **Análise**, à direita — o mesmo jeito do financeiro.

## A barra do topo

| Controle | O que faz |
| --- | --- |
| **Agora** (o recorte de tempo) | Diz **de quando** os números falam. Abre sempre no **Agora**; tocando, você pede uma previsão. Aparece na Visão geral e em Itens |
| **Locais** | Um chip **Todos** e um chip por galpão — e por loja com estoque próprio, com o ícone de loja. Só aparece quando você tem mais de um local |
| **Olho** | Esconde os valores em reais, para abrir o painel na frente de alguém |
| **Operar** (no celular, o botão **+**) | Abre **Nova operação**, com as oito operações de estoque e, embaixo, **Cadastro e regras**: Galpões, Lojas e Regras de estoque |

## O painel abre no agora

Ao abrir, o painel mostra o que está **na prateleira neste momento, pronto para sair**. Para saber quanto vai sobrar numa data futura, toque no recorte de tempo e escolha **Próximos 14 dias** ou uma **Previsão para um período**.

A partir daí a tela **avisa que mudou de assunto**, para ninguém confundir previsão com inventário:

* uma faixa acima do conteúdo diz **"Previsão para …"** e explica: *"Os números abaixo já descontam o que está prometido nesse período — não são o que está na prateleira agora."* — com o botão **Ver agora** para voltar num toque;
* o número grande ganha o selo **PREVISÃO**, com as datas logo abaixo;
* o recorte deixa de dizer **Agora** e passa a dizer, destacado, algo como **Previsão · 15/09 08:00 → 28/09 18:00**.

{% hint style="warning" %}
**Por que o painel não abre mais numa previsão.** Quando ele abria já descontando as duas semanas seguintes, quem olhava via um estoque menor do que o da prateleira e concluía que estava faltando material. Previsão é uma pergunta que você faz de propósito — por isso ela agora se anuncia. Como ler a previsão está em [O estoque de agora e a previsão](posicao-e-previsao.md#prever).
{% endhint %}

## Visão geral

A resposta de cinco segundos, de cima para baixo.

### Indicadores

1. **Na prateleira agora** — o número grande: as unidades **disponíveis**, que dá para prometer já (822, no exemplo abaixo). Numa previsão ele vira **Livre no período**: o dia mais apertado da janela escolhida.
2. **A linha de fatos**, logo abaixo do número — o inventário de agora, por exemplo:

   > *12 reservadas · 3 em reparo · 837 no local · 1.217 com o cliente · 2.054 ao todo*

   As reservadas e o "no local" aparecem sempre; as outras partes, só quando há material nelas: sem nada na bancada, "em reparo" some; sem nada na rua, o "no local" já é o parque inteiro, e "com o cliente" e "ao todo" não aparecem.
3. **Em reparo** — para quem tem acesso à manutenção: quantas unidades estão na bancada e quantas ordens estão abertas (e quantas estão paradas há mais de 15 dias). Toque para ver esses itens.
4. **Sem estoque cadastrado** — quantos produtos ainda não têm estoque, com o lembrete *"Registre a entrada"*. Toque para ver quais são. Veja [Estoque sem cadastro](posicao-e-previsao.md#sem-cadastro).
5. **Patrimônio** — só para quem tem acesso: o valor de hoje e quanto custaria repor tudo.

A faixa de indicadores pode ser **recolhida**. Recolhida, ela vira uma linha de resumo (*"822 disponíveis · 12 reservadas · 837 no local"*), e a sua escolha fica guardada no aparelho.

{% hint style="info" %}
**O que cada número quer dizer** — disponível, reservado, em reparo, em quarentena, no local, com o cliente e ao todo — está explicado, com as contas, em [O estoque de agora e a previsão](posicao-e-previsao.md#agora).
{% endhint %}

### Disponibilidade na janela · aluguel

O gráfico de quanto sobra **em cada dia** do período, já descontando as reservas. Ele fala só de **aluguel**, porque o material de venda sai e não volta, e segue o recorte do topo: no **Agora** ele mostra só o dia de hoje; escolha **Próximos 14 dias** ou um período para ver os dias seguintes. Ali você:

* escolhe **um produto** para ver a linha só dele — ou **dois ou mais**, e o gráfico vira uma **grade** com um item por linha e um dia por coluna;
* toca em **Quem está segurando** para ver **quais pedidos** ocupam o material naquele período.

O passo a passo está em [Prever](posicao-e-previsao.md#prever).

### Últimas movimentações

As entradas e saídas mais recentes, com **Ver todas** para abrir a seção Movimentações. No fim da Visão geral, **Ver os N produtos deste galpão** leva à lista de Itens.

## Itens

A lista de produtos do local escolhido — foi aqui que a antiga tela **Posição** foi parar.

* **Busca** por nome do produto e **Ordenar** por nome, disponível ou reservado.
* **Filtros**, todos de escolha múltipla:

| Filtro | Opções |
| --- | --- |
| **Situação** | Disponível, Reservado, Em reparo, Em quarentena, Esgotado, Prometido a mais, Sem cadastro |
| **Aluguel ou venda** | Aluguel, Venda — aparece quando você trabalha com os dois |
| **Condição (venda)** | Novo, Seminovo, Usado |
| **Categoria**, subcategoria e marca | As do seu catálogo |

Filtrando por **aluguel ou venda** (ou pela condição), os números de cada linha passam a ser **só daquele estoque**, e a tela avisa isso logo acima da lista.

* **Colunas** (em telas largas): **Disponível**, **Com o cliente**, **Reservado**, **Em reparo**, **Quarentena** e **No local** aparecem de saída; **Prometido a mais**, **Físico**, **Tipo de negócio** e **Locais** você liga quando precisar.
* **Selos** que só aparecem na exceção: **sem cadastro** (âmbar), **prometido a mais** (vermelho — já se prometeu mais do que existe naquela janela) e **esgotado**.
* **Caixinhas** em cada linha, para conferir a contagem, mandar para o reparo ou transferir até 25 itens de uma vez. Veja [Operar vários itens de uma vez](operar-varios-itens.md).

### A ficha do item

Toque num produto para abrir a ficha dele.

1. **Em qual estoque?** Quando o produto está em mais de um lugar — dois galpões, ou aluguel e venda no mesmo galpão —, a ficha pergunta primeiro **qual deles** você quer ver. Cada opção mostra o livre, o total e o que está na rua, na bancada ou em quarentena. No rodapé, uma linha soma tudo: *"Ao todo: 60 un em 3 estoques"*. Com um estoque só, a ficha não pergunta nada.
2. **Os números daquele estoque** — disponível (na venda, *À venda*), reservado, em reparo, no local e físico; e, quando houver, em quarentena e com o cliente.
3. **Operar em …** — as operações daquele estoque, já com o local e o tipo de estoque preenchidos. Veja [Operações de estoque](operacoes-de-estoque.md).
4. **Histórico** — as movimentações recentes daquele estoque.

{% hint style="info" %}
**"sem preço avulso".** Uma peça que só acompanha kits — o parafuso da mesa, a cadeira do conjunto — pode ter estoque de aluguel sem ter preço de aluguel no cadastro, porque o kit que a usa é alugado. A ficha explica o caso, por exemplo: *"Sem preço de aluguel avulso — usado no kit Mesa redonda 1.60D, que é alugado."* Não é pendência: onde o material fica separado é um fato do galpão; o preço é o que o cliente vê no catálogo.
{% endhint %}

## Movimentações

Tudo que entrou e saiu, com filtros por **Entradas**, **Vendas**, **Ajustes**, **Avarias e baixas**, **Transferências**, **Reclassificações**, **Reparo** e **Conferência**. Toque numa linha para abrir o registro completo — o que cada movimentação guarda está em [Cada movimentação, em detalhe](posicao-e-previsao.md#movimentacoes).

## Patrimônio

Quanto vale o material: o **valor hoje**, que considera o desgaste, e o **valor para repor**. Veja [Patrimônio](patrimonio.md).

## O que mora fora do painel

* **Galpões** e **Lojas** são cadastros — ficam no menu **Estoque** (e também em **Operar › Cadastro e regras**). Veja [Galpões e disponibilidade](galpoes-e-disponibilidade.md) e [Lojas](lojas.md).
* **Regras de estoque** é política — mora no Motor de Estoque, em **Ajustes › Motores**.
* **Transferências**, **Conferência**, **Manutenção** e **Quarentena** são **filas de trabalho** e têm tela própria no menu Estoque. Veja [Transferências](transferencias.md), [Manutenção](manutencao.md) e [Quarentena](quarentena.md).

{% hint style="info" %}
**Não achou um item no menu?** Algumas telas ficam guardadas quando não fazem parte da sua operação ou quando a fila está vazia — Manutenção e Quarentena, por exemplo, só aparecem quando há algo esperando. Para mostrar um item mesmo assim, use **Personalizar** no menu.
{% endhint %}

{% hint style="success" %}
**Por que isso te faz faturar mais:** com o estoque inteiro numa tela só, você responde "tenho para o dia 20?" sem abrir três telas e sem planilha — e enxerga, no mesmo lugar, o material parado na bancada que poderia estar alugado.
{% endhint %}

## Próximo passo

Entenda cada número e a previsão em [O estoque de agora e a previsão](posicao-e-previsao.md), aprenda as operações em [Operações de estoque](operacoes-de-estoque.md) e veja quanto vale o seu material em [Patrimônio](patrimonio.md). Em dúvida sobre um termo? Consulte o [Glossário](../primeiros-passos/glossario.md).
