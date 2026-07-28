---
icon: object-group
description: Como o LocFlow separa as classes que já vêm prontas das que você cria livremente, sugere agrupar especificações com a mesma capacidade e usa a classe como alvo do roteiro.
---

# Classes veiculares

A **classe** é o primeiro nível da [hierarquia da frota](frota.md#classes-e-especificacoes): o nome que agrupa um tipo de veículo, por baixo do qual ficam as [especificações](frota.md#classes-e-especificacoes) (as fichas técnicas) e, por baixo delas, os veículos com placa.

Na lista de classes, o LocFlow separa dois grupos, um embaixo do outro:

| Grupo | O que é | Tipo de veículo (FIPE) |
| --- | --- | --- |
| **Classes padrão** | As duas que já vêm prontas em toda organização — "Carro Utilitário" e "Caminhão" —, ligadas ao catálogo FIPE. Servem de ponto de partida para cadastrar especificações. | Obrigatório |
| **Minhas classes** | As que você cria, livremente. | Opcional |

{% hint style="info" %}
As classes padrão existem para você já começar a cadastrar especificações, sem esperar nada — mas não são as únicas. Assim que você cria a sua primeira classe, ela aparece separada, em "Minhas classes".
{% endhint %}

## Uma classe sua é um agrupamento livre <a href="#agrupamento-livre" id="agrupamento-livre"></a>

Ao criar uma classe própria, só o **nome** é obrigatório (ex.: "Van Furgão", "Minhas picapes"). O **tipo de veículo** — Carros, Caminhões ou Motos, a base do catálogo FIPE — é **opcional**: ele serve só para filtrar marca, modelo e ano na hora de cadastrar uma especificação dentro dela. Uma classe que mistura fichas de tipos diferentes pode ficar sem esse vínculo.

Isso porque a classe não é uma categoria fechada do sistema — é um **agrupamento seu**. Você escolhe o critério:

- pela **capacidade de carga** — juntar as fichas que, na prática, carregam o mesmo tanto (é o caso mais comum, e o LocFlow ajuda a encontrar essas, veja a seguir);
- ou por qualquer outro critério que faça sentido na sua operação — "minhas picapes", "frota da filial 2", o que for prático para sua equipe.

{% hint style="warning" %}
O risco de tratar fichas diferentes como intercambiáveis é seu. Se você juntar numa classe duas especificações com capacidades bem diferentes, o LocFlow avisa na hora de montar o roteiro (veja [mais abaixo](#alvo-do-roteiro)) — mas quem decide o agrupamento é você.
{% endhint %}

## Sugestão automática de agrupamento <a href="#sugestao-automatica" id="sugestao-automatica"></a>

Você não precisa notar sozinho quando duas fichas "dão no mesmo". Ao abrir a lista de classes, o LocFlow compara a **capacidade de carga** de todas as suas especificações — os mesmos limites por item, o mesmo baú (dimensões) e o mesmo peso máximo — ou seja, a conferência de carga daria **o mesmo resultado** para qualquer uma delas. Quando encontra duas ou mais especificações assim, ainda espalhadas em classes diferentes, ele sugere juntá-las numa classe.

A sugestão aparece num cartão no topo da lista, mostrando:

- quantas especificações têm a mesma capacidade, e quais são;
- um resumo da capacidade em comum (ex.: "20 × Cadeira · 8,40 m³");
- em qual (ou quais) classe elas estão hoje.

Basta tocar em **Agrupar numa classe**, dar um nome e confirmar — o LocFlow cria a classe e move as especificações para ela num só passo. Depois de agrupadas (e sozinhas na classe nova), a sugestão não aparece mais para aquele grupo.

{% hint style="info" %}
Especificações de um **fornecedor de frete** (a frota-espelho dele) não entram nessa sugestão — a organização não reorganiza a frota de terceiros. Veja [Detentor](frota.md#detentor).
{% endhint %}

{% hint style="success" %}
**Por que isso te faz faturar mais.** Cada especificação que entra num agrupamento certo vira mais uma opção de veículo na hora de montar o roteiro — sem você ter que decidir manualmente, toda vez, "essa Kombi serve para essa carga?". Menos tempo organizando a frota, mais veículos elegíveis para cada entrega.
{% endhint %}

## A classe como alvo do roteiro <a href="#alvo-do-roteiro" id="alvo-do-roteiro"></a>

Ao [planejar o roteiro](../logistica/planejando-o-roteiro.md), você não precisa escolher a ficha exata — pode escolher a **classe**. Nesse caso, qualquer veículo do grupo serve, e o LocFlow avalia a capacidade da carga pela **capacidade agregada da classe**:

| Situação das especificações da classe | O que o LocFlow faz |
| --- | --- |
| Todas com a **mesma** capacidade | Confere a carga **por inteiro** — tanto faz qual veículo do grupo sai. |
| Capacidades **diferentes** entre si | Confere a carga pela **menor capacidade comum** (o piso), para caber em qualquer veículo do grupo — com um aviso de que foi assim que ele conferiu. |
| Nenhuma especificação com capacidade cadastrada (ou classe sem nenhuma especificação) | Avisa que não dá para conferir a carga — mas **não impede** você de seguir. |

Como em toda a frota, a classe **nunca bloqueia** o roteiro. Veja como as estratégias de contagem e volume funcionam em [Especificações: capacidade](frota-capacidade.md).

## Situações reais <a href="#situacoes-reais" id="situacoes-reais"></a>

- **Três furgões, marcas diferentes, mesmo baú:** você tem um Fiorino, um Kangoo e uma Saveiro furgão, todos com baú de 6 m³ e limite de 15 cadeiras. Na próxima vez que abrir a lista de classes, o LocFlow sugere juntar os três — um toque, você chama a classe de "Furgão 6m³", e as três fichas passam a valer como uma só na hora de montar o roteiro.
- **Agrupamento sem critério técnico:** você tem picapes de portes variados e prefere só chamar todas de "Minhas picapes" para achar rápido na lista. Cria a classe sem tipo FIPE; como as capacidades não batem, o LocFlow não sugere nada ali — mas você monta o grupo à mão mesmo assim.
- **Roteiro por classe, capacidades iguais:** você planeja o roteiro de amanhã escolhendo a classe "Furgão 6m³" em vez de decidir qual dos três furgões vai. Como as três fichas têm a mesma capacidade, o app confere a carga por inteiro, sem aviso.
- **Roteiro por classe, capacidades diferentes:** a classe "Caminhão" ainda tem uma ficha com baú de 20 m³ e outra com 15 m³. Ao escolher a classe no planejamento, o app avisa que vai conferir pela capacidade menor (15 m³) — se a carga do dia for maior que isso, vale a pena conferir qual veículo especificamente sai.

## Próximo passo <a href="#proximo-passo" id="proximo-passo"></a>

Volte para [Frota](frota.md) para ver a hierarquia completa (classe → especificação → veículo) e a escada de cadastro. Para configurar o que cada especificação carrega, veja [Especificações: capacidade](frota-capacidade.md). E para ver a classe em ação na montagem da rota, vá a [Planejando o roteiro](../logistica/planejando-o-roteiro.md).
