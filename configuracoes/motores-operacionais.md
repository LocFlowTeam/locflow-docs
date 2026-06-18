---
icon: sliders
description: Configure uma vez as regras da sua operação — orçamento, frete, cobrança e logística — e o LocFlow segue o padrão sozinho.
---

# Motores operacionais

Os **motores** são onde você define as regras da sua operação. Em vez de decidir tudo manualmente a cada locação, você configura o padrão uma vez e o LocFlow segue.

| Tipo | Como funciona |
| --- | --- |
| **Versionados** | Guardam histórico de versões — você publica uma nova versão e mantém o registro das anteriores. |
| **Operacionais** | Configuração única, editada direto na tela; vale sempre a versão atual. |

## Operação do orçamento

Define padrões da proposta: **taxa de serviço**, **validade** do orçamento e o intervalo mínimo da logística.

## Motor de frete

Define **como o frete é calculado** e a **política de aprovação**:

* **Automática** — todo frete é aprovado sozinho.
* **Por valor** — acima de um limite que você define, o frete pede aprovação manual.
* **Sempre manual** — todo frete passa por aprovação antes de seguir.

**Qual usar?** Locador que entrega ele mesmo → **Automática** (zero atrito). Operação em crescimento → **Por valor** (controla só os fretes altos). Equipe com vários vendedores → **Sempre manual** (padroniza margem e evita erro de digitação). É o mesmo cálculo de frete — muda só quanto controle você quer.

## Operação da cobrança

Define o destino **padrão** de um valor a favor do cliente — quando uma edição reduz o total abaixo do que já foi pago, ou quando entra um pagamento a mais:

* **Crédito / vale-locação** (recomendado) — vira crédito reaproveitável na próxima locação, sem operação bancária.
* **Reembolso em dinheiro** — devolve o valor ao cliente (estorno ou transferência).

O sistema aplica esse padrão automaticamente e avisa a equipe, que pode trocar a forma em cada caso.

## Motor de logística

Define quando e como a logística acontece:

* **Exigir fatura antes de iniciar a logística** — com isso ligado, a separação e a entrega só começam depois que a fatura do orçamento é gerada.
* **Folga de rota** e **janelas padrão** de entrega e retirada.

### Logística interna (galpão) — opcional

Define se existem etapas **dentro do galpão**. Vale para orçamentos futuros; os em andamento não mudam.

* **Separação interna** (*A separar → Separado*) — ligue se o material é separado no galpão antes de sair. Desligado, a logística começa direto na entrega/retirada.
* **Conferência na devolução** (*A conferir → Conferido*) — só para locação; ligue se, ao voltar, o material passa por conferência antes de finalizar.

**Locadores pequenos**, com pouca variedade de produtos, costumam deixar as duas **desligadas**: separar e conferir é controle que cabe na cabeça, e ligar só criaria cliques. Conforme a operação cresce, ligue a **Separação** primeiro (organiza o que preparar) e depois a **Conferência** (controle da volta, com papéis e evidências). Um pico de demanda não obriga a estruturar o galpão de uma vez — ligue quando justificar.

{% hint style="info" %}
**Exigir fatura antes de iniciar a logística** usa a fatura apenas como sinal de que a cobrança foi registrada — **não** significa que o cliente já pagou. Pergunte-se: você começa a preparar e entregar os itens sem ter gerado a fatura? Se **não**, mantenha ligado.
{% endhint %}

{% hint style="warning" %}
As opções visíveis dependem das **permissões** do seu usuário. Se não encontrar um motor, fale com quem administra a conta.
{% endhint %}