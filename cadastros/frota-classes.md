---
icon: object-group
description: Como o LocFlow separa as classes que já vêm prontas das que você cria livremente, dá um titular a cada uma, sugere agrupar especificações com a mesma capacidade e usa a classe como alvo do roteiro.
---

# Classes veiculares

A **classe** é o primeiro nível da [hierarquia da frota](frota.md#classes-e-especificacoes): o nome que agrupa fichas com a mesma capacidade de carga, por baixo do qual ficam as [especificações](frota.md#classes-e-especificacoes) (as fichas técnicas, cada uma com seu tipo de veículo) e, por baixo delas, os veículos com placa.

Na lista de classes, o LocFlow separa dois grupos, um embaixo do outro:

| Grupo | O que é | Titular |
| --- | --- | --- |
| **Classes padrão** | As duas que já vêm prontas em toda organização — "Carro Utilitário" e "Caminhão". Servem de ponto de partida para cadastrar especificações. | Sempre a sua organização |
| **Minhas classes** | As que você cria, livremente, com o critério que fizer mais sentido para o seu negócio. | Você escolhe — [veja abaixo](#o-titular-da-classe) |

{% hint style="info" %}
As classes padrão existem para você já começar a cadastrar especificações, sem esperar nada — mas não são as únicas. Assim que você cria a sua primeira classe, ela aparece separada, em "Minhas classes".
{% endhint %}

## Uma classe sua é um agrupamento livre <a href="#agrupamento-livre" id="agrupamento-livre"></a>

Ao criar uma classe própria, só o **nome** é obrigatório (ex.: "Van Furgão", "Minhas picapes"). Você não escolhe mais aqui se é Carro, Caminhão ou Moto — essa pergunta é feita direto na [ficha de cada modelo](frota.md#classes-e-especificacoes), porque é ali que ela sempre fez mais sentido: uma classe pode agrupar, por exemplo, um utilitário e uma picape que carregam exatamente o mesmo tanto, sem que isso a torne "sem tipo definido".

Isso porque a classe não é uma categoria fechada do sistema — é um **agrupamento seu**. Você escolhe o critério:

- pela **capacidade de carga** — juntar as fichas que, na prática, carregam o mesmo tanto (é o caso mais comum, e o LocFlow ajuda a encontrar essas, veja a seguir);
- ou por qualquer outro critério que faça sentido na sua operação — "minhas picapes", "frota da filial 2", o que for prático para sua equipe.

{% hint style="warning" %}
O risco de tratar fichas diferentes como intercambiáveis é seu. Se você juntar numa classe duas especificações com capacidades bem diferentes, o LocFlow avisa na hora de montar o roteiro (veja [mais abaixo](#alvo-do-roteiro)) — mas quem decide o agrupamento é você.
{% endhint %}

## O titular da classe <a href="#o-titular-da-classe" id="o-titular-da-classe"></a>

Toda classe tem um **titular** — o mesmo dado que já existe em cada [ficha](frota.md#detentor), só que agora também na classe que as agrupa. O titular pode ser:

- **A sua organização** (o caso comum) — é a sua própria frota.
- **Um fornecedor de frete** — quando a classe agrupa fichas de um terceiro que roda para você (a frota-espelho dele).
- **Um parceiro externo** — quando a classe agrupa fichas de um parceiro da [Rede de Parceiros](../parcerias/visao-geral.md).

{% hint style="info" %}
**Todas as fichas de uma classe são do mesmo titular.** Você não consegue juntar, numa classe só, um veículo seu com um veículo de um fornecedor ou de um parceiro — cada titular tem a(s) sua(s) própria(s) classe(s). É essa regra que garante que, ao escolher a classe no roteiro, o LocFlow sempre sabe **quem** vai rodar a viagem, não só **quanto** cabe nela.
{% endhint %}

{% hint style="success" %}
**Por que isso importa para você.** Ao montar um roteiro, escolher a classe responde duas perguntas de uma vez: "quanto cabe" (a capacidade do grupo) e "quem executa e por quanto" (o titular). Antes, cada ficha respondia isso sozinha, uma de cada vez; agora o grupo inteiro responde junto — menos decisão manual a cada viagem.
{% endhint %}

## Sugestão automática de agrupamento <a href="#sugestao-automatica" id="sugestao-automatica"></a>

Você não precisa notar sozinho quando duas fichas "dão no mesmo". Ao abrir a lista de classes, o LocFlow compara a **capacidade de carga** de todas as suas especificações — os mesmos limites por item, o mesmo baú (dimensões) e o mesmo peso máximo — ou seja, a conferência de carga daria **o mesmo resultado** para qualquer uma delas. Quando encontra duas ou mais especificações assim, ainda espalhadas em classes diferentes, ele sugere juntá-las numa classe.

A sugestão aparece num cartão no topo da lista, mostrando:

- quantas especificações têm a mesma capacidade, e quais são;
- um resumo da capacidade em comum (ex.: "20 × Cadeira · 8,40 m³");
- em qual (ou quais) classe elas estão hoje.

Basta tocar em **Agrupar numa classe**, dar um nome e confirmar — o LocFlow cria a classe e move as especificações para ela num só passo. Depois de agrupadas (e sozinhas na classe nova), a sugestão não aparece mais para aquele grupo.

{% hint style="info" %}
Especificações de um **fornecedor de frete** ou de um **parceiro externo** (fichas de outro titular) não entram nessa sugestão — a organização não reorganiza a frota de terceiros, só a própria. Veja [Detentor](frota.md#detentor) e [O titular da classe](#o-titular-da-classe).
{% endhint %}

{% hint style="success" %}
**Por que isso te faz faturar mais.** Cada especificação que entra num agrupamento certo vira mais uma opção de veículo na hora de montar o roteiro — sem você ter que decidir manualmente, toda vez, "essa Kombi serve para essa carga?". Menos tempo organizando a frota, mais veículos elegíveis para cada entrega.
{% endhint %}

## A classe como alvo do roteiro <a href="#alvo-do-roteiro" id="alvo-do-roteiro"></a>

Ao [planejar o roteiro](../logistica/planejando-o-roteiro.md), você não precisa escolher a ficha exata — pode escolher a **classe**. Nesse caso, qualquer veículo do grupo (do mesmo titular) serve, e o LocFlow avalia a capacidade da carga pela **capacidade agregada da classe**, mostrando um destes selos:

| Selo que você vê | Quando aparece | O que o LocFlow faz |
| --- | --- | --- |
| **Capacidade verificada** | Duas ou mais fichas da classe têm a mesma capacidade cadastrada, e nenhuma ficou de fora da comparação. | Confere a carga **por inteiro** — tanto faz qual veículo do grupo sai. |
| **Capacidade verificada — cobertura parcial** | As fichas comparadas batem entre si, mas alguma outra ficha da classe ainda não tem capacidade cadastrada. | Confere pela capacidade em comum das que já têm dado — e avisa da lacuna, para você completar o cadastro das demais. |
| **Capacidade mista — vale a menor** | As fichas da classe têm capacidades diferentes entre si. | Confere pela **menor capacidade do grupo** (o piso), para caber em qualquer veículo dele — com aviso de que foi assim que conferiu. |
| **Uma ficha só** | A classe tem uma única especificação. | Usa a capacidade dessa ficha, mas **não é uma capacidade verificada de verdade** — comparar um veículo com ele mesmo não prova nada. Assim que uma segunda ficha equivalente entrar na classe, o selo passa a "verificada". |
| **Sem capacidade cadastrada** | Nenhuma ficha da classe tem capacidade cadastrada, ou a classe ainda não tem nenhuma ficha. | Avisa que não dá para conferir a carga — mas **não impede** você de seguir. |

Como em toda a frota, a classe **nunca bloqueia** o roteiro. Veja como as estratégias de contagem e volume funcionam em [Especificações: capacidade](frota-capacidade.md).

## Situações reais <a href="#situacoes-reais" id="situacoes-reais"></a>

- **Três furgões, marcas diferentes, mesmo baú:** você tem um Fiorino, um Kangoo e uma Saveiro furgão, todos com baú de 6 m³ e limite de 15 cadeiras. Na próxima vez que abrir a lista de classes, o LocFlow sugere juntar os três — um toque, você chama a classe de "Furgão 6m³", e as três fichas passam a valer como uma só na hora de montar o roteiro.
- **Agrupamento sem critério técnico:** você tem picapes de portes variados e prefere só chamar todas de "Minhas picapes" para achar rápido na lista. Cria a classe só com o nome; como as capacidades não batem, o LocFlow não sugere nada ali — mas você monta o grupo à mão mesmo assim.
- **Roteiro por classe, capacidades iguais:** você planeja o roteiro de amanhã escolhendo a classe "Furgão 6m³" em vez de decidir qual dos três furgões vai. Como as três fichas têm a mesma capacidade, o app confere a carga por inteiro, sem aviso.
- **Roteiro por classe, capacidades diferentes:** a classe "Caminhão" ainda tem uma ficha com baú de 20 m³ e outra com 15 m³. Ao escolher a classe no planejamento, o app avisa que vai conferir pela capacidade menor (15 m³) — se a carga do dia for maior que isso, vale a pena conferir qual veículo especificamente sai.
- **Classe com uma ficha só:** você acabou de cadastrar sua primeira Kombi e ainda não tem outra igual. A classe "Kombi" existe e já pode ser escolhida no roteiro, mas o selo mostra "Uma ficha só" — o LocFlow usa a capacidade dela mesma, só não chama de "verificada" até você ter uma segunda ficha equivalente para comparar.
- **Classe de um fornecedor:** você contratou um fornecedor de frete e cadastrou a frota-espelho dele. As fichas desse fornecedor formam classes próprias, com o fornecedor como titular — nunca misturadas com as classes da sua frota própria.

## Onde mais a classe aparece <a href="#onde-mais-a-classe-aparece" id="onde-mais-a-classe-aparece"></a>

Além de ser o alvo do roteiro, a classe é reconhecida em mais dois lugares do LocFlow:

- **Dividir a carga em viagens.** Quando uma entrega não cabe num veículo só, o LocFlow propõe as viagens automaticamente também para a classe (não só para a ficha exata), usando a mesma capacidade do grupo — pela capacidade cheia quando é verificada, pela menor quando é mista. Veja [Dividir um movimento em viagens](../logistica/planejando-o-roteiro.md#dividir-um-movimento-em-viagens).
- **A regra de frete.** Se você cobra frete por tipo de veículo, dá para configurar o preço por classe — cobrindo todo o grupo de uma vez, em vez de repetir a mesma regra ficha por ficha. Veja [Motor de frete](../configuracoes/motor-de-frete.md).

## Próximo passo <a href="#proximo-passo" id="proximo-passo"></a>

Volte para [Frota](frota.md) para ver a hierarquia completa (classe → especificação → veículo) e a escada de cadastro. Para configurar o que cada especificação carrega, veja [Especificações: capacidade](frota-capacidade.md). E para ver a classe em ação na montagem da rota, vá a [Planejando o roteiro](../logistica/planejando-o-roteiro.md).
