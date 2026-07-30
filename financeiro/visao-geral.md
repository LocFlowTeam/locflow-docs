---
icon: gauge-high
description: O painel do seu caixa — saldo, entradas, saídas e resultado do período, o recorte por conta, os avisos de trabalho pendente e como o módulo se organiza.
---

# Visão geral do financeiro

A **Visão geral** é a tela que você abre todo dia para responder uma pergunta só: *estou no azul?* Ela mostra o saldo de hoje, o que entrou e o que saiu no período escolhido, o que vence e o que precisa de conferência — nessa ordem.

Você chega nela pelo menu **Financeiro → Gestão Financeira**.

{% hint style="success" %}
**Por que começar por aqui:** o saldo do LocFlow não é digitado por ninguém — ele é a **soma dos lançamentos**. Se o número desta tela te surpreende, a causa está sempre em uma linha do razão, e daqui você chega nela em dois toques.
{% endhint %}

## Como o módulo se organiza

O menu do financeiro tem **cinco destinos**, divididos em dois grupos:

| Grupo | Destino | Para que serve |
| --- | --- | --- |
| **Operação** | **Visão geral** | Como está o caixa hoje |
| **Operação** | [Lançamentos](lancamentos.md) | Todo o razão de entradas e saídas |
| **Operação** | [Contas a pagar](contas-a-pagar-e-a-receber.md) | O que vence e o que já venceu |
| **Análise** | Extrato | Movimentos do mês com saldo acumulado |
| **Análise** | [Relatórios](relatorios.md) | Categorias, insights, DRE e serviços |

No celular, o **título do topo** abre uma lista com as seções (a ativa vem marcada). Em telas largas, os cinco destinos viram **abas** — as de Operação à esquerda, as de Análise à direita, depois do divisor.

### Ajustes do financeiro (a engrenagem)

O que é **estrutura** ou **fila de trabalho** não ocupa o menu do dia a dia: mora atrás da **engrenagem**, no canto do cabeçalho.

| Em Ajustes | O que é |
| --- | --- |
| **Contas** | Onde o dinheiro vive — caixa, banco, carteira. Veja [Contas](contas.md) |
| **Categorias** | O plano de contas. Veja [Categorias e plano de contas](categorias-e-plano-de-contas.md) |
| **Fornecedores** | A quem você paga e os serviços que ele presta. Veja [Fornecedores](fornecedores.md) |
| **Fechamento de caixa** | Conferir o dinheiro que o motorista recebeu na rua |
| **Conciliação** | Extrato do banco × razão, mês a mês |

{% hint style="info" %}
**Por que essas cinco saíram do menu.** Contas, Categorias e Fornecedores você configura uma vez e revisita raramente. Fechamento e Conciliação são **filas**: só importam quando existe algo esperando — e, quando existe, elas se anunciam sozinhas (veja [Quando há trabalho esperando](#trabalho-esperando)). Um menu curto é um menu que você lê.
{% endhint %}

O **Fechamento de caixa** também aparece no **menu principal do app** quando há recebimentos a conferir, com o número de pendências ao lado.

## O olho: esconder os valores

No cabeçalho há um **ícone de olho** que troca todos os valores por `••••`. Ele vale para o módulo inteiro — útil para abrir o financeiro na frente de um cliente, ou compartilhar a tela sem expor faturamento.

## Os dois filtros do topo

Tudo nesta tela responde a dois recortes, lado a lado na mesma barra.

### Período

A pílula de **período** abre uma folha com cinco modos:

| Modo | O que faz |
| --- | --- |
| **Intervalo** | Duas datas quaisquer |
| **Semana** | A semana (segunda a domingo) da data escolhida |
| **Mês** | Um mês civil — é o padrão ao abrir a tela |
| **Últimos dias** | 30, 60 ou 90 dias corridos |
| **Anual** | O ano inteiro |

O recorte só é aplicado quando você toca em **Concluído** — assim a tela não recarrega a cada ajuste.

### Contas

A pílula de **Contas** abre uma folha de **múltipla escolha**: marque quantas quiser e o saldo, o resultado e o gráfico passam a considerar **só elas**. Cada conta aparece com o ícone do seu tipo e o saldo atual, para você decidir sem sair da folha.

* **Todas as contas** é o consolidado — nenhuma fica de fora.
* Com mais de uma marcada, a pílula mostra o recorte (*"2 de 4 contas"*) e ganha destaque, porque quem lê um saldo precisa saber que está vendo uma fatia.
* Abaixo da barra aparece a legenda *"Saldo, resultado e gráfico só de: …"* com os nomes.
* A pílula **Limpar**, ao lado, volta ao consolidado em um toque.

{% hint style="info" %}
O filtro de contas só aparece quando a sua organização tem **mais de uma conta**. Com uma só, ele não teria o que recortar.
{% endhint %}

## O que a tela mostra

1. **Saldo atual** — o herói do topo. É a soma do que já aconteceu (o **realizado**) nas contas do recorte.
2. **Entradas** e **Saídas** — os totais realizados do período.
3. **Resultado** — *o que sobrou (ou faltou)*: entradas menos saídas. Verde quando sobrou, vermelho quando faltou.
4. **Aviso de vencimentos** — uma faixa âmbar quando há contas **vencidas** ou vencendo **hoje**, com o total e um toque para as [Contas a pagar](contas-a-pagar-e-a-receber.md).
5. **Evolução do caixa** — o gráfico de entradas × saídas × saldo acumulado ao longo do período. A legenda liga e desliga cada linha, e você pode **salvar a visão** que usa sempre como um preset nomeado.
6. **Vencimentos** (telas largas) — uma coluna ao lado do gráfico com vencidas, vence hoje e próximos 7 dias.
7. **Últimos lançamentos** — as últimas linhas do razão, com **Ver todos** para a lista completa.

{% hint style="warning" %}
**O previsto não entra no saldo.** Uma conta a pagar que ainda não foi paga (e um recebimento que ainda não caiu) **não** mexe no saldo nem no resultado — ela aparece nas contas a pagar/receber e no *previsto em aberto* das contas. O saldo é dinheiro que já se moveu. O porquê está em [Lançamentos](lancamentos.md#previsto-x-realizado).
{% endhint %}

## Quando há trabalho esperando {#trabalho-esperando}

Logo abaixo do saldo podem aparecer até dois cartões — e eles **só existem quando existe pendência**:

| Cartão | O que significa | Para onde leva |
| --- | --- | --- |
| **N recebimentos a conferir** | Dinheiro ou maquininha que alguém recebeu fora do sistema e a tesouraria ainda não conferiu | Fechamento de caixa |
| **N linhas do extrato a conciliar** | Linhas do extrato bancário importado que ainda não casaram com o razão | Fila de conciliação, já aberta na aba certa |

Com zero pendência, **nada é desenhado** — sem "tudo em ordem" ocupando espaço. É por isso que Fechamento e Conciliação não precisam de lugar fixo no menu: os dois se anunciam quando têm o que dizer. O que cada um resolve está em [Conciliação e fechamento](conciliacao-e-fechamento.md).

## Registrar uma entrada ou saída

O botão **+** (ou **Novo lançamento**, em telas largas) oferece dois caminhos:

* **Nova despesa** — dinheiro saindo.
* **Nova receita** — dinheiro entrando.

Os dois abrem o mesmo passo a passo, descrito em [Lançamentos](lancamentos.md#registrar-um-lancamento). Recebimentos de clientes e repasses a parceiros **você não precisa registrar**: eles entram sozinhos.

## Por porte

| Porte | Como usar esta tela |
| --- | --- |
| **Autônomo / MEI** | Uma conta só, modo **Mês**: olhe o saldo, o resultado e o aviso de vencimentos. É o suficiente para não perder conta nenhuma. |
| **Médio** | Duas ou três contas (caixa e bancos). Use o recorte por conta para conferir cada uma antes de fechar o mês. |
| **Grande** | Modo **Últimos 90 dias** ou **Anual** no gráfico para ver tendência, presets salvos para as visões recorrentes, e os cartões de pendência como fila diária da tesouraria. |

## Situações reais

* **"O saldo está menor do que eu esperava."** Troque o recorte para **uma conta** por vez: o dinheiro pode estar em outra conta, não faltando. Se continuar estranho, abra **Últimos lançamentos → Ver todos** e filtre por **Saídas**.
* **"Apareceu um cartão azul de linhas a conciliar."** Alguém importou o extrato do banco e há linhas sem par no razão. Toque nele: a fila abre direto na aba do extrato.
* **"Meu resultado está negativo, mas tenho saldo."** Normal: o resultado é do **período** escolhido, e o saldo é o acumulado de tudo. Um mês ruim não zera o caixa construído antes.
* **"Preciso mostrar a tela para o contador sem expor valores."** Ligue o **olho**: os números viram `••••` e a estrutura continua visível.

## Próximo passo

* Para entender cada linha do razão e o que o sistema lança sozinho: [Lançamentos](lancamentos.md).
* Para preparar as contas onde o dinheiro vive: [Contas](contas.md).
* Para aprender a ler os números e decidir com eles: [Entender seus números](../conceitos/entender-seus-numeros.md).
