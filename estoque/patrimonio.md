---
icon: landmark
description: Quanto vale o seu estoque — o valor de hoje, que considera o desgaste, o valor para repor tudo novo, o resultado das vendas e o relatório lote a lote.
---

# Patrimônio: quanto vale o seu estoque

Saber **quantas** cadeiras você tem é metade da resposta. A outra metade é **quanto elas valem** — para decidir se compensa repor, para conversar com o contador e para saber o tamanho real do seu negócio. É isso que a seção **Patrimônio** do [Painel de Estoque](painel.md) responde.

Você a encontra em **Estoque › Painel de Estoque › Patrimônio** (no grupo **Análise**). Um resumo também aparece no cartão **Patrimônio** da Visão geral.

{% hint style="info" %}
**Quem vê.** O Patrimônio faz parte de um plano superior e só aparece para quem tem acesso ao patrimônio do estoque. Sem esse acesso, a seção e o cartão simplesmente não existem — não viram "••••". Se você não vê, veja [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md) ou fale com quem administra os [acessos](../configuracoes/colaboradores-e-acessos.md).
{% endhint %}

## Dois valores do mesmo material

| Valor | O que responde |
| --- | --- |
| **Valor hoje** | Quanto o material vale **considerando o desgaste** do uso ao longo do tempo |
| **Valor para repor** | Quanto você gastaria para **comprar tudo novo agora** |

A distância entre os dois é o quanto o seu acervo já envelheceu. Um valor de hoje muito abaixo do de repor é o sinal de que uma renovação grande vem aí — melhor saber agora do que no mês em que as cadeiras começarem a quebrar.

{% hint style="success" %}
**O material alugado continua seu.** O que está na rua, num evento, segue somado no patrimônio — o bem é seu. Só **baixa** e **venda** reduzem o patrimônio.
{% endhint %}

## De onde vêm os valores

O patrimônio nasce das **entradas de estoque**. Ao [registrar uma entrada](operacoes-de-estoque.md#registrar-entrada) você informa:

* o **valor de compra** (por unidade ou o total da nota) — é ele que forma o valor do material;
* opcionalmente, na parte **Depreciação**, a **vida útil** em meses e o **valor residual** por unidade — é o que faz o valor de hoje cair com o tempo. Sem vida útil, o item vale sempre o que custou.

{% hint style="warning" %}
**Material sem entrada não tem valor.** A sobra que você achou numa contagem passa a contar em unidades, mas não tem custo — e por isso não entra no patrimônio. (Na reclassificação é diferente: o material só muda de estoque e leva junto o valor que já tinha.) Se a seção mostra *"Nenhum lote com valor cadastrado ainda"*, é isso: registre o custo nas entradas e o patrimônio aparece.
{% endhint %}

## O que a seção mostra

1. **Quanto vale o estoque hoje** — o número grande, com o valor para repor e o total de unidades logo abaixo (*"R$ 182.400,00 para repor hoje · 2.054 un"*).
2. **Projeção de depreciação · 12 meses** — uma linha descendente de **Hoje** até **+12m**, com quanto o valor do material atual vai cair no próximo ano.
3. **Resultado de vendas no mês** — quando houve venda de estoque: o **Recebido**, o **Custo do material** vendido e o resultado (positivo ou negativo). Vendas antigas, de antes de o custo ser registrado, aparecem contadas à parte.
4. **Por local** — uma linha por galpão (ou loja com estoque próprio), com as unidades, o valor **Hoje** e o valor **Para repor**.
5. **Relatório detalhado, lote a lote** — abre o relatório completo.

O **olho** do topo do painel esconde todos esses valores, para você abrir a tela na frente de alguém.

## O relatório lote a lote

O botão **Relatório detalhado, lote a lote** abre o **Relatório contábil** — *"Valoração por lote · exportável"*. É uma tabela só de leitura, uma linha por lote de compra:

| Coluna | O que mostra |
| --- | --- |
| **Produto** e **Local** | O que é e onde está |
| **Qtd** | Quantas unidades daquele lote ainda existem |
| **Custo** | Quanto custou |
| **Deprec.** | Quanto do valor já se desgastou, em porcentagem |
| **Contábil** | O valor de hoje daquele lote |

No topo, o **valor contábil total**. O botão **Exportar** gera um arquivo **CSV** para mandar ao contador ou abrir numa planilha.

## Situações reais

* **"Quero saber se compensa trocar as tendas este ano."** Compare o valor hoje com o valor para repor, no local onde as tendas ficam. Se o valor de hoje já está perto do residual, o material está no fim da vida útil que você definiu.
* **"O patrimônio está zerado, mas eu tenho material."** O seu estoque provavelmente nasceu de contagens, sem entrada. Registre as entradas com o valor de compra.
* **"Vendi umas cadeiras usadas — ganhei ou perdi?"** Olhe o **Resultado de vendas no mês**: ele compara o que você recebeu com o custo daquelas unidades.

## Próximo passo

Veja como registrar o custo do material em [Operações de estoque](operacoes-de-estoque.md#registrar-entrada), conheça o painel inteiro em [Painel de Estoque](painel.md) e entenda o desgaste do acervo nos seus números em [Entender seus números](../conceitos/entender-seus-numeros.md).
