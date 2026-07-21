---
icon: unlock-keyhole
description: O que destrava a Rede de Parceiros na sua organização — o cadastro do recebedor, a validação de identidade e a aprovação que habilitam a divisão de valores.
---

# Liberando o Programa de Parceiros

Para trabalhar em parceria com outra empresa e **dividir os ganhos de um pedido automaticamente**, o dinheiro precisa entrar pelo **pagamento online** e ser repartido na origem. Esta página é sobre esse pré-requisito: **o que você precisa concluir para a Rede de Parceiros ficar disponível** na sua organização.

{% hint style="info" %}
**Esta página é só a liberação.** Como a parceria funciona no dia a dia — acordos, repasse de pedidos, ganhos e reputação — está na seção [Rede de Parceiros](../parcerias/visao-geral.md), que já descreve tudo o que está no ar.
{% endhint %}

{% hint style="info" %}
**Onde fica:** no menu da sua organização, em **Parceiros**. A tela mostra um botão **"Entenda como funciona"** com o resumo do programa.
{% endhint %}

## O que é <a id="o-que-e"></a>

Imagine que você fecha um pedido com um cliente, mas quem entrega (ou parte do material) vem de uma **empresa parceira**. Em vez de fazer acertos por fora — planilha, conversa de WhatsApp, conferência no fim do mês — o LocFlow registra o **acordo** entre as duas empresas e, quando o cliente paga, **divide os valores conforme o combinado**.

Em palavras simples, como diz a própria tela:

> Você fecha acordos com parceiros e o sistema organiza regras, valores e divisão de ganhos para tudo funcionar com menos trabalho manual.

O programa se apoia em quatro ideias:

| Ideia | O que significa para você |
| --- | --- |
| **Acordos simples e claros** | Você define com quem vai trabalhar e quais regras valem para cada parceria. |
| **Valores combinados antes de começar** | Preço dos itens, frete e condições ficam registrados no acordo — sem conversa perdida. |
| **Comissionamento automático** | Quando o pagamento entra, o sistema divide os valores conforme o combinado entre as partes. |
| **Mais agilidade no dia a dia** | Previsibilidade financeira e menos operação manual em repasses e conferências. |

## Como funciona <a id="como-funciona"></a>

A parceria nasce de um **acordo** entre duas empresas: uma que fecha a venda com o cliente (o lado **vendedor**) e outra que entra com material e/ou logística (o lado **parceiro**). O acordo registra quais itens entram, os valores e como os ganhos se dividem.

O acordo passa por um **fluxo de aceite** — um vai e volta entre as partes até as duas concordarem:

```mermaid
flowchart LR
    A[Voce propoe<br/>o acordo] --> B[Parceiro ajusta<br/>ou aceita]
    B -->|aceita| C[Acordo ativo]
    B -->|ajusta| A
    B -->|recusa| D[Acordo recusado]
```

1. Uma parte **propõe** o acordo (itens, valores, divisão).
2. A outra **ajusta** (faz uma contraproposta) ou **aceita**.
3. Quando ambas concordam, a parceria fica **ativa** e passa a valer para os pedidos repassados.

{% hint style="info" %}
Esse vai e volta evita mal-entendido: nada começa a valer sem o "ok" das duas empresas. Enquanto não há acordo, cada pedido segue normal, só seu.
{% endhint %}

{% hint style="info" %}
O vai e volta do aceite, os itens que entram, o gatilho do repasse e a vigência estão detalhados em [Acordos de parceria](../parcerias/acordos-de-parceria.md).
{% endhint %}

## O funil de liberação <a id="o-funil-de-liberacao"></a>

Para dividir valores de um pedido entre você e um parceiro, o dinheiro precisa entrar pelo **pagamento online** e ser repartido na origem. Por isso, **o Programa de Parceiros só libera depois que a sua integração de pagamento estiver aprovada**.

É o mesmo cadastro do **recebedor** que você usa para receber online — explicado em [Pagamento online](../cobranca/pagamento-online.md). Enquanto a integração não estiver pronta, a tela de Parceiros mostra um **passo a passo** com o que falta e um atalho para concluir.

{% hint style="info" %}
**Atalho:** **Ajustes › Integrações › Integração de Pagamento.** É lá que você cadastra e acompanha o recebedor.
{% endhint %}

### Passo a passo para liberar <a id="passo-a-passo-para-liberar"></a>

A tela acompanha quatro marcos. Cada um acende quando o anterior é concluído:

```mermaid
flowchart LR
    R[1. Cadastrar<br/>recebedor] --> K[2. Gerar link<br/>de validacao]
    K --> V[3. Concluir<br/>validacao - KYC]
    V --> A[4. Aprovacao<br/>do recebedor]
    A --> L[Programa<br/>liberado]
```

| Marco | O que acontece |
| --- | --- |
| **1) Cadastrar recebedor** | Você preenche os dados básicos e bancários da sua locadora. O cadastro é enviado para análise. |
| **2) Gerar link de validação** | Você gera um link e envia ao responsável legal da empresa. |
| **3) Concluir validação (KYC)** | O responsável confirma a identidade pelo link. A partir daí, fica em análise. |
| **4) Aprovação do recebedor** | Quando aprovado, **o Programa de Parceiros é liberado** e o recebimento online fica ativo. |

{% hint style="warning" %}
**A aprovação é automática e pode levar algumas horas.** Ela acontece em segundo plano — você não precisa ficar olhando. Quando quiser conferir, **puxe a tela para baixo para atualizar**. Estar "em validação" **não** é o mesmo que aprovado: é preciso gerar o link e o responsável concluir a confirmação de identidade.
{% endhint %}

Quando tudo fica verde, a tela mostra: **"Tudo pronto! O split de pagamento está habilitado para esta organização."** A partir daí você já pode [entrar na rede](../parcerias/entrando-na-rede.md), fechar [acordos](../parcerias/acordos-de-parceria.md) e [repassar pedidos](../parcerias/repassando-um-pedido.md).

{% hint style="info" %}
**Quem ativa:** o cadastro do recebedor é feito por quem administra a conta. Se você não tem esse acesso, peça ao responsável — o sistema mostra o motivo, ninguém fica travado sem entender o porquê.
{% endhint %}

## Quem recebe o que <a id="quem-recebe-o-que"></a>

Quando um pedido em parceria é pago, o valor que o cliente paga é repartido **na hora**, conforme o acordo, sem você lançar nada à mão.

### Divisão de ganhos <a id="divisao-de-ganhos"></a>

O acordo define:

* **O repasse** — quanto, de cada parcela paga, vai para a empresa parceira.
* **A sua parte** — o que sobra para você depois do repasse e da taxa de plataforma.
* **A taxa de plataforma** — o percentual que o LocFlow retém sobre o valor recebido. O acordo também combina **como essa taxa se divide** entre as duas empresas.
* **Quem cuida de quê** — quem é responsável por **reembolsos** ao cliente, em caso de cancelamento, e quem arca com a **taxa de processamento** do pagamento. O padrão recai sobre o lado vendedor, mas isso faz parte do que se combina.

{% hint style="info" %}
A soma sempre fecha: **a sua parte + a parte do parceiro + a taxa de plataforma = o valor pago pelo cliente**. Nada some, nada some sem registro.
{% endhint %}

{% hint style="warning" %}
Os percentuais, valores e limites exatos do programa fazem parte das **condições comerciais** e podem variar por plano. Confira sempre os números que aparecem **no próprio acordo**, na hora de fechá-lo — é o acordo que vale.
{% endhint %}

## Depois de liberar <a id="depois-de-liberar"></a>

Com a integração aprovada, a Rede de Parceiros fica disponível no **alternador de espaço de trabalho** (o seletor *Operação ↔ Rede de Parceiros*). O caminho a partir daí:

1. [Entrando na rede](../parcerias/entrando-na-rede.md) — o perfil público e a descoberta de outras operações.
2. [Acordos de parceria](../parcerias/acordos-de-parceria.md) — os termos, o aceite das duas partes e a vigência.
3. [Repassando um pedido](../parcerias/repassando-um-pedido.md) — como um pedido seu vai para o parceiro.
4. [O dinheiro da parceria](../parcerias/dinheiro-da-parceria.md) — repasses, ganhos e a divisão no pagamento.

## Situações reais <a id="situacoes-reais"></a>

**"Concluí a validação, mas o programa não liberou."**
Estar "em validação" não é o mesmo que aprovado. A aprovação é automática e **pode levar algumas horas**. Puxe a tela para baixo para atualizar. Se não tiver gerado o **link de validação** e o responsável não tiver concluído, esse é o passo que falta — veja [Pagamento online](../cobranca/pagamento-online.md).

**"Não consigo cadastrar o recebedor."**
O cadastro é feito por quem **administra a conta**. Se você não tem esse acesso, o sistema orienta a pedir ao responsável.

## Próximo passo <a id="proximo-passo"></a>

* [Rede de Parceiros: a visão](../parcerias/visao-geral.md) — como a parceria funciona depois de liberada.
* [Pagamento online](../cobranca/pagamento-online.md) — o recebedor, a validação (KYC) e a aprovação que liberam o programa.
* [A página de pagamento do cliente](../cobranca/pagina-de-pagamento.md) — por onde o dinheiro entra e é repartido.
* [Integrações](integracoes.md) — onde você acompanha tudo que conecta o LocFlow ao mundo de fora.
* [Minha assinatura e créditos](assinatura-e-creditos.md) — recursos avançados podem depender do seu plano.
