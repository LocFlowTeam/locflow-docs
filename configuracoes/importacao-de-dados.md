---
description: >-
  Migre os contatos e o histórico de orçamentos do seu sistema antigo para o
  LocFlow com segurança — planejamento, passo a passo, limites e o que fazer se
  algo der errado.
---

# Importando dados de outro sistema

Se você já usa outro sistema (ou planilhas), não precisa começar do zero: o LocFlow importa a sua base de clientes e o histórico de pedidos deles. Assim, no primeiro dia de uso, sua equipe já sabe **quem é cliente antigo, quem é fidelizado** e quanto cada um já movimentou.

A importação fica em **Ajustes › Importação de Dados** — disponível em todos os planos. Você mesmo faz, sem depender da nossa equipe; e o **?** no topo da tela traz este guia resumido, sempre à mão.

{% hint style="info" %}
A importação traz **dados históricos**: os pedidos entram como registros finalizados, só para consulta e para classificar seus clientes. Eles **não mexem** no seu estoque, na agenda de entregas nem geram cobranças — importar não interfere na operação do dia.
{% endhint %}

## O que dá para importar

| O quê | O que traz | Quando importar |
| --- | --- | --- |
| **Contatos** | Nome, CPF/CNPJ, telefone, e-mail e endereço completo dos seus clientes | **Primeiro** — é a base de tudo |
| **Histórico de orçamentos** | Os pedidos que cada cliente já fez (valor, data e, se quiser, os itens) | **Depois dos contatos** — cada pedido é ligado ao cliente pelo CPF/CNPJ |

{% hint style="success" %}
Ao importar o histórico, o LocFlow reconhece automaticamente o estágio de cada cliente: quem fechou 1 pedido vira **cliente ativo**, quem fechou 2 ou mais vira **cliente fidelizado**. Sua carteira chega classificada — veja o selo na ficha de cada contato.
{% endhint %}

## Antes de começar: planeje a virada

Migrar de sistema é uma mudança de rotina — meia hora de planejamento evita dor de cabeça. O
essencial:

1. **Escolha um momento calmo.** Faça a importação fora do pico da sua operação — para a maioria das locadoras, isso significa evitar os dias de montagem e retirada de eventos (em geral, quintas, sextas e segundas). Um começo de semana tranquilo funciona bem.
2. **Exporte os dados do sistema atual.** Todo sistema tem um "exportar para Excel/CSV". Gere um arquivo de **clientes** e outro de **pedidos** — não precisa arrumar as colunas: o LocFlow pergunta o que cada coluna significa na hora de importar.
3. **Defina um responsável.** Uma pessoa faz a importação do começo ao fim (e vira a referência interna sobre "de onde veio cada dado").
4. **Cadastre o catálogo antes** (produtos e preços). Com o catálogo pronto, o histórico de orçamentos consegue ligar cada item ao produto certo.

{% hint style="success" %}
**Vai trocar de sistema de verdade?** Então leia [Migrar com segurança](migrar-com-seguranca.md):
qual estratégia de virada escolher (direta, gradual ou duplo lançamento), que dia virar, o que
trazer e o que deixar para trás, como conferir se deu certo e o que fazer se algo falhar — com
checklist para imprimir.
{% endhint %}

{% hint style="warning" %}
A regra de ouro de qualquer virada: **cada pedido vive em um sistema só**. O que começou no sistema antigo, termina lá; o que nasceu no LocFlow, vive aqui. Assim ninguém dá baixa duas vezes — nem esquece de dar.
{% endhint %}

## O passo a passo da importação

Abra **Ajustes › Importação de Dados**, escolha **o quê** importar (Contatos ou Histórico de
orçamentos) e siga os **cinco passos**:

### 1. Arquivo

Escolha a planilha (CSV ou Excel). O LocFlow mostra na hora as **três primeiras linhas, exatamente
como estão no seu arquivo**, com as letras das colunas (A, B, C…) igual ao Excel.

{% hint style="info" %}
Confira aqui se a **primeira linha é o cabeçalho** e não um cliente. Se for um cliente, troque o
arquivo colocando a linha de títulos no topo — assim nenhum cadastro se perde.
{% endhint %}

A leitura acontece **no seu aparelho**. Nada é enviado neste passo.

### 2. Ligações

Aqui você diz **o que cada coluna significa**. Toda linha tem dois lados: à esquerda, uma coluna da
**sua planilha** (em fonte de máquina, com a letra da coluna); à direita, o **campo do LocFlow** que
vai receber esse dado. Essa ordem nunca muda.

Os campos aparecem em quatro blocos, do mais importante ao menos:

| Bloco | O que é |
| --- | --- |
| **1 · Obrigatório** | Só o Nome. É o único campo sem o qual o cadastro não existe |
| **2 · Reconhecemos sozinhos** | O que adivinhamos pelo nome do cabeçalho. Confira as amostras e toque em **Confirmar as N ligações** para aprovar todas de uma vez |
| **3 · Quer trazer mais?** | Campos ainda livres, se você quiser aproveitar mais colunas |
| **4 · Não vou importar** | As colunas que ficam de fora — **nomeadas**, com o dado real de cada uma e um botão **Usar** se alguma delas deveria virar um campo |

Cada coluna mostra um **dado de verdade** da sua planilha, e sempre **do mesmo cliente** — assim dá
para comparar colunas parecidas sem adivinhar pelo nome do cabeçalho.

{% hint style="success" %}
Toque em **Ver como vai ficar**: o LocFlow monta a **ficha do cliente pronta**, com um registro real
da sua planilha, e mostra debaixo de cada valor de qual coluna ele veio. É a forma mais rápida de
perceber que o telefone caiu no lugar do CNPJ. No computador, essa prévia fica sempre visível ao lado.
{% endhint %}

### 3. Conferir

O ensaio da importação: **nada é gravado**. O resultado vem em três números:

| Resultado | O que significa |
| --- | --- |
| **Entram** | O cadastro entra completo |
| **Com ressalva** | O cadastro **entra**, mas falta um pedaço (ex.: contato sem CPF/CNPJ) |
| **Ficam de fora** | Falta algo sem o que o cadastro não existe |

O que fica de fora vem **agrupado por motivo** ("Sem nome no arquivo · 18", "CPF/CNPJ inválido · 19"),
não linha a linha — cada motivo é **um conserto só** na sua planilha. Toque em **Ver linhas** para
percorrer as linhas daquele motivo, uma a uma, com o problema destacado e o conserto explicado.

Se preferir corrigir no Excel, **baixe o arquivo** com as linhas de fora e o motivo de cada uma.

### 4. Importar

Aqui, sim, os dados entram. A tela mostra **quantos vão entrar**, o que acontece com quem já existe
e um **anel de progresso** com o avanço real. Pode levar alguns minutos em planilhas grandes —
deixe a tela aberta.

### 5. Pronto

O total que entrou e, se houver, quantas linhas ficaram de fora e por quê. Daqui você vai direto ver
o que importou — ou emenda a próxima planilha.

{% hint style="success" %}
**Depois de importar, confira por amostragem**: abra 5 ou 10 clientes e compare com o sistema antigo
(nome, telefone, quantidade de pedidos). Batendo a amostra, a migração está saudável. As três
conferências completas estão em [Migrar com segurança](migrar-com-seguranca.md).
{% endhint %}

## Limites e desempenho

* **Até 10.000 linhas por arquivo.** Se a sua planilha tiver mais que isso, divida em partes (por exemplo, por ano ou por letra inicial) e importe uma de cada vez — a tela avisa se o arquivo passar do limite;
* Planilhas grandes são importadas **em etapas** (a barra de progresso mostra cada avanço). É normal levar alguns minutos;
* Prefira **CSV ou Excel simples** (uma aba, primeira linha com os títulos das colunas).

## E se algo der errado no meio?

Pode ficar tranquilo — a importação foi desenhada para **nunca perder nem duplicar** dados:

* **Caiu a conexão / fechou a tela durante a importação?** O que já entrou está salvo. Volte à tela e toque em **"Continuar de onde parou"**: ela retoma exatamente de onde parou, sem duplicar nada;
* **Reimportar o mesmo arquivo é seguro**: contatos com o mesmo CPF/CNPJ e pedidos com o mesmo número de origem são reaproveitados, nunca duplicados;
* **Linhas bloqueadas** têm sempre um motivo claro — toque na linha para ver, ou baixe a devolutiva, corrija só o que falhou e reimporte;
* **Errou uma ligação?** Se percebeu na conferência, volte um passo e ajuste — nada foi gravado ainda. Se percebeu depois de importar, fale com o suporte que ajudamos a corrigir.

## Dicas para a planilha

* **CPF/CNPJ é o elo.** É por ele que o histórico encontra o cliente — capriche nessa coluna nos dois arquivos. Com ou sem máscara, tanto faz: o LocFlow normaliza e valida;
* **Número do pedido evita duplicar — e continua pesquisável.** Se a planilha de pedidos tiver o número original de cada um, reimportar o mesmo arquivo nunca cria cópia; e depois de importar, sua equipe encontra qualquer pedido **buscando pelo número antigo** na lista de orçamentos (ele aparece como "nº 1042" ao lado do código novo). O código do LocFlow é a referência oficial daqui para frente — o número antigo fica como ponte durante a transição;
* **Endereço completo entra junto** (CEP, rua, número, bairro, cidade e UF). Se vier pela metade, o cliente entra mesmo assim — só o endereço fica para completar depois;
* **Itens do pedido são opcionais.** No modo **Rápido**, cada pedido entra só com o valor total; no modo **Integridade**, cada item é ligado a um produto do seu catálogo (pelo nome ou código) — se a planilha tiver uma linha por item, linhas com o mesmo número de pedido viram um pedido só. Comece pelo Rápido se quiser velocidade;
* **Colunas que ficam de fora não se perdem**: elas continuam guardadas no histórico da importação;
* **Não tem sistema de onde exportar?** Baixe o **modelo de planilha** (no hub da importação ou no passo do arquivo): ele vem com os títulos certos e uma linha de exemplo preenchida, mostrando em que formato escrever data, CPF/CNPJ e valores.

{% hint style="info" %}
Qualquer dúvida durante a migração, [fale com o suporte](../primeiros-passos/onde-tirar-duvidas.md) — estamos à disposição para acompanhar a sua virada.
{% endhint %}
