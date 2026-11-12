---
icon: file-invoice
description: Como emitir uma nota fiscal pelo LocFlow — a partir do orçamento, de um lançamento ou avulsa —, conferindo a descrição, o local do serviço, onde o ISS é pago e o transporte antes de transmitir.
---

# Emitir uma nota fiscal

A nota fiscal sai **de dentro do LocFlow**, com os dados que você já preencheu: o cliente, os itens e os valores vêm do pedido, e você só confere o que vai na nota antes de transmitir.

{% hint style="info" %}
**Antes da primeira nota**, quem administra a conta precisa configurar a emissão em **Ajustes › Integração Fiscal** — veja [Integração Fiscal](../configuracoes/integracao-fiscal.md). E, para saber qual nota cabe em cada operação, veja [Nota fiscal na locação](../conceitos/nota-fiscal-na-locacao.md) e [Nota fiscal na venda](../conceitos/nota-fiscal-na-venda.md).
{% endhint %}

## Por onde começar

| Caminho | Quando usar |
| --- | --- |
| **Central de notas › Emitir** (menu **Fiscal › Notas Fiscais**) | Qualquer nota — do orçamento, de um lançamento ou avulsa |
| **Emitir nota**, nas ações rápidas do menu | O atalho direto para a emissão |
| As **Ações rápidas** do pedido ganho › **Nota fiscal** | A nota daquele pedido. No computador, a seção mostra cada tipo de nota com o botão de emitir; no celular, a emissão fica na barra de ações da tela |

Nas Ações rápidas do pedido, a seção **Nota fiscal** também lista as **notas emitidas neste orçamento**, com o DANFE e o XML à mão, e o atalho **Central**. Se já existe uma nota ativa daquele tipo — autorizada ou em processamento —, o botão vira **Ver nota** (*"Já emitida para este orçamento."* ou *"Em processamento há 2 h · abra para consultar."*): emitir de novo só depois de um desfecho que libere, como uma recusa ou um cancelamento.

## A tela de emissão

A tela **Emitir nota fiscal** — *"Confira os dados e transmita"* — tem quatro partes.

### 1. O que emitir

**Origem** — de onde vem a nota:

| Origem | O que é | Tipos de nota possíveis |
| --- | --- | --- |
| **Orçamento** | O caminho normal: cliente, itens e valores vêm do orçamento ganho | NFS-e, NF-e de venda, Remessa e Retorno |
| **Lançamento** | Fatura uma entrada já registrada no [financeiro](../financeiro/lancamentos.md) (contas a receber) | NFS-e |
| **Avulsa** | Você informa o cliente e os itens à mão, sem orçamento | NFS-e e NF-e de venda |

**Tipo de nota**:

* **NFS-e** — a nota de serviço, a da locação em si;
* **NF-e de venda** — a nota de produto, quando você vende um item;
* **Remessa (saída)** — acompanha os bens que **saem** do galpão para o cliente; não é venda, regulariza o transporte dos seus itens;
* **Retorno (entrada)** — registra os bens **voltando** ao galpão.

Um tipo com **cadeado** ainda não está liberado: falta ativá-lo ou concluir o credenciamento — ou ele não faz parte do seu perfil de acesso.

Na nota **avulsa**, você escolhe o cliente e monta os itens: **Descrição**, **Qtd.**, **Valor unitário** e, na NF-e, o **NCM** (8 dígitos). **Adicionar item** acrescenta linhas, e o total aparece embaixo.

### 2. Dados da nota

#### Na NFS-e

* **Descrição que vai na nota** — o texto que o seu cliente vai ler. Ele já vem sugerido, e a tela diz de onde: *Do modelo de descrição da sua empresa*, *Vem da descrição do lançamento* ou *Montada a partir dos itens do orçamento*. Você pode editar — a linha passa a dizer **Editada por você**, com **Restaurar** ao lado. O modelo do texto é editado em [Modelos de documento](../documentos/modelos-personalizados.md#descricao-nfse).
* **Campos da hora** — se o modelo da sua empresa pede algo que só existe no momento (o número do **pedido de compra** do cliente, por exemplo), o campo aparece **antes** da descrição: *"Preenchido na hora — pode deixar em branco"*. Em branco, ele some do texto.
* **Local da prestação do serviço** — o município onde o serviço foi feito. Por padrão é o do **endereço de entrega** do orçamento (é onde o material chega e a estrutura é montada); a tela diz de onde veio — entrega, retirada ou endereço da empresa — e você pode trocar.
* Na **NFS-e municipal** (emitida pelo sistema da prefeitura), aparecem também o **Código do serviço (LC 116)**, a **Alíquota ISS (%)** e **Onde o ISS é pago** — veja abaixo. Na **NFS-e Nacional**, a tela pede só a descrição e o local da prestação.

{% hint style="warning" %}
**Se sobrar no texto um campo que o sistema não sabe preencher, a nota não sai.** O botão de emitir trava e a tela diz qual é o campo — melhor parar aqui do que mandar à prefeitura um texto pela metade.
{% endhint %}

#### Onde o ISS é pago (NFS-e municipal)

O local da prestação diz **onde** o serviço foi feito; **Onde o ISS é pago** diz **de qual cidade é o imposto** — e as duas coisas nem sempre coincidem. Quando o serviço foi prestado fora da cidade da sua empresa, a tela avisa — *"O serviço foi prestado em Itu, fora de Campinas, onde fica a empresa. Isso muda a conversa sobre o ISS…"* — para você conferir a escolha:

| Opção | Quando |
| --- | --- |
| **Em** *(cidade da sua empresa)* | A regra geral — o caso da maioria dos serviços. É o padrão |
| **Em** *(cidade onde o serviço foi prestado)* | Só aparece quando o serviço foi prestado em outra cidade. Alguns serviços têm o imposto no local da prestação — montagem de palco, tenda e cobertura, por exemplo. Aqui a **alíquota de ISS** daquela cidade passa a ser obrigatória, porque a prefeitura que emite a nota não calcula o imposto de outra |
| **Não se paga — isenção** | Uma lei do município dispensa o ISS deste serviço |
| **Não se paga — imunidade** | A Constituição proíbe cobrar ISS neste caso (templo, partido, entidade) |

O LocFlow **sugere** uma opção pelo código de serviço cadastrado na sua configuração fiscal e mostra o motivo — mas **a decisão é de quem emite**. Na dúvida, confirme com quem cuida da sua contabilidade: o mesmo pedido pode ter uma parte que é locação e outra que é montagem.

#### Na NF-e

* **Alíquota ICMS (%)** — no Simples Nacional o campo é ignorado (*"Simples ignora — sai com CSOSN"*); no regime normal é obrigatório (*"Obrigatória no regime normal (ex.: 18)"*). Veja [Nota fiscal na venda](../conceitos/nota-fiscal-na-venda.md).

### 3. Transporte (NF-e de um orçamento)

Na NF-e de **venda**, de **remessa** ou de **retorno** emitida a partir de um orçamento, a seção **Transporte** mostra o que vai na nota sobre a viagem da carga. Tudo vem preenchido pelo pedido — você só confere:

| Campo | De onde vem |
| --- | --- |
| **Quem transporta** | Da negociação do orçamento: *Sua equipe entrega* (na remessa, *Sua equipe leva*), *O cliente retira*, *Transportadora contratada por você*, *Transportadora contratada pelo cliente*, *Transportadora de terceiros* ou *Sem transporte*. Na nota de retorno, as opções falam da volta — *Sua equipe busca*, *O cliente devolve*. O número no selo é o código que vai na nota |
| **Veículo** | Placa e UF de quem leva a carga. Com o veículo da sua empresa, a placa é **obrigatória**: vem do roteiro em execução, quando há; sem roteiro, informe |
| **Transportadora** | Nome, CNPJ ou CPF e inscrição estadual — vem do fornecedor de frete do orçamento |
| **Saída** | Data e hora em que a carga sai. Vem do roteiro ou, sem roteiro, da janela combinada com o cliente. Vazia, a nota usa a data e a hora da emissão; nunca pode ser anterior a ela |
| **Local de entrega** (ou de retirada, no retorno) | O endereço físico para onde a carga vai — a obra, o salão do evento —, quando é diferente do cadastro do cliente. O cadastro do cliente continua como destinatário |

A tela só mostra o que a forma de transporte usa: **Sem transporte** não tem veículo nem local, e sai com a data da emissão; com **o cliente retirando**, a nota não declara local de entrega. O que você mudar ganha a marca **Editado por você**, com **Restaurar** para voltar ao sugerido.

{% hint style="info" %}
A **NF-e de venda avulsa** sai **sem transporte**. Para informar veículo, transportadora ou local de entrega, emita a partir de um orçamento.
{% endhint %}

### 4. A nota como vai sair

Antes de transmitir, a tela mostra a nota montada **exatamente como a emissão vai enviá-la** — o mesmo cálculo, sem enviar nada. Itens e valores vêm do orçamento e do catálogo (para mudar, corrija na fonte); o que é da viagem você ajusta na própria tela, e a prévia acompanha.

{% hint style="info" %}
**Na NF-e de venda, o total é o que foi cobrado.** O frete e o desconto do orçamento entram na nota — o total é produtos + frete − desconto. Serviços cobrados à parte no orçamento (montagem, por exemplo) não entram na nota de produto.
{% endhint %}

## Transmitir

Com tudo conferido, toque em **Emitir nota**. A mensagem confirma — *"Nota enviada. A autorização chega em instantes — acompanhe na Central."* — e a nota passa a ser acompanhada na [Central de notas](central-de-notas.md).

O botão muda conforme a situação da emissão — e, quando não está liberado, diz por quê:

| O botão diz | O que falta |
| --- | --- |
| **Emitir em modo teste** | Nada — a integração está em homologação: *a nota sai como teste, sem valor fiscal* |
| **Enviar certificado** | O certificado digital A1, no credenciamento |
| **Ativar** *(tipo de nota)* | Ativar aquele tipo de nota no credenciamento |
| **Concluir credenciamento** | Terminar o cadastro fiscal |
| **Emissor suspenso** | Regularizar a emissão antes de emitir |
| **Fora do seu perfil de acesso** | O seu papel não emite esse tipo de nota — peça a um administrador |

{% hint style="warning" %}
**O orçamento mudou no meio do caminho?** Na NFS-e de um orçamento, se alguém gravar o orçamento entre você abrir a emissão e transmitir, o LocFlow recusa e pede que você revise — a descrição da nota carrega valores do pedido, e nota emitida não se desfaz.
{% endhint %}

## Próximo passo

Acompanhe, reenvie, cancele e corrija as suas notas na [Central de notas](central-de-notas.md), ajuste o texto padrão da NFS-e em [Modelos de documento](../documentos/modelos-personalizados.md#descricao-nfse) e entenda a nota de cada operação em [Nota fiscal na locação](../conceitos/nota-fiscal-na-locacao.md) e [Nota fiscal na venda](../conceitos/nota-fiscal-na-venda.md).
