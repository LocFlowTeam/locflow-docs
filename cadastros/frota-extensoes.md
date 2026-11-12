---
icon: trailer
description: Reboques, carretinhas e carretas como extensões da frota — placa, documento, vistoria e capacidade próprios, e como o engate entra no planejamento e na saída do roteiro.
---

# Extensões

Uma **extensão** é o que se acopla a um veículo para aumentar o que ele leva: **reboque**, **carretinha**, **semirreboque**, **carreta**.

Ela é um recurso **independente** da frota: tem **placa**, **documento** e **situação** próprios — pode estar em manutenção enquanto o veículo roda, e vice-versa — e a sua **capacidade própria**. Na viagem, o que a extensão leva **soma** ao que o veículo que a puxa leva.

{% hint style="info" %}
As extensões fazem parte da [Frota](frota.md) (plano **Pro**). O parceiro externo da [Rede de Parceiros](../parcerias/visao-geral.md) não vê esta aba: ele enxerga só a frota dele.
{% endhint %}

## Onde fica {#onde-fica}

Em **Logística › Frota**, aba **Extensões** (*"Reboques e tudo que engata"*). Ali você busca por nome ou placa, toca em **Nova extensão** para cadastrar e, na lista, muda a situação de cada uma pelas ações **Enviar para manutenção**, **Inativar** e **Reativar** — como nos veículos.

## Cadastrar uma extensão {#cadastrar}

O formulário **Nova extensão veicular** começa lembrando: *"A extensão é um recurso independente: ela não cria uma cópia do veículo-base. A capacidade é dela própria e se declara aqui embaixo."*

| Campo | Para que serve |
| --- | --- |
| **Grupo da extensão** *(obrigatório)* | O grupo das extensões que se substituem (ex.: "Carreta baú 14m"). Escolha um existente ou digite um nome e toque em **Criar o grupo "…"**. *"O planejamento aponta para o grupo, não para a placa."* |
| **Identificador interno** *(obrigatório)* | O nome pelo qual a equipe reconhece a extensão. |
| **Placa da extensão** *(obrigatória)* | A placa dela — que não é a do veículo que a puxa. |
| **Classes de veículo-base compatíveis** | Com quais grupos de veículos ela engata. *"Somente combinações explicitamente marcadas poderão ser planejadas."* |
| **Capacidade da extensão** | *"Quanto esta extensão acrescenta ao veículo-base — é o que o planejamento soma à capacidade da classe escolhida."* |
| **Vistoria da extensão** | Checklist e frequência próprios (veja abaixo). |
| **Documento da extensão (CRLV)** | A validade do licenciamento dela (veja abaixo). |
| **Situação** *(na edição)* | **Ativa**, **Manutenção** ou **Inativa**. |

### Capacidade própria {#capacidade}

A capacidade da extensão usa as mesmas estratégias do [tipo de veículo](frota-capacidade.md) — **contagem de itens**, **volume** e **peso máximo** —, com uma diferença: como não há carroceria com medidas para calcular, o volume entra direto, no campo **Volume útil (m³)**. Se outra extensão do mesmo grupo já tem capacidade cadastrada, dá para **copiar a capacidade de outra extensão do grupo** e ajustar.

{% hint style="warning" %}
**Sem nenhuma medida, a extensão não vai para o roteiro.** Uma extensão sem contagem, volume ou peso cadastrados recebe o aviso: *"Extensão sem contagem, volume ou peso cadastrados: ela não pode ser planejada junto de uma classe de veículo."*
{% endhint %}

### Vistoria da extensão {#vistoria}

A extensão tem **vistoria própria**, com os mesmos gatilhos da vistoria do veículo — a cada roteiro, na primeira saída do dia, em dias da semana, a cada tantos dias ou a cada tantos roteiros. *"Checklist e frequência próprios deste recurso — a validade vem do gatilho, não de uma data digitada."* Ligada, ela precisa de pelo menos um item no checklist. Os gatilhos e modelos estão em [Tipos de veículo: vistoria](frota-vistoria.md).

### Documento (CRLV) {#documento}

**Reboque, semirreboque e carreta têm placa e CRLV próprios** — a carreta não se licencia pelo cavalo. A regra é a mesma do veículo: **documento vencido bloqueia a saída** do roteiro; **documento não cadastrado só avisa**. Veja [Documento do veículo (CRLV)](frota.md#documento-crlv).

## A extensão no roteiro {#no-roteiro}

```mermaid
flowchart LR
    P["Planejamento:<br/>grupo do veículo<br/>+ grupo de extensões"] --> S["Saída:<br/>a placa do veículo<br/>e a placa da extensão"]
    S --> V["Vistoria:<br/>veículo e extensão"]
```

1. **No planejamento**, depois de escolher o grupo do veículo (no campo **Tipo de veículo (classe)**), aparece o convite **Engatar uma extensão** — *opcional*. Você escolhe um **grupo de extensões** (*"Qualquer extensão do grupo"*), não uma placa. A capacidade planejada passa a ser a do **conjunto**: o que o veículo leva **mais** o que a extensão leva.
2. **Na saída**, o engate planejado vira **obrigatório**: quem inicia a rota escolhe a placa do veículo e a da extensão (*"Engatar …"*, marcado como obrigatória). A lista traz as extensões **ativas** daquele grupo; as que não podem sair (por exemplo, com documento vencido) aparecem como **Indisponível**, e as que não engatam no veículo escolhido, como **Não engata neste veículo**. Sair sem a extensão não é possível — a carga foi conferida contra a capacidade do conjunto: *"Este roteiro foi planejado com engate: escolha a extensão."*
3. **Na vistoria**, cada um segue o próprio gatilho — o veículo e a extensão. Quando a vistoria da extensão está vencida, o passo aparece como **Vistoria da composição**, com o **Checklist da extensão** (e o do veículo ao lado, se o dele também venceu).

{% hint style="info" %}
**Na montagem da carga também.** Na bancada de **Cargas e viagens**, cada viagem pode levar um grupo de extensões engatado, como uma segunda caixa ao lado do veículo — e a carga se reparte entre o baú e a carreta. O convite para engatar só aparece para quem tem extensões cadastradas. Veja [Cargas e viagens](../logistica/planejando-o-roteiro.md#cargas-e-viagens).
{% endhint %}

## Situações reais {#situacoes-reais}

- **A carreta que roda com dois cavalos:** você cadastra a carreta uma vez, no grupo "Carreta baú 14m", com placa, CRLV e capacidade dela, e marca os grupos de caminhão que a puxam. No planejamento, escolhe o grupo do caminhão e engata o grupo da carreta; no pátio, o motorista escolhe qual caminhão e qual carreta saem.
- **Carretinha na oficina, carro rodando:** você envia a carretinha para **Manutenção** pela lista de extensões. O carro continua disponível para roteiros sem engate; a carretinha não aparece para engatar até alguém **Reativar**.
- **CRLV da carreta vencido:** na saída, a carreta aparece indisponível. O roteiro planejado com engate espera outra carreta do mesmo grupo — ou a renovação do documento.

## Próximo passo {#proximo-passo}

Volte para [Frota](frota.md) para a visão geral, veja como o grupo funciona em [Grupos da frota](frota-grupos.md) e como o engate entra na rota em [Planejando o roteiro](../logistica/planejando-o-roteiro.md) e [Execução em campo](../logistica/execucao-em-campo.md).
