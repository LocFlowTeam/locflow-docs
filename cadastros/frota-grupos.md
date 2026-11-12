---
icon: object-group
description: O grupo reúne tipos de veículo que carregam a mesma coisa — é ele que o roteiro e o frete enxergam. Como escolher o grupo, aceitar uma sugestão de agrupamento, renomear e ler o selo de capacidade.
---

# Grupos da frota

Um **grupo** reúne **tipos de veículo que carregam a mesma coisa**. Na hora de montar um roteiro, o LocFlow trata **qualquer veículo do grupo como equivalente** — é isso, e só isso, que o grupo significa.

É por isso que o planejamento escolhe o **grupo**, e não a placa: o roteiro diz "vai um Caminhão Toco", e a placa que sai é decidida no dia, entre os veículos do grupo que estiverem disponíveis. O nome do grupo é o que aparece no planejamento, no frete e nas telas que o seu cliente vê.

{% hint style="info" %}
**Antes, "classe veicular".** O grupo é o que o LocFlow chamava de classe. Não existe mais uma tela de classes nem a divisão entre "classes padrão" e "minhas classes": o grupo nasce do cadastro do [tipo de veículo](frota-ficha-tecnica.md). Contas antigas podem ainda ter os grupos "Carro Utilitário" e "Caminhão", que antes eram criados automaticamente — hoje eles são grupos como quaisquer outros. No planejamento do roteiro, o campo ainda aparece como **"Tipo de veículo (classe)"**: a classe ali é o grupo.
{% endhint %}

## Todo tipo entra num grupo {#escolher-o-grupo}

O grupo é o **último bloco** do cadastro do tipo de veículo — e é **obrigatório**. O cartão explica por quê: *"É o grupo que o planejamento e o frete enxergam — e o nome que o cliente vê."*

1. **Sugestão (atalho de um toque).** Quando a capacidade que você digitou combina com um grupo que já existe, a tela mostra esse grupo com quantos tipos equivalentes ele já tem (*"2 tipos equivalentes já estão nele."*) e o botão **Entrar**. Aceitar é opcional.
2. **Escolher outro.** No campo **Grupo** (ou **Ou escolha outro grupo**, quando há sugestão), busque pelo nome.
3. **Criar um novo.** Digite um nome que ainda não existe (ex.: "VUC", "Truck", "Carreta") e toque em **Criar o grupo "…"**.

Sem grupo, o tipo não é salvo: *"Escolha o grupo deste tipo, ou crie um novo."* A busca só mostra grupos do **mesmo titular** do tipo — veja [O titular do grupo](#o-titular-da-classe).

{% hint style="info" %}
**Quem não pode criar grupos só escolhe.** Criar um grupo é uma permissão à parte. Sem ela, a busca continua funcionando, mas a opção de criar não aparece.
{% endhint %}

## Os grupos na tela da frota {#grupos-na-frota}

Em **Logística › Frota**, a aba **Veículos** mostra a frota **reunida por grupo**: o nome do grupo é o cabeçalho de cada bloco, com a quantidade de veículos. Dá para recolher um grupo e filtrar a lista por **Grupo**.

- **Renomear:** toque no **⋯** do cabeçalho do grupo e em **Renomear grupo**. *"O nome é só para você reconhecer o grupo — nada do que ele significa muda."* O nome novo passa a valer em todos os lugares onde o grupo aparece. Em telas largas, onde a lista vira tabela, o **⋯** de cada grupo fica na faixa **Grupos desta página**.
- **Excluir:** não há botão de excluir grupo na tela da frota. Enquanto um grupo tiver um tipo dentro, uma extensão apontando para ele ou um preço de frete cobrando por ele, ele precisa continuar existindo.

## Sugestões de agrupamento {#sugestao-automatica}

Você não precisa notar sozinho quando dois tipos "dão no mesmo". O LocFlow compara a **capacidade de carga** dos seus tipos — os mesmos limites por item, o mesmo volume de baú e o mesmo peso máximo — e, quando encontra tipos equivalentes espalhados em grupos diferentes, sugere juntá-los.

Na aba **Veículos**, para quem pode criar grupos, o cartão **Sugestões de agrupamento** aparece quando há tipos para juntar (ou tipos sem capacidade cadastrada) e mostra:

- *"Estes tipos carregam a mesma coisa mas estão em grupos diferentes. Juntá-los deixa o roteiro tratar qualquer um deles como equivalente."* (ou, quando não há o que juntar, *"Ainda não encontramos tipos com a mesma capacidade de carga para agrupar."*);
- para cada sugestão, quantos tipos têm a mesma capacidade, um resumo da capacidade em comum (ex.: *"20 × Cadeira · 8,4 m³"*), quais são os tipos e em que grupo cada um está hoje.

Toque em **Juntar num grupo**, dê um nome em **Nome do novo grupo** (*"3 tipos vão passar para este grupo. Você pode movê-los de novo depois."*) e confirme em **Juntar**.

A mesma sugestão aparece em mais dois lugares: no **cadastro do tipo** (o atalho **Entrar**, acima) e no **planejamento do roteiro**, quando o grupo escolhido tem capacidades diferentes e existem tipos equivalentes que dá para juntar ali mesmo.

{% hint style="info" %}
**Fica de fora da sugestão:** os tipos da frota de um **parceiro externo** (a sua organização não reorganiza a frota de um parceiro) e os tipos **sem capacidade cadastrada** — o cartão conta quantos estão nessa situação (*"2 tipos elegíveis estão sem capacidade cadastrada e por isso não entram nestas sugestões."*). Para aparecerem nas sugestões, complete a capacidade deles.
{% endhint %}

{% hint style="success" %}
**Por que isso te faz faturar mais.** Cada tipo que entra no grupo certo vira mais uma opção de veículo na hora de montar o roteiro — sem você decidir manualmente, toda vez, "essa Kombi serve para essa carga?". Menos tempo organizando a frota, mais veículos aptos para cada entrega.
{% endhint %}

## O selo de capacidade do grupo <a href="#alvo-do-roteiro" id="alvo-do-roteiro"></a>

Ao [planejar o roteiro](../logistica/planejando-o-roteiro.md), você escolhe o **grupo** — e o LocFlow confere a carga pela **capacidade dos tipos do grupo**, mostrando num selo com que força essa conferência foi feita. (Na bancada de **Cargas e viagens**, o mesmo selo aparece com um nome um pouco mais longo, indicado entre parênteses.)

| Selo | Quando aparece | O que o LocFlow faz |
| --- | --- | --- |
| **Capacidade verificada** | Dois ou mais tipos do grupo têm a mesma capacidade, e nenhum ficou sem capacidade cadastrada. | Confere a carga **por inteiro** — tanto faz qual veículo do grupo sai. |
| **Mista — cobertura parcial** (*Capacidade verificada — cobertura parcial*) | Os tipos comparados batem entre si, mas algum outro tipo do grupo está sem capacidade cadastrada. | Confere pela capacidade em comum dos que têm dado — e avisa da lacuna, para você completar o cadastro. |
| **Capacidade mista** (*Capacidade mista — vale a menor*) | Os tipos do grupo têm capacidades diferentes. | Confere pela **menor** capacidade do grupo, para caber em qualquer veículo dele. |
| **Um tipo só** | Só um tipo do grupo tem capacidade cadastrada. | Usa a capacidade dele, mas **não chama de verificada** — comparar um veículo com ele mesmo não prova nada. |
| **Sem capacidade cadastrada** (ou **Sem especificações**, quando o grupo não tem nenhum tipo) | Nenhum tipo do grupo tem capacidade cadastrada. | Avisa que não dá para conferir a carga — mas **não impede** você de seguir. |

Quando a garantia não é cheia (capacidade mista, cobertura parcial ou sem capacidade cadastrada), o planejamento pede uma confirmação — **Confirmar a capacidade desta classe** — com as opções **Usar esta classe assim mesmo** ou **Escolher outra classe**. Ela é pedida **uma vez por grupo**, não a cada roteiro (volta a ser pedida se a capacidade do grupo mudar).

Como em toda a frota, o grupo **nunca bloqueia** o roteiro. Veja como cada estratégia de capacidade funciona em [Tipos de veículo: capacidade](frota-capacidade.md).

## O titular do grupo <a href="#o-titular-da-classe" id="o-titular-da-classe"></a>

Todo grupo tem um **titular** — o mesmo de cada [tipo](frota-titular.md) que ele reúne:

- **A sua organização** (o caso comum) — a sua própria frota.
- **Um fornecedor de frete** — quando o grupo reúne tipos de um terceiro que roda para você (a frota-espelho dele).
- **Um parceiro externo** — quando o grupo reúne tipos da frota de um parceiro da [Rede de Parceiros](../parcerias/visao-geral.md).

{% hint style="info" %}
**Todos os tipos de um grupo são do mesmo titular.** A busca de grupos, no cadastro do tipo, só mostra grupos do titular dele — tipo de fornecedor pede grupo do fornecedor, e o grupo criado na hora já nasce dele. É essa regra que garante que, ao escolher o grupo no roteiro, o LocFlow sabe **quem** vai rodar a viagem, não só **quanto** cabe nela.
{% endhint %}

## Onde mais o grupo aparece {#onde-mais-o-grupo-aparece}

- **Repartir a carga em viagens.** Na bancada de **Cargas e viagens**, cada viagem é um grupo de veículo (e, quando há, um grupo de extensões engatado), com a ocupação à vista. Veja [Cargas e viagens](../logistica/planejando-o-roteiro.md#cargas-e-viagens).
- **A regra de frete.** Se você cobra frete por tipo de veículo, dá para configurar o preço por grupo — cobrindo o grupo inteiro de uma vez. Veja [Motor de frete](../configuracoes/motor-de-frete.md).

## Situações reais {#situacoes-reais}

- **Três furgões, marcas diferentes, mesmo baú:** você tem um Fiorino, um Kangoo e uma Saveiro furgão, todos com baú de 6 m³ e limite de 15 cadeiras, em grupos diferentes. O cartão **Sugestões de agrupamento** propõe juntar os três — você toca em **Juntar num grupo**, chama de "Furgão 6m³" e confirma.
- **Roteiro pelo grupo, capacidades iguais:** você planeja o roteiro de amanhã escolhendo "Furgão 6m³" em vez de decidir qual dos três sai. O selo é **Capacidade verificada**: a carga é conferida por inteiro, e quem estiver no pátio escolhe a placa.
- **Roteiro pelo grupo, capacidades diferentes:** o grupo "Caminhão" tem um tipo com baú de 20 m³ e outro com 15 m³. Ao escolhê-lo, o app mostra **Capacidade mista** e pede a confirmação uma vez — a carga é conferida pelos 15 m³.
- **O primeiro veículo de um modelo:** você cadastrou a primeira Kombi. O grupo "Kombi" já pode ser escolhido no roteiro, mas o selo diz **Um tipo só** até existir um segundo tipo equivalente para comparar.
- **O grupo com nome de cadastro:** um grupo se chamava "Fiorino 2019 Flex" e o cliente lia isso no orçamento. Você toca no **⋯** do cabeçalho, **Renomear grupo**, e passa a chamá-lo de "Furgão pequeno".

## Próximo passo {#proximo-passo}

Volte para [Frota](frota.md) para a visão geral, veja como cadastrar o que o grupo reúne em [Tipos de veículo](frota-ficha-tecnica.md) e veja o grupo em ação em [Planejando o roteiro](../logistica/planejando-o-roteiro.md).
