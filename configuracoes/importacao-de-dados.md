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

1. Abra **Ajustes › Importação de Dados**;
2. Escolha **o quê** importar (Contatos ou Histórico de orçamentos);
3. **Envie a planilha** (CSV ou Excel) e **mapeie as colunas**: para cada campo, diga qual coluna do seu arquivo o preenche. O LocFlow sugere o mapeamento sozinho e mostra um **dado de exemplo real** ao lado de cada coluna — você confere vendo o dado, sem adivinhar. Colunas com dados que ficarem sem mapeamento são avisadas antes de avançar;
4. **Valide**: nada é gravado ainda. Cada linha é classificada em **OK** (entra limpa), **pendente** (entra com uma ressalva — ex.: contato sem CPF) ou **bloqueada** (não entra — ex.: cliente do pedido não encontrado). **Toque em qualquer linha** para ver os dados dela e o motivo exato da classificação;
5. Se houver bloqueadas, **baixe a devolutiva** — um arquivo com essas linhas e o **motivo** de cada uma. Corrija na sua planilha e importe de novo: o LocFlow **não duplica** o que já entrou;
6. **Aplique**. Uma **barra de progresso** mostra o avanço em tempo real ("1.500 de 5.000 importados") — em planilhas grandes, a importação acontece em etapas e pode levar alguns minutos. Mantenha a tela aberta;
7. **Confira por amostragem**: abra 5 ou 10 clientes e compare com o sistema antigo (nome, telefone, quantidade de pedidos). Batendo a amostra, a migração está saudável.

## Limites e desempenho

* **Até 10.000 linhas por arquivo.** Se a sua planilha tiver mais que isso, divida em partes (por exemplo, por ano ou por letra inicial) e importe uma de cada vez — a tela avisa se o arquivo passar do limite;
* Planilhas grandes são importadas **em etapas** (a barra de progresso mostra cada avanço). É normal levar alguns minutos;
* Prefira **CSV ou Excel simples** (uma aba, primeira linha com os títulos das colunas).

## E se algo der errado no meio?

Pode ficar tranquilo — a importação foi desenhada para **nunca perder nem duplicar** dados:

* **Caiu a conexão / fechou a tela durante a importação?** O que já entrou está salvo. Volte à tela e toque em **"Continuar importação"**: ela retoma exatamente de onde parou;
* **Reimportar o mesmo arquivo é seguro**: contatos com o mesmo CPF/CNPJ e pedidos com o mesmo número de origem são reaproveitados, nunca duplicados;
* **Linhas bloqueadas** têm sempre um motivo claro — toque na linha para ver, ou baixe a devolutiva, corrija só o que falhou e reimporte;
* **Errou o mapeamento?** Se percebeu na validação, volte um passo e ajuste — nada foi gravado ainda. Se percebeu depois de aplicar, fale com o suporte que ajudamos a corrigir.

## Dicas para a planilha

* **CPF/CNPJ é o elo.** É por ele que o histórico encontra o cliente — capriche nessa coluna nos dois arquivos. Com ou sem máscara, tanto faz: o LocFlow normaliza e valida;
* **Número do pedido evita duplicar — e continua pesquisável.** Se a planilha de pedidos tiver o número original de cada um, reimportar o mesmo arquivo nunca cria cópia; e depois de importar, sua equipe encontra qualquer pedido **buscando pelo número antigo** na lista de orçamentos (ele aparece como "nº 1042" ao lado do código novo). O código do LocFlow é a referência oficial daqui para frente — o número antigo fica como ponte durante a transição;
* **Endereço completo entra junto** (CEP, rua, número, bairro, cidade e UF). Se vier pela metade, o cliente entra mesmo assim — só o endereço fica para completar depois;
* **Itens do pedido são opcionais.** No modo **Rápido**, cada pedido entra só com o valor total; no modo **Integridade**, cada item é ligado a um produto do seu catálogo (pelo nome ou código) — se a planilha tiver uma linha por item, linhas com o mesmo número de pedido viram um pedido só. Comece pelo Rápido se quiser velocidade;
* **Colunas que você não mapear não se perdem**: elas ficam guardadas no histórico da importação.

{% hint style="info" %}
Qualquer dúvida durante a migração, [fale com o suporte](../primeiros-passos/onde-tirar-duvidas.md) — estamos à disposição para acompanhar a sua virada.
{% endhint %}
