---
icon: file-signature
description: Defina como cada arquivo é batizado ao ser gerado, compartilhado e enviado para a nuvem — dos PDFs de orçamento e contrato às fotos de prova, boletos e notas fiscais.
---

# Nomes de arquivo

Todo PDF que o LocFlow gera e todo arquivo que ele envia ao seu Google Drive tem um **nome**. Em **Nomes de arquivo** você decide, com calma, **como cada um é batizado** — por exemplo, `ORC-482 | Contrato de locação` — e esse passa a ser o padrão da organização.

{% hint style="success" %}
**Por que vale padronizar:** um nome que começa sempre pelo código do pedido faz o arquivo ser achado em segundos — no WhatsApp do cliente, na pasta do contador ou na busca do Drive. Quem recebe vê um documento organizado; quem procura acha de primeira.
{% endhint %}

## Onde fica {#onde-fica}

Em **Ajustes › Regras e modelos › Nomes de arquivo** — *"Como cada arquivo é batizado ao ser gerado"*. Também há um atalho no rodapé da lista de [Modelos de documento](../documentos/modelos-personalizados.md), para quem aprendeu o caminho antigo.

Só aparece para quem pode **editar o padrão** de pelo menos um dos arquivos.

## As duas listas {#listas}

| Lista | O que tem | Quem pode editar |
| --- | --- | --- |
| **Documentos** | Os PDFs gerados de modelo: **orçamento** (de aluguel e de venda), **contrato** e **ordem de carga** (cada um com a versão de aluguel e a de venda), **recibo de pagamento**, **fatura de locação** e **roteiro** | Quem pode editar o modelo daquele documento |
| **Arquivos enviados à nuvem** | O que vai para o Google Drive sem nascer de um modelo: **provas logísticas** (fotos e vídeos), **boletos**, **documentos fiscais** (PDF e XML), **comprovantes de lançamento**, **conferências de retorno** (fotos e vídeos) e **comprovantes de recebimento** (fotos e vídeos) | Quem administra a [Sincronização em Nuvem](sincronizacao-em-nuvem.md) |

Os modelos de **WhatsApp** ficam de fora: eles viram texto no chat, não arquivo.

## Montando um nome {#montando}

Toque no arquivo (*"Definir o padrão do nome"*) e o editor abre:

1. Monte o nome com **variáveis** — toque nelas para acrescentar (o código do orçamento, a data, o número da nota, o meio de pagamento… conforme o arquivo) — e com o texto fixo que quiser.
2. Confira a **prévia**. Ela usa **dados de exemplo**; no arquivo real, cada variável traz o valor daquele registro.
3. Toque em **Salvar como padrão**. Mudou de ideia? **Descartar** volta ao padrão salvo.

{% hint style="info" %}
**O padrão não engessa ninguém.** Quem gera um documento ainda pode ajustar o nome **daquela geração** — o editor aparece recolhido no próprio preparo do documento.
{% endhint %}

### Um campo que alguém preenche na hora {#campo-na-hora}

Além das variáveis, alguns arquivos aceitam um campo **"Campo que eu preencho na hora"** — por exemplo, o número do pedido de compra do cliente. O nome que você dá ao campo vira a pergunta feita em cada geração.

Esse campo só é oferecido onde existe um momento em que alguém está na tela para responder:

| Arquivo | Quando o campo é perguntado |
| --- | --- |
| Documentos (PDFs de modelo) | Ao gerar o documento |
| **Boletos** | Ao gerar a cobrança |
| **Documentos fiscais** | Ao emitir a nota |
| Provas, comprovantes e conferências | **Não é oferecido** — esses arquivos nascem sem ninguém digitando |

Se o padrão tem um campo sem resposta, a geração avisa antes: *"Falta preencher "X" para gerar — ou deixe em branco."* Deixou em branco? O campo **some do nome** e o arquivo sai do mesmo jeito.

{% hint style="warning" %}
**Vale para os próximos arquivos.** Mudar o padrão de um arquivo enviado à nuvem não renomeia o que já foi enviado — só os próximos envios saem com o nome novo.
{% endhint %}

## Por porte {#por-porte}

| Porte | Como costuma usar |
| --- | --- |
| **Autônomo / MEI** | Deixa o padrão do LocFlow — o código do pedido já vem no começo do nome. |
| **Médio** | Acrescenta o **nome do cliente** às notas fiscais e a data aos comprovantes, para o contador achar mais rápido. |
| **Grande** | Padroniza todos os arquivos da nuvem e usa o campo preenchido na hora para o pedido de compra de clientes corporativos. |

## Situações reais {#situacoes-reais}

* **"O contador reclama que não dá para saber de quem é cada nota."** Em **Documentos fiscais (PDF e XML)**, inclua a variável **Nome do cliente na nota** — o PDF e o XML de cada nota passam a sair identificados.
* **"O cliente pede o número do pedido de compra no nome do boleto."** Em **Boletos**, acrescente um **campo que eu preencho na hora**: ao gerar a cobrança, alguém responde e o número entra no nome.
* **"Quero achar tudo de um pedido no Drive."** Mantenha o **código do pedido** no começo de todos os nomes e pesquise por ele na busca do Google Drive.

## Próximo passo {#proximo-passo}

* [Sincronização em Nuvem](sincronizacao-em-nuvem.md) — para onde vão os arquivos e como ficam as pastas.
* [Modelos de documento](../documentos/modelos-personalizados.md) — o conteúdo de cada documento.
* [Automações](automacoes.md) — gere documentos sozinho quando algo acontece.
