---
icon: truck-fast
description: Como o LocFlow calcula o frete — a Rota Estimada (pior cenário), o princípio "por viagem" (ida e volta como uma coisa só), os perfis e o simulador.
---

# Motor de Frete: como calcula

O **Motor de Frete** é onde você ensina o LocFlow a calcular o transporte sozinho. Você descreve uma vez **como cobra pelo seu frete** — e, a cada orçamento com endereços preenchidos, o sistema mede a rota e aplica as suas regras, sem você fazer conta.

Esta página é sobre **como o cálculo funciona por dentro**. Onde você **usa** o resultado (a chave "Cobrar frete", as abas automático/manual, o botão "Calcular frete") é assunto de [Valores: mão de obra, frete e descontos](../orcamentos/valores.md). Onde você **liga** o motor, junto dos outros, é [Motores operacionais](motores-operacionais.md).

{% hint style="info" %}
**Frete automático precisa do Motor de Frete configurado.** Sem ele, o orçamento abre direto no campo de **frete manual** — você digita um valor fechado e segue. O motor é o que troca "digitar à mão" por "calcular sozinho".
{% endhint %}

## A base de tudo: a Rota Estimada {#a-base-de-tudo-a-rota-estimada}

Antes de qualquer regra, o motor precisa saber **quanto se anda** para atender o pedido. Ele resolve isso com a **Rota Estimada** — e esse é o conceito que destrava tudo o resto.

{% hint style="info" %}
Texto de ajuda do próprio app (tela do motor):

> O motor calcula o frete sobre uma **Rota Estimada** — a rota considerada no pior cenário possível.
>
> É como se só esse orçamento existisse e o veículo saísse do galpão **exclusivamente para ele**, mesmo que na prática outras entregas saiam juntas no mesmo veículo.
{% endhint %}

Por que "pior cenário"? Porque, na hora do orçamento, você ainda não sabe se aquele veículo vai sair só para esse cliente ou cheio de outras entregas. O motor assume o caso mais caro — ida e volta dedicadas — para **nunca subfaturar o transporte**. Quando o roteiro for de fato planejado, depois do pedido ganho, o LocFlow otimiza a logística de verdade; mas o **preço** que o cliente vê nasce dessa estimativa conservadora.

### Por que "2 viagens" num aluguel {#a-base-de-tudo-a-rota-estimada}

Cada **viagem** é **ida e volta como uma coisa só** — a Rota Estimada de um movimento já inclui o caminho de ida e o de volta. E um aluguel típico tem **dois movimentos** (a entrega e a retirada), ou seja, **duas viagens**:

{% hint style="info" %}
Texto de ajuda do app:

> Um aluguel típico envolve **duas viagens**:
> 1. Viagem de entrega (galpão → cliente → galpão)
> 2. Viagem de retirada (galpão → cliente → galpão)
>
> Cada viagem é a **ida e a volta** de um movimento, contadas como uma só. Por isso, valores e limites configurados aqui valem **por viagem**, não por orçamento.
{% endhint %}

```mermaid
flowchart LR
    G1[Galpao] -->|Viagem de entrega: ida| C1[Cliente]
    C1 -->|volta| G2[Galpao]
    G2 -->|Viagem de retirada: ida| C2[Cliente]
    C2 -->|volta| G3[Galpao]
```

Numa **venda** não há devolução: o item sai em definitivo, então sobra **1 viagem** (a entrega, ida e volta). E se o cliente **retira no galpão**, ou **devolve no galpão**, aquele movimento some — e com ele some a sua viagem. O motor só conta o que tem deslocamento real.

## Por viagem, não por orçamento {#por-rota-nao-por-viagem}

Este é o ponto que mais gera confusão — e o que o app mais reforça. **Cada valor que você define é aplicado a cada viagem**, não ao orçamento inteiro.

{% hint style="warning" %}
Texto de ajuda do app — leia com atenção, porque ele evita a sobrecobrança mais comum:

> Cada cobrança que você cria é aplicada **a cada viagem** — não ao orçamento inteiro.
>
> Em um aluguel típico (2 viagens), uma cobrança de **R$ 500 fixo** somaria **R$ 1.000** ao frete final (2 × R$ 500). Por isso é importante pensar **por viagem** ao definir valores.
{% endhint %}

A regra de bolso vem do próprio app:

> Quer cobrar R$ 500 totais no aluguel? Configure **R$ 250 por viagem** — o motor aplica nas 2 viagens (entrega e retirada) e o frete final fecha em R$ 500.

```mermaid
flowchart TB
    V["R$ 250 por viagem"] --> R1["Viagem de entrega: R$ 250"]
    V --> R2["Viagem de retirada: R$ 250"]
    R1 & R2 --> T["Frete final: R$ 500"]
```

Pense sempre em **uma viagem** (um movimento, ida e volta) ao definir um valor. O motor multiplica pelo número de viagens do cenário — e o [simulador](#o-simulador) mostra a soma final antes de você publicar, justamente para não escorregar nisso.

{% hint style="info" %}
**O que dobra e o que não dobra.** O **valor fixo** e a **carga** (peso e volume) contam **uma vez por viagem** — não dobram porque o veículo vai e volta. Já as regras por **km** ou por **tempo** consideram o trajeto **inteiro da viagem** (ida e volta somadas): é a única grandeza que junta os dois trechos.
{% endhint %}

## Os três perfis {#os-tres-perfis}

Configurar o motor começa por uma pergunta única: **como você cobra pelo seu frete?** A resposta abre um de três perfis — do mais enxuto ao mais flexível. Você escolhe o que descreve a sua operação, e **pode trocar de perfil depois**.

> **Como você cobra pelo seu frete?** Escolha a opção que melhor descreve a sua operação. Você pode mudar de perfil depois.

| Perfil | A pergunta que ele responde | O que ele abre |
| --- | --- | --- |
| **Simples** | "Tenho um método único de cobrança" | **Uma** cobrança que vale para todos os fretes. Mais fácil de configurar. |
| **Intermediário** | "Tenho vários métodos de cobrança" | **Várias** cobranças combinadas — uma por situação (município, distância, época do ano…). |
| **Avançado** | "Quero montar regras manualmente" | Editor de regras com condições aninhadas e múltiplas ações. |

{% hint style="success" %}
Não sabe qual escolher? O app marca **Simples** como "mais comum". A maioria das operações começa com uma cobrança só e cresce de perfil quando a vida pede — sem perder o que já configurou.
{% endhint %}

### Perfil Simples {#perfil-simples}

> No perfil simples você configura **uma única cobrança** — aquela que vale para todos os fretes calculados pelo motor.

É o caminho de quem cobra de um jeito só. Exemplo direto do app:

> *"Cobrar R$ 3,50 por km com mínimo de R$ 80"* é uma cobrança simples e suficiente para muitas operações começarem.

E o app já aponta o próximo degrau, para você não se sentir preso:

> Se um dia você precisar tratar situações diferentes (cobrar mais para um município específico, somar uma taxa de combustível, ter preço por época do ano), passe para o perfil **Vários métodos** — lá você adiciona quantas cobranças quiser **sem perder a que já configurou**.

### Perfil Intermediário {#perfil-intermediario}

Aqui você monta uma **lista** de cobranças, e o motor combina todas que se encaixam em cada viagem.

{% hint style="info" %}
Texto de ajuda do app:

> No perfil "vários métodos" você cria uma **lista** de cobranças. Para cada entrega, o motor olha a lista inteira e aplica todas as que se encaixam.
>
> Cobranças com **situações específicas** (como "para Sorocaba" ou "entre 0 e 50 km") são exclusivas: se duas se encaixam, vale só a que aparece primeiro na lista. Reorganize-a para controlar a precedência.
>
> Cobranças com **situações amplas** (como "qualquer entrega" ou "em épocas") sempre somam às demais. Use-as para taxas que valem em cima do valor já calculado.
{% endhint %}

Em resumo: cobrança **específica** = só a primeira da lista vale (reordene para mandar na prioridade); cobrança **ampla** = sempre soma por cima. O exemplo do app fecha a ideia:

> Duas cobranças para Sorocaba só usam a primeira da lista. Uma "Taxa de combustível" com gatilho "qualquer entrega" sempre soma ao valor final, independentemente.

### Perfil Avançado {#perfil-avancado}

O perfil para quem quer controle total. Em vez de "cobranças", você monta **regras** com condições combinadas por **E / OU**, agrupamentos aninhados, múltiplas ações por regra e limites finos. É o mesmo motor por baixo — só com a porta dos detalhes escancarada.

{% hint style="info" %}
**Recurso de operação madura.** O editor avançado faz sentido para quem tem regras de frete realmente complexas (por veículo, por faixa, por época cruzada com distância). Para a maioria, **Simples** ou **Intermediário** dão conta — e o Avançado fica reservado para quando você precisar dele.
{% endhint %}

{% hint style="warning" %}
**Trocar de perfil pode simplificar regras.** Ir de Avançado para Intermediário ou Simples reduz o que não cabe na abstração mais enxuta — o app sempre avisa antes e **preserva a configuração original** até você confirmar. O caminho inverso (subir de perfil) nunca perde nada.
{% endhint %}

## O que é uma cobrança {#o-que-e-uma-cobranca}

Nos perfis Simples e Intermediário você nunca pensa em "regra" — pensa em **cobrança**, que é uma linguagem bem mais natural.

{% hint style="info" %}
Texto de ajuda do app:

> Uma **cobrança** é uma situação que você sabe descrever ("para Sorocaba", "no fim de semana", "para entregas longas") com um valor associado ("R$ 500 fixo", "R$ 3/km", "20% a mais").
>
> Você só pensa em **situações e valores**. O motor analisa cada viagem e aplica todas as cobranças que se encaixam, somando tudo no final.
{% endhint %}

Cada cobrança se monta em poucos passos: **quando ela vale** (o gatilho), **quanto cobra** (valor fixo, por km, por minuto) e, se quiser, **limites** (piso, teto, distância mínima).

### Gatilhos e critérios {#gatilhos-e-criterios}

O **gatilho** é a situação que liga a cobrança.

> O **gatilho** define quando a cobrança se aplica: município, distância, tempo de transporte, raio, peso, volume, épocas do ano ou período do dia.

Para os gatilhos numéricos (km, minutos, kg, m³…), o app faz uma pergunta esperta — **cobrar pela variável** ou **usá-la como filtro**:

> Para variáveis numéricas (km, kg, min, etc.), você decide entre **cobrar por ela** (preço por unidade) ou **usar como critério** (cobrar só quando o valor estiver dentro de um mínimo, máximo ou faixa).

| Você quer… | Escolha | O que acontece |
| --- | --- | --- |
| Multiplicar por quanto andou | **Cobrar por ela** | Define um preço por unidade (ex.: R$ 3 por km). |
| Cobrar só em certos casos | **Usar como critério** | A cobrança só vale se o valor estiver dentro de um mínimo, máximo ou faixa (ex.: "entre 0 e 50 km"). |

Exemplo combinando os dois, direto do app:

> Gatilho "distância" + critério "entre 0 e 50 km" + valor "R$ 100 fixo + R$ 3/km" = cobrança específica para viagens curtas.

{% hint style="info" %}
Os gatilhos de **sazonalidade** (épocas do ano) e **período do dia** usam as listas que você cadastra em [Horários e sazonalidades](horarios-e-sazonalidades.md). Sem nada cadastrado lá, o app avisa que não há épocas/períodos para escolher.
{% endhint %}

### Limites da cobrança {#limites-da-cobranca}

Opcionais, para travar valores extremos. Os textos de ajuda do app explicam cada um:

| Limite | Ajuda do app |
| --- | --- |
| **Cobro no mínimo (piso)** | *"Se o cálculo der menos que esse valor, cobro esse mínimo."* |
| **Cobro no máximo (teto)** | *"Se o cálculo der mais que esse valor, cobro esse máximo."* |
| **Distância mínima cobrada** | *"Para cobranças por km: distâncias menores que esse valor são tratadas como esse valor."* |

{% hint style="warning" %}
**Os limites também valem por viagem.** Um piso de R$ 80 garante R$ 80 em *cada* viagem — num aluguel de 2 viagens, isso é R$ 160 de mínimo no frete. A mesma lógica de [por viagem, não por orçamento](#por-rota-nao-por-viagem) vale aqui.
{% endhint %}

## O simulador {#o-simulador}

Antes de publicar — e a qualquer momento depois — você pode **testar o motor com cenários hipotéticos**, sem criar orçamento de verdade e **sem gastar créditos**.

{% hint style="success" %}
**O simulador é local.** Ele não consulta o mapa nem cria rota real — só roda o seu cálculo de regras com valores que você inventa. Como o próprio app diz: *"Os cálculos são locais — nenhuma rota real é criada."* O cálculo de frete que **consome créditos** é só o do orçamento real, quando mede a rota de verdade.
{% endhint %}

Como funciona: você escolhe o **cenário logístico** (Aluguel ou Venda; cliente retira/devolve no galpão ou não) e o simulador mostra **quantas viagens** aquele cenário gera. Depois você preenche valores hipotéticos (distância, peso, município…) e vê o **frete final**, com o detalhamento de quais regras foram aplicadas e quantas vezes cada uma.

> Espelha os mesmos controles do orçamento: ajuste para ver como o cenário muda a quantidade de viagens calculadas.

É a melhor forma de pegar o erro de sobrecobrança antes que ele chegue num cliente: monte um aluguel, veja o frete fechar em 2× o valor por viagem, e ajuste se não for o que você esperava.

{% hint style="info" %}
Se as suas regras dependem de **especificação veicular**, o simulador avisa que a **distribuição da carga em viagens** ainda não está disponível ali — o cálculo real no orçamento continua funcionando normalmente.
{% endhint %}

## Quando o frete é seu e quando é terceirizado {#composicao-do-frete}

O que você configura aqui é o **custo** de transportar a carga. No orçamento, esse custo vira a **composição do frete**: cada transportadora disponível — a **sua própria organização** e cada **fornecedor de frete** cadastrado — é cotada pelo **seu próprio motor**, e você escolhe quem leva. Se marcar mais de uma, a carga divide as viagens entre elas e o frete final é a **soma das porções**. Sobre um fornecedor, o custo dele é só o começo: você define **quanto repassa ao cliente** — igual ao custo, mais (para ter margem) ou menos (para absorver). O detalhe de como isso aparece está em [A composição do frete](../orcamentos/valores.md#composicao-do-frete).

Quando há fornecedores, o LocFlow também usa uma **estratégia de alocação** para recomendar quem transporta: **menor preço**, **aproveitamento** (prioriza a sua própria frota) ou **manual**. Você define a regra padrão da organização e pode trocá-la só para um orçamento. Como cada transportadora tem o seu motor, versões e histórico próprios, o assunto ganha página inteira em [Motor de Frete por detentor](motor-de-frete-detentor.md).

## Por porte {#por-porte}

A mesma tela serve do autônomo ao grande operador — muda só o quanto você mexe.

| Seu porte | Como configurar o frete |
| --- | --- |
| **Autônomo / micro** | Muitas vezes nem precisa do motor: frete **manual**, valor fechado por pedido. Se quiser automatizar, o perfil **Simples** com uma cobrança "R$ X por km, mínimo R$ Y" resolve. |
| **Médio** | Perfil **Simples** ou **Intermediário**: uma cobrança base + uma taxa de combustível que soma sempre, ou preços diferentes por município. Use o simulador para calibrar. |
| **Grande** | Perfil **Intermediário** com várias cobranças por situação, ou o **Avançado** para regras por veículo/faixa e condições cruzadas. Controle fino, real a real. |

A filosofia é a mesma de todo o LocFlow: **abstrair para quem quer simplicidade, revelar números e flexibilidade para quem quer controle.**

---

## Para quem quer os detalhes {#para-quem-quer-os-detalhes}

Daqui para baixo é detalhe de quem gosta de saber a conta por trás. Você **não** precisa disso para usar o motor.

### A Rota Estimada em números {#a-rota-estimada-em-numeros}

Cada **viagem** é sempre um **par fechado** (a ida tem a sua volta) — a Rota Estimada de um movimento. A quantidade de viagens de um orçamento é o número de **movimentos com deslocamento**:

| Cenário | Movimentos com deslocamento | Viagens |
| --- | --- | --- |
| **Venda** com entrega | Entrega (ida e volta) | **1** |
| **Aluguel** com entrega e retirada | Entrega + Retirada | **2** |
| **Aluguel**, cliente retira no galpão | Só retirada | **1** |
| Cliente retira **e** devolve no galpão | Nenhum | **0** (sem frete a calcular) |

O motor avalia **cada regra contra cada viagem** e **soma** os resultados. Por isso o valor por viagem é a unidade de raciocínio certa.

### Ordem das ações {#ordem-das-acoes}

No perfil **Avançado**, uma regra pode ter várias ações. Independentemente da ordem em que você as cadastrou, o cálculo segue **sempre** esta sequência (texto do app):

> 1. Acréscimo fixo (R$)
> 2. Por unidade (R$/km, R$/min…)
> 3. Acréscimo percentual (%)
> 4. Multiplicador (×)
> 5. Valor fixo (substitui o corrente; ações posteriores atuam sobre ele)

E como as regras se combinam entre si:

> **Primeira compatível** — dentre as regras com esse comportamento, só a de maior prioridade (menor número) é executada. As demais são ignoradas.
>
> **Acumuladora** — sempre executada se as condições baterem, somando ao que as outras regras já calcularam.

(Nos perfis Simples e Intermediário, isso aparece com a linguagem de cobrança "específica" × "ampla" — é a mesma mecânica.)

### Parâmetros disponíveis {#parametros-disponiveis}

O que o motor consegue olhar em cada viagem (texto do app, perfil Avançado):

> **Geotemporais** (condição e ação) — distância percorrida (ida e volta da viagem), distância radial, tempo de transporte com trânsito e sem trânsito.
>
> **Carga** (condição e ação) — peso bruto e volume. Contam **uma vez por viagem** (não dobram na ida e volta); a disposição dos materiais por veículo ainda não é considerada.
>
> **Categóricos** (só condição) — município de origem/destino e **especificação veicular** (o tipo de veículo que leva a carga).
>
> **Temporais** (só condição) — intervalos de tempo do dia e intervalos sazonais anuais. Exigem horários estimados de saída e chegada da Rota.

### Motor versionado {#motor-versionado}

O Motor de Frete guarda histórico (texto do app):

> Toda alteração no motor cria uma nova versão. Versões anteriores ficam preservadas — você consegue auditar exatamente qual configuração foi usada em qualquer frete já calculado.

Na prática: você edita à vontade em **rascunho**, simula, e só quando **publica** o motor passa a valer para os orçamentos novos. Os fretes já calculados continuam atrelados à versão que os gerou — nada muda retroativamente.

{% hint style="info" %}
**Cálculo do frete × aprovação do frete são dois ajustes diferentes.** Esta página é sobre **quanto** o frete custa. **Se** um frete alto precisa de aval antes de o orçamento seguir é a *política de aprovação*, configurada à parte — veja [Aprovação de orçamento](../orcamentos/aprovacao.md) e [Motores operacionais](motores-operacionais.md).
{% endhint %}

## Situações reais {#situacoes-reais}

- **"Coloquei R$ 500 e o frete saiu R$ 1.000."** É o motor aplicando os R$ 500 nas 2 viagens do aluguel. Você queria R$ 500 totais? Configure **R$ 250 por viagem**. Confira no simulador antes de publicar.
- **Taxa de combustível em cima de tudo.** No perfil Intermediário, crie uma cobrança com gatilho "qualquer viagem" e um valor (fixo ou %). Por ser **ampla**, ela sempre soma ao que as outras cobranças já calcularam.
- **Preço diferente por cidade.** Duas cobranças "para Sorocaba" e "para Campinas", cada uma com seu valor. Como são **específicas**, o motor usa a que casar com o destino — e a ordem na lista resolve empates.
- **Frete mínimo para entregas curtas.** Cobrança por km com **piso** de R$ 80: viagens curtas nunca saem abaixo do mínimo operacional. Lembre que o piso vale por viagem.
- **Testar sem gastar crédito.** Antes de mexer no motor de verdade, abra o simulador, monte um aluguel típico e veja o frete final — tudo local, zero consumo.

## Próximo passo {#proximo-passo}

- Veja onde o resultado aparece no orçamento em [Valores: mão de obra, frete e descontos](../orcamentos/valores.md).
- Entenda os movimentos que geram as viagens em [Movimentos, janelas e galpão de origem](../orcamentos/movimentos-e-janelas.md).
- Ligue o motor junto dos outros em [Motores operacionais](motores-operacionais.md).
- Dê um motor a cada fornecedor de frete em [Motor de Frete por detentor](motor-de-frete-detentor.md).
- Cadastre épocas e períodos do dia para os gatilhos temporais em [Horários e sazonalidades](horarios-e-sazonalidades.md).
- Configure **quando** um frete alto trava o orçamento em [Aprovação de orçamento](../orcamentos/aprovacao.md).
- Dúvida em algum termo? Consulte o [glossário](../primeiros-passos/glossario.md).
