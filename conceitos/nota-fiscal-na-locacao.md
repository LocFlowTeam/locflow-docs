---
icon: file-invoice
description: >-
  Locação pura de bem móvel não tem ISS — e a partir de 2027 a nota muda de vez.
  O que isso significa para você, em linguagem clara, e como o LocFlow emite a
  nota: NFS-e Nacional ou Municipal.
---

# Nota fiscal na locação

Emitir nota de locação **não é** emitir nota de serviço. Essa diferença parece técnica, mas é a que mais dá dor de cabeça — e a que mais custa caro quando é feita errado. Esta página explica, sem juridiquês, o que muda para quem loca bens móveis.

{% hint style="danger" %}
**O erro mais caro:** forçar a saída de uma nota de locação com um "código de serviço qualquer" da prefeitura. A nota até sai — mas você passa a recolher **ISS que não é devido**, e recuperar esse dinheiro depois vira processo. Uma nota que "saiu" não é uma nota **correta**.
{% endhint %}

## Locação pura não sofre ISS

Locação **pura** de bem móvel (o item vai, é usado e volta, sem mão de obra embutida) **não é prestação de serviço** — logo, **não incide ISS**.

Isso não é opinião: o **STF** já pacificou o tema na **Súmula Vinculante 31**, e o item da lista de serviços que tratava de locação (o 3.01 da LC 116/2003) foi **vetado**. Não existe código de serviço municipal aplicável à locação pura.

Por isso, quando a sua nota sai como **NFS-e Nacional**, o LocFlow **não pede** um código de serviço da prefeitura. Não é limitação do sistema — é o caminho correto.

## Então qual é o documento certo?

Com a Reforma Tributária, a locação passou a ser fato gerador de **IBS** e **CBS** (os novos tributos), e o documento próprio dela é a **NFS-e Nacional** — emitida no ambiente nacional da Receita, com um código nacional específico, sem ISS.

**Mas há uma condição:** a NFS-e Nacional só funciona se a **prefeitura da sua empresa aderiu ao Emissor Nacional**. Onde o município ainda mantém emissor próprio e não aderiu, a nota continua saindo pela prefeitura. Confira a situação da sua cidade no **Mapa da NFS-e**, no portal gov.br.

| | Locação pura |
| --- | --- |
| **ISS (imposto municipal)** | Não incide |
| **IBS / CBS (novos tributos)** | Incidem |
| **Documento** | NFS-e Nacional — se o município aderiu ao Emissor Nacional |
| **Código de serviço da prefeitura** | Nenhum, na NFS-e Nacional |

## No LocFlow: NFS-e Nacional ou Municipal {#nacional-ou-municipal}

Ao configurar a emissão de notas (**Ajustes › Integrações › Integração Fiscal**), se você marcar a NFS-e, o LocFlow pergunta **"Como emitir a NFS-e?"**:

| Opção | O que a tela diz | Quando escolher |
| --- | --- | --- |
| **NFS-e Nacional** *(exige adesão do município)* | Locação de bem móvel não tem ISS — sem código de serviço municipal. Funciona se a **sua** prefeitura aderiu ao Emissor Nacional. **MEI é sempre nacional.** | Sua prefeitura aderiu ao Emissor Nacional, ou sua empresa é MEI. É a opção que já vem marcada. |
| **NFS-e Municipal** *(prefeitura · com ISS)* | Pela prefeitura, com o código da lista **LC 116** e **ISS**. | Quando o pedido tem **serviço ou mão de obra**, ou quando o seu município mantém emissor próprio e **não aderiu** ao Emissor Nacional. |

Na prática, isso muda o que o LocFlow pede na hora de emitir:

- **No modo Nacional**, a nota não pede código de serviço municipal.
- **No modo Municipal**, a nota sai com o **código de serviço** — você cadastra um código padrão uma vez, na configuração, e pode trocar numa nota específica — e com a **tributação do ISS** (onde o imposto é devido).

{% hint style="warning" %}
**Seu município ainda não aderiu?** Então a nota da locação sai como NFS-e Municipal, que pede um código de serviço. Não escolha um código "qualquer": converse com o seu contador sobre qual código usar e como tratar o ISS no seu caso.
{% endhint %}

Os detalhes da configuração — o modo da NFS-e, o código de serviço padrão, o certificado, o teste e a produção — estão em [Integração Fiscal](../configuracoes/integracao-fiscal.md#nfse-nacional-ou-municipal).

## E quando tem mão de obra junto?

Se o mesmo pedido tem **locação + mão de obra** (operação do item, montagem, serviço técnico), aí sim a **parte do serviço tem ISS** — e ela precisa do código municipal correto.

O caminho certo é **separar as duas coisas**, com valores individualizados:

* **Locação do bem** → segue a trilha da locação pura (sem ISS).
* **Mão de obra / serviço** → NFS-e municipal, com ISS.

{% hint style="warning" %}
O código de serviço da parte de mão de obra depende da natureza concreta do trabalho e varia por município — **quem define é o seu contador**. O LocFlow não escolhe esse código por você.
{% endhint %}

## E o transporte dos itens? {#nf-e-de-remessa}

A nota de locação não é a única que pode acompanhar um pedido. Quando os itens **saem** para o cliente e **voltam**, a **NF-e de remessa** acompanha o transporte: ela **não gera imposto de venda** — é o documento que regulariza a circulação dos seus bens. O **MDF-e** (o manifesto que agrupa as notas de um roteiro) ainda aparece como **Em breve**.

{% hint style="info" %}
**Para quem quer os detalhes.** A NFS-e e a NF-e de remessa estão em todos os planos; a NF-e de venda é do plano Pro (veja [Nota fiscal na venda](nota-fiscal-na-venda.md)). Cada nota emitida **em produção** consome **25 créditos**; as notas de teste, em homologação, não consomem nada. Veja [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md#o-que-consome).
{% endhint %}

## O que muda em 2027 (comece a olhar agora)

2026 é um ano de **teste**, com alíquotas simbólicas (**CBS 0,9% + IBS 0,1%**) e **sem recolhimento**. É a janela para acertar tudo sem custo. A virada de verdade é em **2027** — e três coisas mudam para você:

1. **A nota passa a ser obrigatória.** Hoje a locação pura é documentada por recibo ou fatura. A partir de 2027, o documento passa a ser a NFS-e Nacional.
2. **O valor total da nota muda.** IBS e CBS passam a ser destacados "por fora". Se você tem contratos longos com valor fechado, converse com seu jurídico sobre **cláusula de repasse tributário** antes da virada.
3. **Seu cliente PJ vai querer a nota.** Sem o documento no padrão nacional, ele não toma crédito de IBS/CBS — e quem não emitir vira o fornecedor mais caro da praça.

| Período | O que acontece |
| --- | --- |
| **2026** | Fase de teste (CBS 0,9% + IBS 0,1%), sem recolhimento |
| **2027** | Começa a cobrança da CBS; PIS e Cofins são extintos |
| **2027 → 2032** | Transição: ISS e ICMS caem, IBS sobe |
| **2033** | Fim da transição: IBS e CBS 100% vigentes |

{% hint style="info" %}
**Isto é orientação técnica** sobre como o sistema emite o documento, **não assessoria tributária**. As regras variam por município e a Reforma está mudando mês a mês — valide com o seu contador antes de mudar sua rotina de emissão.
{% endhint %}
