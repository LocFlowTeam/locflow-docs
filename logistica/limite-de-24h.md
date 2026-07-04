---
icon: clock
description: Por que um roteiro cobre no máximo 24 horas — um dia operacional, um turno. A regra, o porquê e as referências de mercado e técnicas por trás dela.
---

# O limite de 24h do roteiro

Um **roteiro** é **uma viagem só**: a sequência de paradas que a equipe cumpre numa ida à rua, saindo do galpão e voltando a ele. No LocFlow, essa viagem cobre **no máximo 24 horas** — **um dia operacional, um turno**. Movimentos espalhados por vários dias **não** entram no mesmo roteiro: cada dia vira um roteiro próprio.

{% hint style="info" %}
Esta página explica **o porquê** do número e deixa as referências registradas. Para o passo a passo de montar a rota, veja [Planejando o roteiro](planejando-o-roteiro.md).
{% endhint %}

## A regra, em uma frase

> Um roteiro vai do **começo da janela mais cedo** ao **fim da janela mais tarde** entre as suas paradas — e essa faixa não pode passar de **24 horas**.

Se você tentar selecionar dois movimentos cujas janelas estão a **mais de 24h de distância** (por exemplo, uma entrega de **hoje** e outra de **amanhã**), o LocFlow **recusa na hora** e sugere separar em outro roteiro. Movimentos de **dias diferentes** devem virar **roteiros separados — um por dia**.

## Como funciona na prática

Ao montar o roteiro, o app vigia o **horizonte** (a faixa de tempo coberta pelas janelas das paradas) a cada parada que você adiciona:

* Se a nova parada **caberia** dentro das 24h, ela entra normalmente.
* Se a nova parada **estoura** as 24h, o app **não a inclui** e mostra um aviso na hora:

> **Fora do horizonte do roteiro** — Com esta parada as janelas cobrem ~X; um roteiro vai até 24h. Provável data distante — separe em outro roteiro.

O mesmo limite vale quando você usa o **laço** para adicionar várias paradas de uma vez (as que estouram o horizonte ficam de fora, com aviso) e quando você dispara as **ações de mapa** (otimizar e traçar a rota) — todas reforçam as 24h.

{% hint style="success" %}
**O aviso é um detetive de erro de data.** Na maioria das vezes, uma parada "fora do horizonte" não é um caso real de viagem de vários dias — é uma **data digitada errada** numa das janelas. O app te mostra isso **antes** de você sair, em vez de você descobrir o problema na rua.
{% endhint %}

**A solução é sempre a mesma:** se as entregas são mesmo de dias diferentes, monte **um roteiro por dia**. Cada viagem fica enxuta, otimizável e fiel ao que a equipe vai fazer naquele turno.

## Por que 24h?

O número não é arbitrário. Ele junta a **prática do mercado**, a **realidade do turno do motorista** e uma **recomendação técnica** do motor de otimização que usamos (o Google). Aqui ficam o raciocínio e as fontes, para qualquer pessoa rastrear de onde veio a decisão.

### 1. Roteirização é uma operação diária

A roteirização de **última milha** (a entrega final ao cliente) é, por natureza, uma operação **de cada dia**. O padrão do mercado é **otimizar dinamicamente as ordens daquele dia** — e replanejar no dia seguinte com as novas entregas. Quando se fala em "roteirização multi-dia", o que se quer dizer é uma **sequência de rotas diárias** (uma por dia, recalculada a cada dia), **não** uma única viagem contínua que atravessa vários dias.

Modelar o roteiro como "um dia" é, portanto, alinhar a ferramenta ao jeito como a operação realmente acontece.

Referências:

* [Last-Mile Delivery Route Optimization — Upper](https://www.upperinc.com/blog/last-mile-delivery-route-optimization/)
* [Last-Mile Route Optimization — Locus](https://locus.sh/blogs/last-mile-route-optimization/)
* [The Math of Last-Mile Multi-Stop Route Planning — Nuvizz](https://nuvizz.com/blog/math-of-last-mile-multi-stop-route-planning/)

### 2. O turno do motorista cabe em um dia

Uma jornada real de motorista é tipicamente de **8 a 10 horas**. Ou seja, **24h é até generoso** para **uma** rota: cobre folgadamente os casos longos (rotas extensas, saídas de madrugada, retornos noturnos) **sem** bloquear roteiros legítimos de um dia. Acima disso, já não é "uma viagem" — são turnos diferentes, que pedem roteiros diferentes.

{% hint style="info" %}
No Brasil, a jornada do motorista é **regulada por lei** — a chamada "Lei do Motorista" (Lei 13.103/2015), que estabelece limites de tempo de direção e descanso. Citamos como **contexto geral**: o ponto é que uma única jornada de condução é, por definição, algo que **cabe dentro de um dia** — reforçando que "um roteiro = um turno" reflete a realidade (e a lei) da operação.
{% endhint %}

### 3. Recomendação técnica do Google (o motor de otimização)

O LocFlow usa a **API Google Route Optimization** (a função `optimizeTours`) para calcular a melhor sequência de paradas. A documentação do Google **recomenda explicitamente** modelar **um único dia** no horizonte global de tempo quando há custo por hora — por questão de **performance** do cálculo.

O limite **duro** do Google é muito maior: cerca de **365 dias** (31.536.000 segundos) entre o início e o fim do horizonte global. Ou seja, **as 24h são uma escolha nossa**, deliberadamente **mais restrita** que o limite do Google, para **enxugar o problema** e evitar artefatos no resultado (como a rota "esticar" para o dia seguinte só porque foi obrigada a encaixar uma entrega distante na mesma viagem).

Referências:

* [Google Route Optimization — referência da API (RPC)](https://developers.google.com/maps/documentation/route-optimization/reference/rpc/google.maps.routeoptimization.v1)
* [Google Route Optimization — lista de parâmetros](https://developers.google.com/maps/documentation/route-optimization/parameter-list)

### 4. O benefício prático: um problema bem-formado

Ao garantir "um dia" **já na nossa aplicação** (um **portão de segurança**, antes mesmo de chamar o Google), enviamos ao motor de otimização uma **janela de tempo enxuta e bem-formada**. Isso traz dois ganhos de uma vez:

* **Melhor performance** — o solver trabalha sobre um horizonte pequeno, como o próprio Google recomenda.
* **Resultados que fazem sentido** — sem horizonte inflado, o solver não é empurrado a escolhas estranhas (por exemplo, sugerir uma **saída no meio da tarde** porque foi obrigado a encaixar, na mesma viagem, uma entrega que só acontece no dia seguinte).

{% hint style="success" %}
**Resumo:** as 24h não são um limite técnico que "sobrou" — são uma **decisão de produto**. Elas mantêm o roteiro fiel à operação (um turno, um dia), respeitam o que o mercado e o motor de otimização recomendam, e fazem o LocFlow te entregar rotas mais rápidas de calcular e mais sensatas de executar.
{% endhint %}

## Situações reais

* **Entrega de hoje e entrega de amanhã na mesma seleção.** Ao tocar na parada de amanhã, o app avisa *"Fora do horizonte do roteiro"* e não a inclui. Você monta **dois roteiros**: um para hoje, outro para amanhã.
* **Laço pegou paradas de dois dias.** Você cerca uma região no mapa e o app adiciona as do dia que você está planejando, deixando de fora as de outro dia, com aviso. Planeje o outro dia em seguida.
* **Era erro de digitação.** Uma parada aparece "fora do horizonte" por estar marcada para a semana que vem. Você confere, vê que a data certa era hoje, corrige a janela no orçamento e ela passa a caber no roteiro.

## Perguntas rápidas

**Posso aumentar o limite para mais de 24h?**
Não. O limite é uma regra do LocFlow, pensada para manter cada roteiro como **uma viagem de um dia**. Para outro dia, é outro roteiro.

**E se minha rota de verdade passa da meia-noite?**
Sem problema: o limite é de **24 horas corridas**, não "até a meia-noite". Uma viagem que sai à noite e volta de madrugada cabe tranquilamente, porque a faixa coberta continua dentro de 24h.

**Por que o app me barra logo na seleção, e não só quando otimizo?**
Para te avisar **o quanto antes** — geralmente é sinal de uma **data errada** numa parada. Barrar já na seleção evita você montar um roteiro inteiro para só então descobrir que duas paradas nunca caberiam na mesma viagem.

## Próximo passo

* [Planejando o roteiro](planejando-o-roteiro.md) — montar a rota passo a passo.
* [Movimentos, janelas e galpão de origem](../orcamentos/movimentos-e-janelas.md) — de onde vêm as janelas de horário de cada parada.
* [Visão geral da logística](visao-geral.md) — onde o roteiro se encaixa no todo da operação.
