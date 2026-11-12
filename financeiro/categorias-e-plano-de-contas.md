---
icon: tags
description: Como o plano de contas organiza o dinheiro que entra e sai — categorias padrão, suas categorias, subcategorias, a operação que cada uma sustenta, o recurso que ela exige, o serviço associado e o arquivamento.
---

# Categorias e plano de contas

O **plano de contas** é a lista de categorias que diz **em que** o dinheiro entrou ou saiu. É ele que faz o relatório responder *"quanto gastei com manutenção este mês?"* em vez de mostrar uma pilha de lançamentos sem grupo.

Você o encontra em **Gestão Financeira → engrenagem (Ajustes) → Categorias**.

{% hint style="success" %}
**Por que vale investir cinco minutos aqui:** categoria bem escolhida é relatório pronto. Sem ela, todo fim de mês vira uma conferência item por item para descobrir onde o dinheiro foi.
{% endhint %}

## Como a tela se organiza

A tela segue o mesmo formato das outras listagens do LocFlow:

* **Busca** por nome de categoria **ou** de subcategoria — buscar "pedágio" traz a subcategoria e também a categoria-mãe dela, para você ver o contexto.
* **Filtros** por tipo (receitas, despesas ou tudo), situação (ativas, arquivadas ou todas) e **serviço associado**.
* **Itens por página** e navegação — a paginação conta **categorias-mãe**: uma mãe nunca se separa das subcategorias dela ao virar a página.
* **Totais do recorte** no topo: Receitas, Despesas e Saldo do que está visível.
* Em cada categoria-mãe, três números: o **Total do período** (a família inteira), **Só nesta** (o que foi lançado direto na categoria-mãe, sem as filhas) e **Nas subcategorias** (a soma das filhas). Os dois últimos somam o primeiro.

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

O total da categoria-mãe **já inclui** o das subcategorias. Na listagem as subcategorias aparecem sempre visíveis, recuadas sob a mãe — é assim que se lê um plano de contas. E o que foi lançado **direto na mãe** (sem escolher uma filha) não some: ele aparece em **Só nesta**.

Para criar uma subcategoria, use **Nova categoria**, marque **Subcategoria** em *Onde ela fica?* e escolha a categoria-mãe.

## Serviço associado {#servico-associado}

No campo **Serviço prestado**, marcar uma categoria como **Frete**, **Mão de obra**, **Montagem**, **Desmontagem**, **Layout** ou **Outro** liga aquele custo ao **serviço que você cobra** do cliente.

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

## Criar e editar uma categoria

Use **Nova categoria** (o botão **+**) para criar: primeiro o **Tipo** (Despesa ou Receita) e **Onde ela fica?** — **Categoria principal** ou **Subcategoria**, escolhendo a mãe. Para editar, toque na linha (ou no cartão). O resto do formulário é o mesmo nos dois casos:

| Campo | Para que serve |
| --- | --- |
| **Nome** | Como a categoria aparece nos lançamentos e nos relatórios. Vale para as padrão e para as suas |
| **Ícone** | O desenho que identifica a categoria na lista e na grade de categorias do lançamento |
| **Recurso no lançamento** | *O recurso que esta categoria destaca — e pode exigir — em cada lançamento*: **Nenhum**, **Veículo**, **Funcionário** ou **Galpão**. Escolhido um, o interruptor **Não salvar o lançamento sem o veículo** (ou o funcionário, ou o galpão) torna o campo obrigatório — *Combustível* sem veículo, por exemplo, deixa de entrar no custo por veículo. Desligado, o campo fica em destaque, mas pode ficar em branco |
| **Sustenta qual operação?** | **Não sei**, **Aluguel**, **Venda** ou **As duas**. *Fica pré-selecionado no lançamento; quem lança pode trocar.* É o que permite a margem por operação — veja [A natureza](lancamentos.md#natureza) |
| **Serviço prestado** (opcional) | Liga o custo ao serviço que você cobra — veja [acima](#servico-associado) |

Na edição, você ainda pode **arquivar ou reativar** — só nas categorias que você criou.

{% hint style="info" %}
**A subcategoria herda da mãe.** Quando a mãe exige um recurso e a subcategoria não declara nenhum, ela segue a regra da mãe, e o formulário diz de onde vem: *"Herda de “Combustível”: o lançamento vai exigir o veículo."* As categorias de folha de pagamento do plano padrão exigem sempre o funcionário: todo lançamento de pessoal é de alguém.
{% endhint %}

{% hint style="warning" %}
Renomear uma categoria muda o nome **em todo o histórico**, inclusive nos relatórios de meses anteriores. Isso é intencional: é a mesma conta, com outro nome. Se você quer um grupo novo sem mexer no passado, crie uma categoria nova.
{% endhint %}

## Onde a categoria aparece depois

* Em cada **lançamento** (entrada ou saída) que você registra na Gestão Financeira.
* Nos **relatórios** por categoria, que agrupam o mês pelo plano de contas.
* Nas **taxas do pagamento online**, que o sistema lança sozinho na categoria padrão correspondente — veja [Taxas do pagamento online](../cobranca/taxas-do-gateway.md).
* Nos **repasses a parceiros**, também lançados automaticamente — veja [O dinheiro da parceria](../parcerias/dinheiro-da-parceria.md).
