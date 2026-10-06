---
icon: robot
description: Quando acontecer algo no seu fluxo, o LocFlow faz o resto. Configure "quando X, faça Y" e pare de lembrar de gerar o mesmo documento toda vez.
---

# Automações

A seção **Automações** responde a uma pergunta simples: *o que você faz toda vez, sem exceção, e não deveria precisar lembrar?*

Ganhou o orçamento → gera o contrato. Emitiu a cobrança → gera a fatura de locação. São passos que você já dá; a automação apenas deixa de exigir que você os dê.

Toda automação tem sempre duas partes — **quando** algo acontece, **faça** alguma coisa:

> Quando o cliente fechar → gerar Contrato de locação · só aluguel

{% hint style="info" %}
A tela fica em **Ajustes › Automações**. Ela está disponível a partir do plano **Starter** e depende de duas **permissões** distintas, que o **Administrador** já tem: **ver** as automações e **gerenciá-las**. Quem só vê enxerga a lista, mas não encontra os botões de criar, ligar e ajustar.
{% endhint %}

## Criando a primeira

Se você ainda não tem nenhuma automação, a tela não abre com um formulário em branco — ela oferece **duas receitas prontas**:

- **Ganhei o orçamento → gerar o Contrato**
- **Gerei uma cobrança → gerar a Fatura de locação**

Toque em **Usar** e a folha abre com o essencial já escolhido; você só confere e ativa. Se quiser outra combinação, **Montar do zero** abre a mesma folha em branco. Abrir uma automação nova **sempre começa do zero** — a folha não traz o rascunho da vez anterior.

### As três perguntas

A folha faz três perguntas, nesta ordem:

| Passo | O que você escolhe |
| --- | --- |
| **1. Quando…** | O fato que dispara a automação. |
| **2. Faça…** | O que o LocFlow faz quando aquilo acontece. |
| **3. Detalhes** | **Qual documento**, **como gerar** e, no fato "quando o cliente fechar", **só para** quais pedidos (aluguel e/ou venda). |

A ordem não é enfeite: escolher o fato primeiro é o que permite ao passo 2 oferecer **só o que faz sentido naquele fato**. Combinação impossível nunca aparece na lista.

<a id="como-gerar"></a>

#### Como gerar

Escolhido o documento, aparece **Como gerar** — o mesmo painel das **Ações rápidas** do orçamento, com as opções daquele documento:

* a **lista de itens** agrupada (kits juntos) ou normal;
* **com ou sem fotos** dos itens, quando o modelo tem coluna de foto;
* no **contrato**, **com ou sem o orçamento anexado**.

O painel já começa **do jeito que você costuma gerar aquele documento** à mão. O que ficar escolhido ali vale para **toda** geração automática daquela regra. A folha também diz para onde o arquivo vai: *"O arquivo é gerado na sua conta, em Documentos do pedido"* — e, com a [Sincronização em Nuvem](sincronizacao-em-nuvem.md) conectada, ele também é enviado ao seu Google Drive assim que fica pronto.

No fim, um botão explícito: **Ativar automação**. Nada é salvo pela metade — uma automação meio configurada dispararia com metade das escolhas, e isso não pode acontecer com contrato e cobrança.

{% hint style="warning" %}
**Não dá para criar a mesma automação duas vezes** — seriam dois documentos idênticos a cada disparo. Se você já tem uma igual, a folha avisa: se ela está **ativa**, use **Ajustar como gerar** na lista para mudar a forma de gerar; se está **pausada**, ligue-a de volta em vez de criar outra.
{% endhint %}

## Quando (os fatos disponíveis)

| Fato | O que significa | Recorte disponível |
| --- | --- | --- |
| **Quando o cliente fechar** | No instante em que o orçamento passa a ganho. | Aluguel, venda, ou os dois |
| **Quando eu gerar uma cobrança** | Quando uma fatura é emitida para o pedido. | — |
| **Quando o cliente pagar tudo** | Quando a última parcela é baixada. | — |

{% hint style="warning" %}
**"Quando o cliente pagar tudo" nem sempre tem um pedido por trás.** Uma cobrança avulsa ou de avaria não nasce de um orçamento — e um documento do pedido não pode ser gerado sem pedido. Nesses casos a automação simplesmente **não faz nada**, e isso **não conta como erro**: ela continua ligada e valendo para as próximas.

A folha avisa disso **antes** de você ativar, e a regra na lista mostra o rodapé *"não vale para cobrança avulsa"*.
{% endhint %}

## Faça (o que a automação pode fazer)

Hoje há uma ação: **Gerar documento**. Você escolhe qual:

| Documento | Quando costuma ser usado |
| --- | --- |
| **Contrato de locação** | O documento que o cliente assina. |
| **Orçamento em PDF** | A proposta para mandar ao cliente. |
| **Fatura de locação** | O documento de cobrança. |
| **Ordem de carga** | O que a equipe leva para separar o material. |
| **Recibo de pagamento** | A prova de que o cliente pagou. |

Outras ações — **abrir uma tarefa**, **mandar mensagem no WhatsApp** — aparecem na lista **desabilitadas, com o motivo**. Elas estão ali de propósito: é assim que você sabe para onde a seção vai, sem precisar perguntar.

## Só para aluguel, só para venda

No fato **"quando o cliente fechar"** você pode recortar: **Aluguel e venda**, **Só aluguel** ou **Só venda**. É o que impede um contrato de locação de sair num pedido de venda.

Quando você deixa em **Aluguel e venda**, a automação vale para os dois — não é um filtro vazio, é a escolha de não recortar.

## A lista: cada automação é uma frase

Depois de criada, cada automação aparece como **uma frase com um interruptor**:

> Quando o cliente fechar → gerar Contrato de locação
> *só aluguel*

Cada linha também mostra:

* o selo **Ativa** ou **Pausada**;
* **onde o arquivo vai parar** — *Em Documentos do pedido* e, com a nuvem conectada, *e no seu Drive*;
* **como ela gera** — por exemplo, *"itens agrupados · com o orçamento anexado"*. As automações criadas antes de existir o **Como gerar** dizem *"do jeito padrão do modelo"*;
* o botão **Ajustar como gerar**, que muda a forma de gerar **sem apagar** a regra e criar outra.

O interruptor **liga e desliga na hora**. Desligar não apaga a configuração: a automação para de agir e continua ali, pronta para voltar.

## O que esperar depois de ativar

- **O documento não sai na hora, e não deveria.** Gerar um PDF leva alguns segundos; segurar a tela por isso seria pior. Na seção **Documentos gerados**, nas Ações rápidas do pedido, aparece uma linha **"Gerando…"**; quando o arquivo fica pronto, ela dá lugar ao documento, como qualquer outro.
- **A automação só vale daqui para frente.** Criar uma regra hoje **não** gera documento de pedido fechado no mês passado. Isso é deliberado: uma regra nova nunca deve produzir uma enxurrada de arquivos retroativos.
- **Ela não passa por cima do que você fez.** Se uma pessoa já gerou aquele documento, a automação não o substitui.
- **Falta de informação não é erro.** Se o modelo do documento tem um campo que só uma pessoa sabe preencher, a linha mostra *"Falta preencher "X" para gerar este documento."* — e espera por você em vez de falhar.
- **Pedidos importados de planilha não disparam automação.** A importação grava os pedidos direto, sem passar pelo fluxo de criação — o que também evita que importar trezentos orçamentos gere trezentos documentos de uma vez.

## Perguntas frequentes

**Ganhei, cancelei e ganhei o mesmo orçamento de novo. O contrato sai duas vezes?**
Sai um contrato para cada vez que o pedido foi ganho — porque o acordo mudou, e o contrato anterior descreve algo que não vale mais. O arquivo novo substitui o antigo na lista de documentos do pedido. Se você já tinha enviado o PDF anterior ao cliente, mande o novo.

**Emiti a cobrança pelo app e marquei "gerar a fatura de locação". Com a automação ligada, saem duas?**
Não. É o mesmo documento na mesma chave — o arquivo é um só.

**Posso editar uma automação?**
Em parte. **Como gerar** se muda na própria regra, pelo botão **Ajustar como gerar**, sem apagar nada. Já o **fato** e o **documento** ainda não se editam: desligue a automação que não serve mais e crie outra. Remover pela tela vem em seguida.

**Mudei como eu gero o contrato à mão. A automação acompanha?**
Não. A regra guarda o **Como gerar** que ficou escolhido nela. Para mudar, use **Ajustar como gerar** na lista.

**Existe automação que já vem ligada?**
Não nesta versão. Tudo o que a seção faz, você ligou.

## Veja também

- [Modelos de documento](../documentos/modelos-personalizados.md) — o conteúdo do documento que a automação gera.
- [Nomes de arquivo](nomes-de-arquivo.md) — como o arquivo gerado é batizado.
- [Central de Notificações](central-de-notificacoes.md) — avisar pessoas é outra coisa, e mora ali.
- [Sincronização em Nuvem](sincronizacao-em-nuvem.md) — para onde o documento gerado vai depois.
