---
icon: filter
description: O funil do LocFlow — os estados do orçamento, a jornada com o próximo passo sugerido e como fechar (ganho, perda ou cancelamento).
---

# Acompanhando e fechando

Depois de criar a proposta, você acompanha cada orçamento até o fechamento. A tela de orçamentos tem duas visões: o **funil** (kanban, padrão) — colunas por etapa, onde você arrasta o card para mudar de fase — e a **lista** tradicional, com busca e filtros. Em ambas você abre as **Ações rápidas** de um orçamento para ver onde ele está, o que fazer a seguir e gerar documentos.

{% hint style="info" %}
O funil é de **uma natureza por vez** — alterne entre **Aluguel** e **Venda** no topo. Cada card mostra a **chance de fechar** (uma estimativa para você priorizar quem cobrar primeiro). Prefere a visão clássica? Alterne para **Lista**.
{% endhint %}

## Os estados do orçamento

Todo orçamento tem um **estado comercial** — onde ele está no funil. Os estados dependem da natureza (locação ou venda).

```mermaid
flowchart LR
    AB[Em aberto] --> NEG[Em negociacao]
    NEG --> PR[Pre-reservado<br/>opcional - locacao]
    PR --> RES[Reservado<br/>ganho - locacao]
    NEG --> RES
    AB --> RES
    NEG --> VEN[Vendido<br/>ganho - venda]
    AB --> VEN
    NEG --> PER[Perdido]
    AB --> PER
    RES --> CAN[Cancelado]
    VEN --> CAN
    RES --> FIN[Finalizado<br/>fim do ciclo - automatico]
    VEN --> FIN
    PER --> NEG
    CAN --> NEG
```

| Estado | O que significa | Quando aparece |
| --- | --- | --- |
| **Em aberto** | Criado, ainda sem ação. | Sempre — é onde o orçamento nasce. |
| **Em negociação** | Enviado ao cliente, aguardando a resposta. | Aluguel e venda. |
| **Pré-reservado** | Um "segurar" o aluguel antes de confirmar de vez. | **Opcional**, só locação. |
| **Reservado** | Aluguel confirmado — o **ganho** da locação; o estoque é bloqueado. | Locação. |
| **Vendido** | Venda confirmada — o **ganho** da venda. | Venda. |
| **Perdido** | A proposta não fechou (no funil, antes do ganho). | Aluguel e venda. |
| **Cancelado** | Cancelado **depois** de ganho — já havia compromissos. | Pós-reserva/venda. |
| **Finalizado** | A **logística** terminou (o material cumpriu o ciclo). A cobrança segue independente. | No fim da logística, automaticamente. |

{% hint style="info" %}
**Finalizado é automático — você não arrasta para cá.** O LocFlow encerra o ciclo **da logística** sozinho quando ela termina: na **venda**, quando a entrega se conclui (ou o cliente retira no balcão); na **locação**, quando os itens voltam — e, se a sua operação usa **conferência**, só depois de conferidos. Veja [Visão geral da logística](../logistica/visao-geral.md).
{% endhint %}

{% hint style="success" %}
**Finalizado não fecha a cobrança.** O "Finalizado" é sobre a **logística**, não sobre o financeiro. Se você entregou sem ter faturado antes, **ainda pode gerar a cobrança** de um pedido já finalizado — os dois eixos são independentes, para você nunca ficar sem como cobrar o que já saiu.
{% endhint %}

{% hint style="info" %}
**A pré-reserva é opcional.** Ela serve para "segurar" um aluguel enquanto o cliente decide, sem confirmar de vez. Quem prefere pode **pular** essa etapa e ir direto de Em aberto ou Em negociação para **Reservado**. Use se ajudar a sua operação; ignore se não precisar.
{% endhint %}

### "Pendente" não é um estado do funil

Você pode ver um orçamento marcado como **Pendente** numa faixa tracejada **acima** das colunas do funil. É fácil confundir com "em aberto" — mas **não é**. "Pendente" é uma **pré-etapa por política**: o orçamento está **congelado aguardando a aprovação** de um responsável (por exemplo, porque o frete passou de um limite que você definiu). Ele continua tendo seu estado comercial normal por baixo (Em aberto, Em negociação…), só não pode avançar enquanto não for aprovado.

{% hint style="warning" %}
Não trate Pendente como "em aberto". Um orçamento Pendente **não está parado por falta de ação sua** — está esperando um **aval**. Aprovado, ele entra (volta) no funil e segue normalmente; rejeitado com motivo, volta para edição. O detalhe de quem aprova e como está em [Aprovação de orçamentos](aprovacao.md).
{% endhint %}

## Quando o orçamento vence (a validade) {#quando-o-orcamento-vence}

Todo orçamento tem uma **data de validade** — por quantos dias a proposta fica "de pé" a partir da criação (padrão **7 dias**, ajustável no [Motor de Orçamento](../configuracoes/motor-de-orcamento.md#validade-do-orcamento) e alterável em cada orçamento). É o prazo que você combina com o cliente: *"esse valor vale até tal dia."*

Passou dessa data, o orçamento está **vencido** — e vencido tem uma consequência concreta: **ele não avança mais**. Preços, disponibilidade e regras podem ter mudado desde que você montou a proposta, então o LocFlow **não deixa** você marcar como em negociação, pré-reservar, reservar, vender ou reabrir um orçamento fora da validade sem antes resolver isso.

Você reconhece um vencido **de imediato**, sem precisar tentar movê-lo:

* no **funil**, ele sai das colunas normais e se agrupa em **Expirados** (uma faixa âmbar, logo acima de "Fora do funil");
* na **lista**, o card ganha um **selo âmbar "Expirado"** no lugar da chance de fechar;
* ao **abrir** o orçamento, um **aviso no topo** avisa que ele está expirado (com a data em que venceu) e oferece dois botões: **Renovar validade** e **Criar novo**.

{% hint style="warning" %}
**Vencido não é um novo estado do funil** — é a validade que passou. Por baixo, o orçamento continua no estado em que estava (Em aberto, Em negociação…); ele só fica **impedido de seguir** até você agir. Pense nele como um orçamento "dormindo": ainda está ali, mas a proposta daquele jeito não vale mais. (É parecido com o **Pendente** logo acima: uma condição sobre o orçamento, não uma coluna do funil.)
{% endhint %}

### O que fazer com um orçamento vencido

Você tem três caminhos, conforme a conversa com o cliente:

| Caminho | Quando usar | Como |
| --- | --- | --- |
| **Renovar** | O combinado ainda vale — só passou do prazo. | Edite o orçamento e **estenda a data de validade**. Ele volta a andar, do mesmo ponto. |
| **Criar um novo** | Preços ou proposta mudaram — virou outra conversa. | Faça um **orçamento novo** com os valores atuais e mande ao cliente. O antigo fica de histórico. |
| **Encerrar** | O cliente não voltou e não vai fechar. | Marque como **Perdido** com o motivo *"Cliente não respondeu"* — vira aprendizado no seu funil. |

{% hint style="info" %}
**Por que a validade te protege:** ela evita que um preço de dois meses atrás feche hoje, no automático. Quando o cliente reaparece com um orçamento vencido na mão, você não fica preso ao número antigo — **atualiza a validade** (se ainda faz sentido) ou **refaz a proposta** com os valores de agora, sem constrangimento: *"esse orçamento já venceu; faço um novo rapidinho e te mando."*
{% endhint %}

{% hint style="warning" %}
**Vencer também solta a pré-reserva.** Enquanto o orçamento está dentro da validade, os itens ficam **pré-reservados**; depois de vencer, deixam de ficar segurados e voltam a ficar livres para outro cliente. Veja [Duração, cobrança e bloqueio de uso](duracao-e-bloqueio.md) e o [Motor de Orçamento](../configuracoes/motor-de-orcamento.md#validade-do-orcamento).
{% endhint %}

## A jornada e o próximo passo sugerido

Ao abrir as **Ações rápidas** de um orçamento, a tela é organizada em torno da **jornada** — onde o pedido está e para onde vai naturalmente.

```mermaid
flowchart TB
    LT[Linha do tempo<br/>onde estou no funil] --> PP[Proximo passo sugerido<br/>o avanco natural em destaque]
    PP --> DOC[Documentos<br/>o que esta fase libera]
```

* **Linha do tempo** — a sequência da natureza (Em aberto → Negociação → … → Reserva/Venda), com a etapa atual destacada, as concluídas com um *check* e as futuras numeradas. No celular ela aparece compacta ("etapa X de Y") e expande ao toque; em telas grandes vira um passo a passo horizontal.
* **Próximo passo sugerido** — o avanço natural do funil em destaque (um botão grande com o verbo da ação, ex.: **Reservar**, **Vender**), e as demais transições possíveis como atalhos ("Ou avance de outra forma").
* **Documentos** — os arquivos que aquela fase libera (veja a seção a seguir).

{% hint style="success" %}
**Por que a jornada te ajuda a faturar:** em vez de uma lista de botões soltos, você vê *um* próximo passo claro. Menos dúvida, menos pedido esquecido no meio do funil — e cada toque te empurra para o fechamento.
{% endhint %}

### Mudando de fase

Você muda o estado de duas formas, e as duas fazem a **mesma coisa** por baixo:

* **No funil:** arraste o card para outra coluna.
* **Nas Ações rápidas:** toque no próximo passo sugerido (ou num dos atalhos).

Quando a mudança avança o funil, o LocFlow te leva às **Ações rápidas** já com o novo estado, para você confirmar e seguir.

## Quais documentos cada fase libera

O LocFlow só oferece os documentos que **fazem sentido** no estado atual — você não vê um contrato de reserva num orçamento ainda em aberto. A tabela abaixo é o que o sistema mostra hoje, por estado e natureza:

| Estado | Locação | Venda |
| --- | --- | --- |
| **Em aberto** | WhatsApp · Orçamento em PDF | WhatsApp · Orçamento em PDF |
| **Em negociação** | WhatsApp · Orçamento em PDF | WhatsApp · Orçamento em PDF |
| **Pré-reservado** | WhatsApp · Orçamento em PDF · Contrato de pré-reserva | — (não existe na venda) |
| **Reservado** *(ganho)* | Contrato de reserva · **Fatura de locação** · Ordem logística | — |
| **Vendido** *(ganho)* | — | Contrato de venda · Ordem logística |
| **Perdido / Cancelado** | Nenhum (a única ação é **reabrir**) | Nenhum (a única ação é **reabrir**) |

Alguns detalhes úteis:

* **WhatsApp** gera um texto pronto para colar no chat do cliente — você copia ou abre direto.
* **Orçamento em PDF** é o arquivo da proposta, com layout ajustável.
* **Ordem logística** lista os itens com a carga (dimensões, peso e volume) para o galpão e a rota.
* **Fatura de locação** é o documento de cobrança do aluguel (valores, parcelas e vencimentos) — por isso só aparece na locação.

{% hint style="info" %}
**Gere a cobrança antes da fatura em PDF.** Se você gerar a fatura de locação antes de ter emitido a cobrança, o LocFlow avisa: *"A fatura sai com os valores previstos do orçamento, mas sem parcelas, vencimentos nem situação de pagamento — recomendamos gerar a cobrança antes para refletir os prazos reais."*
{% endhint %}

### Gerar e enviar sem trocar de tela

A geração é **embutida**: ao clicar num documento, o preparo abre ali mesmo (num painel à direita em telas grandes, numa folha que sobe no celular) — você não sai das Ações rápidas. No preparo você:

* edita o **nome do arquivo**;
* ajusta **opções deste envio** — como apresentar os kits (linha única ou kit "pai" com componentes recuados) e exibir ou ocultar a **coluna de fotos** dos itens, para uma versão mais enxuta;
* vê uma **pré-visualização ao vivo**;
* e finaliza com **Compartilhar** ou **Baixar** (PDF), ou **Copiar / Abrir** (WhatsApp).

## Marcar como ganho (reservado / vendido)

Marcar um orçamento como **ganho** é o momento que liga a operação. Ao reservar (locação) ou vender (venda), o LocFlow encadeia o resto sozinho:

* gera a **fatura** correspondente, com parcelas (veja [Faturas e parcelas](../cobranca/faturas-e-parcelas.md));
* libera a **logística** de entrega e retirada — ou só de entrega, na venda (veja [Logística](../logistica/visao-geral.md)).

Depois do ganho, as Ações rápidas trocam o "próximo passo" por uma seção **Acompanhar operação**, com o estado da **cobrança** e da **logística** lado a lado e o atalho para cada uma.

{% hint style="info" %}
**Faltou agendar algo?** Antes de reservar ou vender, o LocFlow confere os pré-requisitos (por exemplo, datas de entrega e retirada). Se faltar alguma coisa, ele abre a edição já apontando o que resolver — em **âmbar**, como um aviso — em vez de só recusar a ação. Você ajusta e confirma em um toque.
{% endhint %}

{% hint style="success" %}
**Por que isso te faz faturar mais:** no instante em que você ganha o pedido, a cobrança já existe e a equipe já sabe que tem entrega para preparar. Você para de "esquecer de faturar" e de descobrir tarde demais que o material não foi separado. Pedido ganho vira dinheiro entrando e operação rodando — sem retrabalho.
{% endhint %}

## Editando depois de ganho {#editando-depois-de-ganho}

Precisou ajustar um orçamento já ganho? Pode editar — o LocFlow reflete a mudança na **fatura**, na **logística** e no **estoque** automaticamente. Mas há limites, e vale conhecê-los antes de prometer a mudança ao cliente.

### O limite dos itens é a entrega, não o despacho {#limite-dos-itens}

| Momento | Dá para mexer nos itens? |
| --- | --- |
| Antes de despachar (a separar, separado) | **Sim.** |
| **Com o caminhão já na rua** (saiu para entrega) | **Sim** — a diferença vira um movimento novo a encaixar num roteiro. |
| **Material com o cliente** (entregue, retirado no balcão) ou já em reversa/conferência | **Não.** *"Os itens não podem ser alterados após o despacho."* Só valores mudam. Para trocar materiais, **crie um novo orçamento**. |

### A edição pode ser recusada por estoque {#recusada-por-estoque}

{% hint style="warning" %}
**Contraintuitivo, mas proposital: só adiar a entrega em dois dias já pode travar o salvamento.** Quando você mexe em **itens** ou em **datas**, o LocFlow refaz a checagem de disponibilidade sobre a **janela nova** (descontando a reserva deste mesmo pedido). Se o material não couber, a edição é recusada:

> *"Não há estoque disponível para todos os itens na janela de uso."*

ou, se a sua regra permite furar com limite, a mensagem do **teto de overbooking**. Ajuste as quantidades, escolha outra data ou reveja as regras em [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md).
{% endhint %}

Há ainda um terceiro motivo de recusa, mais raro: quando as datas novas **não permitem calcular a janela de bloqueio de uso**, ou quando o **bloqueio manual** que você definiu não cobre a logística nova. Veja [Duração, cobrança e bloqueio de uso](duracao-e-bloqueio.md#politica-de-bloqueio).

### O efeito na operação (e no parceiro) {#efeito-na-operacao}

Toda edição pós-ganho tem efeito colateral do outro lado: o roteiro pode ficar **desatualizado**, a reserva de estoque é reconciliada, e a mudança pode até **quebrar a promessa de outro pedido**. Isso tem uma página própria — leia [Quando um pedido muda depois de fechado](../logistica/quando-um-pedido-muda.md).

{% hint style="danger" %}
**Se o pedido já foi repassado a um parceiro, mexer nos itens devolve a decisão a ele.** O aceite dele era sobre o pedido antigo: mudar os itens faz a operação voltar a "aguardando a decisão do parceiro", e ele pode recusar. Fale com ele antes — veja [O pedido já estava com um parceiro](../logistica/efeitos-na-parceria.md#itens-revogam-o-aval).
{% endhint %}

> Quando a mudança for grande e os itens já tiverem chegado ao cliente, a recomendação costuma ser **abrir um novo orçamento** em vez de remendar o atual — fica mais limpo para você e para o cliente.

## Perda e cancelamento (com motivo) {#perda-e-cancelamento-com-motivo}

Nem todo orçamento fecha — e tudo bem. O LocFlow separa duas situações, e em ambas pede um **motivo** (da lista) ou uma **observação** escrita:

* **Perdido** — a proposta não avançou, **antes** do ganho. Não há compromisso financeiro nem logístico para desfazer.
* **Cancelado** — o negócio cai **depois** de reservado/vendido. Como já existiam fatura e logística, o cancelamento tem consequências a tratar.

| Situação | Quando | Exemplos de motivo |
| --- | --- | --- |
| **Perdido** | Antes do ganho (no funil) | Cliente não respondeu · Preço · Redução de escopo · Desistência do evento · Mudança de data · Fora da área de entrega · Estoque indisponível · Capacidade operacional |
| **Cancelado** | Depois do ganho | Desistência do evento · Mudança de data · Inadimplência · Erro no orçamento · Estoque indisponível · Capacidade operacional |

{% hint style="success" %}
**Por que registrar o motivo vale a pena:** com o tempo, o motivo das perdas vira um mapa do seu negócio — se "Preço" aparece sempre, talvez sua tabela esteja fora do mercado; se é "Não respondeu", o problema é o follow-up. Saber **por que** você perde é o primeiro passo para perder menos.
{% endhint %}

### Nem sempre dá para cancelar (nem para voltar atrás) {#travas-do-encerramento}

Depois do ganho já existem compromissos — então o LocFlow confere antes de deixar você encerrar. As travas são **diferentes** nos dois caminhos, e de propósito: cancelar é um **desfecho legítimo** do negócio (pode acontecer até depois da entrega); "voltar para negociação" **apaga a história**, e por isso é mais restrito.

| Situação | **Cancelar** | **Voltar para negociação** |
| --- | --- | --- |
| A fatura tem **algum pagamento** (total ou parcial) | **Barra.** *"Estorne ou cancele a cobrança antes."* | **Barra.** Vira reembolso, que é outro fluxo. |
| A **rota já saiu** (execução iniciada) | Passa — fica registrada a pendência a conciliar. | **Barra.** |
| Material **já entregue ou retirado** | Passa — é justamente o caso do evento que acabou. | **Barra.** Registre a devolução antes. |
| A **fatura em aberto** | Fica como está — você decide o que fazer com a cobrança. | É **cancelada automaticamente**, junto com as cobranças online pendentes. |

{% hint style="warning" %}
**Se o pedido foi repassado a um parceiro, encerrar tem mais um custo.** O repasse é desfeito, o parceiro é avisado com o valor que saiu dos ganhos dele, e um cancelamento **em cima da hora depois do aceite** pesa na sua reputação na rede — a menos que você escolha, na lista, um motivo que descreve um ato do cliente (desistência do evento, mudança de data, preço, achou outro fornecedor ou inadimplência) — motivo escrito à mão não isenta. Leia [Cancelar ou reverter um pedido repassado](../logistica/efeitos-na-parceria.md#cancelar-repassado).
{% endhint %}

O que o encerramento desfaz na operação (roteiros, projeções, estoque) está detalhado em [Reverter o ganho e cancelar](../logistica/quando-um-pedido-muda.md#reverter-e-cancelar).

Um orçamento **Perdido** ou **Cancelado** pode ser **reaberto** para uma nova tentativa — ele volta para a negociação. Nas Ações rápidas, esses estados aparecem como um aviso convidando a reabrir; nos documentos, nada é oferecido (a única ação é reabrir). A exceção é a **validade**: se o orçamento já **venceu**, não dá para reabrir por cima do prazo — antes você **renova a validade** ou parte para um **orçamento novo** (veja [Quando o orçamento vence](#quando-o-orcamento-vence)).

## Por porte: você acompanha do seu jeito

| Porte | Como costuma usar |
| --- | --- |
| **Pequeno** | O funil já basta: arrasta o card, fecha o negócio, gera o PDF/WhatsApp. Sem aprovação, sem fila de Pendentes. |
| **Médio** | Usa o "próximo passo sugerido" para não deixar pedido travado e começa a registrar **motivos de perda** para entender onde escorrega o faturamento. |
| **Grande** | Times separados (vendedor monta, gestor aprova), Pendentes de aprovação como rotina, e os relatórios de perda viram decisão de preço e de área de atendimento. |

## Situações reais

- **Cliente sumiu:** mandou o orçamento, cobrou duas vezes, sem resposta. Marca como **Perdido** com o motivo "Cliente não respondeu" — e, se ele voltar mês que vem, é só **reabrir** (desde que ainda esteja dentro da validade).
- **Voltou tarde, orçamento vencido:** o cliente reaparece três semanas depois querendo fechar, mas a validade já passou. Você abre o orçamento, vê que está **vencido** e decide: **estende a validade** (se o preço ainda vale) ou **cria um novo** com os valores de agora. O sistema não deixa reservar por cima do prazo vencido — de propósito.
- **Fechou na hora:** cliente confirmou o aluguel pelo WhatsApp. Você arrasta o card para **Reservado** no funil — a fatura nasce e a entrega já entra na fila.
- **Esperando o aval do gestor:** o orçamento aparece como **Pendente** na faixa de cima porque o frete passou do limite. Não é "em aberto" — está congelado até alguém aprovar. Veja [Aprovação de orçamentos](aprovacao.md).
- **Evento cancelou:** o cliente desmarcou a festa depois de reservar. Você marca **Cancelado** com o motivo "Desistência do evento" — e o LocFlow desfaz a logística sozinho. Se o cliente **já tinha pago** (mesmo só o sinal), o cancelamento é **barrado** até você estornar ou cancelar a cobrança: dinheiro do cliente dentro de casa não se apaga por mudança de status.
- **Adiei a entrega e o sistema não deixou salvar:** a data nova caiu numa semana em que o material já está comprometido. Não é bug — é o LocFlow evitando que você prometa o que não tem. Veja [A edição pode ser recusada por estoque](#recusada-por-estoque).

## Próximo passo

Orçamento ganho? Siga para a [cobrança](../cobranca/faturas-e-parcelas.md) ou para a [logística](../logistica/visao-geral.md). Precisou mexer no pedido depois de fechado? [Quando um pedido muda depois de fechado](../logistica/quando-um-pedido-muda.md) responde o que acontece com a rota, o estoque e o parceiro. Quando um orçamento aparece como **Pendente**, veja [Aprovação de orçamentos](aprovacao.md). Para o quadro geral, volte ao [ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md).
