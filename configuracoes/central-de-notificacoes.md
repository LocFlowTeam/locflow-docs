---
icon: bell
description: Avise as pessoas certas, na hora certa — defina o que dispara cada aviso, quem recebe (canais) e com que destaque (nível de atenção).
---

# Central de Notificações

A **Central de Notificações** avisa as pessoas certas, na hora certa, sobre o que acontece no seu negócio — de um valor a favor do cliente a uma parada pulada na rota. Você define **quais avisos** sua organização recebe, **quem** recebe cada um e **com que destaque**.

{% hint style="info" %}
As notificações são da **organização** (não de um usuário específico). Quem decide para quem cada aviso vai é o **canal** (quem recebe + como — ver "Canais de notificação"). Cada pessoa vê, na própria Central, os avisos destinados a ela.
{% endhint %}

## Como cada notificação funciona

Toda notificação tem quatro partes:

| Parte | O que é |
| --- | --- |
| **Acionador** | O que dispara o aviso: um **evento** (ex.: a equipe saiu do galpão) ou uma **data** (ex.: "3 dias antes do evento"). |
| **Canal** | Para onde o aviso vai. Cada tipo aponta para um **canal**, que define **quem recebe** e **como** o aviso é distribuído (ver "Canais de notificação"). |
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

## Canais de notificação

Um **canal** é a camada que decide **quem recebe** e **como**. Em vez de configurar o destinatário em cada aviso, você configura **canais** e os **reaproveita** entre vários tipos de aviso.

Cada canal tem:

| Parte | O que é |
| --- | --- |
| **Pool (quem)** | De onde saem os destinatários: **toda a organização**, pessoas com certas **competências** (ex.: Vender orçamentos, Operação logística), o **responsável pela operação** (descoberto na hora — ex.: quem está executando a rota) ou o **cliente** (futuro, via WhatsApp). Dá para combinar. |
| **Roteamento (como)** | Como a pool vira destinatário(s): ver abaixo. |

### Roteamento: todos ou rodízio

| Roteamento | O que faz |
| --- | --- |
| **Todos** (broadcast) | Todo mundo da pool recebe. |
| **Rodízio** (round-robin) | Distribui **1-a-1**, em revezamento: cada novo aviso vai para a **próxima pessoa** da pool. |

**Exemplo (rodízio):** Pedro e João são vendedores. Chegam 10 orçamentos novos por dia. Com um canal de **rodízio** sobre a competência "Vender orçamentos", os avisos de follow-up são distribuídos igualmente — o 1º vai para o Pedro, o 2º para o João, o 3º para o Pedro… A mesma ideia serve para separadores/conferentes dividindo ordens.

{% hint style="info" %}
A distribuição do rodízio é **justa mesmo com reprocessamentos**: um mesmo evento nunca "pula" alguém da fila.
{% endhint %}

### Canais padrão

Toda organização já vem com canais prontos — por exemplo **"Toda a organização"**, **"Responsável pela operação"** (ex.: quem está executando a rota) e **"Vendedores (rodízio)"**. Você pode editar a pool e o roteamento deles, criar canais novos, e escolher qual canal cada aviso usa. Os canais são geridos em **Ajustes → Motores → Central de Notificações → Gerenciar canais**.

## O que você pode ser avisado (catálogo)

> A coluna **Status** mostra o que já está disponível e o que está **em breve**.

### Cobrança

| Notificação | Quando avisa | Canal padrão | Nível | Status |
| --- | --- | --- | --- | --- |
| Reembolso ou crédito resolvido | Um valor a favor do cliente virou crédito/vale ou reembolso | Organização | Importante | Disponível |
| Pagamento confirmado | O cliente pagou (online) | Organização | Importante | Em breve |
| Parcela a vencer | Faltam X dias para o vencimento | Cliente (WhatsApp) | Informativo | Em breve |
| Parcela vencida / inadimplência | A parcela passou do vencimento | Financeiro | Importante | Em breve |

### Logística

Os avisos de execução já permitem mirar **quem está executando a rota** (além da organização ou de competências).

| Notificação | Quando avisa | Canal padrão | Nível | Status |
| --- | --- | --- | --- | --- |
| Saída do galpão | A equipe saiu para iniciar a rota | Organização | Informativo | Disponível |
| Chegada ao galpão | A equipe retornou ao fim do roteiro | Organização | Informativo | Disponível |
| Desvio da rota | Uma parada foi pulada durante a execução | Organização | Importante | Disponível |
| Entrega ou retirada concluída | A equipe concluiu uma parada | Organização | Informativo | Disponível |
| Roteiro em execução alterado | O orçamento de uma parada mudou com a rota **já em andamento** | Quem está executando a rota | Crítico | Disponível |
| Entrega/devolução no balcão | O cliente retirou ou devolveu presencialmente | Organização | Informativo | Em breve |

### Orçamento

| Notificação | Quando avisa | Canal padrão | Nível | Status |
| --- | --- | --- | --- | --- |
| Novo orçamento para follow-up | Quando um orçamento é criado | Vendedores (rodízio) | Importante | Disponível |
| Follow-up de lead | X dias antes de uma data do orçamento (lembrete de retomar o contato) | Cliente + quem vende | Importante | Em breve |
| Orçamento prestes a expirar | Faltam X dias para a validade | Quem vende | Importante | Em breve |
| Aguardando aprovação | Um orçamento/frete precisa de aprovação manual | Quem aprova | Importante | Em breve |

{% hint style="info" %}
Esta lista cresce com o tempo. Os itens marcados como **Em breve** dependem de recursos que estão chegando (lembretes por data, mensagens de WhatsApp). Se há um aviso que faria diferença para a sua operação, fale com o suporte.
{% endhint %}

## Configurando (Central de Notificações)

Você chega à configuração por **Ajustes → Central de Notificações** (atalho direto) ou por **Ajustes → Motores → Central de Notificações**. Os avisos ficam **agrupados por módulo** (Cobrança, Logística, Orçamento), com busca; escolha um aviso para configurá-lo. Por tipo de aviso você pode:

1. **Ligar ou desligar** o aviso.
2. **Escolher o nível de atenção** (Crítico / Importante / Informativo).
3. **Escolher o canal** (quem recebe e como). Use **Gerenciar canais** para editar a pool e o roteamento, ou criar canais novos — e reaproveite o mesmo canal em vários avisos.

{% hint style="info" %}
Para um canal por **competência**, atribua a competência aos colaboradores (na **função** de cada um). Aí o canal entrega só para quem a tem — e, no modo **rodízio**, reveza entre eles.
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