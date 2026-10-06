---
icon: file-invoice-dollar
description: >-
  Vendeu um produto? A nota é a NF-e (modelo 55), com ICMS. Diferente da locação.
  O que muda por regime, o que você precisa ter cadastrado e como corrigir uma
  nota já autorizada.
---

# Nota fiscal na venda

Quando você **vende** um produto (não aluga), o documento é a **NF-e — Nota Fiscal Eletrônica de produto (modelo 55)**. Ela é bem diferente da nota de locação: aqui o item **sai em definitivo** e a operação **tem ICMS**.

{% hint style="info" %}
**Locação × venda em uma frase:** locação é serviço/uso temporário (o bem volta, sem ICMS) e vai por NFS-e; venda é saída definitiva de mercadoria e vai por NF-e, com ICMS. No LocFlow isso é decidido pelo **tipo de negócio do orçamento** (Aluguel ou Venda) — ver [Locação e venda](locacao-e-venda.md).
{% endhint %}

{% hint style="info" %}
**A NF-e de venda é recurso do plano Pro**, como a própria venda. A NFS-e e a NF-e de remessa estão em todos os planos. E, dentro da equipe, emitir NF-e de venda é uma permissão à parte: o papel Operador / Atendente não nasce com ela — quem concede é o dono ou o administrador (veja [Papéis, funções e competências](papeis-funcoes-competencias.md)).
{% endhint %}

## O que muda conforme o seu regime

A tributação do ICMS na NF-e depende do regime tributário da sua empresa:

| Regime | Como o ICMS aparece na nota |
| --- | --- |
| **Simples Nacional / MEI** | Sai com **CSOSN** (sem destaque de ICMS na nota) — você recolhe pelo DAS. A nota informa o crédito de ICMS que o seu cliente pode aproveitar. |
| **Lucro Presumido / Real** | Sai com **CST 00** e **destaque de ICMS** (alíquota conforme a operação/UF). |

O LocFlow monta o código (CST ou CSOSN) a partir do seu regime — você não escolhe à mão. O que você informa, na hora de emitir, é a **Alíquota ICMS (%)**, e ela segue o regime:

| Regime | O campo Alíquota ICMS (%) |
| --- | --- |
| **Simples Nacional / MEI** | Opcional e ignorado — o próprio campo avisa: *"Simples ignora — sai com CSOSN"*. |
| **Lucro Presumido / Real** | **Obrigatório** — *"Obrigatória no regime normal (ex.: 18)"*. Sem ele, a nota não segue. |

## O que você precisa ter cadastrado

* **NCM em cada produto.** A NF-e de produto **exige o NCM** (a classificação fiscal da mercadoria, com 8 dígitos) de todo item vendido. Sem NCM no catálogo, a nota não sai. É o cadastro mais importante para vender com nota — veja [Catálogo: produtos](../cadastros/catalogo-produtos.md#fiscal).
* **Inscrição Estadual** da sua empresa (a NF-e de produto exige IE, diferente da NFS-e).
* **Certificado digital A1** e o credenciamento fiscal concluído — veja [Integração Fiscal](../configuracoes/integracao-fiscal.md).

{% hint style="warning" %}
**Venda para outro estado, a consumidor final:** operações interestaduais a não-contribuinte podem envolver **DIFAL** (diferencial de alíquota). O LocFlow bloqueia a emissão nesses casos por segurança — trate o DIFAL com o seu contador antes de faturar.
{% endhint %}

## Com ou sem transporte

Quando você emite a NF-e de venda **a partir de um orçamento**, a nota ganha a seção **Transporte** — quem transporta, o veículo e a saída — e o **local de entrega**, já sugeridos a partir do pedido; o que você ajustar ali é o que sai na nota.

Uma **nota avulsa** (emitida sem orçamento) sai **sem transporte**, e a tela avisa: *"A nota sai sem transporte — para veículo, transportadora ou local de entrega, emita a partir de um orçamento."*

## Corrigir uma nota já autorizada: a carta de correção {#carta-de-correcao}

Errou um dado numa NF-e que a SEFAZ já autorizou? Nem sempre é preciso cancelar. Na ficha da nota, **Corrigir com carta de correção** envia à SEFAZ uma **carta de correção (CC-e)**, que fica vinculada à nota.

| A carta corrige, por exemplo | A carta **não** corrige |
| --- | --- |
| Quem transporta, a transportadora, a placa e a UF do veículo | Valores, preço, quantidade, base de cálculo, alíquota ou imposto |
| Endereço ou local de entrega | Quem emite ou quem recebe a nota (CNPJ/CPF, razão social, troca de cliente) |
| A descrição de um item | A data de emissão ou a data de saída |
| As informações adicionais da nota | |

Nos casos que a carta não corrige, o caminho é **cancelar a nota em até 24 h e emitir outra**.

* O texto da correção tem de **15 a 1.000 caracteres**.
* São **até 20 cartas por nota** — e **só a última vale**: cada carta substitui a anterior. Se você já corrigiu algo antes, repita na nova carta tudo o que ainda precisa valer.
* A carta **não consome créditos**.

## O que muda em 2027 (Reforma)

A venda de produto também entra na Reforma Tributária: **IBS e CBS** passam a incidir e a nota vai carregar os novos grupos de tributos. Em 2026 as alíquotas são simbólicas (fase de teste), mas o preenchimento correto já é monitorado pela Receita desde abril/2026. Estamos preparando a NF-e para esses campos.

**Por que isso importa para você:** seu cliente PJ só aproveita o crédito de IBS/CBS (e hoje o de ICMS) se você emitir a nota no padrão. Quem não emite vira o fornecedor mais caro.

{% hint style="info" %}
**Isto é orientação técnica** sobre como o sistema emite o documento, **não assessoria tributária**. As regras variam por operação, estado e produto — valide com o seu contador antes de mudar sua rotina de emissão.
{% endhint %}
