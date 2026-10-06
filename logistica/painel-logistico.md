---
icon: table-columns
description: A operação inteira numa tela — um recorte só (período, mundo, filtros) e seis jeitos de olhar para ele: mapa, mês, dia, lista, kanban e tabela.
---

# Painel Logístico

O **Painel Logístico** é a mesa de controle da logística. Ele responde, numa tela só, às perguntas do dia: **quanto trabalho existe**, **onde** o material precisa estar, **quando** cada coisa acontece e **em que pé** está cada pedido — sem abrir orçamento por orçamento.

Você o encontra no menu **Logística › Painel Logístico**. Ele aparece para quem pode ver roteiros. Numa operação que só atende na loja (o cliente sempre retira e devolve presencialmente), a mesma tela se chama **Atendimentos**: ali não há rota a planejar, e o vocabulário acompanha.

{% hint style="success" %}
**Por que isso te ajuda:** o calendário, o mapa, a fila e o quadro de etapas eram telas separadas, cada uma com o seu filtro. Agora todas olham para **o mesmo recorte** — os números do topo, os cartões de baixo e a visão do meio sempre falam do mesmo universo. Você troca o jeito de olhar sem perder o que já filtrou.
{% endhint %}

## Um recorte, seis visões <a id="seis-visoes"></a>

A ideia central é simples: **você recorta uma vez** (período, mundo, filtros, busca) e **escolhe como enxergar** esse recorte. Trocar de visão **nunca muda a conta** — só a forma de olhar.

| Visão | A pergunta que ela responde | Quando usar |
| --- | --- | --- |
| **Mapa** | Onde o material precisa estar | Para ver a distribuição do dia e escolher o que planejar junto. |
| **Mês** | Quando cada coisa acontece | Para enxergar o volume da semana e do mês e achar os picos. |
| **Dia** | A que horas, hora a hora | Para conferir a agenda de um dia, com o marcador de **agora**. |
| **Lista** | Tudo em ordem, para conferir | Para passar pelos movimentos um a um, com o selo de urgência. |
| **Kanban** | Em que pé está cada pedido | Para acompanhar (e avançar) as etapas de cada pedido. |
| **Tabela** | Colunas que você escolhe | Em telas largas, para ler muitos movimentos de uma vez. |

{% hint style="info" %}
**A Tabela só aparece em tela larga** (computador ou tablet deitado). No celular, a Lista responde à mesma pergunta em cartões — e um link que abra a Tabela no telefone cai direto na Lista.
{% endhint %}

O painel **lembra a última visão** que você usou **neste aparelho**. Na primeira vez, ele abre no **Mapa** (ou na **Lista**, numa operação só de loja), e o período começa em **Amanhã** — a pergunta das sete da manhã costuma ser "o que sai amanhã?".

Enquanto os dados chegam, a tela mostra um **esqueleto** no lugar dos números: ela nunca afirma "zero entregas" antes de saber.

## O filtro: tudo num lugar só <a id="filtros"></a>

Todos os recortes moram num botão só, **Filtros**. O número no botão diz **quantos recortes estão ligados**. A **busca** fica fora, ao lado: ela é uma pergunta aberta (um cliente, um código), não um recorte. E **Limpar filtros** desfaz tudo de uma vez — recortes, busca, janela de horário e seleção — e, se você tinha escolhido datas, devolve o período ao padrão.

| Grupo | O que recorta |
| --- | --- |
| **Período** | **Hoje**, **Amanhã**, **7 dias**, **Período** (você escolhe as datas) ou **Tudo**. |
| **Mundo da operação** | **Na rota** (nós levamos), **Na loja** (o cliente vem à loja) ou **Tudo** (os dois mundos). |
| **Tipo** | Entregas ou retiradas. No mundo da loja, as palavras mudam para **Retiradas** e **Devoluções**. |
| **Estado** | Livres, em roteiro, em execução ou concluídos. Na loja: **A atender** ou **Concluídos**. |
| **Loja ou base** | Uma ou mais lojas e galpões de saída que aparecem no recorte. |
| **Procedência** | O que é da sua estrutura × o que está com a [Rede de Parceiros](../parcerias/visao-geral.md) — e de quais parceiros. Só aparece para quem vê os acordos de parceria. |

{% hint style="info" %}
**Os dois mundos, ditos em voz alta.** O trabalho que a sua equipe **leva** até o cliente e o que o cliente **vem buscar** na loja são operações diferentes — e o painel nunca os soma sem dizer. Se a sua operação só trabalha num dos mundos, no lugar da escolha aparece uma faixa que diz qual é (por exemplo, *"esta operação entrega e recolhe no endereço do cliente"*).
{% endhint %}

## A faixa de números <a id="faixa-de-numeros"></a>

No topo, a faixa resume o recorte: **entregas**, **retiradas** e **itens** — sempre **por mundo**. A carga que a sua equipe leva (itens em veículo seu) e a que o cliente busca na loja têm cada uma a sua conta.

* Vendo **Tudo**, aparecem os dois blocos; **tocar num bloco** mostra só aquele mundo.
* **Tocar no número de itens** abre a lista com **produto e quantidade** — no navegador, dá para baixá-la em planilha (CSV).
* Quando há movimentos livres no recorte, o atalho **Selecionar N sem roteiro** leva todos eles de uma vez para a seleção do [planejamento](planejando-o-roteiro.md). Dá para desfazer pelo aviso que aparece.

## Como ler as cores <a id="cores"></a>

Nas visões **Dia** e **Lista**, a cor diz **em que etapa do ciclo** o movimento está (na **Tabela**, a coluna **Situação** diz o mesmo em texto, e o ⚠ e a marca de atraso aparecem ao lado do código):

| Cor | Estado | O que significa | Sua ação |
| --- | --- | --- | --- |
| **Âmbar** | **Livre** (sem roteiro) | O movimento existe e ainda não entrou num roteiro. | Planejar |
| **Vermelho com ⚠** | **Urgente** | Livre, e a janela começa em menos de **4 horas** (ou o prazo que a sua operação definiu) — ou já começou, mas ainda não virou atraso. | Planejar já |
| **Marrom, com ícone de histórico** | **Atrasado** | A janela abriu há mais de **24 horas** (ou o prazo que a sua operação definiu) e segue sem roteiro. | Conferir o que aconteceu |
| **Verde** | **Em roteiro** | Já está num roteiro planejado. | Aguardar a saída |
| **Verde-azulado** | **Em execução** | O roteiro dele está na rua agora. | Acompanhar |
| **Cinza** | **Concluído** | Já aconteceu. | Histórico |
| **Azul** | **Cliente na loja** | O cliente vem retirar ou devolver na loja. Nunca entra em roteiro. | Só receber |

{% hint style="warning" %}
**Urgente e atrasado não são a mesma coisa.** Urgente ainda dá para atender: saindo agora, o combinado é cumprido. Atrasado é a janela que já passou sem roteiro — não há mais o que planejar dentro do combinado; o que se faz é **conferir**: foi executado e ninguém registrou? O pedido morreu? Os dois prazos são da sua operação: ajuste em **Ajustes › Motores › Logística › Urgência e atraso** (veja [Urgência e atraso](../configuracoes/motores-operacionais.md#urgencia-e-atraso)).
{% endhint %}

Além da cor:

* **As setas dizem o que acontece:** **↗** o material **sai** (a equipe entrega, ou o cliente retira na loja); **↙** o material **volta** (a equipe recolhe, ou o cliente devolve na loja).
* **A janela diz se foi combinada:** ao lado do horário, **combinado** (com o ícone de aperto de mãos) = horário **acertado com o cliente**; **estimado** (com a ampulheta) = previsão, que ainda pode mudar.
* **Carga dividida em viagens** aparece como um movimento por viagem (*"V1/2"*, *"V2/2"*): a viagem 1 pode já estar num roteiro enquanto a 2 segue livre. Veja [Cargas e viagens](planejando-o-roteiro.md#cargas-e-viagens).
* Os horários seguem o **fuso da operação** — o marcador **agora** do Dia também, mesmo que o aparelho esteja em outro fuso.

## O Mapa <a id="mapa"></a>

O Mapa mostra onde cada entrega e cada retirada do recorte precisa acontecer. Aqui o pino é um **círculo**, e cada parte dele diz uma coisa só:

| Parte do pino | O que diz |
| --- | --- |
| **Preenchimento** | **De quem é o trabalho:** branco = da sua equipe; **magenta** = está com a Rede de Parceiros (quem leva é o parceiro). |
| **Seta** | **O que acontece:** ↗ o material sai; ↙ o material volta. |
| **Anel** | **O estado:** cinza = livre (pode entrar num roteiro); roxo = em roteiro ou em execução; roxo grosso = selecionado para planejar. |
| **Esmaecido** | O que **já aconteceu**. |

* O **galpão de saída** é o marcador roxo. O cliente que vem **à loja** não vira pino próprio: ele aparece no **marcador azul da loja**, que cresce com o que está pendente lá.
* No computador, **passar o mouse** num pino mostra um relance; **tocar** (ou clicar) abre a [ficha do movimento](#ficha-do-movimento).
* Quando vários movimentos ficam um em cima do outro, o mapa mostra um pino com o **número**: tocar nele **aproxima** até separá-los — e, se eles dividem o mesmo endereço, abre a lista para você escolher qual ver.
* O **laço** (ferramenta do canto do mapa; no computador, tecla **S**) cerca uma região e seleciona de uma vez o que pode ser planejado. A seleção anterior pode ser desfeita pelo aviso.
* As **camadas** escondem entregas, retiradas, o que já está em roteiro ou as lojas — só do desenho; os números do topo continuam os mesmos.

{% hint style="info" %}
**Endereço sem ponto no mapa não some.** Ele é contado numa tarja no topo do mapa, que lista quais são — listar é de graça. **Resolver** a localização usa o mapa por trás do app e consome **1 crédito por endereço novo** (endereços já resolvidos não custam nada). Dá para resolver um por vez ou todos de uma vez, sempre com o custo na tela antes de você aceitar. Endereço sem CEP, rua ou cidade não ganha o botão: resolvê-lo gastaria crédito sem achar nada. Veja [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md).
{% endhint %}

{% hint style="warning" %}
**Não confunda com o mapa do planejamento.** Quando você [planeja um roteiro](planejando-o-roteiro.md), o pino é numerado e a cor diz a **ordem da parada** — o mesmo azul que no Painel é "a loja", lá é "parada 1". São duas linguagens, de propósito, e elas não dividem a mesma tela.
{% endhint %}

## Mês e Dia <a id="mes-e-dia"></a>

* **Mês** mostra o **volume**: cada dia traz as contagens por mundo (por exemplo, *"12↑ 7↓"* da rota e *"5 loja"*) e mini-barras escaladas pelo maior dia — o pico salta aos olhos. Aqui a cor diz o **tipo**, não o estado: verde para o que sai, âmbar para o que volta e azul para a loja. **Tocar num dia** recorta o período para ele.
* **Dia** abre a agenda daquele dia, **hora a hora**, com o marcador **agora** quando é hoje. É onde você confere a sequência real de uma saída.

## Lista, Kanban e Tabela <a id="lista-kanban-tabela"></a>

**Lista** — todos os movimentos do recorte em ordem, com o selo de urgência e, nos pedidos da Rede, o nome de quem está com o trabalho. É a visão para conferir, item por item.

**Kanban** — um quadro com **uma coluna por etapa** do pedido. A **cor do cabeçalho da coluna** é a **fase** da operação (no galpão, na conferência, na rua, encerrado) e serve para você achar o bloco certo rolando o quadro. O **cartão** é que fala do pedido: a etapa real e se ele **pode avançar** — quando não pode, o cartão diz por quê. Um pedido **misto** (parte o cliente leva, parte a equipe entrega) aparece nos dois mundos, sempre na **mesma coluna**: a etapa é do pedido, e o pedido é um só.

**Tabela** — as colunas que você escolhe (janela, situação, onde, itens, galpão, procedência, roteiro e, para os livres, *"por que não planeja"*). Só em tela larga.

### Avançar uma etapa pelo Kanban <a id="avancar-pelo-kanban"></a>

O Kanban também **registra o que aconteceu fora do app** — por exemplo, a entrega que a equipe fez sem registrar na rua. Arrastar um cartão para a etapa seguinte (ou tocar nele e escolher a ação) abre uma folha curta:

1. **Quando aconteceu** — **Agora** (já vem marcado) ou **Outro momento**, com data e hora. Dá para registrar "a retirada foi ontem".
2. **Por que registrar agora** e o **aceite** de que o registro tem efeitos reais (baixa de estoque, cobrança, repasse ao parceiro) — pedidos só quando o avanço **fecha** a entrega ou a retirada, ou quando você **encerra** o pedido.
3. **Quem executou** (opcional) — o motorista e o veículo, nas etapas de rua.
4. Se a sua política exige prova e ela não existe, quem tem a permissão de dispensar escreve o **motivo da dispensa**.

{% hint style="info" %}
**Mover cartões pede a mesma permissão do registro retroativo** — a da [execução em lote](execucao-em-lote.md). Quem não a tem acompanha o quadro, mas não move os cartões (o próprio quadro avisa). Duas etapas não andam por arraste: a **conferência de retorno** é registrada item a item na tela de [Conferência](conferencia.md) (o cartão leva até lá), e o **atendimento na loja** é confirmado por quem opera a loja — no próprio cartão (**Confirmar retirada** ou **Confirmar devolução**) ou na fila da [Loja](balcao.md).
{% endhint %}

Ao levar um pedido para **A conferir**, a conferência de retorno abre normalmente — mesmo que você registre que a retirada foi ontem. Se ela **não puder abrir** (por exemplo, o pedido não tem galpão ou loja de devolução), a etapa avança e o aviso sai **em âmbar**, dizendo o motivo, no lugar do "Etapa avançada." em verde. Veja [Quando a conferência não abre](conferencia.md#quando-a-conferencia-nao-abre).

## A ficha do movimento <a id="ficha-do-movimento"></a>

Tocar num movimento, em qualquer visão, abre a **ficha** dele — numa **coluna ao lado** em telas largas, numa **folha que sobe de baixo** no celular. Ela mostra a janela (combinada ou estimada), o endereço, o estado, o roteiro que o leva (ou por que ainda não está em nenhum), as viagens e a trajetória do movimento (correções depois de uma edição do pedido, novas tentativas e a execução). Conforme o caso e as suas permissões, dali você:

* **Adiciona ao planejamento** (ou remove) — e, com vários selecionados, **planeja um roteiro** com todos;
* **Inclui num roteiro** que já existe ou **cria um roteiro** só com ele;
* **Abre na Loja**, quando é o cliente que vem retirar ou devolver;
* Abre o **orçamento** ou a [logística do pedido](jornada-do-pedido.md).

## Os cartões da operação <a id="cartoes-da-operacao"></a>

Abaixo da visão ficam os **cartões da operação** — cortes do mesmo recorte, que você liga, desliga e reordena em **Personalizar** (a escolha fica guardada para você, naquela organização):

| Cartão | O que mostra |
| --- | --- |
| **Movimentos por hora** | Quantos movimentos caem em cada hora. Ele tem um **pincel**: arrastar sobre as barras recorta uma **janela de horário** (ou de dias, quando o período tem vários), e todas as visões passam a falar só dela. |
| **Por região da entrega** | De onde vem o volume da rota — por cidade, ou por bairro quando tudo é numa cidade só. |
| **Itens da carga** | Os produtos e as quantidades do recorte. |
| **Movimentação por loja** | O que passa por cada loja. |
| **Pronto para o cliente** | Quantos atendimentos da loja já estão separados esperando o cliente, contra os que ainda faltam separar. |
| **Dias vizinhos** | O volume dos dias em volta do período, para ver se amanhã é o pico da semana. Tocar num dia recorta o período para ele. |
| **Roteirizado vs solto** | Dos movimentos que podem entrar num roteiro, quantos já têm um. |

**Dias vizinhos** e **Roteirizado vs solto** começam desligados — ligue-os em **Personalizar**. Cartão de um mundo que a sua operação não tem **não aparece** — nem no Personalizar. E cartão que não teria o que mostrar no recorte atual sai da tira, para um cartão cheio de zeros não ser lido como problema.

## Os pedidos da Rede de Parceiros <a id="rede"></a>

Um pedido [repassado pela rede](../parcerias/repassando-um-pedido.md) é marcado em **magenta** em todas as visões: o selo com o elo (⛓) e o nome de quem está com o trabalho na Lista e no Dia; só o elo no Kanban e na Tabela (que pode mostrar a coluna **Procedência**); no Mês, um ponto magenta com quantos movimentos do dia correm pela rede; e o preenchimento do pino no Mapa. O texto do selo diz em que pé está o repasse: **Aguarda** (o parceiro ainda não aceitou), **Prazo expirou**, **Com** (a logística é dele agora) e **Rede ·** (já voltou).

{% hint style="info" %}
Nada disso aparece para quem **não tem permissão para ver a rede** — e, nesse caso, os pedidos repassados se parecem com os seus. É o que se quer: quem está na rua precisa saber onde entregar, não de quem é o contrato.
{% endhint %}

## Tela cheia <a id="tela-cheia"></a>

O botão **Tela cheia** amplia a visão e esconde o resto da página — útil para o mapa ou o mês num monitor grande. Mesmo em tela cheia, o **Filtros** e o **Limpar filtros** continuam à mão, e **Reduzir** volta ao normal.

## O sinal no menu <a id="sinal-no-menu"></a>

Quando há **movimento urgente sem roteiro**, o item **Painel Logístico** do menu acende um **sinal vermelho "!"**, sem número. Com o sinal aceso, o clique abre o painel direto na **Lista**, com o período alargado para trás — assim o movimento que acendeu o sinal está na tela, mesmo que a janela dele já tenha começado. Movimento **atrasado** não acende o sinal: ele tem marca própria no painel. Veja [Os números no menu](visao-geral.md#os-numeros-no-menu).

## Por porte <a id="por-porte"></a>

| Porte | Como o painel te serve |
| --- | --- |
| **Começando** | Abre o Mapa ou a Lista de amanhã, vê o que está âmbar e planeja. O filtro quase nunca é necessário. |
| **Crescendo** | O Mês mostra os picos da semana; o ⚠ diz o que planejar primeiro; o Kanban mostra quem está em que etapa. |
| **Estruturado** | Vários galpões, lojas e parceiros: o filtro por base e por procedência, a Tabela e os cartões viram a mesa de controle do dia. |

## Situações reais <a id="situacoes-reais"></a>

* **Sete da manhã, "o que sai amanhã?":** o painel já abre em Amanhã. No Mapa você vê os pinos livres (anel cinza) concentrados num bairro, dá um laço neles e leva tudo para o planejamento.
* **O menu acendeu o "!":** você toca no Painel Logístico, cai na Lista com os urgentes e planeja primeiro os que têm ⚠.
* **Semana de festa junina:** no Mês, a quinta e a sexta saltam aos olhos pelas mini-barras. Você toca na quinta e confere hora a hora no Dia.
* **A entrega foi feita sem o app:** no Kanban, você arrasta o cartão para *Entregue*, marca **Outro momento** com a hora real, escreve o motivo e informa quem levou.
* **Loja e rota no mesmo dia:** você escolhe **Na loja** no filtro e vê só quem vem buscar e devolver; o cartão **Pronto para o cliente** mostra o que já está separado.
* **Pedido com o parceiro:** o pino magenta mostra que a entrega daquele pedido é dele — você acompanha, mas quem planeja e executa é o parceiro.

## Próximo passo <a id="proximo-passo"></a>

Para transformar os âmbares em roteiro, veja [Planejando o roteiro](planejando-o-roteiro.md). Para acompanhar as viagens que já saíram, [Acompanhando seus roteiros](acompanhando-roteiros.md). Para o caminho completo de um pedido, a [Visão geral da logística](visao-geral.md).
