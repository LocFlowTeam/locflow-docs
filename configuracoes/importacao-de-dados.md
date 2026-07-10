---
description: >-
  Migre os contatos e o histórico de orçamentos do seu sistema antigo para o
  LocFlow com segurança — planejamento, passo a passo e boas práticas para não
  atrapalhar a operação.
---

# Importando dados de outro sistema

Se você já usa outro sistema (ou planilhas), não precisa começar do zero: o LocFlow importa a sua base de clientes e o histórico de pedidos deles. Assim, no primeiro dia de uso, sua equipe já sabe **quem é cliente antigo, quem é fidelizado** e quanto cada um já movimentou.

A importação fica em **Ajustes › Importação de Dados** — disponível em todos os planos. Você mesmo faz, sem depender da nossa equipe; e se precisar, o suporte está à disposição.

{% hint style="info" %}
A importação traz **dados históricos**: os pedidos entram como registros finalizados, só para consulta e para classificar seus clientes. Eles **não mexem** no seu estoque, na agenda de entregas nem geram cobranças — importar não interfere na operação do dia.
{% endhint %}

## O que dá para importar

| O quê | O que traz | Quando importar |
| --- | --- | --- |
| **Contatos** | Nome, CPF/CNPJ, telefone, e-mail e endereço dos seus clientes | **Primeiro** — é a base de tudo |
| **Histórico de orçamentos** | Os pedidos que cada cliente já fez (valor, data, itens) | **Depois dos contatos** — cada pedido é ligado ao cliente pelo CPF/CNPJ |

{% hint style="success" %}
Ao importar o histórico, o LocFlow reconhece automaticamente o estágio de cada cliente: quem fechou 1 pedido vira **cliente ativo**, quem fechou 2 ou mais vira **cliente fidelizado**. Sua carteira chega classificada.
{% endhint %}

## Antes de começar: planeje a virada

Migrar de sistema é uma mudança de rotina — meia hora de planejamento evita dor de cabeça:

1. **Escolha um momento calmo.** Faça a importação fora do pico da sua operação — para a maioria das locadoras, isso significa evitar os dias de montagem e retirada de eventos (em geral, quintas, sextas e segundas). Um começo de semana tranquilo ou um horário de baixa funciona bem.
2. **Exporte os dados do sistema atual.** Todo sistema tem um "exportar para Excel/CSV". Gere um arquivo de **clientes** e outro de **pedidos** — não precisa arrumar as colunas: o LocFlow pergunta o que cada coluna significa na hora de importar.
3. **Defina um responsável.** Uma pessoa faz a importação do começo ao fim (e vira a referência interna sobre "de onde veio cada dado").
4. **Cadastre o catálogo antes** (produtos e preços). Ele não é importado por planilha — e, com o catálogo pronto, o histórico de orçamentos consegue ligar cada item ao produto certo.

## Operação pequena ou grande? Duas formas de virar a chave

### Operação pequena: virada direta

Importe tudo de uma vez e comece a usar o LocFlow no dia seguinte:

1. Importe os **contatos**;
2. Importe o **histórico de orçamentos**;
3. A partir daí, crie os novos orçamentos **só no LocFlow**.

Mantenha o sistema antigo aberto **apenas para consulta** por 30 dias — se sentir falta de alguma informação, ela ainda está lá.

### Operação média ou grande: virada gradual

Se você tem muitos pedidos acontecendo ao mesmo tempo, não precisa (nem deve) virar tudo num dia:

1. **Semana 1** — importe contatos e histórico; a equipe conhece o sistema com os dados reais de vocês, sem pressão;
2. **Semanas 2 e 3** — comece a criar **os novos orçamentos** no LocFlow (por exemplo, metade dos pedidos novos, depois todos), enquanto os pedidos já em andamento terminam o ciclo no sistema antigo;
3. **Semana 4 em diante** — todo pedido novo nasce no LocFlow; o sistema antigo fica só para consultar o passado.

{% hint style="warning" %}
A regra de ouro da virada gradual: **cada pedido vive em um sistema só**. O que começou no sistema antigo, termina lá; o que nasceu no LocFlow, vive aqui. Assim ninguém dá baixa duas vezes — nem esquece de dar.
{% endhint %}

## O passo a passo da importação

1. Abra **Ajustes › Importação de Dados**;
2. Escolha **o que** importar (Contatos ou Histórico de orçamentos);
3. **Envie a planilha** (CSV ou Excel) e **mapeie as colunas**: para cada campo, diga qual coluna do seu arquivo o preenche. O LocFlow sugere o mapeamento sozinho e mostra um **dado de exemplo real** ao lado de cada coluna — você confere vendo o dado, sem adivinhar;
4. **Valide**: nada é gravado ainda. Cada linha é classificada em **OK** (entra limpa), **pendente** (entra com uma ressalva — ex.: contato sem CPF) ou **bloqueada** (não entra — ex.: cliente do pedido não encontrado);
5. Se houver bloqueadas, **baixe a devolutiva** — um arquivo com essas linhas e o **motivo** de cada uma. Corrija na sua planilha e importe de novo: o LocFlow **não duplica** o que já entrou;
6. **Aplique**. Pronto — os registros são criados na sua organização;
7. **Confira por amostragem**: abra 5 ou 10 clientes e compare com o sistema antigo (nome, telefone, quantidade de pedidos). Batendo a amostra, a migração está saudável.

## Dicas para a planilha

* **CPF/CNPJ é o elo.** É por ele que o histórico encontra o cliente — capriche nessa coluna nos dois arquivos. Com ou sem máscara, tanto faz: o LocFlow normaliza e valida;
* **Número do pedido evita duplicar.** Se a planilha de pedidos tiver o número original de cada um, reimportar o mesmo arquivo nunca cria cópia;
* **Endereço completo entra junto** (CEP, rua, número, bairro, cidade e UF). Se vier pela metade, o cliente entra mesmo assim — só o endereço fica para completar depois;
* **Itens do pedido são opcionais.** No modo **Rápido**, cada pedido entra só com o valor total; no modo **Integridade**, cada item é ligado a um produto do seu catálogo (pelo nome ou código). Os dois podem ser usados — comece pelo Rápido se quiser velocidade;
* **Colunas que você não mapear não se perdem**: elas ficam guardadas no histórico da importação.

## Se algo der errado

* **Linhas bloqueadas** têm sempre um motivo claro na devolutiva — corrija só elas e reimporte;
* **Reimportar é seguro**: contatos com o mesmo CPF/CNPJ e pedidos com o mesmo número de origem são reaproveitados, nunca duplicados;
* **Arquivo muito grande?** Divida a planilha em partes (por exemplo, por ano) e importe uma de cada vez.

{% hint style="info" %}
Qualquer dúvida durante a migração, [fale com o suporte](../primeiros-passos/onde-tirar-duvidas.md) — estamos à disposição para acompanhar a sua virada.
{% endhint %}
