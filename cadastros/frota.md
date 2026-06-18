---
icon: truck
description: Como cadastrar sua frota no LocFlow — do "iniciar sem veículo" ao veículo com placa, organizado em classes e especificações com capacidade e vistoria.
---

# Frota

A frota é o conjunto de veículos que leva seus [bens móveis](../primeiros-passos/glossario.md) até o cliente e os traz de volta. No LocFlow, você cadastra a frota para **planejar roteiros com veículo e capacidade** — saber o que cabe em cada carro, quem está disponível e quanto a entrega vai render.

Mas calma: cadastrar a frota **não é obrigatório para começar**. O LocFlow abstrai para quem está começando e revela detalhe para quem cresceu. Você sobe a escada no seu ritmo.

{% hint style="info" %}
A Frota faz parte dos recursos **Pro**. Se você ainda não vê o módulo, é porque seu plano não o inclui — e tudo bem: dá para operar entregas sem ele (veja a seguir).
{% endhint %}

## A escada da frota

Você não precisa configurar tudo de uma vez. Cada degrau acrescenta controle, sem travar o anterior.

```mermaid
flowchart LR
    A[Iniciar sem veiculo] --> B[Veiculo com placa]
    B --> C[Classes]
    C --> D[Especificacoes]
    D --> E[Capacidade e vistoria]
```

| Degrau | O que você ganha | Para quem |
| --- | --- | --- |
| **Iniciar sem veículo** | Entrega sai mesmo sem frota cadastrada | Quem está começando ou faz entrega avulsa |
| **Veículo com placa** | Saber qual carro saiu e seu status | Quem tem 1 ou 2 carros próprios |
| **Classes** | Agrupar a frota por tipo (carro, caminhão, moto) | Quem tem veículos variados |
| **Especificações** | Ficha técnica por modelo (marca, ano, combustível) | Quem quer organizar por modelo |
| **Capacidade e vistoria** | Saber o que cabe e checar o carro antes de rodar | Quem otimiza carga e cuida da manutenção |

### Degrau 1 — Iniciar sem veículo (opcional)

Você pode **iniciar uma entrega ou retirada sem selecionar nenhum veículo**. O LocFlow nunca trava o caminho mais simples: se você ainda não cadastrou a frota, ou se a entrega é avulsa, o sistema avisa que o registro ficará sem veículo (um aviso suave, não bloqueante) e deixa você seguir com um toque.

{% hint style="success" %}
**Por que isso te ajuda:** ninguém deixa de entregar por falta de cadastro. Você começa a faturar hoje e organiza a frota depois, quando fizer sentido. Zero fricção para quem está começando.
{% endhint %}

### Degrau 2 — Veículo com placa e status

Quando quiser controle, cadastre o veículo. O essencial é simples:

- **Placa** — obrigatória (ex.: `ABC1D23`). É o que identifica o veículo na rua.
- **Identificador interno** — opcional, o apelido que sua equipe usa (ex.: "Caminhão 01").
- **Especificação** — qual ficha técnica esse veículo segue (veja o degrau 4).

Todo veículo **nasce Ativo**. O status muda por **ações** na lista da frota, não no cadastro:

| Status | O que significa |
| --- | --- |
| **Ativo** | Disponível para receber roteiros |
| **Manutenção** | Parado para reparo — não entra em novas atribuições |
| **Inativo** | Fora de operação — não aparece para atribuir |

{% hint style="info" %}
Quando um veículo está rodando em um roteiro não concluído, ele aparece como **Em trânsito**, mesmo estando Ativo. Assim você não atribui dois roteiros ao mesmo carro por engano.
{% endhint %}

### Degraus 3 e 4 — Classes e Especificações

Aqui está a organização que dá inteligência à frota. São três níveis encaixados:

```mermaid
flowchart TD
    C["Classe<br/>(ex.: Caminhao Toco)"] --> E1["Especificacao<br/>(VW Delivery 2022, Diesel)"]
    C --> E2["Especificacao<br/>(MB Accelo 2020, Diesel)"]
    E1 --> V1["Veiculo<br/>placa ABC1D23"]
    E1 --> V2["Veiculo<br/>placa DEF4G56"]
    E2 --> V3["Veiculo<br/>placa GHI7J89"]
```

- **Classe** é só o **nome** que você dá a um tipo de veículo. Você informa o nome (ex.: "Caminhão Toco") e escolhe o **tipo de veículo** entre **Carros**, **Caminhões** ou **Motos** (base do catálogo FIPE). O sistema cuida do código por trás — você não precisa se preocupar com ele.
- **Especificação** é a **ficha técnica** de um modelo dentro de uma classe. Você escolhe a classe e, em seguida, **marca, modelo e ano** vêm prontos do catálogo FIPE (basta buscar e selecionar). O **combustível** vem sugerido pela FIPE, e você pode ajustar (Gasolina, Etanol, Diesel, Flex, GNV, Elétrico).
- **Veículo** é a unidade real, com **placa**, ligada a uma especificação.

Pense assim: a **Classe** diz *que tipo* de veículo é, a **Especificação** diz *qual modelo*, e o **Veículo** diz *qual carro* (a placa).

### A especificação guarda capacidade e vistoria

Ao criar uma especificação, dois blocos **opcionais** dão superpoderes à frota:

**Capacidade** — o que cabe no veículo:

- **Dimensões do baú** — comprimento, largura e altura em metros. O LocFlow calcula o **volume (m³)** automaticamente. (É tudo-ou-nada: ou você informa as três medidas, ou nenhuma.)
- **Limites de contagem** — quantos de cada **produto** ou **kit** cabem por viagem (ex.: "10 tendas", "4 geradores"). Você seleciona o item do catálogo e a quantidade.

**Vistoria** — o checklist de checagem do veículo:

- **Template** — o nome do checklist (ex.: "Checklist padrão").
- **Frequência (dias)** — de quantos em quantos dias a vistoria deve ser refeita (ex.: 30).
- **Itens do checklist** — o que conferir antes de rodar (ex.: "Pneus", "Lona traseira", "Óleo"). Adicione quantos quiser.

{% hint style="success" %}
**Por que capacidade e vistoria fazem você ganhar mais:** com a capacidade definida, o LocFlow avalia se a carga cabe e ajuda a otimizar o roteiro — menos viagens, mais entregas por dia. Com a vistoria em dia, você evita o carro quebrar no meio da rota (frete perdido, cliente irritado, avaria no material). Frota organizada = operação que não para.
{% endhint %}

## Situações reais

- **Locadora de festas começando:** ainda não cadastrou frota. Recebe um pedido, despacha a entrega **sem veículo** e entrega na hora. Mês que vem, cadastra a Kombi com placa para começar a controlar.
- **Quem tem caminhão e van:** cria duas classes ("Caminhão Toco" e "Van Furgão"), uma especificação por modelo e os veículos com placa. Agora sabe, na hora de planejar, qual carro tem baú maior para a carga do dia.
- **Frota que cresceu:** define a capacidade do baú e os limites por produto ("cabem 10 tendas no Toco"). O sistema passa a alertar quando a carga não cabe e sugere a melhor distribuição — e a vistoria a cada 30 dias mantém os caminhões rodando sem surpresa.

## Próximo passo

Com a frota pronta, veja [Planejando o roteiro](../logistica/planejando-o-roteiro.md) e [Execução em campo](../logistica/execucao-em-campo.md). Em dúvida sobre um termo? Consulte o [Glossário](../primeiros-passos/glossario.md) ou veja [Onde tirar dúvidas](../primeiros-passos/onde-tirar-duvidas.md).
