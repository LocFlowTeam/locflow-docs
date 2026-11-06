---
icon: list-check
description: As listas do LocFlow com os nomes que a sua empresa usa — tipos de serviço, tipos de local e motivos de perda e de cancelamento, sem perder o histórico nem as regras.
---

# Campos Personalizados

Toda locadora tem o seu jeito de falar. Uma chama de **Buffet** o que o sistema chama de *Espaço de eventos*. Outra cobra **Instalação elétrica** como serviço próprio e nunca usa *Layout*. Em **Campos Personalizados** você adapta as listas do LocFlow a isso: cria opções com os nomes da sua empresa e tira da frente o que não faz parte do seu negócio.

A tela fica em **Ajustes › Regras e modelos › Campos Personalizados**. O que você muda ali vale para toda a sua empresa.

## As listas que você pode personalizar {#listas}

A tela tem três abas, e cada lista diz onde ela aparece:

| Aba | Lista | Onde aparece |
| --- | --- | --- |
| **Serviços** | Tipos de serviço | No cadastro de fornecedores e nos acréscimos do orçamento |
| **Locais e Logística** | Tipos de local | No endereço do cliente, na entrega e na retirada do orçamento e nos endereços salvos |
| **Operação / Outros** | Motivos de perda | Ao marcar um orçamento como perdido |
| **Operação / Outros** | Motivos de cancelamento | Ao cancelar um pedido já fechado |

{% hint style="info" %}
**O que continua como está:** os endereços de galpão, loja e parceiro mantêm os tipos de local padrão, e as categorias financeiras continuam com os serviços padrão.
{% endhint %}

## Adicionar uma opção {#adicionar}

1. Abra a aba da lista e toque em **Adicionar opção**.
2. Em **Nome**, escreva como a sua equipe chama essa opção, com 3 a 60 caracteres.
3. Em **Funciona como**, escolha qual opção padrão ela segue. Os motivos de perda não perguntam isso.
4. Toque em **Adicionar**.

A opção nova entra depois das padrão, em ordem alfabética, e passa a aparecer nos formulários.

{% hint style="warning" %}
**Dois nomes iguais na mesma lista não dá,** mesmo com acento ou maiúsculas diferentes. Se o nome é de uma opção que você desativou, o app avisa para reativá-la em vez de criar outra. Em listas diferentes o mesmo nome é aceito: *Chuva* pode ser motivo de perda e de cancelamento.
{% endhint %}

## Funciona como: o nome é seu, a regra continua a mesma {#funciona-como}

O nome é o que a sua equipe lê. A regra vem da opção padrão que ele segue, então criar uma opção nunca muda como o sistema calcula ou confere as coisas.

| Lista | O que **Funciona como** define | Exemplo |
| --- | --- | --- |
| **Tipos de local** | As regras do endereço. Um local que segue **Condomínio** também pede o complemento | *Buffet* funciona como **Espaço de eventos** |
| **Tipos de serviço** | Em qual serviço ele entra no relatório de margem e qual categoria é sugerida na despesa | *Instalação elétrica* funciona como **Mão de obra** |
| **Motivos de cancelamento** | De quem foi a iniciativa. O que parte do cliente não pesa contra você na Rede | *Chuva no dia do evento* funciona como **Desistência do evento** |
| **Motivos de perda** | Nada, por isso a pergunta não aparece: o motivo só aparece na ficha e nos relatórios | *Mudou de ideia* |

Nos motivos de cancelamento, contam como iniciativa do cliente: **Desistência do evento**, **Mudança de data**, **Preço**, **Foi para um concorrente** e **Inadimplência**.

{% hint style="warning" %}
**Frete não aparece em Funciona como.** Só o **Frete** padrão libera a frota do fornecedor e o motor de frete, então nenhum serviço novo faz esse papel. Para um fornecedor cotar transporte, marque o Frete no cadastro dele. Veja [Fornecedores de frete](../parcerias/fornecedores-de-frete.md#servicos).
{% endhint %}

## Mudar o nome de uma opção {#mudar-o-nome}

Toque no lápis de uma opção que você criou. Enquanto nenhum registro usa a opção, o nome muda à vontade.

Quando ela já está em uso, o app recusa e explica o caminho:

> *"Esta opção está em 3 registros, que guardam o nome atual. Para usar outro nome, crie uma opção nova e desative esta."*

Isso acontece porque os cadastros e orçamentos antigos guardam o nome escolhido naquele momento. Trocar só na lista separaria os dois. O que a opção segue pode mudar a qualquer momento, desde que o nome fique igual.

## Desativar e excluir {#desativar-e-excluir}

| Ação | Onde fica | Sem uso | Em uso |
| --- | --- | --- | --- |
| **Desativar** | O interruptor, em qualquer opção | Sai da lista na hora | O app diz em quantos cadastros ou orçamentos ela está e pede confirmação |
| **Excluir** | A lixeira, só nas opções que você criou | O app confirma: *"Ninguém usa esta opção ainda. Ela sai da lista de vez."* | Não exclui: oferece desativar |

{% hint style="success" %}
**O histórico não se perde.** Ao desativar uma opção em uso, ela sai da lista para os próximos registros, e o que já foi gravado continua mostrando o mesmo nome. Quem abre um registro antigo ainda vê a opção dele ali.
{% endhint %}

Alguns detalhes:

* **Para trazer de volta,** ligue o interruptor. Uma opção desativada fica na lista com a etiqueta **Desativada**.
* **As opções padrão** levam a etiqueta **Padrão do Sistema**. Você pode desativá-las, mas não renomear nem excluir.
* **Uma lista nunca fica vazia.** A última opção ativa não pode ser desativada: ative outra antes. Nos tipos de serviço, o Frete não conta para isso, porque o acréscimo do orçamento não o oferece.
* **Um endereço novo começa no primeiro tipo ativo.** É **Residencial**, enquanto ele estiver ativo.

## O atalho no próprio campo {#atalho}

Não precisa sair do que está fazendo. Quem tem a permissão vê **+ Gerenciar tipos** ou **+ Gerenciar motivos** junto do campo:

* no endereço do cliente, da entrega, da retirada e nos endereços salvos;
* no cadastro de fornecedores;
* no acréscimo do orçamento;
* ao marcar como perdido ou cancelar um pedido.

O atalho abre a mesma lista por cima do formulário. Ao fechar, você volta ao que estava preenchendo, com a opção nova já na lista.

## Quem pode mudar as listas {#quem-pode}

| Quem | O que acontece |
| --- | --- |
| **O dono** e o **Administrador** | Têm a permissão, junto com o resto da gestão |
| **Os outros papéis prontos** | Não têm. Escolhem as opções nos formulários, mas não veem a tela nem o atalho |
| **Um papel personalizado** | Só tem se você incluir a permissão **Campos personalizados** nele |

Para ajustar um papel, veja [Colaboradores e acessos](colaboradores-e-acessos.md).

## Por porte {#por-porte}

| Se você é… | Como costuma usar |
| --- | --- |
| **Autônomo / micro** | Desative o que nunca usa, e as listas ficam mais curtas na hora de preencher. |
| **Médio** | Crie os serviços e os tipos de local com os nomes que a equipe já fala, escolhendo bem o que cada um segue. |
| **Grande** | Combine os nomes antes de criar e deixe a permissão com poucas pessoas: a mudança vale para a empresa inteira, e um nome em uso não muda depois. |

## Situações reais {#situacoes-reais}

* **"Aqui a gente fala buffet."** Você cria o tipo de local *Buffet*, que funciona como **Espaço de eventos**. A equipe passa a escolher pelo nome de sempre.
* **O serviço que não estava na lista.** Você cobra *Instalação elétrica* e cria o serviço seguindo **Mão de obra**. Ele aparece no fornecedor e no acréscimo, e o relatório de margem o conta como mão de obra.
* **O motivo que ninguém usa.** *Evento incompatível* nunca foi escolhido na sua empresa. Você desativa, e a lista fica mais curta para quem encerra um pedido.
* **Criou com o nome errado.** Se ninguém usou, é só corrigir no lápis. Se já está em uso, crie a opção certa e desative a antiga.

## Próximo passo {#proximo-passo}

* Veja como o tipo do local aparece no pedido em [Endereços e endereços salvos](../orcamentos/enderecos.md#tipo-do-local).
* Para lançar os serviços no preço, veja [Valores: acréscimos, frete e descontos](../orcamentos/valores.md#campos-do-acrescimo).
* Para os serviços do fornecedor, veja [Fornecedores](../financeiro/fornecedores.md).
* Para os motivos de encerramento, veja [Perda e cancelamento](../orcamentos/acompanhando-e-fechando.md#perda-e-cancelamento-com-motivo).
