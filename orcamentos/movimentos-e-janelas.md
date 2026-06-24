---
icon: calendar-clock
description: Como o orçamento organiza a ida e a volta dos seus itens — os movimentos, as janelas de horário e de onde sai cada carga.
---

# Movimentos, janelas e galpão de origem

Quando você monta um orçamento, não basta dizer **o que** vai sair: o LocFlow também ajuda a definir **quando** os itens se movem e **de onde** eles saem. Essa parte do formulário é a seção de **movimentos logísticos** — o "vai e volta" do pedido.

A boa notícia: você não precisa preencher tudo de uma vez. Dá para começar com um "ainda não sei" e refinar depois. E o que muda entre **locação** e **venda** o sistema já cuida sozinho.

{% hint style="info" %}
Esta página fala da seção de movimentos **dentro do orçamento**. Para entender a operação em campo depois que o pedido é fechado, veja [Visão geral da logística](../logistica/visao-geral.md).
{% endhint %}

## O conceito: um movimento logístico

Um **movimento logístico** é cada deslocamento dos seus itens. O LocFlow descreve cada movimento com três informações, na própria ajuda da tela:

> **Entrega** é quando os itens são levados ao local do evento. **Retirada** é quando são recolhidos após o evento. Cada movimento tem uma **data** e um **intervalo de horário**.

Ou seja, todo movimento responde a três perguntas:

- **Para onde / de onde vai?** (o destino e o galpão de origem)
- **Quando?** (a data e a janela de horário)
- **Quem faz?** (a sua equipe leva/busca, ou o cliente vai até o galpão)

### Locação tem duas pontas; venda tem uma

A diferença mais importante depende da **natureza** do orçamento (entenda em [Locação e venda](../conceitos/locacao-e-venda.md)):

| | Locação (aluguel) | Venda |
| --- | --- | --- |
| **Movimentos** | **Saída** (entrega) **e** retorno (retirada) | Só a **saída** (entrega) |
| **O item** | Vai e **volta** | Sai em **definitivo** |
| **Na tela** | Dois grupos: saída → retorno | Um grupo só |

Em locação, a seção mostra dois blocos encadeados — primeiro a **saída do material**, depois o **retorno** —, com um separador entre eles indicando que um acontece **depois** do outro. Em venda, o ciclo termina na entrega, então o segundo bloco simplesmente não aparece.

## Quem leva e quem busca

Cada ponta do movimento tem uma decisão simples, controlada por um botão:

- **Sua equipe leva / busca** (o padrão): seus itens saem do galpão e vão até o destino. Esse é o movimento "com deslocamento".
- **Cliente retira no galpão** (na saída) ou **Cliente devolve no galpão** (no retorno, só em locação): o cliente vem até você. Aqui não há endereço de destino — basta dizer **qual galpão** e **em que data**.

{% hint style="info" %}
Quando o cliente retira no galpão, a entrega "pela equipe" some — não há trajeto para montar. O mesmo vale para a devolução no galpão no retorno. Você só escolhe o galpão e a data.
{% endhint %}

## As janelas de horário

Aqui está o coração da seção: a **janela** de cada movimento — a data mais a faixa de horário em que ele deve acontecer. Ao tocar no "?" ao lado de **Janela de Entrega** (ou de Retirada), o LocFlow explica os três conceitos abaixo. Os textos a seguir são exatamente os da ajuda do app.

### Movimento

> Entrega é quando os itens são levados ao local do evento. Retirada é quando são recolhidos após o evento. Cada movimento tem uma data e um intervalo de horário.

### Intervalo Salvo

> Selecione um horário predefinido: o **Horário Comercial** da organização para aquele dia da semana, ou um **Período** cadastrado (ex.: Manhã, Tarde). As opções são ordenadas pelo horário de encerramento.

Na prática, ao escolher "Intervalo Salvo" você vê uma lista de opções prontas. A opção de **Horário Comercial** aparece com a faixa daquele dia (por exemplo, *Horário Comercial (08:00–18:00)*) e os **Períodos** que você cadastrou (Manhã, Tarde…) aparecem logo abaixo. Se o dia escolhido cair fora do expediente, a opção de horário comercial aparece **desabilitada** como *Fora do Horário Comercial* — é o sistema te avisando que aquele dia não tem expediente.

{% hint style="success" %}
**Por que isso te poupa tempo:** ao trocar a data, o LocFlow já re-seleciona a primeira janela salva disponível para o novo dia. Você cadastra seus horários uma vez (em [Horários e sazonalidades](../configuracoes/horarios-e-sazonalidades.md)) e o resto vira clique.
{% endhint %}

### Intervalo Exclusivo

> Defina uma **janela personalizada**. Informe o horário **máximo** de entrega/retirada. O sistema calcula automaticamente o **início** com base no **intervalo mínimo logístico** configurado.

É a opção para quando o caso foge do padrão. Você informa só o horário-limite ("Entregar até no máximo…") e o LocFlow recua o início sozinho, usando o **intervalo mínimo logístico** que você configurou (o tempo de folga que sua operação precisa). Se quiser, depois ajusta o início manualmente.

{% hint style="info" %}
Se você não tem horário comercial nem períodos cadastrados, o seletor "Salvo × Exclusivo" nem aparece — a janela já entra direto no modo exclusivo (você informa o horário-limite).
{% endhint %}

### As validações da janela

Ainda na mesma ajuda, o LocFlow resume as regras que ele cobra de você:

> A data de **entrega não pode ser posterior à data do evento**. Se entrega e evento forem **no mesmo dia** e o evento tiver horário definido, a entrega deve ser **concluída antes** do horário do evento.

Além dessas, há a checagem óbvia de coerência: no intervalo exclusivo, **o início precisa ser anterior ao fim**.

#### Quando o intervalo fica apertado

Se você montar um intervalo exclusivo **menor** que o seu intervalo mínimo logístico, o LocFlow não te bloqueia — ele te **avisa**. Aparece a mensagem *"Intervalo mínimo não respeitado"* com duas saídas:

- **Aceito correr o risco** — mantém a janela apertada (você assume o risco de atraso).
- **Definir novo intervalo** — limpa a janela para você refazer com folga.

{% hint style="warning" %}
Janela apertada é uma decisão sua, não um erro. Mas é por isso que existe o aviso: uma entrega sem folga vira atraso em campo, e atraso com o cliente custa caro. Use "correr o risco" com consciência.
{% endhint %}

### Combinei a janela com o cliente?

Logo abaixo da janela há um detalhe pequeno que rende muito: o botão **"Já combinei esta janela com o cliente"**. Marcar isso diz ao LocFlow que aquele horário é um **combinado**, não só uma estimativa sua — informação que o planejamento de roteiro usa depois para tratar a parada com mais firmeza. Deixe desmarcado enquanto for só um palpite seu.

## "Ainda não sei quando" (o a definir)

Nem todo orçamento já nasce com data fechada. Por isso, cada movimento tem o botão **"Você sabe quando?"**. Desligue-o e a data/janela some, dando lugar a um lembrete discreto do prazo:

| Situação | O que o LocFlow lembra |
| --- | --- |
| Entrega, locação | *Defina a entrega até a reserva do orçamento* |
| Entrega, venda | *Defina a entrega até a venda do orçamento* |
| Retirada (equipe) | *Defina a retirada até a reserva do orçamento* |
| Retirada no galpão (locação) | *Defina a data da retirada no galpão até a reserva do orçamento* |
| Retirada no galpão (venda) | *Defina a data da retirada no galpão até a venda do orçamento* |
| Devolução no galpão | *Defina a data da devolução no galpão até a reserva do orçamento* |

Em outras palavras: você pode mandar o orçamento para o cliente **sem** a data ainda fechada, mas precisa defini-la **antes de ganhar o pedido** (reservar, na locação; vender, na venda). O sistema te cobra na hora certa — não antes.

{% hint style="success" %}
**Para quem está começando:** não trave seu orçamento esperando o cliente decidir a data. Deixe "ainda não sei", envie a proposta e refine quando ele confirmar. O prazo só aperta no fechamento.
{% endhint %}

## O galpão de origem (de onde sai a carga)

Toda saída precisa partir de **algum lugar**: o **galpão de origem**. No bloco "De onde sai?", o LocFlow ordena seus galpões por **proximidade do destino** e indica quais conseguem atender aquele endereço.

### O caminho feliz

1. Você informa o **destino** (para onde os itens vão).
2. Toca em **Avaliar disponibilidade**.
3. O LocFlow calcula a distância de cada galpão até o destino e lista os galpões **ordenados pelo mais próximo**, mostrando quais cobrem o local.
4. O melhor galpão dentro do alcance é **selecionado automaticamente** — você só confirma.

Se você tem **um único galpão** cadastrado, ele já vem escolhido sozinho: não há o que ranquear.

### Cada carga sai de um galpão só

Esta é uma regra importante de entender, porque ela atravessa o orçamento **e** o roteiro: hoje, **a carga de um movimento sai de um único galpão**. O LocFlow ainda **não agrega itens de galpões diferentes** numa mesma saída — cada movimento aponta para um galpão de origem, e é de lá que tudo sai.

Isso se reflete diretamente no [planejamento do roteiro](../logistica/planejando-o-roteiro.md): um roteiro **parte de um único galpão** (o do primeiro movimento que você adiciona). Movimentos que saem de outro galpão não entram no mesmo roteiro — eles formam **outra** rota, com a sua própria saída. É por isso que, ao montar a rota, o app recusa um movimento de outro galpão com *"Sai de outro galpão"*.

{% hint style="info" %}
**Por que um galpão por vez?** Uma viagem com a equipe carregando, saindo e entregando é, na vida real, **um caminhão partindo de um pátio**. Misturar duas origens na mesma viagem muda a logística (precisaria passar num galpão, carregar mais, e só então rodar). Manter "uma saída, um galpão" deixa o roteiro fiel ao que de fato acontece na rua.
{% endhint %}

{% hint style="warning" %}
**Em breve — operação multi-galpão.** Estamos trabalhando para o futuro em que um pedido pode **somar estoque de vários galpões**: o orçamento verifica a disponibilidade somando o que existe em cada galpão e, no roteiro planejado daquele pedido, a rota já nasce sabendo que **sai de um galpão, passa em outro para pegar mais material** e segue para as entregas. Por enquanto, cada carga sai de um galpão só — e roteiros de galpões diferentes são planejados separadamente.
{% endhint %}

### Os estados de disponibilidade

Cada galpão aparece com um indicador do que o sistema sabe sobre ele:

| O que você vê | O que significa |
| --- | --- |
| **Disponibilidade desconhecida** | Ainda não avaliamos a proximidade (a lista veio "crua", sem cálculo). Aparece antes de você tocar em *Avaliar disponibilidade*. |
| **Dentro da área de atendimento** | O galpão **cobre** aquele destino — a distância está dentro do raio que você cadastrou para ele. |
| **Fora do raio de atendimento** | O destino está **mais longe** do que o raio do galpão. A opção fica desabilitada — não dá para escolher esse galpão para esse local. |

{% hint style="info" %}
Antes de informar o destino, o galpão fica esperando: *"Informe o destino para avaliar a disponibilidade dos galpões."* É o destino que destrava o cálculo de proximidade.
{% endhint %}

### Quando nenhum galpão alcança

Se **nenhum** dos seus galpões cobre o destino, o LocFlow não deixa você seguir no escuro. Ele mostra qual ficou mais perto e por quanto faltou — algo como:

> Nenhum galpão atende o local fornecido. O galpão mais próximo encontrado foi *Galpão Central*, que aceita até 30,0 km de raio, enquanto o local tem 42,5 km de distância dele. Ajuste os cadastros dos galpões ou selecione outro local.

E te oferece duas saídas: **Ajustar destino** (talvez o endereço esteja com o pino fora do lugar) ou rever os raios dos galpões no cadastro. Saiba mais em [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md).

{% hint style="warning" %}
**Avaliar a disponibilidade consome créditos.** O cálculo de proximidade usa o mapa, então o botão sempre mostra *"Consome até X crédito(s)"* — cobra-se no máximo **1 crédito por endereço novo** a resolver, e é **grátis** quando o endereço já foi calculado antes. Reavaliar o mesmo destino não cobra de novo.
{% endhint %}

### Reavaliar quando algo muda

Se você mexer no destino depois de já ter avaliado — trocar o endereço ou arrastar o pino no mapa —, o LocFlow marca a lista como **desatualizada** e oferece **Reavaliar disponibilidade**. Importante: se o galpão que estava escolhido sair do alcance com o novo destino, ele é **desmarcado automaticamente** e você é avisado de que ficou fora do raio. Nada de carga saindo de um galpão que não alcança o cliente.

## Espelhar o trajeto na retirada (locação)

Na locação, a retirada (o retorno) costuma sair do **mesmo lugar** da entrega. Para não fazer você digitar tudo de novo, o LocFlow **espelha** o trajeto da entrega na retirada por padrão.

- Com **um galpão só**, ele mostra direto o endereço da entrega num cartão com **Editar** — claro e sem rodeios.
- Com **vários galpões**, aparece *"Usando mesmo trajeto da entrega"* e um botão **Alterar**, que pergunta o que você quer mudar: **o endereço de retirada** ou **o galpão de origem**. Você muda só o que for diferente e pode voltar ao mesmo trajeto depois.

{% hint style="info" %}
Se o cliente **retira no galpão** (não há entrega pela equipe), não existe trajeto para espelhar — a retirada com deslocamento pede destino e galpão próprios.
{% endhint %}

## Por porte: como cada operação usa esta seção

| Seu perfil | Como aproveitar |
| --- | --- |
| **Autônomo / pequeno** | Um galpão, datas no "ainda não sei" até o cliente confirmar, janela no Intervalo Salvo. O sistema escolhe o galpão e a janela por você. |
| **Médio** | Vários galpões com raios bem cadastrados, períodos do dia (Manhã/Tarde) para padronizar janelas, e o "já combinei com o cliente" para o roteiro confiar nos horários. |
| **Grande** | Ranking de galpões por proximidade vira roteirização eficiente; intervalos exclusivos para casos especiais; o intervalo mínimo logístico protege a operação de janelas apertadas em escala. |

## Situações reais

**"Vendi um lote de cadeiras usadas."** Orçamento de **venda**: só há o bloco de **entrega**. Escolha o destino, o galpão de origem mais próximo e a data. Sem retorno — o item sai em definitivo.

**"Aluguel de palco, o cliente busca e devolve no galpão."** Ligue **Cliente retira no galpão** e **Cliente devolve no galpão**. Some o endereço de destino dos dois lados; você só informa qual galpão e as datas de retirada e devolução.

**"Entrega e retirada no mesmo endereço."** Deixe a retirada **espelhar** a entrega (o padrão na locação). Mexa só na data/janela da retirada.

**"O cliente ainda não decidiu a data."** Desligue **"Você sabe quando?"** nos movimentos. Envie o orçamento; defina as datas antes de **reservar** (locação) ou **vender** (venda).

**"O endereço ficou longe e nenhum galpão atende."** Confira o pino do destino em **Ajustar destino**. Se estiver certo, talvez seja o caso de ampliar o raio de um galpão em [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md).

## Próximo passo

- [Criando um orçamento](criando-um-orcamento.md) — a seção de movimentos no contexto do orçamento inteiro.
- [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md) — cadastrar raio e endereço dos seus galpões.
- [Horários e sazonalidades](../configuracoes/horarios-e-sazonalidades.md) — montar o horário comercial e os períodos do dia.
- [Visão geral da logística](../logistica/visao-geral.md) — o que acontece com os movimentos depois do pedido fechado.
