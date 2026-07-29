---
icon: tags
description: Como o plano de contas organiza o dinheiro que entra e sai — categorias padrão, suas categorias, subcategorias, serviço associado e arquivamento.
---

# Categorias e plano de contas

O **plano de contas** é a lista de categorias que diz **em que** o dinheiro entrou ou saiu. É ele que faz o relatório responder *"quanto gastei com manutenção este mês?"* em vez de mostrar uma pilha de lançamentos sem grupo.

Você o encontra em **Gestão Financeira → Categorias**.

{% hint style="success" %}
**Por que vale investir cinco minutos aqui:** categoria bem escolhida é relatório pronto. Sem ela, todo fim de mês vira uma conferência item por item para descobrir onde o dinheiro foi.
{% endhint %}

## Como a tela se organiza

A tela segue o mesmo formato das outras listagens do LocFlow:

* **Busca** por nome de categoria **ou** de subcategoria — buscar "pedágio" traz a subcategoria e também a categoria-mãe dela, para você ver o contexto.
* **Filtros** por tipo (receitas, despesas ou tudo), situação (ativas, arquivadas ou todas) e **serviço associado**.
* **Itens por página** e navegação — a paginação conta **categorias-mãe**: uma mãe nunca se separa das subcategorias dela ao virar a página.
* **Totais do recorte** no topo: Receitas, Despesas e Saldo do que está visível.

Em telas grandes você vê uma **tabela** (com escolha de colunas pelo botão *Colunas*); no celular, **cartões** — mesmos dados, mesma ação.

{% hint style="info" %}
Os totais são do **mês corrente** e acompanham os filtros. Eles somam apenas as **categorias-mãe** visíveis: o total da mãe já inclui as subcategorias, então somar as duas contaria o mesmo dinheiro duas vezes.
{% endhint %}

## Categorias padrão × suas categorias

| | Categorias padrão | Suas categorias |
| --- | --- | --- |
| **De onde vêm** | Já vêm prontas com a sua locadora | Você cria |
| **Para que servem** | São onde o sistema encaixa o que registra sozinho: recebimento do cliente, repasse ao parceiro, taxa do pagamento online | Detalhar a operação com o seu vocabulário |
| **Renomear** | Sim | Sim |
| **Arquivar** | Não | Sim |

As padrão não podem ser arquivadas porque **o lançamento automático precisa de um destino**: se ela desaparecesse, o próximo recebimento não teria onde entrar. Renomear resolve o caso real — se na sua locadora "Receita de locação" se chama "Aluguel", troque o nome e siga.

## Subcategorias

Servem para **detalhar sem multiplicar o relatório**:

* **Manutenção de ativos** fica como a linha que você acompanha no mês.
* **Peças**, **Insumos** e **Terceiros** contam a história por dentro dela.

O total da categoria-mãe **já inclui** o das subcategorias. Na listagem as subcategorias aparecem sempre visíveis, recuadas sob a mãe — é assim que se lê um plano de contas.

Para criar uma subcategoria, use **Nova categoria** e escolha a categoria-mãe.

## Serviço associado

Marcar uma categoria como **Frete**, **Mão de obra**, **Montagem**, **Desmontagem**, **Layout** ou **Operador** liga aquele custo ao **serviço que você cobra** do cliente.

É o que permite ao relatório comparar os dois lados: o que você **gasta** com frete × o que você **cobra** de frete. Sem esse vínculo, os dois números existem em telas separadas e ninguém junta.

{% hint style="info" %}
O serviço associado é opcional. A maioria das categorias não aponta para nenhum — e está tudo bem.
{% endhint %}

## Arquivar em vez de excluir

Arquivar tira a categoria das próximas escolhas e **preserva o histórico**:

* Os lançamentos antigos continuam nela.
* Os relatórios de meses fechados não mudam.

Excluir apagaria o passado — por isso o LocFlow não oferece essa opção. Se você criou uma categoria por engano e ela nunca foi usada, arquivar tem o mesmo efeito prático: ela sai do caminho.

Para arquivar: toque na categoria e use **Arquivar**. Para trazê-la de volta, filtre por **Arquivadas** e use **Reativar**.

## Editando uma categoria

Toque na linha (ou no cartão) para abrir a edição. Você pode:

1. **Renomear** — vale para as padrão e para as suas.
2. **Trocar o serviço associado** — inclusive para "Nenhum".
3. **Arquivar ou reativar** — só nas categorias que você criou.

{% hint style="warning" %}
Renomear uma categoria muda o nome **em todo o histórico**, inclusive nos relatórios de meses anteriores. Isso é intencional: é a mesma conta, com outro nome. Se você quer um grupo novo sem mexer no passado, crie uma categoria nova.
{% endhint %}

## Onde a categoria aparece depois

* Em cada **lançamento** (entrada ou saída) que você registra na Gestão Financeira.
* Nos **relatórios** por categoria, que agrupam o mês pelo plano de contas.
* Nas **taxas do pagamento online**, que o sistema lança sozinho na categoria padrão correspondente — veja [Taxas do pagamento online](../cobranca/taxas-do-gateway.md).
* Nos **repasses a parceiros**, também lançados automaticamente — veja [O dinheiro da parceria](../parcerias/dinheiro-da-parceria.md).
