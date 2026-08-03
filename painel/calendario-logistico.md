---
icon: calendar-days
description: O calendário logístico mostra cada movimento real da sua operação — entrega e retirada, viagem por viagem — e a cor diz em que pé cada um está no ciclo, do livre ao concluído.
---

# Calendário logístico

O **calendário logístico** é a sua agenda da operação — o lugar em que se entra **todo dia**. Ele mostra, dia a dia, **cada movimento real**: uma entrega ou uma retirada de um pedido ganho. A **cor** diz em que pé aquele movimento está no ciclo operacional; o **âmbar com ⚠** diz exatamente onde agir primeiro.

É a leitura que responde "**o que eu preciso organizar para os próximos dias?**" — sem abrir pedido por pedido.

{% hint style="info" %}
Este calendário é **só de logística** — entrega e retirada de [itens](../primeiros-passos/glossario.md). Ele **não** mostra a chance de fechar um orçamento (isso vive no [funil de vendas](../orcamentos/acompanhando-e-fechando.md)). Aqui tudo já é movimento de material a organizar.
{% endhint %}

{% hint style="success" %}
**Quando há movimento urgente, o próprio menu avisa:** o item **Calendário** acende um **sinal vermelho de atenção**. Sem número, de propósito — quem diz *quais* e *quantos* é a própria grade, pelos ⚠. Sinal apagado = nada vencendo; pode seguir o dia.
{% endhint %}

## O que o calendário mostra <a id="o-que-e-o-calendario"></a>

A unidade do calendário é o **movimento real** — não o orçamento, não o roteiro. Cada entrega e cada retirada de um pedido ganho vira **uma barra própria** na grade.

E quando a carga foi **dividida em viagens** (não coube num veículo só), **cada viagem é um movimento**: você vê "V1/2", "V2/2" — porque a viagem 1 pode já estar num roteiro enquanto a viagem 2 segue livre. O rótulo aparece na grade, na visão dia e no detalhe, para você nunca confundir o que está resolvido com o que ainda falta.

Tocar num movimento abre os **detalhes do orçamento**: de onde ele veio, o que foi combinado, em que pé está **aquela viagem** e qual roteiro a carrega — e de lá você abre o orçamento, a logística ou o roteiro.

{% hint style="info" %}
Os dados são **reais**: vêm direto dos seus orçamentos ganhos e roteiros. O que você vê é a sua operação.
{% endhint %}

## Como ler a cor: o ciclo do movimento <a id="como-ler-cores-niveis"></a>

A cor resume **em que etapa do ciclo operacional** o movimento está:

| Cor | Estado | O que significa | Sua ação |
| --- | --- | --- | --- |
| **Âmbar** | **Livre (sem roteiro)** | O movimento existe e ainda **não entrou** num roteiro | **Planejar** |
| **Âmbar + ⚠** | **Urgente** | Livre com a janela começando em **menos de 48h** | **Planejar JÁ** |
| **Verde** | **Em roteiro** | Já está num roteiro planejado (dia, veículo, equipe) | Aguardar a saída |
| **Teal** | **Em execução** | O roteiro dele está **na rua agora** | Acompanhar |
| **Cinza** | **Concluído** | **Já aconteceu** — ancorado na hora real do registro | Histórico |
| **Azul** | **Cliente no galpão** | O cliente vem **retirar ou devolver** no seu galpão | Só receber |

{% hint style="warning" %}
O **âmbar** é o seu sinal de ação — e o **⚠** é a fila de prioridade dela. Abra o calendário, ataque os ⚠ primeiro, depois os âmbares dos próximos dias.
{% endhint %}

{% hint style="info" %}
**Azul é outra conversa.** Cliente no galpão **nunca entra em roteiro** e **nunca vira urgência de planejamento** — não há rota a montar; o compromisso é estar pronto para receber. Por isso ele tem cor própria, fora da escala do ciclo.
{% endhint %}

## As setas: o que acontece <a id="os-icones-quem-e-responsavel"></a>

Cada movimento traz uma **seta** — as mesmas do mapa do roteiro:

| Seta | Significa |
| --- | --- |
| **↗ (sai)** | O material **sai** — nossa equipe entrega, ou o cliente retira no galpão. |
| **↙ (volta)** | O material **volta** — nossa equipe recolhe, ou o cliente devolve no galpão. |

**O que acontece** você lê pela seta; **quem opera** você lê pela **cor** (azul = cliente no galpão; as demais = o ciclo da equipe).

A cronologia de um aluguel é sempre **entrega(s) → evento → retirada**; uma [venda](../conceitos/locacao-e-venda.md) tem **só a entrega** (o item sai em definitivo, sem retirada).

## O evento do cliente vive no detalhe <a id="evento-no-detalhe"></a>

O calendário é de **movimentos** — o **evento** (a data do cliente que o aluguel atende) não ocupa a grade. Ele aparece ao abrir os **detalhes do orçamento**, na linha do tempo, sempre **entre a entrega e a retirada**.

{% hint style="info" %}
**Evento sem horário informado aparece como "sem horário informado"** — nunca como meia-noite ou outro horário inventado. Com início e fim informados, você vê o intervalo; com só uma ponta, "a partir de HH:mm" ou "até HH:mm".
{% endhint %}

## Selecionar direto do calendário <a id="selecionar-para-planejar"></a>

Movimento **livre** (âmbar) pode ser **selecionado para o planejamento** direto do calendário ou da lista de movimentos — a seleção é a **mesma** nas duas telas, e o movimento selecionado ganha um **selo de check** na banda.

A unidade da seleção é a **viagem**: selecionar a viagem 2 **não arrasta** a viagem 1 (cada roteiro é a rota de **um** veículo — viagens irmãs normalmente saem em roteiros distintos, ao mesmo tempo). Ao montar um roteiro, a viagem usada sai da seleção; as irmãs **ficam**, prontas para o próximo.

{% hint style="info" %}
Só entra na seleção o que **pode ser roteirizado agora**. Uma retirada cuja entrega ainda nem saiu aparece no calendário (você enxerga o futuro), mas a seleção fica indisponível com o motivo: *aguarda a etapa anterior*.
{% endhint %}

## Adaptado à sua forma de operação <a id="adaptado-a-operacao"></a>

O calendário **fala a língua da sua operação**, conforme a **Forma de operação** do [Motor de Logística](../configuracoes/motores-operacionais.md):

* **Só no balcão**: não há rota a planejar — o calendário fala em **atendimentos** (retirada e devolução no galpão), e a escala do ciclo nem aparece na legenda.
* **Só pela equipe**: o foco é o ciclo Livre → Em roteiro → Em execução → Concluído.
* **Mista**: os dois convivem.

Em todos os casos a **legenda é dinâmica**: mostra só o que **existe** no conjunto que você está vendo — sem ensinar símbolo que não está na tela.

## A janela: combinada × estimada <a id="janela-combinada-x-estimada"></a>

O **traço** de cada janela de horário diz se aquele intervalo já foi **fechado com o cliente**:

* **Linha cheia = combinada com o cliente.** Ex.: o cliente confirmou a entrega entre 9h e 11h — a janela está fechada.
* **Linha pontilhada = estimada.** Ainda **não foi alinhada com o cliente** — é a sua previsão e **pode mudar**.

## O fuso horário <a id="fuso-horario"></a>

Os horários aparecem no **fuso da operação** (indicado no topo). Quando um movimento foi **combinado em outro fuso** — por exemplo, um cliente em outra região do país —, um **selo** indica o fuso original, para você não se confundir na hora de ligar para confirmar.

## Mês, dia e tela cheia <a id="mes-dia-e-tela-cheia"></a>

O calendário tem duas visões, alternadas no topo:

* **Mês** — a visão geral: cada **movimento** é uma barra no seu intervalo; quando barras se sobrepõem no tempo, aparecem **uma abaixo da outra**. Tocar numa barra abre o detalhe daquela viagem.
* **Dia** — a agenda daquele dia, hora a hora, com **uma raia por roteiro**: é onde você confere a sequência real de uma saída (e os rótulos **V1/2** dizem qual viagem é qual).

Há ainda o botão de **tela cheia**, que abre o calendário numa tela dedicada (estilo agenda) — útil em telas grandes para enxergar a semana inteira de uma vez.

{% hint style="info" %}
**Em telas estreitas (celular), cada dia vira um resumo.** Em vez das barras com horário, cada dia mostra só os **ícones dos fatos** ("↗ › ↙") — o que acontece em cada dia; quem opera você lê pela cor. Para horários e janelas, **toque o dia**.
{% endhint %}

## Filtros <a id="filtros"></a>

O botão de **filtros** recorta o que está na tela — e mostra ao lado só o que está aplicado:

* **Tipos** — livre (sem roteiro), em roteiro, concluído.
* **Galpões** — quando você tem mais de um, filtrar por galpão de origem.
* **Quem opera** — só a equipe, ou só cliente no galpão.
* **Natureza** — aluguel ou venda.

Há também o botão de **legenda** (mostrar/ocultar), que exibe a escala de cores, as setas e os traços diretamente sobre o calendário.

## Como planejar o dia e a semana <a id="planejar-o-dia-e-a-semana"></a>

Uma rotina simples para usar o calendário todo dia:

1. **Olhe o menu:** se o Calendário está com o **sinal vermelho**, há urgência esperando.
2. **Abra na visão Mês** e ataque os **⚠** primeiro: são movimentos livres com a janela em menos de 48h. Selecione-os e monte um [roteiro planejado](../logistica/planejando-o-roteiro.md).
3. **Depois, os âmbares** dos próximos dias — planeje antes que virem ⚠.
4. **Olhe os pontilhados:** janelas ainda não confirmadas com o cliente. Confirme as dos próximos dias.
5. **Confie no verde e no teal:** em roteiro e na rua — é acompanhar, não mexer.

## Por porte

| Porte | Como o calendário te serve |
| --- | --- |
| **Começando** | Poucos movimentos, quase tudo âmbar. O calendário já te diz o que planejar antes de cada entrega. |
| **Crescendo** | Vários roteiros por semana se sobrepondo. As barras por viagem e o filtro por galpão evitam que algo passe batido. |
| **Estruturado** | Operação cheia, vários galpões e fusos. A tela cheia e os filtros viram a sua mesa de controle do dia. |

## Situações reais <a id="situacoes-reais"></a>

* **Entrega da semana sem roteiro:** o pedido foi ganho e a entrega aparece **âmbar**. Selecione-a e monte o roteiro → vira **verde**.
* **Janela em menos de 48h:** o âmbar ganha o **⚠** (e o menu acende o sinal). É o primeiro item do seu dia.
* **Carga dividida:** a viagem 1 saiu no ROT-7 (**verde/teal**) e a viagem 2 segue **âmbar** — o calendário mostra as duas separadas ("V1/2" e "V2/2"), e você seleciona só a que falta.
* **Cliente retira no galpão:** sem rota — o movimento aparece **azul**; você só confirma a janela em que ele vem buscar.
* **Locação de evento em outra cidade:** o horário foi combinado no fuso do cliente. O calendário mostra no **fuso da sua operação** e exibe o **selo** do fuso original.

## Próximo passo <a id="proximo-passo"></a>

* Para transformar os **âmbares** em verde: [Planejando o roteiro](../logistica/planejando-o-roteiro.md).
* Para entender as fases por trás de cada movimento: [Visão geral da logística](../logistica/visao-geral.md).
* Para a chance de **fechar** um orçamento (que **não** está aqui): [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md).
