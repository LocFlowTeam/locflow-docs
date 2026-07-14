---
icon: file-invoice-dollar
description: >-
  Vendeu um produto? A nota é a NF-e (modelo 55), com ICMS. Diferente da locação.
  O que muda por regime e o que você precisa ter cadastrado.
---

# Nota fiscal na venda

Quando você **vende** um produto (não aluga), o documento é a **NF-e — Nota Fiscal Eletrônica de produto (modelo 55)**. Ela é bem diferente da nota de locação: aqui o item **sai em definitivo** e a operação **tem ICMS**.

{% hint style="info" %}
**Locação × venda em uma frase:** locação é serviço/uso temporário (o bem volta, sem ICMS) e vai por NFS-e; venda é saída definitiva de mercadoria e vai por NF-e, com ICMS. No LocFlow isso é decidido pela **natureza do orçamento** — ver [Locação e venda](locacao-e-venda.md).
{% endhint %}

## O que muda conforme o seu regime

A tributação do ICMS na NF-e depende do regime tributário da sua empresa:

| Regime | Como o ICMS aparece na nota |
| --- | --- |
| **Simples Nacional / MEI** | Sai com **CSOSN** (sem destaque de ICMS na nota) — você recolhe pelo DAS. A nota informa o crédito de ICMS que o seu cliente pode aproveitar. |
| **Lucro Presumido / Real** | Sai com **CST 00** e **destaque de ICMS** (alíquota conforme a operação/UF). |

O LocFlow monta isso automaticamente a partir do seu regime — você não precisa escolher CST/CSOSN à mão.

## O que você precisa ter cadastrado

* **NCM em cada produto.** A NF-e de produto **exige o NCM** (a classificação fiscal da mercadoria) de todo item vendido. Sem NCM no catálogo, a nota não sai. É o cadastro mais importante para vender com nota.
* **Inscrição Estadual** da sua empresa (a NF-e de produto exige IE, diferente da NFS-e).
* **Certificado digital A1** e o credenciamento fiscal concluído.

{% hint style="warning" %}
**Venda para outro estado, a consumidor final:** operações interestaduais a não-contribuinte podem envolver **DIFAL** (diferencial de alíquota). O LocFlow bloqueia a emissão nesses casos por segurança — trate o DIFAL com o seu contador antes de faturar.
{% endhint %}

## O que muda em 2027 (Reforma)

A venda de produto também entra na Reforma Tributária: **IBS e CBS** passam a incidir e a nota vai carregar os novos grupos de tributos. Em 2026 as alíquotas são simbólicas (fase de teste), mas o preenchimento correto já é monitorado pela Receita desde abril/2026. Estamos preparando a NF-e para esses campos.

**Por que isso importa para você:** seu cliente PJ só aproveita o crédito de IBS/CBS (e hoje o de ICMS) se você emitir a nota no padrão. Quem não emite vira o fornecedor mais caro.

{% hint style="info" %}
**Isto é orientação técnica** sobre como o sistema emite o documento, **não assessoria tributária**. As regras variam por operação, estado e produto — valide com o seu contador antes de mudar sua rotina de emissão.
{% endhint %}
