---
icon: money-bill-transfer
description: Monte as cobranças que calculam o frete — quando cada uma incide, cobrar por uma medida ou usá-la como critério, e o que fazer quando se sobrepõem.
---

# Montando as cobranças do frete

O **Motor de Frete** é onde você ensina o LocFlow a **calcular sozinho o valor do transporte**. Em vez de digitar o frete à mão a cada orçamento, você descreve uma vez como cobra — "R$ 4 por quilômetro", "R$ 500 fixo para Sorocaba", "taxa de combustível em toda viagem" — e o sistema aplica isso automaticamente no orçamento.

Esta página é sobre **montar essas cobranças**: quando cada uma entra, como ela calcula o valor, e o que acontece quando duas se aplicam à mesma viagem. Aqui você está configurando o **cálculo** do frete.

{% hint style="info" %}
Não confunda com a **política de aprovação** do frete (automática / acima de um limite / sempre manual), que vive no **Motor Operacional de Frete** e está em [Aprovação de orçamentos](../orcamentos/aprovacao.md). São coisas diferentes: lá você decide **quem precisa autorizar** um frete; aqui você decide **quanto ele custa**.
{% endhint %}

## O que é uma cobrança {#o-que-e-uma-cobranca}

Você pensa em **cobranças**, não em fórmulas. Uma **cobrança** responde a duas perguntas:

1. **Quando ela se aplica?** — em qualquer viagem, só para certos municípios, só acima de tantos km, só em alta temporada… Isto é o **gatilho**.
2. **Quanto ela cobra?** — um valor fixo, um valor por quilômetro, um valor por minuto, ou uma combinação desses.

Você pode ter **uma só** cobrança que vale para todo frete, ou **várias** cobranças, cada uma para uma situação. O cálculo final do frete de um orçamento é a soma do que cada cobrança aplicável apurar em **cada viagem**.

### Como você cobra pelo seu frete? {#perfis}

Ao abrir o motor, o LocFlow pergunta qual perfil descreve a sua operação. A escolha não muda o resultado do cálculo — muda **quanto** você precisa configurar:

| Perfil | Para quem |
| --- | --- |
| **Tenho um método único de cobrança** | *"Uma cobrança que vale para todos os fretes. Mais fácil de configurar."* É o **mais comum**. |
| **Tenho vários métodos de cobrança** | *"Várias cobranças combinadas — uma por situação (município, distância, época do ano…)."* |
| **Quero montar regras manualmente** | *"Editor avançado com condições aninhadas e múltiplas ações por regra."* |

Você pode trocar de perfil depois. Esta página cobre os perfis de **uma** e de **várias** cobranças — que dão conta da grande maioria das operações.

## Passo 1 — Quando essa cobrança se aplica? {#gatilho}

O **gatilho** é a situação que liga a cobrança. O LocFlow organiza as opções por eixo:

| Eixo | Gatilhos | O que significa |
| --- | --- | --- |
| **Universal** | Qualquer viagem | *"Cobra sempre, em toda viagem."* |
| **Percurso da viagem** | Município de destino · Município de origem · Distância percorrida · Tempo de transporte · Distância em linha reta | Pelo lugar, pelos quilômetros, pela duração ou pela distância radial entre origem e destino. |
| **Carga e veículo** | Peso da carga · Volume da carga · Especificação veicular | Pela carga transportada ou pelo **tipo de veículo** que a viagem usa (baú, utilitário, guincho…). |
| **Quando o frete acontece** | Sazonalidade · Período do dia | Em épocas do ano (Natal, alta temporada…) ou faixas do dia (manhã, pico…). |

{% hint style="info" %}
**Sazonalidade** e **período do dia** usam as épocas e os horários que você cadastra em [Horários e sazonalidades](horarios-e-sazonalidades.md). Se a lista aparecer vazia, cadastre-os primeiro: *"Cadastre épocas em Configurações para usar esse gatilho."*
{% endhint %}

Escolher um gatilho **substitui** o anterior — cada cobrança tem **um** gatilho. Alguns pedem detalhe ali mesmo: município pede a lista de cidades; **especificação veicular** pede quais veículos.

{% hint style="info" %}
A **especificação veicular** liga a cobrança ao **tipo de veículo** da viagem — você escolhe entre as especificações que já cadastrou na Frota (baú, utilitário, guincho, refrigerado…). É útil quando o custo do frete muda conforme o veículo, não conforme o destino ou a distância. Se a lista aparecer vazia, cadastre-as primeiro: *"Cadastre especificações na Frota para usar esse gatilho."*
{% endhint %}

### A cobrança é por viagem, não por orçamento {#por-rota-nao-por-viagem}

Esse é o aviso operacional mais importante do motor, e ele aparece destacado na tela. **Verbatim:**

> **A cobrança é por viagem, não por rota.**
>
> Cada viagem é ida e volta. Um valor fixo de R$ 250, por exemplo, vira:
>
> **Venda:** R$ 250 — 1 viagem (a entrega)
> **Aluguel:** R$ 500 — 2 viagens (entrega + retirada)
>
> Km e minutos já somam a ida e a volta de cada viagem.

Em palavras: o LocFlow calcula cada **viagem** — cada movimento (a entrega ou a retirada) — separadamente, tratando a **ida e a volta como uma coisa só**. Uma entrega é **uma** viagem; na locação, a **retirada** é outra. Por isso uma cobrança de **R$ 100 fixo** num aluguel não vira R$ 100 no frete: ela incide em **cada viagem** aplicável (nas duas), fechando **R$ 200**.

{% hint style="warning" %}
Pense no valor da cobrança como o custo de **uma viagem** (um movimento, ida e volta), não da operação inteira. É o que evita sobrecobrar sem perceber.
{% endhint %}

{% hint style="info" %}
**Entrega e retirada custam o mesmo por viagem.** Numa locação, as duas viagens vão para o **mesmo destino** — a cidade do cliente —, então toda cobrança (por município, distância, tempo, peso…) incide **igual** na entrega e na retirada. **Não dá para definir um preço só para a entrega e outro só para a retirada:** o motor calcula por viagem (ida e volta) e não separa os dois movimentos. É por isso que um aluguel típico fecha em **2× o valor da viagem**.
{% endhint %}

## Passo 2 — Cobrar por essa medida, ou usá-la como critério? {#cobrar-x-criterio}

Quando o gatilho é **numérico** (distância, tempo, distância em linha reta, peso ou volume), o LocFlow faz uma pergunta extra — porque uma medida pode servir a dois papéis bem diferentes:

| Escolha | O que faz | Verbatim |
| --- | --- | --- |
| **Cobrar por ela** | A medida **vira preço**: você define um valor por unidade no próximo passo. | *"Vou definir um preço por [unidade] no próximo passo."* |
| **Usar como critério** | A medida **vira condição**: a cobrança só entra quando a medida está dentro de um valor que você definir. | *"Cobrar só quando [medida] estiver dentro de um valor que eu definir."* |

Esta é a distinção central do motor. Um exemplo com **distância**:

* **Cobrar por ela** → "cobro R$ 4 **por quilômetro** rodado". A distância multiplica o valor.
* **Usar como critério** → "só cobro a taxa de longa distância **a partir de 50 km**". A distância apenas **liga ou desliga** a cobrança; o valor vem do Passo 3.

Quando você escolhe **usar como critério**, define o recorte:

| Modo | Significa |
| --- | --- |
| **A partir de** | A medida tem que ser **maior ou igual** ao valor (ex.: distância ≥ 50 km). |
| **Até** | A medida tem que ser **menor ou igual** ao valor (ex.: peso ≤ 100 kg). |
| **Entre dois valores** | A medida tem que cair numa **faixa** (ex.: entre 50 e 100 km). |

{% hint style="info" %}
A mesma medida pode aparecer em **duas** cobranças com papéis diferentes: uma usa a distância **como critério** ("acima de 50 km, +R$ 80 fixo") e outra cobra **por ela** ("R$ 4/km em toda viagem"). Não há contradição — são cobranças distintas que somam.
{% endhint %}

## Passo 3 — Quanto você cobra por viagem? {#quanto-cobrar}

Aqui você define o valor. São **três formatos combináveis** — pode ligar quantos quiser, e eles **se somam**:

| Formato | O que faz | Verbatim |
| --- | --- | --- |
| **Valor fixo** | Um valor em reais sempre que a cobrança se aplica. | *"Cobro esse valor sempre que a cobrança se aplica."* |
| **Por km rodado** | Multiplica o valor pela distância da viagem (ida e volta). | *"Multiplico esse valor pela distância da viagem (ida e volta)."* |
| **Por minuto de transporte** | Multiplica o valor pela duração da viagem (ida e volta) em minutos. | *"Multiplico esse valor pela duração da viagem (ida e volta) em minutos."* |

No formato **por minuto** você ainda escolhe **considerar trânsito** (estimativa do mapa, mais realista) ou não (tempo de rota ideal).

Combinar é o caso comum: uma cobrança "Qualquer viagem" com **R$ 30 fixo + R$ 4 por km** vira, numa viagem cujo trajeto de ida e volta dá 20 km, `30 + (4 × 20) = R$ 110` — **por viagem**.

{% hint style="info" %}
O cálculo por **km** e por **minuto** usa a **rota real** medida no mapa entre o galpão e o destino — não a linha reta nem faixa de CEP. Por isso o cálculo de frete no orçamento **consome créditos** (ele consulta o mapa). Veja [Valores](../orcamentos/valores.md#frete).
{% endhint %}

## Passo 4 — Limites (opcional) {#limites}

A maioria das cobranças não precisa de nada aqui. Os limites servem para **controlar valores extremos**, e cada um vale **por viagem**, igual à cobrança:

| Limite | Verbatim |
| --- | --- |
| **Cobro no mínimo (piso)** | *"Se o cálculo der menos que esse valor, cobro esse mínimo."* |
| **Cobro no máximo (teto)** | *"Se o cálculo der mais que esse valor, cobro esse máximo."* |
| **Distância mínima cobrada** | *"Para cobranças por km: distâncias menores que esse valor são tratadas como esse valor."* |

Exemplo: cobrança "R$ 4/km" com **piso de R$ 50**. Uma entrega de 8 km daria R$ 32, mas o piso garante o mínimo de **R$ 50**. Já a **distância mínima cobrada** atua antes da conta — se você define 10 km, uma viagem de 6 km é calculada **como se fosse 10 km**.

## Como as cobranças se combinam (ou conflitam) {#combinar-x-conflitar}

Quando você tem **várias** cobranças, o LocFlow precisa saber se elas **somam** ou se **uma exclui a outra**. Ele decide isso sozinho, pela natureza do gatilho — você não precisa entender o mecanismo, mas vale conhecer a lógica:

```mermaid
flowchart TD
    A[Cobranças que se aplicam à mesma viagem] --> B{Que tipo de gatilho?}
    B -->|Qualquer viagem, sazonalidade,<br/>período, a partir de / até| C[SOMAM<br/>todas entram no cálculo]
    B -->|Município, especificação veicular,<br/>faixa entre dois valores| D[EXCLUSIVAS<br/>só a primeira da lista vale]
```

* **Acumuladoras (somam):** "Qualquer viagem", sazonalidade, período do dia e os critérios **a partir de** / **até** isolados. São cobranças que se **empilham** — a taxa de combustível soma à cobrança por km, que soma à taxa de alta temporada.
* **Exclusivas (a primeira vence):** município (origem ou destino), **especificação veicular** e **faixas** (entre dois valores). Estas expressam "para *este* caso, *este* preço" — não faz sentido somar "R$ 500 para Sorocaba" com "R$ 700 para Campinas", nem "R$ 300 no baú" com "R$ 150 no utilitário", na mesma viagem.

### Quando duas exclusivas se sobrepõem {#conflito}

Se você cadastra duas cobranças exclusivas que **podem valer ao mesmo tempo** (por exemplo, uma lista de municípios que inclui a mesma cidade), o LocFlow avisa na hora de salvar. **Verbatim:**

> **Essas duas cobranças se sobrepõem.**
> Quando ambas se aplicam à mesma entrega, o motor usa só a primeira da lista. Escolha qual deve vir primeiro.

Você decide a ordem com **Manter esta ordem** ou **Inverter ordem**. A que ficar **em primeiro** é a que prevalece quando as duas se aplicam.

{% hint style="info" %}
Esse aviso só aparece para cobranças **do mesmo tipo** de gatilho que claramente se cruzam (dois municípios, duas especificações veiculares, duas faixas de distância…). Sobreposições entre **tipos diferentes** (um município *e* uma faixa de km) não geram esse aviso — elas dependem da rota concreta e são resolvidas no momento do cálculo.
{% endhint %}

## Situações reais {#situacoes-reais}

| Situação | Como montar |
| --- | --- |
| **Cobro sempre por distância** | Uma cobrança · gatilho **Qualquer viagem** · **Por km rodado** (ex.: R$ 4/km). Perfil de cobrança única resolve. |
| **Taxa fixa de saída + por km** | Uma cobrança · **Qualquer viagem** · ligue **Valor fixo** (R$ 30) **e** **Por km** (R$ 4). Eles somam, por viagem. |
| **Preço fechado por cidade** | Uma cobrança por município de destino, cada uma com seu **Valor fixo**. São **exclusivas**: a viagem cai numa cidade só. |
| **Preço por tipo de veículo** | Uma cobrança **Especificação veicular** para o **baú** (ex.: R$ 300 fixo) e outra para o **utilitário** (ex.: R$ 150 fixo). São **exclusivas**: cada viagem usa um veículo só, então vence a primeira compatível — nunca somam. |
| **Cobro só viagens longas** | Gatilho **Distância**, **usar como critério**, **a partir de 50 km**; no valor, **R$ 80 fixo**. Abaixo de 50 km, não entra. |
| **Frete mais caro na alta temporada** | Uma cobrança extra com gatilho **Sazonalidade** (a época cadastrada) e um **Valor fixo**. Ela **soma** ao frete normal naquele período. |
| **Garantir um mínimo de frete** | Na sua cobrança por km, abra **Limites** e defina **Cobro no mínimo** (piso). |

## Por porte {#por-porte}

| Porte | Como costuma usar |
| --- | --- |
| **Autônomo / MEI / pequeno** | Uma **cobrança única** (perfil "método único") — geralmente por km, ou um fixo simples. Configura em minutos e esquece. |
| **Médio** | Algumas cobranças combinadas: por km em toda viagem + faixas ou municípios para casos especiais + um piso de frete. |
| **Grande / muitas filiais** | Várias cobranças por município e faixas, com sazonalidade e período do dia; quando precisa de lógica fina (condições aninhadas), o editor manual. |

O LocFlow **abstrai para o pequeno e revela para o grande**: você começa com uma cobrança e vai acrescentando situações conforme a operação pede.

## Para quem quer os detalhes {#detalhes}

* **1 cobrança = 1 regra de cálculo.** Os três formatos (fixo, por km, por minuto) ligados na mesma cobrança viram **componentes somados** dentro dela; a ordem matemática é cuidada pelo sistema.
* **A ordem da lista importa só para as exclusivas.** Entre cobranças que somam, a ordem é indiferente. Entre exclusivas que se cruzam, vale **a primeira** — é o que o aviso de sobreposição deixa você decidir.
* **As exclusivas são avaliadas antes das acumuladoras.** Isso permite o padrão "para Sorocaba uso R$ 500 fixo, **e em cima disso** somo a taxa de combustível": a cobrança específica define a base, e as que somam se acrescentam.
* **"A partir de 0" não é critério.** Se você marca "usar como critério" mas o mínimo é zero, na prática a cobrança vale para qualquer rota — o sistema entende isso como "cobrar sempre".

## Próximo passo {#proximo-passo}

* Onde o resultado aparece no orçamento: [Valores: acréscimos, frete e descontos](../orcamentos/valores.md#frete)
* Quem autoriza fretes altos: [Aprovação de orçamentos](../orcamentos/aprovacao.md)
* Cadastrar épocas e horários para os gatilhos: [Horários e sazonalidades](horarios-e-sazonalidades.md)
* Visão geral dos motores: [Motores operacionais](motores-operacionais.md)
