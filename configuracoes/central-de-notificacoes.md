# Central de Notificações

A **Central de Notificações** avisa as pessoas certas, na hora certa, sobre o que acontece no seu negócio — de um valor a favor do cliente a uma parada pulada na rota. Você define **quais avisos** sua organização recebe, **quem** recebe cada um e **com que destaque**.

{% hint style="info" %}
As notificações são da **organização** (não de um usuário específico). Quem decide para quem cada aviso vai é o **público-alvo**. Cada pessoa vê, na própria Central, os avisos destinados a ela.
{% endhint %}

## Como cada notificação funciona

Toda notificação tem quatro partes:

| Parte | O que é |
| --- | --- |
| **Acionador** | O que dispara o aviso: um **evento** (ex.: a equipe saiu do galpão) ou uma **data** (ex.: "3 dias antes do evento"). |
| **Público-alvo** | Quem recebe. Você pode **combinar vários**: **toda a organização**, pessoas com certas **competências** (ex.: operação logística), **quem está por trás da operação** (ver abaixo) ou o **cliente** (futuro, via WhatsApp). |
| **Nível de atenção** | Quanto o aviso deve **interromper** quem recebe (ver abaixo). |
| **Ação (opcional)** | Um botão de atalho para resolver — ex.: "Abrir a fatura", "Ver no roteiro". |

### Responsável pela operação

Alguns avisos podem mirar **quem está por trás daquela operação**, sem você precisar nomear ninguém — o sistema descobre na hora:

- na **logística**, é **quem está executando a rota** (o motorista/condutor);
- em outros casos seria, por exemplo, **quem vende** o orçamento.

Isso é útil para falar direto com a pessoa certa. Nem todo aviso tem um responsável "por trás" — quando tem, a opção aparece na configuração daquele tipo.

### Níveis de atenção

O nível descreve **quanto a notícia deve interromper** quem recebe — e isso define **como** o aviso chega:

| Nível | Como aparece |
| --- | --- |
| **Crítico** | **Alerta na tela** (modal que interrompe) + som (se a pessoa ativou) + fica no sino. Exige olhar agora. |
| **Importante** | Um **aviso discreto** no topo + fica no sino. Bom ver logo, sem travar o trabalho. |
| **Informativo** | Só conta no **sino** (sem interromper). Você confere quando quiser. |

O sistema sugere um nível padrão para cada tipo, e **sua organização pode mudar** o nível de cada um.

{% hint style="warning" %}
Avisos **críticos** miram um público **estreito** (a pessoa diretamente envolvida — ex.: quem está executando a rota) para não interromper quem não tem a ver com aquilo.
{% endhint %}

## O que você pode ser avisado (catálogo)

> ✅ = já disponível · 🔜 = em breve

### Cobrança

| Notificação | Quando avisa | Público padrão | Nível | |
| --- | --- | --- | --- | --- |
| Reembolso ou crédito resolvido | Um valor a favor do cliente virou crédito/vale ou reembolso | Organização | Importante | ✅ |
| Pagamento confirmado | O cliente pagou (online) | Organização | Importante | 🔜 |
| Parcela a vencer | Faltam X dias para o vencimento | Cliente (WhatsApp) | Informativo | 🔜 |
| Parcela vencida / inadimplência | A parcela passou do vencimento | Financeiro | Importante | 🔜 |

### Logística

Os avisos de execução já permitem mirar **quem está executando a rota** (além da organização ou de competências).

| Notificação | Quando avisa | Público padrão | Nível | |
| --- | --- | --- | --- | --- |
| Saída do galpão | A equipe saiu para iniciar a rota | Organização | Informativo | ✅ |
| Chegada ao galpão | A equipe retornou ao fim do roteiro | Organização | Informativo | ✅ |
| Desvio da rota | Uma parada foi pulada durante a execução | Organização | Importante | ✅ |
| Entrega ou retirada concluída | A equipe concluiu uma parada | Organização | Informativo | ✅ |
| Roteiro em execução alterado | O orçamento de uma parada mudou com a rota **já em andamento** | Quem está executando a rota | Crítico | ✅ |
| Entrega/devolução no balcão | O cliente retirou ou devolveu presencialmente | Organização | Informativo | 🔜 |

### Orçamento

| Notificação | Quando avisa | Público padrão | Nível | |
| --- | --- | --- | --- | --- |
| Follow-up de lead | X dias antes de uma data do orçamento (lembrete de retomar o contato) | Cliente + quem vende | Importante | 🔜 |
| Orçamento prestes a expirar | Faltam X dias para a validade | Quem vende | Importante | 🔜 |
| Aguardando aprovação | Um orçamento/frete precisa de aprovação manual | Quem aprova | Importante | 🔜 |

{% hint style="info" %}
Esta lista cresce com o tempo. Os itens 🔜 dependem de recursos que estão chegando (lembretes por data, mensagens de WhatsApp). Se há um aviso que faria diferença para a sua operação, fale com o suporte.
{% endhint %}

## Configurando (Central de Notificações)

Em **Ajustes → Motores → Central de Notificações**, por tipo de aviso você pode:

1. **Ligar ou desligar** o aviso.
2. **Escolher o nível de atenção** (Crítico / Importante / Informativo).
3. **Escolher quem recebe** — e você pode **combinar mais de um**: toda a organização, por **competência** (ex.: Operar logística, Conferência, Separação) e/ou **quem está por trás da operação** (ex.: quem está executando a rota), quando o aviso permite.

{% hint style="info" %}
Para mirar por competência, atribua a competência aos colaboradores (na **função** de cada um). Aí o aviso vai só para quem a tem.
{% endhint %}

## Vendo e gerenciando os avisos

Toque no **sino** (no topo) para abrir a Central. Os avisos ficam **agrupados por módulo** (Cobrança, Logística, Orçamento), com o número de não-lidos, e **ordenados por urgência e horário** — os novos e os antigos juntos, para você ter o histórico completo.

- Cada aviso mostra o **nível** e a **hora exata** em que foi emitido.
- O **botão de ação** (ex.: "Abrir a fatura", "Ver no roteiro") fica sempre visível — em destaque quando é novo, discreto depois (para você lembrar o que precisou fazer).
- Tocar na ação **marca como visto** e abre o atalho. Quando não há ação, um **"OK, entendi"** marca como visto. **Nada some** — o histórico permanece.

## Preferências (suas, neste aparelho)

Diferente da configuração da organização, suas **preferências** valem só para você, no seu aparelho (em **Ajustes → Conta → Notificações e avisos**):

- **Som de notificação** — toca um som quando chega um aviso em tempo real.
- **Notificações pop-up** — recebe avisos mesmo com o app fechado/em segundo plano (pede sua permissão).