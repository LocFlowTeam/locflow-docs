---
icon: receipt
description: A Central de notas — todas as notas fiscais num lugar só, como acompanhar a autorização, consultar a prefeitura ou a SEFAZ na hora, reenviar uma nota recusada, cancelar, corrigir e baixar o PDF e o XML.
---

# Central de notas

Toda nota fiscal que o LocFlow emite — a NFS-e da locação, a NF-e da venda, a NF-e de remessa que acompanha os seus [bens móveis](../primeiros-passos/glossario.md) — fica num lugar só: a **Central de notas**, no menu **Fiscal › Notas Fiscais**.

É aqui que você **emite**, **acompanha** até a autorização, **reenvia** o que foi recusado, **cancela**, **corrige** e **baixa** o PDF e o XML.

{% hint style="info" %}
**Antes da primeira nota**, a emissão precisa estar configurada — empresa, certificado digital e os tipos de nota que você vai usar. Isso é feito por quem administra a conta, em **Ajustes › Integração Fiscal**. Veja [Integração Fiscal](../configuracoes/integracao-fiscal.md). Para entender qual nota cabe em cada operação, veja [Nota fiscal na locação](../conceitos/nota-fiscal-na-locacao.md) e [Nota fiscal na venda](../conceitos/nota-fiscal-na-venda.md).
{% endhint %}

## Quem vê e quem emite

* A Central aparece para quem tem permissão de **ver notas fiscais**. O papel **Operador / Atendente** já nasce vendo, emitindo e cancelando **NFS-e** e **NF-e de remessa**.
* A **NF-e de venda** é recurso de plano superior e uma permissão à parte, concedida pelo dono ou pelo administrador.
* **Cada ação cobra a permissão do tipo da nota.** Quem cuida de NFS-e e remessa não vê a NF-e de venda na lista, não abre a ficha dela e não a cancela. A tela só oferece emitir, consultar, reenviar e cancelar o que o seu papel permite.

Veja [Papéis, funções e competências](../conceitos/papeis-funcoes-competencias.md) e [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md).

## A lista de notas

A Central abre em **Todas as notas fiscais**, com:

* **Emitir**, no topo — abre a [emissão](emitir-nota.md). Sem nenhuma nota ainda, a lista vazia oferece **Emitir primeira nota**.
* **Busca** por código do orçamento ou nome do cliente.
* **Filtros**:

| Filtro | Opções |
| --- | --- |
| **Tipo de nota** | NFS-e, NF-e produto, NF-e remessa |
| **Status** | Autorizadas, Processando, Rejeitadas, Canceladas |
| **Módulo de origem** | Orçamento, Roteiro, Movimento, Avulsa |

* **Agrupar** — junta as notas pelo orçamento de onde vieram (as que não vêm de um orçamento ficam agrupadas pela origem).

Cada nota mostra o tipo e o número, o cliente, o orçamento de origem, o valor e a data. Toque para abrir a ficha.

## A ficha da nota

A ficha mostra a **linha do tempo** da nota (*Solicitada → Processada → Autorizada*, ou o desfecho: *Rejeitada*, *Cancelada*), o cliente, os itens e o total e, quando existem:

* **Texto que foi na nota** — a descrição exatamente como foi transmitida, e de onde ela veio (do modelo da empresa, editada na hora ou montada a partir dos itens);
* a **chave de acesso**;
* as **cartas de correção** da nota;
* o orçamento de origem (*"Gerada do orçamento ORC-1234"*).

Embaixo, as ações — que mudam conforme a situação da nota.

### Nota autorizada: baixar, cancelar, corrigir

* **DANFE** e **XML** — baixam o PDF e o XML da nota. O download entra na fila de transferências do app, mostrando quanto falta; e, se a [Sincronização em Nuvem](../configuracoes/sincronizacao-em-nuvem.md) estiver ligada, os arquivos também vão para o seu Drive, com o nome definido em [Nomes de arquivo](../configuracoes/nomes-de-arquivo.md).
* **Cancelar** — pede o **motivo do cancelamento** (de 15 a 255 caracteres: a SEFAZ exige uma justificativa) e **Confirmar cancelamento**. Algumas prefeituras não aceitam cancelar a NFS-e pelo sistema: nesse caso o botão não aparece, e a ficha diz o motivo.
* **Corrigir com carta de correção** — só na NF-e. Veja [Carta de correção](#carta-de-correcao).

### Nota em processamento: consultar agora

Depois de enviada, a nota espera a resposta da prefeitura (NFS-e) ou da SEFAZ (NF-e). A ficha diz há quanto tempo — *"Aguardando a prefeitura/SEFAZ há 2 h."* — e quando será a próxima consulta: *"Próxima consulta automática em 6 h · última há 10 min. Prefeituras podem levar horas; você pode consultar agora."*

O LocFlow consulta sozinho, com intervalo crescente — a cada **10 minutos** na primeira hora, de **hora em hora** no primeiro dia, a cada **6 horas** na primeira semana e, daí em diante, **uma vez por dia** —, até a nota ter uma resposta. Não precisa ficar olhando.

Se quiser saber agora, toque em **Consultar agora**:

| A resposta | O que significa |
| --- | --- |
| **Nota autorizada** | Pronto: a nota vale |
| **Nota rejeitada — veja o motivo** | O motivo aparece na ficha — veja abaixo |
| **Ainda em processamento no provedor** | O autorizador ainda não respondeu. A consulta automática continua |
| **Consultado há pouco** | Aguarde alguns segundos para consultar de novo |

{% hint style="info" %}
**Você não precisa ficar vigiando.** Quando uma nota é recusada — ou passa de **30 dias** sem resposta —, chega um aviso na [Central de Notificações](../configuracoes/central-de-notificacoes.md) — e tocar nele abre direto a ficha da nota.
{% endhint %}

### Nota rejeitada: reenviar

O motivo da recusa aparece na ficha, por escrito. O que fazer depende do caso:

| Caso | O botão | O que fazer |
| --- | --- | --- |
| **Tempo excedido** — o provedor desistiu de esperar a resposta | **Reenviar** e **Configuração** | A nota **não foi confirmada como autorizada**. Antes de reenviar, confira no portal da prefeitura (na NF-e, no portal da NF-e) se ela saiu por lá — para não emitir em duplicidade. Se não saiu, revise as pendências da configuração fiscal (o item da lista de serviços, o código tributário do município, o endereço do cliente) e reenvie: a mesma nota é aceita de novo |
| **Outra recusa** | **Corrigir e reenviar** | Abre a emissão com os dados da nota, para você corrigir o que o motivo aponta e transmitir de novo |
| **NFS-e Nacional num município que não aderiu** | **Ajustar modo de NFS-e** | Reenviar daria a mesma recusa: o caminho é mudar o modo da NFS-e na Integração Fiscal (coisa de quem administra) |

{% hint style="info" %}
**Quando a prefeitura não responde.** Uma NFS-e municipal pode ficar em processamento enquanto a prefeitura não dá retorno — o provedor encerra a espera em até **7 dias**. Quando isso acontece — ou quando o provedor devolve um erro —, a nota vira **Rejeitada** na hora, já com a orientação do que fazer.
{% endhint %}

## Carta de correção {#carta-de-correcao}

Errou um dado numa **NF-e já autorizada**? Nem sempre é preciso cancelar. A **carta de correção** corrige um dado da nota sem emitir outra — ela vai para a SEFAZ e fica vinculada à nota.

1. Na ficha da NF-e autorizada, toque em **Corrigir com carta de correção** (depois da primeira, **Nova carta**).
2. Em **O que corrigir**, escreva a correção — por exemplo, *"Onde se lê frete por conta do destinatário, leia frete próprio do remetente."* O contador ao lado mostra quantos caracteres faltam ou sobram (de 15 a 1.000).
3. Toque em **Enviar carta**.

As cartas aparecem na ficha, numeradas, com o texto, a data e o PDF e o XML de cada uma.

{% hint style="warning" %}
**Só a última carta vale.** Cada carta **substitui** a anterior — se você já corrigiu algo antes, repita na nova carta tudo o que ainda precisa valer. São até **20 cartas por nota**. E a carta não corrige tudo: valores, impostos, quem emite ou quem recebe e as datas ficam de fora — nesses casos, cancele a nota em até 24 h e emita outra. O que a carta corrige e o que não corrige está em [Nota fiscal na venda](../conceitos/nota-fiscal-na-venda.md#carta-de-correcao).
{% endhint %}

{% hint style="danger" %}
**Se a tela disser que não deu para confirmar o envio, não mande outra carta às cegas.** Quando a resposta da SEFAZ se perde no caminho, a ficha avisa: *confira as cartas desta nota antes de enviar de novo*. Uma segunda carta substituiria a primeira e gastaria mais uma das 20.
{% endhint %}

A carta pode ser enviada por quem tem a permissão de **cancelar** aquele tipo de nota — as duas são ações sobre uma nota já autorizada.

## A nota no resto do LocFlow

* **No orçamento** — as [Ações rápidas](../orcamentos/acompanhando-e-fechando.md) do pedido ganho têm o grupo **Nota fiscal**, com as notas emitidas para aquele pedido (DANFE e XML à mão) e o atalho **Central**. Veja [Emitir uma nota fiscal](emitir-nota.md).
* **No financeiro** — uma nota **avulsa** autorizada cria uma **entrada prevista** no seu razão, com a origem *Documento fiscal*: o faturado que ainda vai entrar. A nota de um pedido não cria nada novo, porque aquela receita já entra pela cobrança. Veja [Lançamentos](../financeiro/lancamentos.md#o-que-o-locflow-lanca-sozinho).
* **Notas de teste** (emitidas enquanto a integração está em homologação) não têm valor fiscal e não entram no financeiro.

## Próximo passo

Emita a sua próxima nota em [Emitir uma nota fiscal](emitir-nota.md), configure a emissão em [Integração Fiscal](../configuracoes/integracao-fiscal.md) e escreva o texto padrão da NFS-e em [Modelos de documento](../documentos/modelos-personalizados.md#descricao-nfse).
