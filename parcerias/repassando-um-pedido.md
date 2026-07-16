---
icon: arrow-right-arrow-left
description: O passo a passo de repassar um pedido ganho a um parceiro — esboço grátis, comparativo, aceite, prazos, desistência e o que cada estado significa.
---

# Repassando um pedido

**Onde fica:** a ação **"Repassar a parceiro"** aparece nas **ações do orçamento** quando ele foi **ganho** e existe acordo que cobre os itens. O acompanhamento vive na **Rede de Parceiros › Reservas em parceria** (lista + detalhe de cada repasse).

Repassar é isto: você fechou um pedido com o **seu** cliente, mas quem vai executar a operação — separar o material, entregar, retirar — é um **parceiro**. O LocFlow cuida do meio do caminho inteiro: mostra **qual parceiro rende mais** para você, envia a **solicitação**, controla o **prazo de aceite**, e deixa o dinheiro combinado no [acordo](acordos-de-parceria.md) pronto para a divisão. O cliente continua sendo seu; a logística passa a ser do parceiro.

{% hint style="info" %}
**Pré-requisito: um acordo ativado.** O repasse só existe por cima de um **acordo de parceria ativado** que cubra os itens do pedido — é ele que diz quanto o parceiro ganha por item, qual o prazo de aceite e como o frete se resolve. Se você ainda não tem um, comece por [Acordos de parceria](acordos-de-parceria.md).
{% endhint %}

## Quando repassar {#quando-repassar}

Dois requisitos, nada mais:

1. **O orçamento está ganho.** Repasse é para pedido fechado — enquanto está em negociação, ele é só seu.
2. **Existe um acordo ativado que cobre os itens.** Todo item do pedido precisa estar nos termos de pelo menos um acordo.

Com os dois valendo, a linha **"Repassar a parceiro"** aparece nas ações do orçamento. Se nenhum acordo cobre os itens, a tela não te deixa no escuro: ela **explica o que falta** — qual acordo cobriria e o que ficou de fora — em vez de simplesmente esconder a opção.

{% hint style="success" %}
**Para quem está começando:** se você tem **um** parceiro e **um** acordo, o repasse é apertar um botão e esperar o aceite. Toda a sofisticação desta página — comparativo, créditos, ranking — só aparece quando você tem **mais de um candidato** para escolher.
{% endhint %}

## A tela de repasse: duas fases {#tela-de-repasse}

Calcular a rota real de cada parceiro até a operação **consome créditos** (é uma consulta de mapa por rota). Por isso a tela trabalha em **duas fases**: primeiro tudo o que é **grátis**, depois — só com o seu "ok" — o cálculo pago.

```mermaid
flowchart LR
    A[Escolher o pedido] --> B[Fase 1: esboço grátis<br/>candidatos por margem antes do frete]
    B --> C{Custo estimado?}
    C -->|zero| D[Comparativo final]
    C -->|há rotas a calcular| E[Você escolhe quais candidatos<br/>calcular e autoriza o gasto]
    E --> D
    D --> F[Repassar ao parceiro escolhido]
```

### Fase 1 — o esboço grátis {#esboco-gratis}

Assim que você escolhe o pedido, o LocFlow monta um **esboço sem gastar nada**: a lista de candidatos elegíveis, ranqueada pela **margem antes do frete** — os preços do acordo de cada um contra o preço que o seu cliente pagou. É a primeira leitura de "quem tende a render mais".

Junto do esboço vem a **transparência de créditos**: quanto custaria, **no máximo**, calcular as rotas reais de todos os candidatos. Você decide **quais** candidatos valem o cálculo (por exemplo, só os 3 do topo) — a estimativa mostra o teto de créditos, o seu saldo atual e quanto sobraria depois. Nada é debitado até você confirmar.

{% hint style="info" %}
**Custo zero segue sozinho.** Quando não há rota a calcular — por exemplo, todos os acordos com **frete a combinar** —, a tela nem pergunta: vai direto ao comparativo final, grátis.
{% endhint %}

### Fase 2 — o comparativo final {#comparativo}

Autorizado o cálculo, cada candidato ganha um **card completo**, e o ranking passa a ser pela **sua margem real** — a mesma conta que vai valer na liquidação do dinheiro:

| No card | O que mostra |
| --- | --- |
| **VOCÊ LUCRA** | A sua margem no pedido com **este** parceiro: o que o cliente paga menos o repasse (itens pelo preço do acordo + frete do parceiro). É o número que ordena a lista. |
| **Frete por perna** | O custo de transporte do parceiro, aberto por movimento (entrega, retirada), calculado pelas regras de preço **dele**. |
| **Reputação** | Estrelas e selo do parceiro, mais o índice de confiabilidade — a sua experiência (e a da rede) com ele. Veja [Reputação e boas práticas](reputacao-e-boas-praticas.md). |
| **Disponibilidade** (parceria entre organizações) | Se a parceira tem **estoque** dos itens na data da operação — detalhado logo abaixo. |

Escolheu o card, tocou em repassar — a solicitação parte para o parceiro.

### Disponibilidade de estoque {#disponibilidade}

Na parceria **entre organizações**, os itens vão sair do estoque **da parceira**. Por isso o comparativo já consulta a disponibilidade dela para a janela da operação:

| O que o card mostra | O que significa | O que acontece |
| --- | --- | --- |
| **Disponível** | A parceira tem os itens na data. | Card normal, pronto para repassar. |
| **Sem estoque para a data** | Os itens estão comprometidos com outras operações na janela. | O card fica **desabilitado** — repassar seria prometer o que ela não tem. |
| **Estoque não cadastrado — confirme com o parceiro** | A parceira nunca cadastrou aqueles itens no estoque dela. | Só um **aviso** — o repasse segue, mas confirme por fora. |

### Frete a combinar {#frete-a-combinar}

Acordo cujo frete é **manual** (a combinar por operação) não tem rota a calcular — o candidato aparece numa seção própria, **"Frete a combinar por operação"**, abaixo do ranking, com a margem **parcial** (só dos itens). Ele não compete pelo topo porque falta uma peça da conta: o transporte vocês fecham por fora, operação a operação.

### Viagem com frete fixado {#frete-fixado}

Se, lá no orçamento, alguma viagem teve o frete **fixado a uma transportadora específica** (na composição do frete), os acordos que **conflitam** com essa fixação ficam de fora do comparativo — e a tela avisa:

{% hint style="warning" %}
*"Uma das viagens deste orçamento tem o frete fixado a outra transportadora — os acordos que conflitam ficaram fora. Refaça o frete sem essa fixação para repassar."*

O caminho é reabrir o [frete do orçamento](../orcamentos/valores.md#composicao-do-frete), desfazer a fixação e voltar ao repasse.
{% endhint %}

## A solicitação chega ao parceiro {#solicitacao}

Todo repasse é uma **solicitação** — o parceiro nunca é atropelado. Ele recebe uma notificação e abre o detalhe da reserva, onde vê:

* **A operação:** o que entregar, onde, quando — tudo o que precisa para decidir se dá conta.
* **Os itens e quantidades**, já nos termos do acordo.
* **Quanto ele ganha** — os preços do acordo, nunca o preço que o **seu** cliente pagou. O seu comercial é seu.

E decide:

* **Aceitar** — ele assume a logística da operação. Na parceria entre organizações, o material passa a sair do **estoque dele**: o sistema traduz os itens pelo mapeamento do acordo e reserva no galpão dele mais próximo da entrega. Há um guarda no aceite: **sem estoque disponível na janela, o aceite é barrado** (itens que ele nunca cadastrou não barram — só avisam).
* **Recusar** — sempre com **motivo obrigatório**, que chega a você. A posse do pedido volta e você repassa a outro parceiro ou opera você mesmo.

{% hint style="info" %}
**"Fora do acordo":** quando a solicitação carrega algum **desvio** dos termos (por exemplo, uma condição que o acordo não previu), a tela do parceiro lista os desvios numa seção própria e o aceite vira um **aval comercial** — ele revisa e aprova ou rejeita sabendo exatamente o que está fora.
{% endhint %}

## O prazo de aceite {#prazo-de-aceite}

O acordo define uma **janela de aceite** — quantas horas antes da operação o parceiro precisa responder (zero = sem prazo). Enquanto a solicitação aguarda, o detalhe mostra o limite: *"Aceite até \[data e hora] para assumir esta operação."*

Estourou o prazo? **O sistema expira a solicitação sozinho** — uma varredura roda de tempos em tempos, você não precisa vigiar. A posse do pedido **volta para você**, que pode re-repassar a outro parceiro ou tocar a operação com a própria estrutura. Para o parceiro, deixar expirar gera uma **penalidade leve** no índice de confiabilidade — respeitar prazos é parte da reputação na rede.

## Desistência depois do aceite {#desistencia}

Aceitou e a realidade mudou? O parceiro pode **desistir**, sempre com motivo. O acordo define uma **janela de desistência** (padrão de 24 horas antes da operação):

| Quando desiste | O que acontece |
| --- | --- |
| **Dentro da janela** | É um direito — sem registro contra ele. A posse volta para você re-repassar. |
| **Fora da janela (tardia)** | A desistência fica no **histórico** e gera **penalidade média** no índice de confiabilidade — quanto mais perto da operação, mais te deixa na mão. |

Na parceria entre organizações, a desistência também **libera** o estoque que estava reservado no galpão do parceiro.

## Reverter o ganho desfaz o repasse {#reverter-ganho}

Se você **reverte o ganho** do orçamento — o cliente desistiu, o negócio voltou à negociação —, o repasse é **cancelado automaticamente**. O parceiro é notificado, o estoque espelhado (se houver) é liberado, e a reserva fica registrada como **"Orçamento revertido — repasse desfeito"**. Nenhuma ação manual, nenhuma ponta solta.

## Depois do aceite: a execução é do parceiro {#execucao}

Com o aceite, a **posse logística** da operação é do parceiro: a entrega e a retirada entram nos **roteiros dele**, e é a equipe dele que executa em campo — do jeito que a [Logística](../logistica/visao-geral.md) do LocFlow sempre funciona, só que do lado de lá. Você acompanha pelo detalhe da reserva.

E a responsabilidade é real: um **movimento pulado** (falha de entrega) gera a penalidade **mais pesada** do índice de confiabilidade. O parceiro que aceita, entrega.

{% hint style="info" %}
**E o dinheiro?** O quanto o parceiro ganha vem dos **preços do acordo × quantidades × fator de locação** (as mesmas diárias/locações do preço ao cliente), mais o frete dele — e a liquidação acontece pelo gatilho do acordo (no pagamento, na entrega ou na retirada). O acompanhamento vive no Financeiro: **Repasses** (para você) e **Meus Ganhos** (para o parceiro), com o selo "Rede". Os detalhes dessa divisão estão em [O dinheiro da parceria](dinheiro-da-parceria.md).
{% endhint %}

## O ciclo da solicitação {#ciclo-da-solicitacao}

O caminho completo de um repasse, do envio ao desfecho:

```mermaid
stateDiagram-v2
    [*] --> Aguardando: você repassa
    Aguardando --> Aceito: parceiro aceita
    Aguardando --> Recusado: parceiro recusa (motivo)
    Aguardando --> Expirado: prazo de aceite estoura
    Aguardando --> Cancelado: ganho revertido
    Aceito --> Desistido: parceiro desiste (motivo)
    Aceito --> Cancelado: ganho revertido
    Aceito --> EmExecucao: operação nos roteiros do parceiro
    Recusado --> Aguardando: re-repasse a outro parceiro
    Expirado --> Aguardando: re-repasse a outro parceiro
    Desistido --> Aguardando: re-repasse a outro parceiro
```

O **re-repasse** é sempre a mesma solicitação seguindo para **outro** parceiro — você volta ao comparativo e escolhe de novo.

## Os estados, como a tela mostra {#estados}

A mesma reserva aparece com rótulos diferentes conforme **quem olha** — a tela fala com você no seu papel:

| Estado | O vendedor vê | O parceiro vê |
| --- | --- | --- |
| Aguardando resposta | **Aguardando parceiro** | **Aguardando você** |
| Aceita | **Aceito** | **Aceito** |
| Recusada | **Recusado** | **Recusado** |
| Desistida pós-aceite | **Parceiro desistiu** | **Você desistiu** |
| Prazo estourado | **Prazo expirou — retomado** | **Prazo de aceite expirou** |
| Ganho revertido | **Orçamento revertido — repasse desfeito** | **Orçamento revertido — repasse desfeito** |
| Com desvio dos termos | **Fora do acordo — aguardando parceiro** | **Fora do acordo — revise** |

Todos aparecem na lista e no detalhe de **Rede › Reservas em parceria** — e a linha "Repasse a parceiro" nas ações do orçamento reflete o mesmo estado, com atalho para o detalhe.

## Situações reais {#situacoes-reais}

- **Evento no fim de semana, sua agenda cheia.** Pedido ganho, dois parceiros com acordo. O esboço mostra os dois, você calcula as rotas (2 créditos), o comparativo diz que o parceiro A te dá R$ 180 a mais de margem. Repassa, ele aceita em uma hora, a operação some da sua agenda.
- **O parceiro não respondeu.** A solicitação mostrava "Aceite até sábado, 10h". Domingo o sistema expirou sozinho: você viu **"Prazo expirou — retomado"**, re-repassou ao segundo colocado e o índice do primeiro sentiu a penalidade leve.
- **Card apagado no comparativo.** A parceira aparece com **"Sem estoque para a data"** — as mesas dela estão em outro evento na mesma janela. O card desabilita e te poupa de um aceite que seria barrado de qualquer jeito.
- **Cliente cancelou tudo.** Você reverteu o ganho do orçamento; o repasse se desfez sozinho, o parceiro foi avisado e o estoque dele voltou a ficar livre. Zero telefonema.

## Próximo passo {#proximo-passo}

- Ainda não tem acordo? Monte um em [Acordos de parceria](acordos-de-parceria.md).
- Entenda os dois modelos de parceria em [Parcerias: a visão](visao-geral.md).
- Trabalha com um parceiro convidado, sem organização própria? Veja [Parceiro logístico externo](parceiro-logistico-externo.md).
- Como o pedido vira operação em campo: [Logística: visão geral](../logistica/visao-geral.md).
