---
icon: weight-hanging
description: Como o LocFlow decide se a carga cabe no veículo — contagem e volumétrica, e por que o baú fechado libera o cálculo por volume.
---

# Especificações: capacidade

A **capacidade** é o que diz ao LocFlow se a carga de uma viagem **cabe** no veículo. Você configura a capacidade dentro de cada [especificação](frota.md) (a ficha técnica de um modelo), e o app usa essa configuração na hora de [planejar o roteiro](../logistica/planejando-o-roteiro.md): conforme você monta a rota, ele soma o que vai ser transportado e compara com o que o veículo comporta.

É sempre um **aviso, nunca um bloqueio**. Quando a carga não cabe, o app destaca o problema para você decidir — tirar uma parada, dividir em duas viagens ou trocar o veículo. Você nunca fica travado.

{% hint style="info" %}
A capacidade é **opcional**. Uma especificação sem capacidade configurada funciona normalmente — o app só não consegue avaliar se a carga cabe (mostra um aviso de "não verificado", e segue). Veja a [escada da frota](frota.md#a-escada-da-frota): você sobe esse degrau quando faz sentido. **A exceção:** se você marcar o veículo como **baú fechado**, aí as dimensões do baú passam a ser **obrigatórias** (veja abaixo).
{% endhint %}

## As estratégias de capacidade {#estrategias}

No LocFlow, "capacidade" não é um número único. São **estratégias** diferentes de medir o que cabe, cada uma boa para um tipo de carga. Na tela de capacidade da especificação, você ativa uma ou mais — cada uma com seu próprio cartão numerado.

| # | Estratégia | O que mede | Selo |
| --- | --- | --- | --- |
| 1 | **Contagem de itens** | Quantos de cada produto ou kit cabem fisicamente | `EMPÍRICA` |
| 2 | **Volumétrica (m³)** | O volume do baú (C × L × A) contra a cubagem da carga | `CUBAGEM` |
| 3 | **Empacotamento inteligente (3D)** | Simulação do arranjo da carga | `EM BREVE` |

{% hint style="info" %}
A tela traz um quadro lateral **"Como a capacidade é calculada"** que resume tudo isto numa linha do tempo. O texto de abertura: *"Na operação, as estratégias ativas rodam em ordem. A primeira que reprovar limita a carga."*
{% endhint %}

### 1 · Contagem de itens {#contagem}

A contagem é a forma mais direta — e a mais fácil de configurar. Você responde, na prática: **"quantas unidades de cada item cabem nessa viagem?"**

O cartão a descreve como *"Quantos produtos/kits cabem fisicamente. Avaliada primeiro."* — por isso o selo **EMPÍRICA**: é o número que você sabe de cabeça, da experiência ("no Toco cabem 10 tendas").

Para configurar, você adiciona **linhas de limite**:

- **Item** — escolhido do seu [catálogo](catalogo-produtos.md) numa **busca única**: produtos **e** kits aparecem juntos (como no orçamento), cada um com a **miniatura**, o **nome** e a etiqueta **Produto** ou **Kit**. Você não escolhe a "natureza" antes — busca direto pelo nome e toca no item.
- **Quantidade** — quantas unidades daquele item cabem (um número inteiro, maior que zero); depois toque em **Adicionar item**.

Você adiciona quantas linhas quiser, uma por item. Cada uma entra na lista com a miniatura e o **nome** do item (não o código). Não dá para repetir o mesmo item duas vezes — o app avisa *"Este item já foi adicionado."*

{% hint style="success" %}
**Por que isso te ajuda:** a contagem é a régua que você já tem na cabeça, agora dentro do sistema. Se "cabem 10 tendas no Toco", o app passa a alertar quando a viagem do dia tenta levar a décima primeira — antes de o motorista descobrir na rampa de carga.
{% endhint %}

Você pode deixar a contagem **ativa sem nenhuma linha**. Nesse caso o app mostra *"Nenhum limite adicionado. A capacidade pode ficar sem limites por item."* — ou seja, ela existe mas não restringe nada ainda.

### 2 · Volumétrica (m³) {#volumetrica}

A volumétrica raciocina por **espaço**, não por contagem: ela calcula o **volume útil do baú** e compara com o volume que a carga ocupa.

As **medidas do baú** ficam no passo **2 · Carroceria** (não dentro do cartão da estratégia): ao ligar **"Baú fechado"**, aparecem ali os três campos — **comprimento**, **largura** e **altura**, em metros — e o LocFlow calcula o **volume do baú (m³)** sozinho, mostrando o resultado na hora.

Por isso o cartão da volumétrica, na seção de estratégias, é **só informativo** (não tem campos): ele mostra o **status** — *"Pronta — volume do baú X m³"* quando as medidas estão cadastradas, ou um lembrete para informá-las na Carroceria. O selo é **CUBAGEM**, e ela é avaliada **automaticamente** quando a carga é mista (não é uma chave que você liga/desliga).

{% hint style="success" %}
**Por que a volumétrica importa para carga mista:** quando a viagem leva itens variados (mesa, tenda, gerador), contar "quantos de cada" não responde se tudo cabe junto. O volume responde: a soma do que vai ocupando precisa caber no espaço do baú.
{% endhint %}

## O baú fechado e suas dimensões {#bau-fechado}

A chave que liga tudo isso é **"Baú fechado"**, no passo **2 · Carroceria** — *"Carroceria fechada e cubável. Exige as dimensões do baú (abaixo) e habilita a estratégia volumétrica."*

A regra é direta: **um baú fechado é cubável e por isso exige as três medidas cadastradas.** Ao marcar "Baú fechado", os campos de comprimento, largura e altura aparecem logo abaixo e passam a ser **obrigatórios** — sem eles, o app **não deixa salvar** a especificação (*"Baú fechado exige as três medidas…"*). É o que fecha a lacuna do "volume não verificado": se o baú é fechado, o volume tem que estar lá.

**E o baú aberto?** Um caminhão de carroceria aberta (uma prancha, um carro-de-boi) não tem um espaço fechado com volume confiável — a carga passa das laterais, empilha para cima. Para esses, você **deixa "Baú fechado" desligado**: não há dimensões a informar e a volumétrica simplesmente **não se aplica** (a contagem continua disponível normalmente).

{% hint style="info" %}
A **contagem** não depende do baú — você pode usá-la em qualquer veículo. A diferença entre baú **aberto** e **fechado** é o que decide se a volumétrica entra em cena: aberto → não se aplica; fechado → exige as dimensões e fica pronta.
{% endhint %}

```mermaid
flowchart TD
    A[Carroceria do veiculo] --> B{Bau fechado?}
    B -- Sim --> C[Informe C x L x A<br/>obrigatorio: volumetrica pronta]
    B -- Nao --> D[Bau aberto<br/>volumetrica nao se aplica; so contagem]
```

## Custo operacional: peso e combustível {#custo-operacional}

A especificação tem um passo **opcional** chamado **"Custo operacional"** — separado dos demais porque o cadastro já é longo, e **tudo nele é opcional**. Ele alimenta duas coisas no [planejamento do roteiro](../logistica/planejando-o-roteiro.md): a **capacidade por peso** e a **estimativa de combustível**.

| Campo | Para que serve |
| --- | --- |
| **Peso máximo de carga (kg)** | Mais uma régua de capacidade: o app avisa quando a carga **ultrapassa o peso** que o veículo aguenta — mesmo que caiba em volume. |
| **Consumo (km/L)** | Quantos quilômetros o veículo faz por litro. |
| **Preço do combustível (R$/L)** | Quanto custa o litro abastecido. |

### Capacidade por peso

O **peso máximo** funciona como as outras estratégias, mas pela **balança**: a otimização inteligente **pula** uma parada cuja carga faria o veículo passar do peso (*"acima do peso máximo do veículo"*), e o aviso de capacidade do roteiro também olha o **pico de peso** ao longo da rota. É o caso clássico de carga **pesada e pequena** (sacos de cimento, peças de ferro): cabe no baú de sobra, mas estoura o eixo.

### Estimativa de combustível

**Consumo e preço andam juntos** — informe os dois (sozinhos, um não vira custo). Com eles, o app calcula o **custo de combustível por km** e, no planejamento, mostra o **custo estimado da rota** (no card *"Ida e volta"* e no roteiro salvo). Ao preencher, o próprio cadastro já mostra uma **prévia** do custo por km.

{% hint style="info" %}
São **estimativas de planejamento**, baseadas no consumo médio que você declarou — servem para comparar rotas e decidir, não são um valor cobrado. Veja onde aparecem em [Planejando o roteiro](../logistica/planejando-o-roteiro.md#o-resumo-ida-e-volta).
{% endhint %}

## Como o app decide se a carga cabe {#avaliacao}

Quando você [planeja um roteiro](../logistica/planejando-o-roteiro.md) com um veículo (ou só a especificação) escolhido, o LocFlow avalia a capacidade automaticamente. Vale entender o que ele faz por baixo:

1. **Carga vazia ou sem alvo concreto** → não há o que avaliar: o app aprova com um aviso (por exemplo, quando você escolheu uma *classe* de veículo em vez de um veículo específico, ou nenhum).
2. **Carga de um único item** (só tendas, por exemplo) → entra a **contagem**: ele soma a quantidade total e compara com o limite que você cadastrou para aquele item.
3. **Carga com itens diferentes** (mistura de produtos/kits) → entra a **volumétrica**: ele soma a cubagem de tudo e compara com o volume do baú.

Quando a estratégia escolhida **não tem como verificar**, o app **não bloqueia** — e agora diz o **motivo exato**, em vez de um "não verificado" genérico:

- **Baú aberto** → a volumétrica não se aplica (o veículo não é cubável).
- **Baú fechado sem dimensões** → falta cadastrar as medidas do baú na especificação (a corrigir).
- **Sem limite do item** → falta cadastrar a quantidade-limite daquele item para a contagem.

{% hint style="info" %}
A avaliação olha o **pico** da viagem, não só o fim. Numa rota com várias entregas e retiradas, o ponto mais cheio pode estar no meio do caminho — é esse momento que o app verifica, porque é onde a carga corre risco de não caber.
{% endhint %}

No planejamento do roteiro, esse raciocínio aparece **didático**: o painel mostra a estratégia escolhida e, ao expandir **"Como chegamos nessa estratégia"**, exibe o passo a passo — *passo 1 contagem (pulada porque a carga é mista), passo 2 volumétrica (o resultado), passo 3 inteligente 3D (ainda não avaliada)*. Assim você entende **por que** aquela estratégia foi usada, não só o resultado.

A mensagem que aparece quando estoura é direta. Pela contagem: *"A carga (12) excede o limite de 10 unidade(s) deste item."* Pela volumétrica: *"O volume da carga excede o volume do baú."*

{% hint style="warning" %}
**É sempre um aviso, não um bloqueio.** Mesmo quando a carga não cabe, você consegue criar o roteiro — o LocFlow destaca a parada crítica e deixa a decisão com você. A filosofia é a mesma da [frota como um todo](frota.md): nunca travar o caminho da operação.
{% endhint %}

## Bloco avançado {#avancado}

<details>

<summary>Combinando estratégias e o empacotamento 3D</summary>

**Posso ativar contagem e volumétrica ao mesmo tempo?** Sim — a seção de capacidade diz *"Ative uma ou mais estratégias... pode combinar contagem e volumétrica."* Na configuração, as duas convivem: você define limites por item **e** as dimensões do baú na mesma especificação.

**Empacotamento inteligente (3D).** O terceiro cartão — *"Simulação 3D do arranjo da carga para máximo aproveitamento."* — está marcado **EM BREVE** e ainda não pode ser ativado. A ideia futura é simular como as peças se encaixam de fato no baú (não só o volume bruto), para apertar ao máximo cada viagem.

{% hint style="info" %}
**Em breve:** o empacotamento 3D vai além de somar volumes — ele considera o formato e o encaixe das peças. Por enquanto, contagem e volumétrica já cobrem a grande maioria das operações.
{% endhint %}

</details>

## Situações reais {#situacoes}

- **Locadora de tendas, um produto só:** a viagem leva só tendas. Você cadastra na contagem "10 tendas" no caminhão Toco. Quando o roteiro do dia tenta levar 12, o app avisa que a carga excede o limite — você divide em duas viagens antes de sair.
- **Festa completa, carga mista:** mesas, cadeiras, tendas e som na mesma rota. Aqui a contagem não basta. Você marca o baú como fechado, informa as medidas (4,20 × 2,10 × 2,10 m → o app calcula ~18,5 m³) e o LocFlow passa a somar o volume de tudo e avisar quando não cabe junto.
- **Caminhão de carroceria aberta:** uma prancha que leva andaimes. Você tenta ligar a volumétrica e ela aparece bloqueada — "Disponível apenas para baú fechado". Faz sentido: sem caixa fechada, não há volume confiável. Você usa a contagem ("cabem 30 quadros de andaime") e segue.

## Próximo passo {#proximo-passo}

A capacidade é só um dos blocos da especificação. Veja a página principal de [Frota](frota.md) para entender classes, veículos e a vistoria. Para ver a capacidade em ação, vá a [Planejando o roteiro](../logistica/planejando-o-roteiro.md) — é lá que o aviso "a carga cabe?" aparece. Em dúvida sobre um termo? Consulte o [Glossário](../primeiros-passos/glossario.md).
