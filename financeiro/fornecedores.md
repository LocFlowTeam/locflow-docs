---
icon: store
description: Quem recebe o seu dinheiro — uma lista só com todos os fornecedores, os serviços que cada um presta, a categoria (Direto, Indireto, Estratégico), a Matriz de Kraljic e o total já pago.
---

# Fornecedores

**Fornecedor** é quem recebe o seu dinheiro: o posto que abastece a frota, a operadora do telefone, a oficina que conserta os bens móveis, o contador, a transportadora que faz o frete. Cadastrá-los transforma uma pilha de despesas soltas em respostas — *com quem eu mais gasto?*, *quanto essa oficina já levou este ano?*, *de quem eu não posso ficar sem?*

É **uma tela só**, com duas portas que levam ao mesmo lugar:

* **Cadastros Base → Fornecedores**, no menu principal;
* **Gestão Financeira → engrenagem (Ajustes) → Fornecedores**.

{% hint style="info" %}
**Não vê o item no menu?** Numa organização recém-configurada, **Fornecedores** começa guardado no menu principal — use **Personalizar** no menu para mostrá-lo, ou entre pela engrenagem do financeiro. O item aparece para quem tem a permissão do cadastro base **ou** a do financeiro.
{% endhint %}

{% hint style="success" %}
**Por que o cadastro se paga rápido:** marcando **os serviços que cada fornecedor presta**, cada despesa dele já nasce na **categoria certa** — sem você escolher na lista toda vez. E o relatório passa a comparar o que você **gasta** com aquele serviço e o que você **cobra** por ele.
{% endhint %}

## Todos os fornecedores numa lista

A lista reúne os fornecedores que nasceram em lugares diferentes, cada um dizendo **de onde veio**:

| Origem | O que é |
| --- | --- |
| **Ficha do financeiro** | Quem você cadastrou aqui ou ao lançar uma despesa |
| **Contatos** | Um contato da sua agenda com o papel **Fornecedor** |
| **Parceiros → Fornecedores** | Uma transportadora parceira, que executa frete nos seus pedidos — veja [Fornecedores de frete](../parcerias/fornecedores-de-frete.md) |

Quem já tem ficha no financeiro não ganha legenda (é o caminho de sempre); os demais mostram *em Contatos* ou *em Parceiros → Fornecedores* logo abaixo do nome.

## Cadastrar um fornecedor

Toque em **+** (**Novo fornecedor**):

* **Com a permissão do cadastro base**, o cadastro começa pelos dados da pessoa ou empresa — a mesma tela de [Contatos](../cadastros/contatos.md), com o papel **Fornecedor** já marcado — e depois pede o que é específico do fornecedor. Assim ninguém é cadastrado duas vezes.
* **Só com a permissão do financeiro**, abre a folha **Novo fornecedor**, enxuta de propósito:

| Campo | Obrigatório | Para que serve |
| --- | --- | --- |
| **Nome do fornecedor** | Sim | Como ele aparece nas despesas e nos relatórios |
| **Celular** | Não | Ter o contato à mão quando precisar cobrar uma nota |
| **CPF/CNPJ** | Não | Identificar sem ambiguidade — e é campo de busca |
| **Que serviços ele presta?** | Não | O vínculo que faz a sugestão de categoria funcionar |
| **Categoria** e **Matriz de Kraljic** | Não | Veja [A categoria do fornecedor](#categoria) |
| **Contato vinculado** | Não | Liga a ficha a um contato da agenda |

Também dá para criar um fornecedor **de dentro de uma despesa**: no lançamento, em *Para quem você paga?*, toque em **Outro** — a busca acha quem já existe ou cadastra um novo, sem perder o que você já preencheu.

## Os serviços que o fornecedor presta

São seis, os mesmos do plano de contas: **Frete**, **Mão de obra**, **Montagem**, **Desmontagem**, **Layout** e **Outro**. Marque quantos couberem — uma transportadora presta frete; um prestador que monta e desmonta estrutura marca os dois.

### Por que isso importa

```mermaid
flowchart LR
    F[Fornecedor presta<br/>MONTAGEM] --> D[Despesa dele<br/>no razao]
    D --> S[Categoria de MONTAGEM<br/>vem sugerida]
    S --> R[Relatorio compara:<br/>gasto x cobrado em montagem]
```

Ao escolher esse fornecedor numa despesa, se você **ainda não escolheu categoria**, o LocFlow sugere a categoria do mesmo serviço e avisa que foi sugestão — *"Categoria sugerida: Montagem de terceiros. Pelo serviço que este fornecedor presta. Troque se não for o caso."*

Duas garantias que valem saber:

* A sugestão **nunca sobrescreve** uma categoria que você já escolheu.
* Ela é sempre **visível e reversível** — a categoria continua sua para trocar.

{% hint style="info" %}
**Fornecedor sem serviço marcado funciona** — ele só não sugere nada. A lista mostra isso na própria linha: *"Sem serviço vinculado — a despesa não vai sugerir a conta"*. É um convite, não um erro.
{% endhint %}

## A categoria do fornecedor {#categoria}

Cada fornecedor pode ganhar uma **categoria**, pela natureza do que ele fornece:

| Categoria | O que é |
| --- | --- |
| **Direto** | Participa da entrega ao cliente; se falhar, a operação para |
| **Indireto** | Sustenta a empresa sem aparecer para o cliente: telefonia, dados, energia, escritório |
| **Estratégico** | Difícil de substituir ou com tecnologia exclusiva; pesa no longo prazo |
| **Sem categoria** | Ninguém classificou ainda — fica em **âmbar**, visível, esperando você |

Para classificar, toque no fornecedor e use **Categorizar**. **Tudo é opcional**: nada bloqueia um pagamento por falta de categoria. Mas "Sem categoria" fica à vista e é filtrável — é a sua fila de trabalho.

{% hint style="info" %}
**Categorizar quem ainda não tem ficha cria a ficha.** Um contato com papel Fornecedor ou uma transportadora parceira ainda não tem ficha no financeiro. Ao categorizá-lo, a ficha nasce na hora — *"Cria a ficha deste fornecedor no financeiro"* — e a linha muda sem você recarregar a tela.
{% endhint %}

### Matriz de Kraljic (opcional)

Para quem quer ir além da categoria, a seção retraída **Matriz de Kraljic (opcional)** posiciona o fornecedor em dois eixos:

* **Impacto financeiro** — *quanto pesa no que você gasta?* (Baixo ou Alto);
* **Risco de abastecimento** — *é difícil substituir?* (Baixo ou Alto).

Com os dois escolhidos, o LocFlow mostra o **quadrante**:

| Quadrante | Quando |
| --- | --- |
| **Rotineiro** | Baixo impacto e fácil de substituir: papelaria, linhas extras |
| **Gargalo** | Baixo impacto, mas difícil de substituir: o serviço que valida o CPF no cadastro |
| **Alavancado** | Alto impacto e fácil de substituir: computadores da equipe, muitas opções no mercado |
| **Estratégico** | Alto impacto e difícil de substituir: o fornecedor direto do seu serviço principal |

## O que a tela mostra

No topo, **quatro cartões** — **Direto**, **Indireto**, **Estratégico** e **Sem categoria** —, cada um com quantos fornecedores tem. Tocar num cartão filtra a lista por ele (e dá para marcar mais de um). O número de **Sem categoria** é o que você quer ver cair.

Abaixo, uma linha por fornecedor:

* o **nome**, o selo da **categoria** e, quando é o caso, **Presta frete** e **Arquivado**;
* a **origem** (quando não é uma ficha do financeiro) e o **contato** (celular e documento);
* os **chips dos serviços**, cada um com o seu ícone;
* à direita, **quanto já saiu** para aquele fornecedor — e, nas transportadoras, o frete já pago e o frete a pagar.

Em telas largas, a lista vira uma tabela com as colunas Fornecedor, Categoria, Serviços, Origem, Contato, Situação, Já pago e Frete a pagar.

**Busca** por nome, CPF/CNPJ ou celular; três recortes — **Ativos**, **Inativos** e **Todos** —; e filtros por **Categoria**, **Onde está cadastrado**, **Serviço que presta** e **Quadrante de Kraljic**.

{% hint style="info" %}
**Quem entra pelo cadastro base não vê o caixa.** Sem a permissão do financeiro, os valores pagos não aparecem — nem como "R$ 0", que afirmaria algo falso —, e o celular e o documento das fichas também ficam ocultos.
{% endhint %}

## As ações de um fornecedor

Toque na linha para abrir as ações. Aparecem as que fazem sentido para aquele cadastro e para o seu acesso:

| Ação | O que faz |
| --- | --- |
| **Categorizar** | Escolhe a categoria e a posição na Matriz de Kraljic |
| **Editar ficha** | Corrige nome, telefone, documento e serviços da ficha do financeiro. Deixar um campo em branco **limpa** aquele campo |
| **Serviços e frete em Parceiros** | Abre o cadastro de parceria da transportadora |
| **Ver contato** | Abre o contato na agenda |
| **Arquivar** / **Reativar** | *Sai do seletor de despesas novas; o histórico fica* |
| **Cancelar em Parceiros** | *Deixa de ser oferecido em novos serviços e sai do pool de frete.* O histórico é preservado, e a ficha do financeiro continua |

{% hint style="info" %}
**Renomear vale para todo o histórico.** O fornecedor é o mesmo, com outro nome — as despesas antigas passam a exibir o nome novo. Se o que você quer é um fornecedor **diferente**, cadastre um novo.
{% endhint %}

## Arquivar em vez de excluir

**Arquivar** é a "exclusão" do módulo — e preserva o passado:

* o fornecedor sai do seletor de uma **despesa nova**;
* ele continua **nomeando as despesas já lançadas**, e os relatórios de meses anteriores não mudam;
* a linha fica esmaecida com o selo **Arquivado**.

Não há confirmação, porque é reversível ali mesmo: filtre por **Inativos** e use **Reativar**.

## Fornecedor de frete: na mesma lista

As **transportadoras** que você contrata para executar frete — as que aparecem na distribuição de frete de um pedido, com frota e regra de preço próprias — estão **nesta mesma lista**, com a origem *Parceiros → Fornecedores* e o selo **Presta frete**. O que é próprio delas (os serviços do catálogo, a frota, o preço do frete) se configura em **Serviços e frete em Parceiros**, descrito em [Fornecedores de frete](../parcerias/fornecedores-de-frete.md).

{% hint style="info" %}
Quando um pedido com transportadora é reservado, o custo dela já entra sozinho como **conta a pagar**, sem você lançar nada — e aparece, na linha dela, como **frete a pagar**.
{% endhint %}

## Por porte

| Porte | O que cadastrar |
| --- | --- |
| **Autônomo / MEI** | Os cinco ou seis que se repetem todo mês: posto, telefonia, contador, oficina. |
| **Médio** | Todos, com os **serviços** marcados — é o que faz o relatório por serviço ficar honesto. |
| **Grande** | Todos, com CPF/CNPJ e **categoria**. Revise o cartão **Sem categoria** de tempo em tempo e use a Matriz de Kraljic para os que pesam: fornecedor estratégico sem plano B é risco de operação. |

## Situações reais

* **"Sempre erro a categoria da gasolina."** Cadastre o posto como fornecedor e marque o serviço de **frete**. Na próxima despesa, escolha o posto e a categoria vem sugerida.
* **"Troquei de oficina."** Arquive a antiga: ela sai das próximas escolhas e continua nomeando os consertos do ano passado.
* **"Quero saber quanto gastei com aquele prestador."** A coluna da direita, na linha dele, mostra o total já pago. Para o recorte por período, use o insight **por fornecedor** em [Relatórios](relatorios.md).
* **"Cadastrei 'Posto' e 'Posto Shell' por engano."** Arquive o duplicado e siga usando um só. As despesas antigas continuam onde estão.
* **"O fornecedor que eu cadastrei nos Contatos não aparece no financeiro."** Ele aparece nesta lista com a origem *Contatos*. Categorize-o: a ficha do financeiro nasce na hora.

## Próximo passo

* Para lançar uma despesa com fornecedor, veículo e forma de pagamento: [Lançamentos](lancamentos.md#registrar-um-lancamento).
* Para preparar as categorias que os serviços apontam: [Categorias e plano de contas](categorias-e-plano-de-contas.md).
* Para ver o gasto por fornecedor no período: [Relatórios: como ler](relatorios.md).
