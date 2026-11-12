---
icon: gears
description: O tipo de veículo descreve o que um modelo carrega — marca, modelo, ano, baú, capacidade e vistoria — e vale para todos os veículos iguais. Os seis blocos do cadastro, a FIPE como atalho e a cópia da capacidade.
---

# Tipos de veículo

O **tipo de veículo** responde **o que aquele modelo carrega**: marca, modelo, ano, combustível, se tem baú fechado, quanto cabe dentro e com que frequência passa por vistoria.

Ele é **compartilhável**: se você tem cinco Fiorinos iguais, é **um tipo e cinco veículos**. Mudou a medida do baú? Muda num lugar só e vale para os cinco. A **placa** e o **identificador interno** ("Caminhão 01") são do **veículo**, não do tipo — é o que diferencia um carro do outro.

{% hint style="info" %}
**Antes, "especificação" ou "ficha técnica".** O tipo de veículo é o que o LocFlow chamava de especificação veicular. Alguns botões ainda usam a palavra "ficha" — como **Usar uma ficha existente** e **Criar uma ficha nova**, no cadastro do veículo —, mas é tudo o mesmo cadastro: o tipo.
{% endhint %}

## Onde fica {#onde-fica}

Em **Logística › Frota**, aba **Tipos de veículo** (*"O que cada modelo carrega"*). Ali você:

- busca por marca ou modelo;
- toca em **Novo tipo** para cadastrar;
- toca num tipo para abrir a ficha dele — com a capacidade, a lista de **veículos com esta ficha** e o atalho **Adicionar veículo com esta ficha**.

Também dá para criar um tipo **sem sair do cadastro do veículo**: no passo **Tipo** de **Novo veículo**, escolha **Criar uma ficha nova**. Ali entram identificação, carroceria, capacidade e grupo; a vistoria, o custo de combustível e o titular ficam no cadastro completo, por esta aba.

## Os seis blocos do cadastro {#blocos}

O formulário **Novo tipo de veículo** tem seis blocos, um embaixo do outro. No topo, um resumo vai mostrando o que você já preencheu.

| # | Bloco | O que você informa | Obrigatório? |
| --- | --- | --- | --- |
| 1 | **Identificação** | Carro, caminhão ou moto; marca, modelo e ano; combustível; identificação interna; e o titular, quando liberado | Tipo, marca, modelo e ano |
| 2 | **Carroceria** | Se é **baú fechado** — e, se for, as dimensões internas do baú | As três medidas, se o baú for fechado |
| 3 | **Capacidade · estratégias** | Contagem de itens, volume e peso máximo | Não — mas sem nenhuma, a carga não é conferida |
| 4 | **Vistoria** | Quando o veículo é checado e o que conferir | Não (vem desligada) |
| 5 | **Custo operacional** | Consumo e preço do combustível | Não (vem desligado) |
| 6 | **Grupo** | O grupo do tipo — um existente ou um novo | **Sim** |

### 1 · Identificação: a FIPE é atalho, não obrigação {#identificacao}

Marca, modelo e ano são campos de **digitação livre**. O botão **Preencher pela FIPE** é só um **atalho** para não digitar: ele abre a busca do catálogo FIPE (tipo, marca, modelo, ano) e preenche tudo de uma vez — inclusive o combustível sugerido. Quando o preenchimento veio da FIPE, a tela mostra o código (*"Cód. FIPE … · preenchido pela FIPE"*); se você editar marca, modelo ou ano à mão, o vínculo com a FIPE é desfeito.

Como a FIPE não é obrigatória, dá para cadastrar o que não está nela: **carretinha**, **utilitário adaptado**, **importado**.

| Campo | O que é |
| --- | --- |
| **Tipo de veículo** | Carro, Caminhão ou Moto |
| **Marca**, **Modelo**, **Ano** | Livres (ou pela FIPE) |
| **Combustível** | Gasolina, Etanol, Diesel, Flex, GNV ou Elétrico |
| **Identificação interna** | O nome curto do tipo — veja abaixo |

A **identificação interna** é o *"nome curto exibido nas listas e ao montar o roteiro"*; o nome técnico (marca, modelo e ano) fica como informação secundária. Assim que você completa marca, modelo e ano, o LocFlow **sugere** um nome — diferente dos tipos que você já tem — e você aceita com **Usar sugestão** ou digita o seu ("Baú grande", "Strada da equipe A").

{% hint style="info" %}
**Por que um apelido?** "VW Delivery 2022" não diz nada para quem está no pátio. "Baú grande" diz. O apelido é a linguagem da sua equipe — e é por ele que o tipo fica fácil de reconhecer numa lista cheia.
{% endhint %}

### 2 e 3 · Carroceria e capacidade {#carroceria-e-capacidade}

A **carroceria** diz se o veículo tem **baú fechado** (*"Carroceria fechada e cubável — habilita a volumétrica e pede as dimensões abaixo."*). A **capacidade** diz quanto cabe, por quatro estratégias: contagem de itens, volume, peso máximo e — em breve — o empacotamento 3D. Tudo isso está em detalhe em [Tipos de veículo: capacidade](frota-capacidade.md).

{% hint style="warning" %}
Um tipo **sem contagem, volume ou peso** pode ser salvo, mas a tela avisa: *"Tipo sem contagem, volume ou peso cadastrados: o sistema não confere carga nem sugere agrupamento para ela."* Vale preencher pelo menos uma medida.
{% endhint %}

### Copiar a capacidade de outro veículo do grupo {#copiar-capacidade}

Contar quantas peças cabem num veículo dá trabalho — e não faz sentido recontar tudo para o segundo veículo idêntico. Quando outro tipo **do mesmo grupo** já tem capacidade cadastrada, o bloco de capacidade mostra **Copiar de outro veículo do grupo** (*"Há 1 com capacidade cadastrada."*).

1. Toque em **Copiar de outro veículo do grupo**.
2. Escolha de onde copiar — cada opção mostra o resumo do que vem junto, como *"12 itens contados · 18 m³ · 3.500 kg"*.
3. Pronto: *"Capacidade copiada — Veio de … Ajuste se este veículo for diferente."*

O valor copiado **passa a ser deste tipo** e é editável — não fica amarrado ao de origem: cada um continua com a medição própria. Se você já tinha preenchido alguma capacidade, a folha avisa que ela será substituída.

{% hint style="info" %}
Como o atalho depende do grupo, ele aparece quando o tipo já tem grupo — na edição, ou depois de escolher o grupo no último bloco do cadastro.
{% endhint %}

### 4 e 5 · Vistoria e custo operacional {#vistoria-e-custo}

- **Vistoria** (opcional): o checklist de inspeção do veículo, com a frequência por gatilho — veja [Tipos de veículo: vistoria](frota-vistoria.md).
- **Custo operacional** (opcional): **Ativar custo operacional** abre **Consumo (km/L)** e **Preço do combustível (R$/L)**. Com os dois, o cadastro mostra *"Custo de combustível estimado: R$ … por km rodado."* — veja [Custo operacional](frota-capacidade.md#custo-operacional).

### 6 · Grupo: o último passo, e obrigatório {#grupo}

Todo tipo entra num **grupo** — e é **você** quem escolhe qual: um existente, pela busca, ou um novo, digitado ali mesmo (**Criar o grupo "…"**). Quando a capacidade que você digitou combina com um grupo que já existe, a tela **sugere** esse grupo, com um botão **Entrar**. Sem grupo, o tipo não é salvo: *"Escolha o grupo deste tipo, ou crie um novo."* Entenda o que o grupo significa em [Grupos da frota](frota-grupos.md).

## Editar um tipo {#editar}

Abra o tipo na aba **Tipos de veículo** e edite. Tudo o que você muda vale para **todos os veículos daquele tipo** — é a vantagem de descrever o modelo uma vez só. Na edição, o titular também pode ser trocado (veja [Titular do tipo](frota-titular.md)).

## Situações reais {#situacoes-reais}

- **Cinco Fiorinos iguais:** você cadastra um tipo "Fiorino baú" (marca, modelo e ano pela FIPE, baú fechado com as medidas, "cabem 15 cadeiras") e cinco veículos com placas diferentes. Meses depois, descobre que cabem 16: muda no tipo e vale para os cinco.
- **A carretinha que não está na FIPE:** você digita marca, modelo e ano à mão e salva — a FIPE é atalho, não regra.
- **O segundo caminhão de outra marca, mesmo baú:** você cria o tipo novo, escolhe o grupo "Caminhão Toco" e toca em **Copiar de outro veículo do grupo** — a contagem que alguém já fez no pátio vem pronta, e você só confere.

## Próximo passo {#proximo-passo}

Veja como medir o que cabe em [Tipos de veículo: capacidade](frota-capacidade.md), como programar a checagem em [Tipos de veículo: vistoria](frota-vistoria.md) e como o grupo entra no roteiro em [Grupos da frota](frota-grupos.md). Para a visão geral, volte a [Frota](frota.md).
