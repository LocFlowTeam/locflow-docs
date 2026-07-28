---
icon: user-gear
description: Papéis, funções e competências — como o LocFlow controla quem vê e faz o quê, do dono que faz tudo à equipe com acesso sob medida.
---

# Papéis, funções e competências

Conforme a equipe cresce, a pergunta deixa de ser "como faço?" e vira "**quem pode fazer?**". O LocFlow separa isso em três ideias simples — e você usa só o que precisar.

{% hint style="success" %}
**Valor:** cada pessoa enxerga só o que usa. O motorista abre o app e vê **a rota dele** — não o financeiro nem o catálogo. Menos confusão, menos erro, e você delega sem medo.
{% endhint %}

## Os três conceitos

```mermaid
flowchart LR
    P[Papel<br/>o que a pessoa VÊ e FAZ] --- F[Função<br/>o cargo na operação]
    F --- C[Competência<br/>a habilidade]
```

| Conceito | Responde | Exemplo |
| --- | --- | --- |
| **Papel** | O que a pessoa **acessa** no sistema (permissões) | *Motorista* só vê roteiros atribuídos a ele |
| **Função** | O **cargo** dela na operação | *Vendedor*, *Motorista*, *Atendente* |
| **Competência** | A **habilidade** que a função carrega | *Dirigir veículos*, *Vender orçamentos*, *Separação* |

A competência é o que liga a pessoa às tarefas: um canal de notificação "por competência" entrega só para quem tem aquela habilidade (ex.: avisos de follow-up vão para quem tem **Vender orçamentos**).

## Papéis prontos (você não monta do zero)

O LocFlow já vem com papéis de cada cargo — é só escolher ao convidar alguém:

| Papel | Para quem | Enxerga |
| --- | --- | --- |
| **Administrador** | O sócio ou braço direito | Praticamente tudo — só o que **encerra a conta** (apagar a organização, mexer no contrato de assinatura) fica exclusivo do dono |
| **Operador / Atendente** | Gestão e dia a dia | Orçamentos, frota, roteiros, equipe |
| **Motorista** | Quem roda a rota | Só os roteiros atribuídos a ele |
| **Separador** | Galpão (ida) | A fila *A separar → Separado* |
| **Conferente** | Galpão (volta) | A fila *A conferir → Conferido* |
| **Operador de Balcão** | Loja física (as duas pontas) | O [balcão](../logistica/balcao.md) — entrega **e** recebe do cliente, e pode registrar **em lote** |

{% hint style="info" %}
O **dono** entra como **Superadmin** (acesso total) — por isso, quem está sozinho nem percebe que papéis existem. Eles só aparecem quando você convida a primeira pessoa.
{% endhint %}

### E o parceiro? {#papel-de-parceiro}

O **Parceiro Externo** também é um papel — mas ele **não aparece nesta lista**, e isso é de propósito: parceiro não é colaborador, e o caminho para criá-lo é outro (**Rede de Parceiros → convidar parceiro**, não **Colaboradores**). O papel é **fixo**: você não o escolhe, não o marca junto com outro e não o edita.

O que ele faz é bem mais do que "ver roteiros": ele é o **gestor da logística dos pedidos que você repassou a ele**, dentro da sua conta e só ali.

| Ele pode | Ele não pode |
| --- | --- |
| Criar, editar e executar os **próprios roteiros** (só os dele) | Ver os roteiros da sua equipe, nem atribuir roteiro a alguém |
| Registrar execução **em lote** (o pedido é dele) | **Otimizar rota** pelo mapa — ele roteiriza sem gastar o seu crédito |
| Cadastrar e editar a **própria frota** (especificações e veículos) | Ver ou usar a sua frota |
| Confirmar o **balcão** do que foi repassado a ele | Confirmar balcão em lote (isso é da sua retaguarda) |
| Configurar o **próprio recebedor** bancário, para receber o repasse | Ver os seus outros clientes, orçamentos ou colaboradores |
| Aceitar, recusar ou renegociar acordos e repasses **dele** | **Dispensar evidência** — ele está em campo para produzir a prova |
| Registrar que recebeu do cliente na porta, **se o acordo permitir** | Ver o seu link de pagamento ou a sua carteira |

→ Entenda o papel por inteiro em [Parceiro Logístico Externo](../parcerias/parceiro-logistico-externo.md) e o convite em [Entrando na rede](../parcerias/entrando-na-rede.md).

## Como isso escala (a filosofia na prática)

| Porte | Como você usa |
| --- | --- |
| **Começando** | Só o dono, acesso total. Nada a configurar. |
| **Crescendo** | Convida a equipe com os **papéis prontos** — um clique por pessoa. |
| **Estruturada** | **Personaliza** papéis e funções, permissão a permissão, por cargo. |

## Próximo passo

* Para convidar e dar acesso, veja [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md).
* Para trabalhar com gente de fora, veja [Rede de Parceiros: a visão](../parcerias/visao-geral.md).
* Em dúvida com um termo? Consulte o [Glossário](../primeiros-passos/glossario.md).
