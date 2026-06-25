---
icon: truck
description: O card de Logística no painel resume sua operação física em três pilhas — o que precisa sair, voltar e o que está travado por falta de informação.
---

# O card de Logística no painel

No [painel](o-painel.md), o card de **Logística** é um espelho rápido do **chão da sua operação**: o que precisa sair do galpão, o que precisa voltar e o que está **travado por falta de um dado**. Ele não fala de dinheiro nem de chance de fechar — isso é assunto dos cards de funil e faturamento. Aqui é só a **lista de tarefas físicas**.

{% hint style="info" %}
A ajuda dentro do próprio card resume assim: *"A Logística é a sua lista de tarefas do galpão — o que carregar, levar, buscar e guardar. Não fala de dinheiro nem de chance de fechar: é o chão da operação."*
{% endhint %}

A ideia é você bater o olho no painel e saber, sem abrir nada, **se a operação está em dia ou se tem algo te esperando**. Quando está tudo certo, o card mostra apenas: **"Nada pendente — operação em dia."**

## As três pilhas <a href="#as-tres-pilhas" id="as-tres-pilhas"></a>

Todo movimento ainda **não concluído** dos seus pedidos cai em **uma** destas três pilhas:

| Pilha | O que reúne | Cor |
| --- | --- | --- |
| **Pendente de informação** | Movimentos que **ainda não dá para montar** porque falta um dado. | Âmbar (destaque) |
| **Precisa sair** | Entregas — material que **deixa o galpão** e vai ao cliente. | Roxo |
| **Precisa voltar** | Retiradas e devoluções — material que **retorna** ao galpão (só na [locação](../primeiros-passos/glossario.md)). | Roxo |

Cada pilha mostra **quantos** itens tem e uma **prévia dos mais urgentes** (os primeiros da fila, ordenados por data). Se houver mais do que cabe na prévia, aparece um **"+N mais"** — o restante você vê no [acompanhamento de roteiros](../logistica/acompanhando-roteiros.md).

{% hint style="success" %}
A pilha **Pendente** só aparece **quando há algo pendente** — e, quando aparece, vem **em primeiro lugar**. Sem pendências, o card já começa direto pelo "Precisa sair / Precisa voltar". É uma lista de **fazer e desbloquear**, não um relatório de desempenho: por isso não tem "% concluído".
{% endhint %}

### Precisa sair, precisa voltar <a href="#precisa-sair-precisa-voltar" id="precisa-sair-precisa-voltar"></a>

Essas duas pilhas são a operação normal, sem nenhum problema pendente:

* **Precisa sair** são as **entregas**: o que a equipe carrega e leva (ou que o cliente vem buscar). É o material saindo.
* **Precisa voltar** são as **retiradas e devoluções**: o que a equipe vai buscar de volta (ou que o cliente devolve). É o material retornando — só existe em locação, já que na venda o item não volta.

Cada linha mostra o **código do pedido**, o **cliente** e o **selo de papel** (Rota ou Balcão — veja [abaixo](#selo-rota-balcao)). Os mais próximos da data vêm primeiro, para você priorizar o que é para já.

### Pendente de informação <a href="#pendente-de-informacao" id="pendente-de-informacao"></a>

Esta é a pilha mais importante do card — e por isso fica em **âmbar** e na frente. Ela junta os movimentos que estão **bloqueados por falta de um dado**: enquanto a informação não chega, você **não consegue montar a rota nem avisar o cliente**.

{% hint style="info" %}
A ajuda do card descreve esta pilha como *"o coração do bloco: itens bloqueados por falta de um dado"* — *"Enquanto esses dados não chegam, você não consegue montar a rota nem avisar o cliente. Por isso aparecem em destaque (âmbar) e em primeiro lugar — são o que alguém precisa resolver agora."*
{% endhint %}

Um pedido entra aqui quando, mesmo já **ganho**, ainda falta algo para virar uma operação real. As pendências possíveis, com a etiqueta que aparece em cada item:

| Etiqueta | O que está faltando | Onde resolver |
| --- | --- | --- |
| **Sem horário** | O movimento ainda **não tem janela** (data/horário) combinada — está preso a "o dia do evento" ou "algum dia", sem hora. | No [orçamento: movimentos e janelas](../orcamentos/movimentos-e-janelas.md). |
| **Sem responsável** | Ainda **não foi definido quem transporta** — sua equipe leva, ou o cliente vem ao galpão? | No movimento do orçamento. |
| **Sem endereço** | A equipe transporta, mas **falta o endereço de destino**. | No [endereço do orçamento](../orcamentos/enderecos.md). |

Um mesmo item pode ter **mais de uma** etiqueta ao mesmo tempo (por exemplo, sem horário **e** sem responsável). Resolvido o que falta, ele **sai da pilha âmbar** sozinho e passa para "Precisa sair" ou "Precisa voltar".

{% hint style="warning" %}
A pendência **"Sem endereço"** depende de dados que nem sempre chegam ao painel hoje — em parte da operação, esse aviso pode **não aparecer** no card mesmo quando o endereço falta. As pendências de **horário** e **responsável** são as que você verá com mais frequência. *(Em ajuste — veja as notas de revisão.)*
{% endhint %}

> **"Pendente de informação" é diferente de "pendente de aprovação".** No card de Logística, pendente quer dizer *falta um dado para operar*. Já a aprovação de um orçamento (aguardando alguém aprovar antes de virar negócio) é outra coisa, do mundo comercial — veja [Aprovação de orçamentos](../orcamentos/aprovacao.md).

## O selo de papel: Rota ou Balcão <a href="#selo-rota-balcao" id="selo-rota-balcao"></a>

Cada movimento das pilhas "Precisa sair" e "Precisa voltar" traz um **selo de papel** que responde a uma pergunta simples: **quem se desloca?**

* **Rota** (ícone de caminhão): **sua equipe** monta a rota e leva ou busca o material no endereço do cliente.
* **Balcão** (ícone de loja): **o cliente vem até o galpão** — ele retira ou devolve no balcão, sem viagem da sua parte.

{% hint style="info" %}
A ajuda do card: *"O selo de papel diz quem faz: Rota (sua equipe monta a rota) ou Balcão (cliente vem ao galpão). Isso muda o que planejar, não a pilha."*
{% endhint %}

O selo **não muda a pilha** — uma entrega continua em "Precisa sair" seja ela Rota ou Balcão. Ele muda **o que você precisa preparar**: um item de **Rota** pede endereço e roteiro; um de **Balcão** dispensa trajeto, basta ter o galpão e a data certos. É o mesmo conceito de "retira/devolve no balcão" que você define no [movimento do orçamento](../orcamentos/movimentos-e-janelas.md), que aparece com mais detalhe na [jornada do pedido](../logistica/jornada-do-pedido.md) e que tem sua própria fila em [Balcão: retirada e devolução no galpão](../logistica/balcao.md).

## Como ler o card, da esquerda para a direita <a href="#como-ler-o-card" id="como-ler-o-card"></a>

```mermaid
flowchart LR
    A[Pendente de informação<br/>âmbar - só se houver] --> B[Precisa sair<br/>entregas]
    B --> C[Precisa voltar<br/>retiradas e devoluções]
```

1. **Tem âmbar?** Comece por aí — são os bloqueios que só você (ou alguém combinando com o cliente) destrava.
2. **Precisa sair** mostra o que está pronto para a rua, do mais urgente para o menos.
3. **Precisa voltar** mostra o que tem de retornar — fique de olho nas datas para não deixar item parado no cliente.

Para agir de fato, abra o **[acompanhamento de roteiros](../logistica/acompanhando-roteiros.md)**: o card resume, e a tela de roteiros é onde você planeja, separa e executa.

## De onde vem o dado <a href="#de-onde-vem-o-dado" id="de-onde-vem-o-dado"></a>

{% hint style="success" %}
**Estes números são reais.** O card de Logística lê os **seus orçamentos ganhos** e seus movimentos diretamente da operação (a mesma fonte do calendário logístico). Não há valores de exemplo aqui: o que você vê é o que está de fato na sua fila. Se o card não carregar, ele avisa em vez de inventar números.
{% endhint %}

O card aparece de acordo com a sua **permissão de logística** e com o seu plano. Quem ainda não usa logística não vê o card poluindo o painel; conforme a operação cresce, ele entra para organizar o galpão sem que você precise de planilha à parte — a [filosofia do LocFlow](../primeiros-passos/filosofia.md) de **abstrair para o pequeno e escalar para o grande**.

## Situações reais

* **"Bati o olho e tinha um item âmbar 'Sem horário'."** Aquela entrega foi ganha, mas ninguém combinou a janela com o cliente. Abra o orçamento, defina o horário, e o item migra para "Precisa sair" — pronto para entrar num roteiro.
* **"Vejo 4 em 'Precisa voltar' e nenhuma pendência."** Sua operação está fluindo: são quatro devoluções a buscar (ou que o cliente devolve no balcão). Priorize pela data e organize a coleta.
* **"O card diz 'operação em dia', mas eu sei que tenho entregas amanhã."** Itens **já concluídos** não entram nas pilhas. Se uma entrega de amanhã não aparece, confira se ela não foi marcada como executada antes da hora.

## Para quem quer os números <a href="#para-quem-quer-os-numeros" id="para-quem-quer-os-numeros"></a>

A classificação é **determinística** — sem estatística, sem chance de fechamento. Para cada movimento ainda não concluído:

1. **A pendência vem primeiro.** O movimento é marcado **Pendente** se faltar **qualquer** um destes: horário/janela combinada, responsável definido, ou (quando a equipe transporta) endereço de destino. As etiquetas listam **todos** os motivos juntos.
2. **Sem pendência, decide o tipo.** Entrega → **Precisa sair**; retirada/devolução → **Precisa voltar**.
3. **O selo de papel** é à parte: é **Balcão** quando o responsável é "cliente vem ao galpão"; caso contrário, **Rota**.

Dentro de cada pilha, a ordem é por **urgência**: o movimento com a **data projetada mais próxima** vem primeiro; itens **sem data** vão para o fim. A prévia mostra os **3 primeiros** de cada pilha e o restante vira "+N mais".

## Próximo passo

* [Visão geral do painel](o-painel.md)
* [Acompanhando seus roteiros](../logistica/acompanhando-roteiros.md)
* [Visão geral da logística](../logistica/visao-geral.md)
* [Movimentos, janelas e galpão de origem](../orcamentos/movimentos-e-janelas.md)
* [A jornada de um pedido (Ver Logística)](../logistica/jornada-do-pedido.md)
