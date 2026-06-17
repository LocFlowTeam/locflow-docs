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

## Operação da cobrança

Define o destino **padrão** de um valor a favor do cliente — quando uma edição reduz o total abaixo do que já foi pago, ou quando entra um pagamento a mais:

* **Crédito / vale-locação** (recomendado) — vira crédito reaproveitável na próxima locação, sem operação bancária.
* **Reembolso em dinheiro** — devolve o valor ao cliente (estorno ou transferência).

O sistema aplica esse padrão automaticamente e avisa a equipe, que pode trocar a forma em cada caso.

## Motor de logística

Define quando e como a logística acontece:

* **Exigir fatura antes de iniciar a logística** — com isso ligado, a separação e a entrega só começam depois que a fatura do orçamento é gerada.
* **Folga de rota** e **janelas padrão** de entrega e retirada.

{% hint style="info" %}
**Exigir fatura antes de iniciar a logística** usa a fatura apenas como sinal de que a cobrança foi registrada — **não** significa que o cliente já pagou. Pergunte-se: você começa a preparar e entregar os itens sem ter gerado a fatura? Se **não**, mantenha ligado.
{% endhint %}

{% hint style="warning" %}
As opções visíveis dependem das **permissões** do seu usuário. Se não encontrar um motor, fale com quem administra a conta.
{% endhint %}