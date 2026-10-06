---
icon: calendar-clock
description: Como o orçamento organiza a ida e a volta dos seus itens — quem leva e quem traz de volta, quando (as faixas de horário) e de qual galpão sai a carga.
---

# Movimentos, janelas e galpão de origem

Quando você monta um orçamento, não basta dizer **o que** vai sair: o LocFlow também ajuda a definir **quando** os itens se movem e **de onde** eles saem. Essa parte do formulário são as seções **Saída do material** e **Retorno do material** — o "vai e volta" do pedido.

A boa notícia: você não precisa preencher tudo de uma vez. Dá para mandar a proposta com a data ainda em aberto e refinar depois. E o que muda entre **locação** e **venda** o sistema já cuida sozinho.

{% hint style="info" %}
Esta página fala dos movimentos **dentro do orçamento**. Para entender a operação em campo depois que o pedido é fechado, veja [Visão geral da logística](../logistica/visao-geral.md).
{% endhint %}

## O conceito: um movimento logístico

Um **movimento logístico** é cada deslocamento dos seus itens. O LocFlow descreve cada movimento assim, na própria ajuda da tela:

> **Entrega** é quando os itens são levados ao local do evento. **Recolha** é quando são recolhidos após o evento. Cada movimento tem uma **data** e um **intervalo de horário**.

Ou seja, todo movimento responde a três perguntas:

- **Quem faz?** (a sua equipe leva e recolhe, ou o cliente vai até a loja)
- **Para onde / de onde?** (o destino e o galpão de origem)
- **Quando?** (a data e a faixa de horário)

### Locação tem duas pontas; venda tem uma

A diferença mais importante depende do **tipo de negócio** do orçamento (entenda em [Locação e venda](../conceitos/locacao-e-venda.md)):

| | Locação (aluguel) | Venda |
| --- | --- | --- |
| **Movimentos** | **Saída** (entrega) **e** retorno (recolha) | Só a **saída** (entrega) |
| **O item** | Vai e **volta** | Sai em **definitivo** |
| **Na tela** | Duas seções: **Saída do material** → **Retorno do material** | Uma seção só |

Em locação, o formulário mostra as duas seções, uma depois da outra — primeiro a **saída do material**, depois o **retorno**. Em venda, o ciclo termina na entrega, então o retorno simplesmente não aparece.

## Quem leva e quem traz de volta {#quem-leva}

Cada seção começa com uma pergunta de duas respostas:

| Seção | Pergunta | Respostas |
| --- | --- | --- |
| **Saída do material** | **Quem leva o material?** | **Equipe entrega** · **Cliente retira** |
| **Retorno do material** *(só locação)* | **Quem traz de volta?** | **Equipe recolhe** · **Cliente devolve** |

- **Equipe entrega / Equipe recolhe:** seus itens saem do galpão e vão até o cliente — ou voltam de lá. É o movimento "com deslocamento": você diz **para onde levar** (ou **de onde recolher**) e **quando**.
- **Cliente retira / Cliente devolve:** o cliente vem até você, na **loja** — o seu ponto de atendimento, vinculado a um galpão (veja [Lojas](../estoque/lojas.md)). Aqui não há endereço de destino: basta dizer **em qual loja** (*Onde o cliente retira?* / *Onde o cliente devolve?*) e **em que data**.

{% hint style="info" %}
Quando o cliente retira na loja, a entrega "pela equipe" some — não há trajeto para montar. O mesmo vale para a devolução na loja, no retorno. Você só escolhe a loja e a data (a linha mostra *Loja · horário comercial*). Na locação, escolher **Cliente retira** já sugere **Cliente devolve** — e a devolução acompanha a loja da retirada até você escolher outra. No dia, o atendimento acontece em **Logística › Minha Loja** — veja [Loja: retirada e devolução pelo cliente](../logistica/balcao.md).
{% endhint %}

{% hint style="info" %}
Se o **Formato padrão** do [Motor de Logística](../configuracoes/motores-operacionais.md#motor-de-logistica) é **Só loja** ou **Só rota**, a pergunta nem aparece: a seção já diz o modo (*Cliente retira na loja* ou *Entrega pela equipe*), e a escolha fica em **Operação avançada**, no fim da seção — abra só quando um pedido fugir do padrão. Mudou ali? O pedido ganha o selo *"Exceção neste orçamento — sua operação é só na loja"* (ou *só por rota*). No formato **Mista** (o padrão), as perguntas ficam sempre à mão.
{% endhint %}

## As janelas de horário

Aqui está o coração da seção: **quando** cada movimento acontece — a data mais a **faixa de horário**. Com a equipe levando, a linha começa como **Quando entregar?**; no retorno, **Quando recolher?**. Toque nela para abrir os campos:

* **Data de Entrega** (ou **Data de Recolha**) — na locação, o calendário destaca a data do evento como referência: a saída vai no máximo até o dia do evento, e o retorno começa a partir dele (na venda, que não tem evento, o calendário fica livre);
* **Faixa de horário** — o intervalo em que o movimento deve acontecer, escolhido em chips.

Ao tocar no **?** ao lado de **Faixa de horário**, abre a ajuda **Janela Logística**, com os conceitos abaixo.

### Movimento

> Entrega é quando os itens são levados ao local do evento. Recolha é quando são recolhidos após o evento. Cada movimento tem uma data e um intervalo de horário.

### Os horários salvos {#intervalo-salvo}

Na ajuda, eles aparecem como **Intervalo Salvo**:

> Selecione um horário predefinido: o **Horário Comercial** da organização para aquele dia da semana, ou um **Período** cadastrado (ex.: Manhã, Tarde). As opções são ordenadas pelos que começam mais cedo no dia.

Na prática, a faixa é uma fileira de chips: o **horário comercial** do dia escolhido (por exemplo, *Horário Comercial (08:00–18:00)*) e os **períodos** que você cadastrou (Manhã, Tarde…). Se o dia escolhido cair fora do expediente, o chip do horário comercial aparece **desabilitado** como *Fora do Horário Comercial*: havendo períodos cadastrados, a faixa vai para o primeiro deles; sem nenhum, ela vira personalizada, com um aviso de que aquele dia não tem horário comercial.

{% hint style="success" %}
**Por que isso te poupa tempo:** ao trocar a data, o LocFlow já ajusta a faixa ao horário daquele dia. Você cadastra seus horários uma vez (em [Horários e sazonalidades](../configuracoes/horarios-e-sazonalidades.md)) e o resto vira toque. Faltou um período? O chip **+ Novo período** cria um ali mesmo — nome, **Começa às**, **Termina às** e **Salvar período** — e ele já fica escolhido. (O chip aparece para quem pode editar os horários da organização.)
{% endhint %}

### A faixa personalizada {#intervalo-exclusivo}

Na ajuda, ela aparece como **Intervalo Exclusivo**:

> Defina uma **janela personalizada**. Informe o horário **máximo** de entrega/recolha. O sistema calcula automaticamente o **início** com base no **intervalo mínimo logístico** configurado.

É o chip **Personalizada**, para quando o caso foge do padrão. Você informa o limite — **Precisa estar entregue até** (ou **Precisa estar recolhido até**) — e o LocFlow sugere o **A partir de**, recuando pela folga mínima que a sua operação configurou. Depois, ajuste livremente; logo abaixo, uma linha resume o intervalo e quanto tempo de janela ele dá.

{% hint style="info" %}
Se você não tem horário comercial nem períodos cadastrados, só existe a **Personalizada** — a janela já entra nesse modo.
{% endhint %}

### As validações da janela

Ainda na mesma ajuda, o LocFlow resume as regras que ele cobra de você:

> A data de **entrega não pode ser posterior à data do evento**. Se entrega e evento forem **no mesmo dia** e o evento tiver horário definido, a entrega deve ser **concluída antes** do horário do evento.

Além dessas, há a checagem óbvia de coerência: na faixa personalizada, **o início precisa ser anterior ao fim**.

#### Quando o intervalo fica apertado

Se a faixa personalizada ficar **menor** que a folga mínima da sua operação, o LocFlow não decide por você — ele pergunta. Abre o aviso **Intervalo apertado**, que lembra a folga configurada, com duas saídas:

- **Aceito correr o risco** — mantém a faixa; fica um lembrete âmbar de que o risco de atraso foi aceito.
- **Definir novo intervalo** — enquanto a faixa continuar curta, o orçamento não salva: ajuste os horários ou escolha outro chip.

Fechar o aviso sem escolher conta como **Definir novo intervalo** — o caminho sem decisão é o seguro.

{% hint style="warning" %}
Janela apertada é uma decisão sua, não um erro. Mas é por isso que existe o aviso: uma entrega sem folga vira atraso em campo, e atraso com o cliente custa caro. Use "correr o risco" com consciência.
{% endhint %}

### Já está combinado com o cliente? {#combinado}

Escolhidos o dia e a faixa, aparece a pergunta **Já está combinado com o cliente?** — **Sim** ou **Ainda não** (o padrão). Responder **Sim** diz ao LocFlow que aquele horário é um **combinado**, não só uma estimativa sua: no planejamento do roteiro a janela vira compromisso firme, e no calendário a parada aparece como combinada. Deixe em **Ainda não** enquanto for só um palpite seu.

### O que essas janelas fazem com o seu estoque

Vale saber: **é daqui que sai o bloqueio de estoque**. O LocFlow não olha as datas do evento para decidir por quanto tempo um item fica indisponível — ele olha estes movimentos, porque é a **saída** que tira o item do galpão e o **retorno** que o traz de volta.

| O que você preenche aqui | O que vira lá no bloqueio |
| --- | --- |
| Janela da **entrega** pela equipe (o dia e a faixa) | O **início** da faixa abre o bloqueio |
| Janela da **recolha** pela equipe (o dia e a faixa) | O **fim** da faixa fecha o bloqueio |
| **Retirada ou devolução na loja** pelo cliente | Vale o **dia inteiro** — não há hora garantida |
| Movimento [**a definir**](#a-definir) | Ainda não abre nem fecha nada: sem as duas pontas agendadas, a política não calcula o bloqueio, e o pedido só pode ser reservado depois que você agendar o que falta |

Sobre esse período o Motor de Estoque ainda soma a **folga** configurada. Por isso, escolher a faixa com cuidado não é burocracia: **quanto mais justa a faixa, mais apertado (e mais rentável) o bloqueio**. Uma recolha marcada para "terça, das 8h às 12h" libera o item na terça à tarde; a mesma recolha das 14h às 18h, só à noite. Já a devolução do cliente na loja, na terça, trava a terça inteira — na loja não há hora garantida.

{% hint style="warning" %}
**As datas precisam fazer sentido entre si.** O material tem de sair **antes** de o evento começar e voltar **depois** de ele terminar. Se você agendar um recolhimento antes do fim do evento, o LocFlow avisa e pede correção — não deixa passar. Entenda a regra em [Duração, cobrança e bloqueio de uso](duracao-e-bloqueio.md#a-regra-que-o-locflow-cobra-de-voce).
{% endhint %}

#### E se eu mudar a janela depois de fechar o pedido? {#mudar-a-janela-depois}

O bloqueio **não fica congelado** no que valia no dia do fechamento: ao editar um pedido **já ganho**, ele é **recalculado sobre as datas novas**. Adiou a entrega em uma semana? O item deixa de ficar preso na semana antiga e passa a ficar preso na nova, liberando aquela agenda para outro cliente.

Duas consequências que vale conhecer **antes** de remarcar:

* **Se você definiu um bloqueio manual** para aquele pedido, é ele que prevalece — e ele precisa **cobrir a logística nova**. Se não cobrir, a edição é recusada até você ajustá-lo.
* **A remarcação passa por uma nova checagem de disponibilidade.** Se a data nova cair numa janela em que o material já está comprometido, o LocFlow **não deixa salvar** (*"Não há estoque disponível para todos os itens na janela de uso"*).

Os efeitos completos de mexer num pedido fechado — no roteiro, no estoque e no parceiro — estão em [Quando um pedido muda depois de fechado](../logistica/quando-um-pedido-muda.md#mudar-a-data).

## Quando a data ainda não está combinada {#a-definir}

Nem todo orçamento já nasce com data fechada — e não precisa. Enquanto você não escolhe a data de um movimento, ele fica **a definir**: a linha mostra a pergunta (**Quando entregar?**, **Quando recolher?**, **Quando o cliente retira?**, **Quando o cliente devolve?**) com um lembrete discreto do prazo. Não existe opção a marcar — não escolher já é o "a definir", e o **x** do campo de data desfaz uma escolha e volta a ele.

| Situação | O que o LocFlow lembra |
| --- | --- |
| Entrega pela equipe, locação | *Defina a entrega até a reserva do orçamento* |
| Entrega pela equipe, venda | *Defina a entrega até a venda do orçamento* |
| Recolha pela equipe | *Defina a retirada até a reserva do orçamento* |
| Retirada na loja (locação) | *Defina a data da retirada na loja até a reserva do orçamento* |
| Retirada na loja (venda) | *Defina a data da retirada na loja até a venda do orçamento* |
| Devolução na loja | *Defina a data da devolução na loja até a reserva do orçamento* |

Em outras palavras: você pode mandar o orçamento para o cliente **sem** a data fechada, mas precisa defini-la **antes de ganhar o pedido** (reservar, na locação; vender, na venda). O sistema te cobra na hora certa — não antes: ao reservar ou vender, se faltar, o campo abre sozinho com o aviso âmbar do que falta (por exemplo, *"Informe o dia e a janela de horário da entrega."*).

{% hint style="success" %}
**Para quem está começando:** não trave seu orçamento esperando o cliente decidir a data. Deixe a data em aberto, envie a proposta e preencha quando ele confirmar. O prazo só aperta no fechamento.
{% endhint %}

## O galpão de origem (de onde sai a carga) {#galpao-de-origem}

Toda saída pela equipe parte de **algum galpão**. No LocFlow, quem **sugere** a origem é o sistema: o galpão que tem o material do pedido e, entre iguais, o **mais perto do cliente**. Quem vende não precisa decidir logística para salvar a proposta.

Onde essa escolha aparece depende de quantos galpões você tem e de como a sua organização configurou a **Seleção de origens**, no Motor de Estoque:

| Situação | O que você vê na Saída do material |
| --- | --- |
| **Um galpão só** | Nada a escolher: ele é a origem. |
| **Vários galpões, seleção Manual** *(o padrão)* | O bloco **Sai de** aparece no pedido, com o galpão sugerido, o **Trocar** e os galpões de apoio — a escolha final é sua. |
| **Vários galpões, seleção Automática** | O sistema escolhe a saída e completa a rota com os galpões que alcançam o endereço do cliente; o bloco fica guardado em **Operação avançada**, no fim da seção. |

Um erro de galpão sempre abre o bloco, onde quer que ele esteja — ninguém corrige o que está escondido. Veja a configuração em [Motores operacionais](../configuracoes/motores-operacionais.md#motor-de-estoque).

### Um pedido pode somar o estoque de vários galpões {#varios-galpoes}

Ao conferir se há material para o pedido, o carrinho soma **o que a sua empresa tem**, não o que está num galpão só. Um pedido de 200 com 180 no galpão A e 20 no B é atendido — a conta é a mesma que você faz de cabeça: *"eu tenho isso?"*. As exceções são de propósito: quando o **cliente retira na loja**, conta o que está ao alcance daquela loja — o estoque dela ou, se ela não guarda estoque, o do galpão que a abastece (é lá que ele vai buscar); com a **Seleção de origens Automática**, só entram os galpões cujo raio alcança o cliente; e, depois que o pedido é **ganho**, a conta passa a olhar a rota de origens que ficou gravada para ele (veja abaixo).

Quando o pedido é **ganho**, o LocFlow decide de onde sai cada parte e grava essa rota de origens: o galpão principal e, se for preciso, os **galpões de apoio** por onde a viagem passa para completar a carga. De onde sai o material é assunto da **operação**, não da venda.

Isso chega ao [planejamento do roteiro](../logistica/planejando-o-roteiro.md) do jeito natural: o roteiro tem um **galpão-base** (de onde a equipe sai e para onde volta) e pode ter **galpões de apoio** no caminho. A regra é uma só:

> **Todo galpão de que um movimento precisa tem de estar na rota do roteiro** (base + apoios).

Se faltar algum, o app diz exatamente qual: *"O movimento precisa do galpão X, que não está na rota do roteiro (base + apoios). Adicione o galpão à rota ou remova o movimento."* — e você resolve acrescentando o galpão à rota, sem precisar quebrar o roteiro em dois.

{% hint style="info" %}
**Como isso fica na rua.** A equipe sai do galpão-base já carregada, para num galpão de apoio para pegar o que falta e segue para as entregas. Em cada parada de galpão o motorista **registra o que carregou ali** — é assim que o estoque de cada galpão baixa pelo que de fato saiu de lá, e não por estimativa.
{% endhint %}

### Os estados de disponibilidade

Com o bloco da origem à vista, cada galpão aparece com um indicador do que o sistema sabe sobre ele em relação ao destino:

| O que você vê | O que significa |
| --- | --- |
| **Cobertura não avaliada** | Ainda não deu para medir — falta o destino ou a localização dele. O botão **Avaliar cobertura** faz a conta. |
| **Dentro da área de atendimento** | O galpão **cobre** aquele destino — a distância está dentro do raio que você cadastrou para ele. No galpão escolhido, aparece como **Cobre o destino**. |
| **Fora do raio de atendimento** | O destino está **mais longe** do que o raio do galpão. **Não bloqueia**: o app avisa — *"Este galpão está fora do raio de atendimento do destino. Você pode seguir assim mesmo."* |

{% hint style="info" %}
Antes de informar o destino, o bloco espera: *"Informe o destino para avaliar a cobertura dos galpões."* Quando o endereço já tem a localização, a cobertura do galpão escolhido é conferida sem custo; o **Avaliar cobertura** mede a distância de cada galpão até o destino e ordena a lista **pelo mais próximo**.
{% endhint %}

Com a origem fora da tela (um galpão só, ou a seleção Automática), o aviso aparece junto do endereço — por exemplo: *"O endereço está fora do raio de atendimento do galpão Central. Ajuste em Operação avançada ou confirme mesmo assim."*

### Quando nenhum galpão alcança

Se, depois de avaliar, **nenhum** dos seus galpões cobre o destino, o LocFlow diz — *"Nenhum galpão cobre este destino. Confira o endereço acima, ou ajuste o raio de atendimento em Estoque › Galpões."* — e mesmo assim deixa você escolher a origem em **Trocar**: ele avisa, não trava. Confira primeiro o endereço (talvez o pino esteja fora do lugar) e, se ele estiver certo, reveja o raio dos galpões em [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md).

{% hint style="warning" %}
**Avaliar a cobertura consome créditos.** O cálculo usa o mapa; por isso o app pergunta antes, mostrando até quantos créditos a avaliação pode consumir. Avaliar é opcional: sem ela nada trava, e a cobertura do galpão escolhido continua sendo conferida pela localização que o endereço já tem.
{% endhint %}

### Reavaliar quando algo muda

Se você mexer no destino depois de avaliar — trocar o endereço ou arrastar o pino —, a lista fica desatualizada e o botão vira **Reavaliar cobertura**. O galpão escolhido **não é desmarcado** por sair do raio: o app avisa, e a decisão continua sua. Se a origem tinha sido escolhida pelo sistema, ele pode trocá-la pela mais adequada ao endereço novo; se foi você quem escolheu (pelo **Trocar**), ela fica.

## Espelhar o trajeto no retorno (locação) {#espelhar}

Na locação, o retorno costuma sair do **mesmo lugar** da entrega. Para não fazer você digitar tudo de novo, o **Retorno do material** **espelha** a entrega por padrão: aparece a linha **Volta pelo mesmo trajeto, invertido** — do endereço da entrega de volta ao galpão — e você só define **quando recolher**.

- **Editar** abre o trajeto do retorno, para você mudar o endereço de recolha (**De onde recolher?**) ou o galpão para onde a carga volta.
- **Voltar a espelhar** desfaz a diferença e volta ao mesmo trajeto da entrega.

{% hint style="info" %}
Se o cliente **retira na loja** (não há entrega pela equipe), não existe trajeto para espelhar — a recolha com deslocamento pede destino e galpão próprios.
{% endhint %}

## Por porte: como cada operação usa esta seção

| Seu perfil | Como aproveitar |
| --- | --- |
| **Autônomo / pequeno** | Um galpão, datas em aberto até o cliente confirmar, faixa pelo horário comercial. O sistema escolhe o galpão e a faixa por você. |
| **Médio** | Vários galpões com raios bem cadastrados, períodos do dia (Manhã/Tarde) para padronizar as faixas, e o *Já está combinado com o cliente?* respondido para o roteiro confiar nos horários. |
| **Grande** | A origem conferida no bloco **Sai de** (ou entregue à seleção automática), faixas personalizadas para casos especiais e a folga mínima protegendo a operação de janelas apertadas em escala. |

## Situações reais

**"Vendi um lote de cadeiras usadas."** Orçamento de **venda**: só há a **Saída do material**. Escolha o destino e a data; o galpão de saída o sistema sugere. Sem retorno — o item sai em definitivo.

**"Aluguel de palco, o cliente busca e devolve na loja."** Em **Quem leva o material?**, escolha **Cliente retira** — o retorno já vira **Cliente devolve**. Some o endereço de destino dos dois lados; você só informa a loja e as datas de retirada e devolução.

**"Entrega e retirada no mesmo endereço."** Deixe o retorno **espelhar** a entrega (o padrão na locação). Mexa só no **quando recolher**.

**"O cliente ainda não decidiu a data."** Não escolha a data dos movimentos — eles ficam **a definir**. Envie o orçamento; defina as datas antes de **reservar** (locação) ou **vender** (venda).

**"O endereço ficou longe e nenhum galpão atende."** Confira o pino do destino. Se estiver certo, talvez seja o caso de ampliar o raio de um galpão em [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md) — enquanto isso, o app avisa, mas deixa seguir.

## Próximo passo

- [Criando um orçamento](criando-um-orcamento.md) — os movimentos no contexto do orçamento inteiro.
- [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md) — cadastrar raio e endereço dos seus galpões.
- [Horários e sazonalidades](../configuracoes/horarios-e-sazonalidades.md) — montar o horário comercial e os períodos do dia.
- [Visão geral da logística](../logistica/visao-geral.md) — o que acontece com os movimentos depois do pedido fechado.
