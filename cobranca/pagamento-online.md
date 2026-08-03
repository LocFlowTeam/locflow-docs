---
icon: credit-card
description: Link de pagamento (PIX, boleto e cartão) com baixa automática em tempo real. Ative o recebedor e receba mais rápido.
---

# Pagamento online

Com o pagamento online, o cliente paga **direto por um link**, sem você precisar registrar nada. Quando ele paga, a fatura se atualiza sozinha — **em tempo real**. É a forma mais rápida e segura de receber, e a que mais reduz inadimplência. Serve igual para **locação** e para **venda** de bens móveis.

{% hint style="success" %}
**Por que isso te faz receber mais:** quanto mais fácil pagar, mais gente paga — e mais cedo. Um PIX que o cliente abre e quita em segundos cobra melhor do que uma promessa de "te mando depois". Recebimento mais rápido, menos cobrança atrasada, menos calote.
{% endhint %}

## Como funciona

```mermaid
flowchart LR
    A[Gera o link na fatura] --> B[Envia ao cliente]
    B --> C[Cliente abre e paga]
    C --> D[LocFlow recebe a confirmacao]
    D --> E[Baixa automatica<br/>em tempo real]
```

1. Na fatura, gere o **link de pagamento**.
2. Envie ao cliente — copie e mande por WhatsApp, e-mail, ou compartilhe pelo próprio celular.
3. O cliente abre a página de pagamento e paga a parcela.
4. O LocFlow recebe a confirmação e dá a **baixa automática**, atualizando a fatura na hora.

Operador e cliente acompanham o mesmo link ao vivo: quando o cliente gera ou paga uma cobrança, a sua tela atualiza sozinha — sem precisar recarregar nada.

## O link de pagamento

O link é **público e por fatura**: o cliente paga **parcela a parcela** por uma página segura. Você controla **quais métodos** o link aceita.

| Método | Padrão | Observação |
| --- | --- | --- |
| **PIX** | Ligado | Vem habilitado por padrão — o jeito mais rápido de receber. |
| **Boleto** | Desligado | Você liga quando quiser. Exige o endereço do cliente. |
| **Cartão** | Desligado | Você liga quando quiser. |

Por padrão o link já vem só com **PIX**. Para aceitar boleto ou cartão, basta ligar o método no link — um toque. **Mantenha sempre ao menos um método habilitado.**

{% hint style="info" %}
**Dados do cliente:** alguns métodos pedem mais informação. **CPF/CNPJ e e-mail** são exigidos por todos — sem eles, o link nem é gerado. O **boleto** ainda precisa do **endereço**. O LocFlow mostra um checklist do que falta e deixa você completar ali mesmo, no mesmo gesto.
{% endhint %}

### Endereço personalizado do link

O link pode usar um endereço amigável com o nome da sua empresa, deixando a página de pagamento com a **sua identidade** — mais confiança para o cliente pagar. Domínio totalmente personalizado é um recurso dos planos superiores; veja [Domínio personalizado](../configuracoes/dominio-personalizado.md).

## Pré-requisitos por método

Cada método pede um conjunto mínimo de dados do cliente. Alguns **bloqueiam** (sem eles a cobrança não é gerada); outros são apenas **recomendados** (ajudam, mas não travam).

| Método | Bloqueia sem | Recomendado | Por quê |
| --- | --- | --- | --- |
| **PIX** | CPF/CNPJ, e-mail | Telefone | O telefone melhora o registro, mas não trava a geração. |
| **Boleto** | CPF/CNPJ, e-mail, **endereço** | — | O boleto é registrado: sem endereço completo, a página do boleto não abre para o cliente. |
| **Cartão** | CPF/CNPJ, e-mail | Endereço | O endereço de cobrança é pedido **no momento do pagamento** (CEP do pagador); o cadastro só pré-preenche. |

{% hint style="info" %}
Quando você liga **boleto** e falta o endereço, o LocFlow abre uma folha para completar e só habilita o método **depois que você salva** — o botão fica "Salvar e habilitar Boleto". Você nunca habilita um método que ainda não consegue cobrar.
{% endhint %}

O checklist do link mostra cada dado com um ✓ (já tem) ou um ponto âmbar (falta), e ao lado os ícones dos métodos que o exigem. **CPF/CNPJ e e-mail faltando** desligam o botão de gerar o link inteiro — porque nenhum método cobra sem eles.

## Cancelar e recriar: o que acontece com a cobrança anterior

Há **no máximo uma cobrança aberta por parcela**. Por isso, antes de criar uma nova cobrança para a mesma parcela, o LocFlow pede o cancelamento da anterior e acompanha a resposta do provedor.

* **PIX:** depois que o cancelamento é confirmado, o QR Code e o copia-e-cola param de funcionar.
* **Boleto:** o registro da cobrança é cancelado no LocFlow e no provedor — mas **o título não sai do DDA do cliente**. Entenda o porquê logo abaixo.

```mermaid
flowchart LR
    P[Parcela em aberto] -->|gera PIX| C1[Cobranca PIX aberta]
    C1 -->|troca de metodo| X[Cancelamento solicitado]
    X -->|provedor confirma| C2[Nova cobranca]
```

## Boleto cancelado continua no DDA — e isso não é um defeito do LocFlow

Todo boleto registrado entra numa base centralizada do sistema bancário (a CIP), que é o que o
DDA do seu cliente lê. Tirar um título dessa base antes da hora exige que o **emissor** comande a
baixa do registro — e o provedor de pagamentos usado pelo LocFlow (Stone/Pagar.me) **não executa
esse comando**. É uma limitação do emissor, confirmada por escrito pelo suporte do provedor: nem
ele consegue retirar o título.

Na prática, para um boleto cancelado:

* O título **continua aparecendo no DDA** do seu cliente até cerca de **60 dias após o
  vencimento** — depois disso expira sozinho e some.
* Durante esse período, o boleto **continua tecnicamente pagável** no banco. Se o cliente pagar
  mesmo assim, o LocFlow captura o pagamento e o trata como **recebimento tardio** — o dinheiro
  entra no histórico financeiro e você decide o destino (vale-locação ou devolução).
* O seu cliente **não tem nenhuma obrigação de pagar** um título de cobrança cancelada. O DDA é
  uma vitrine dos boletos emitidos no nome dele, não uma lista de dívidas exigíveis.

{% hint style="warning" %}
**O que dizer ao seu cliente (B2B):** "o boleto foi cancelado e não deve ser pago; ele continuará
visível no seu DDA por até 60 dias após o vencimento porque o registro bancário expira sozinho —
isso é do sistema bancário, não uma cobrança em aberto." Empresas com fluxo de contas a pagar
automatizado devem **remover o título da esteira de pagamento** para evitar pagamento indevido.
{% endhint %}

{% hint style="info" %}
Por isso, prefira **PIX** quando houver chance de o valor ou o método mudarem: o QR cancelado
para de funcionar na hora. Use boleto quando a cobrança for firme — cancelamentos de boleto
deixam esse rastro no DDA que gera dúvida para o pagador.
{% endhint %}

**Importante — abrir a página de novo NÃO invalida o código.** Se o cliente já está vendo um PIX ou boleto e atualiza a página (ou volta nela), o LocFlow **reaproveita a mesma cobrança aberta** daquele método em vez de criar outra. O QR Code e o boleto que ele tem na mão continuam valendo. Só uma **troca de método** (ou um cartão, que é sempre uma nova tentativa) inicia a substituição do instrumento anterior.

**Recebeu parte por fora (dinheiro, maquininha)?** Registrar uma baixa manual — ou um recebimento na rua — muda o valor que resta a receber, então o PIX/boleto em aberto daquela parcela **é cancelado junto**: ele cobrava o valor antigo. O LocFlow avisa antes de você confirmar e, se ainda restar saldo, já oferece **gerar o novo PIX ou boleto pelo valor certo** na mesma tela.

{% hint style="info" %}
**Cartão é diferente:** cada tentativa de cartão é uma transação própria, então o cartão nunca "reaproveita" — e a resposta é na hora (aprovado ou recusado, com o motivo em português).
{% endhint %}

## Pagamento confirmado não se desfaz na mão

Diferente da baixa manual (que você lança e pode corrigir), o pagamento online é uma **transação real**, processada pelo recebedor. Não existe botão de "desfazer": o dinheiro saiu da conta do cliente e entrou na sua, e isso não se apaga por decisão de operador.

Se sobrar valor a favor do cliente (por exemplo, uma edição que reduz o total depois de já ter sido pago), o LocFlow resolve pela **política de cobrança** da sua locadora — **crédito/vale** ou **reembolso**. Veja [Faturas e parcelas](faturas-e-parcelas.md).

### E se o dinheiro voltar mesmo assim? {#estorno}

Um pagamento pode voltar por fora do LocFlow: você pede o reembolso ao processador, ou o cliente **contesta a compra no cartão** (chargeback). Quando isso acontece, o LocFlow é avisado pelo processador e **reage sozinho**:

- a **parcela reabre** na fatura — o cliente volta a dever;
- a **entrada sai do seu financeiro**, para o seu saldo não mostrar um dinheiro que não está mais lá;
- se aquele pagamento carregava um **repasse de parceria** repartido na fonte, o repasse é revertido junto.

Se esse dinheiro já tinha virado **vale-locação**, o LocFlow primeiro desconta o saldo de vale que
ainda estiver disponível. Quando o cliente já usou uma parte ou todo o vale, somente a diferença
sem lastro vira uma **nova cobrança avulsa** no nome dele. O vale nunca fica negativo, e o histórico
mantém ligados o crédito original, o estorno e a cobrança de recuperação.

{% hint style="warning" %}
**O que o sistema não desfaz é o dinheiro que já se moveu.** Se o repasse ao parceiro já tinha sido **quitado** por você antes do estorno, o valor **não** volta automaticamente da conta dele — recuperar isso é uma conversa comercial entre vocês. Os detalhes de como o estorno afeta repasse e taxa estão em [O dinheiro da parceria](../parcerias/dinheiro-da-parceria.md#estorno).
{% endhint %}

---

## Ativando o recebimento

Para receber online, a sua organização precisa de uma **integração de pagamento ativa** — o **recebedor**, a conta da sua locadora que vai receber os valores das cobranças. A ativação é um cadastro guiado e passa por uma **verificação** (KYC) antes de liberar.

Você configura tudo em **Configurações → Pagamento (Integração de Pagamento)**. Enquanto a integração não está ativa, a seção de cobrança online da fatura explica o motivo e oferece o atalho para ativar.

{% hint style="info" %}
**Quem ativa:** o cadastro do recebedor é feito por quem administra a conta. Se você não tem esse acesso, o sistema orienta a pedir ao responsável — ninguém fica travado sem entender o porquê.
{% endhint %}

### Recebedor, KYC e aprovação

São três coisas que costumam confundir — explicadas em um lugar só, no texto do próprio app:

> **Recebedor** — a conta da sua locadora que vai receber os valores das cobranças.
> **Validação (KYC)** — checagem de identidade exigida por lei. O responsável confirma os dados pelo link.
> **Aprovação** — o recebedor libera os recebimentos. Só então a integração fica **Ativa**.

### O cadastro guiado do recebedor

O cadastro é um **wizard de 4 passos** (leva cerca de 8 minutos) e já vem **pré-preenchido** com os dados da sua organização para reduzir digitação.

```mermaid
flowchart LR
    P1[1. Identificacao] --> P2[2. Endereco e contato]
    P2 --> P3[3. Dados PF ou PJ]
    P3 --> P4[4. Conta bancaria]
```

| Passo | O que você informa |
| --- | --- |
| **1 · Identificação** | Quem vai receber: tipo (Pessoa Física ou Jurídica), nome, e-mail e CPF/CNPJ. Pode dar uma descrição interna (ex.: "Conta para recebimento das locações"). |
| **2 · Endereço e contato** | Endereço **completo** (incluindo complemento e ponto de referência) e um telefone. A verificação exige todos os campos. |
| **3 · Dados (PF ou PJ)** | **Pessoa Física:** data de nascimento, renda mensal e ocupação. **Pessoa Jurídica:** razão social, nome fantasia, faturamento anual e um **sócio administrador** completo (o representante legal com poderes de gestão). |
| **4 · Conta bancária** | Banco, agência, conta e dígito, tipo de conta e titular. Mostra um **resumo** dos passos anteriores para conferência antes de concluir. É a conta para onde os recebimentos vão. |

{% hint style="info" %}
**Atalhos que poupam digitação:** no cadastro PJ, você pode marcar "usar o mesmo endereço/nome/e-mail/telefone do recebedor" para o sócio administrador, sem reescrever tudo. Em locadoras pequenas, o sócio costuma ser a mesma pessoa e o mesmo endereço da empresa.
{% endhint %}

{% hint style="warning" %}
**Na edição, alguns campos travam:** depois do cadastro criado, o **tipo de pessoa** e o **documento (CPF/CNPJ)** ficam bloqueados — mudá-los exigiria reabrir o cadastro no recebedor. Para corrigir esses dois, fale com o suporte.
{% endhint %}

### Estados da integração

A integração caminha por quatro marcos: **Cadastrar recebedor → Validação (KYC) → Aprovação → Recebendo.** Os estados que você vê:

```mermaid
flowchart LR
    I[Inativo] -->|cadastra o recebedor| V[Em validacao / KYC]
    V -->|aprovado| A[Ativo]
    V -.recusado.-> R[Recusado]
    R -->|revisa e reenvia| V
    A -.bloqueado.-> B[Bloqueado]
```

| Estado | O que significa | O que fazer |
| --- | --- | --- |
| **Inativo** | Recebedor ainda não cadastrado. | Faça o cadastro guiado em 4 passos. |
| **Em validação (KYC)** | Cadastro enviado, aguardando a verificação de identidade. | **Gere o link de KYC** e envie ao responsável para confirmar a identidade. Depois, é aguardar a aprovação. |
| **Recusado** | A análise recusou o cadastro. | Revise os dados (documento e conta bancária) e **reenvie** para uma nova análise. |
| **Bloqueado** | A integração foi bloqueada. | Fale com o suporte para reativar. |
| **Ativo** | Tudo aprovado. | Pronto: PIX, boleto e cartão liberados nas cobranças, com repasse no seu banco. |

{% hint style="info" %}
**O link de KYC** é o passo que mais gente esquece. Estar "Em validação" **não** é o mesmo que "Ativo": é preciso gerar o link de verificação e o responsável concluir a confirmação de identidade. Só depois da aprovação a cobrança online libera.
{% endhint %}

## Recebíveis e transferências

Quando um cliente paga, o dinheiro **não cai direto** na sua conta bancária: ele fica retido no recebedor por um período (prazo de liquidação) e depois é transferido. Em **Configurações → Pagamento → Recebíveis** você acompanha o saldo e define como o dinheiro chega até você.

| Saldo | O que é |
| --- | --- |
| **Disponível** | Já pode ser sacado/transferido para a sua conta agora. |
| **Em liquidação** | Ainda no prazo de processamento, aguardando liberar (em geral até 2 dias úteis). |

- **Transferência automática** (recomendada) — o saldo disponível vai para a sua conta sozinho, na frequência que você definir.
- **Transferência manual** — com a automática desligada, o saldo acumula e você **saca o valor que quiser, quando quiser** (até o limite do disponível).

{% hint style="info" %}
**Por que o dinheiro não cai na hora:** segundo o próprio app, quando sua organização recebe um pagamento o valor fica **retido por um período que depende das configurações de transferência**. "Disponível" pode ser sacado agora; "em liquidação" ainda está no prazo do processador e não foi liberado para saque.
{% endhint %}

---

## Por porte

| Porte | Como tratar o pagamento online |
| --- | --- |
| **Autônomo / MEI** | Deixe só **PIX** (o padrão) e ligue a **transferência automática**. Você gera o link, manda no WhatsApp e o dinheiro entra sozinho. Não precisa pensar em mais nada. |
| **Médio** | Ligue **boleto** para clientes PJ que pedem, mantenha o checklist de dados em dia e acompanhe **disponível × em liquidação** para prever o caixa. |
| **Grande** | Combine os três métodos, use **transferência manual** para concentrar saques, e o **domínio personalizado** no link para reforçar a marca na hora de pagar. |

## Situações reais

- **PIX no fechamento:** orçamento ganho, você gera o link e manda o PIX por WhatsApp. O cliente paga em dois minutos; a parcela fica **Paga** na hora e a logística pode seguir. Sem cobrança manual, sem espera.
- **Boleto para empresa:** o cliente é PJ e prefere boleto. Você completa o endereço no checklist, o LocFlow salva e habilita o **boleto** no link, e envia. Quando ele paga, a baixa cai sozinha.
- **Cliente atualizou a página:** o cliente já estava com o QR Code do PIX aberto e recarregou a página. O LocFlow reaproveita a **mesma** cobrança — o código que ele tinha continua valendo, sem virar um novo.
- **Cobrança por telefone:** o cliente liga querendo pagar. Direto da parcela, o operador gera o PIX e passa o código; assim que o cliente paga, a tela do operador atualiza ao vivo.

{% hint style="success" %}
**Receba mais rápido, com menos inadimplência:** PIX e link prontos no instante do fechamento, baixa automática e confirmação em tempo real. O cliente paga onde está, e você acompanha o dinheiro entrar sem mover um dedo.
{% endhint %}

## Próximo passo

- A fatura nasce quando você **gera a cobrança** — veja [Emitindo a cobrança](emitindo-a-cobranca.md).
- Para entender parcelas, status e valores a favor do cliente, volte a [Faturas e parcelas](faturas-e-parcelas.md).
- Para registrar o que entra **por fora** do sistema, veja [Recebendo pagamentos](recebendo-pagamentos.md).
