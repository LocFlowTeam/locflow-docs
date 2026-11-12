---
icon: building
description: De quem é o tipo de veículo — da sua empresa ou de um fornecedor de frete — e o que isso muda no frete, nos grupos e ao trocar o titular.
---

# Titular do tipo

Todo [tipo de veículo](frota-ficha-tecnica.md) tem um **titular**: de quem é aquele veículo.

- Quase sempre o titular é a **sua empresa** — o tipo descreve um veículo seu.
- Quando você contrata frete de terceiros, pode cadastrar o tipo do veículo **do fornecedor**. Aí o titular é ele — e **o preço daquela viagem sai do motor de frete dele**, não do seu.

{% hint style="info" %}
**Antes, "detentor".** O titular é o que o LocFlow chamava de detentor da especificação. É o mesmo dado.
{% endhint %}

## Onde o campo aparece {#onde-aparece}

O titular fica no bloco **Identificação** do cadastro do tipo, no campo **Titular do tipo**. As opções são **Sua empresa** (o padrão) e os seus **fornecedores de frete** — só os que você marcou como transportadores.

Ao **criar** um tipo, o campo **só aparece** quando:

- o seu plano e as suas permissões liberam o **frete por fornecedor** (recurso do plano Pro); e
- existe pelo menos um fornecedor de frete cadastrado.

Fora disso, o campo não aparece e o tipo nasce da sua empresa. Na **edição**, o titular é sempre mostrado — mas só quem tem esse acesso consegue trocá-lo.

## A frota-espelho do fornecedor {#frota-espelho}

Os tipos de um fornecedor formam a **frota-espelho** dele: você espelha, dentro do LocFlow, os veículos que aquele parceiro usa para te atender. Assim, na hora de cotar o frete no orçamento e de planejar um roteiro com frete terceirizado, o sistema sabe qual veículo do fornecedor está em jogo, com que capacidade — e o frete sai do motor de frete dele. Na lista de tipos, o cartão de um tipo de fornecedor exibe um **selo com o nome do fornecedor**, para você distinguir num relance o que é seu do que é terceirizado.

Como cadastrar o fornecedor e montar a frota-espelho: [Fornecedores de frete](../parcerias/fornecedores-de-frete.md). Como o motor de frete dele calcula: [Motor de Frete por detentor](../configuracoes/motor-de-frete-detentor.md).

## O titular e o grupo {#titular-e-grupo}

O [grupo](frota-grupos.md) de um tipo precisa ser do **mesmo titular**. Por isso, no cadastro do tipo, a busca de grupos só mostra os grupos do titular escolhido — tipo de fornecedor pede grupo do fornecedor —, e um grupo criado ali mesmo já nasce dele. Você não mistura frota própria com frota de um fornecedor no mesmo grupo.

## Trocar o titular {#trocar}

Na **edição** de um tipo, com o acesso certo, dá para trocar o titular escolhendo outro no campo **Titular do tipo**:

- a troca é feita **na hora**: o tipo **e todos os veículos dele** passam para o novo titular, e o app confirma quantos mudaram (*"2 veículos passam a pertencer a …"*);
- a troca fica **bloqueada** enquanto um preço de frete **ativo** usar esse tipo — o app recusa e diz o motivo.

{% hint style="warning" %}
**Depois de trocar, confira o grupo.** Como o grupo precisa ser do mesmo titular, a busca de grupos passa a mostrar os do titular novo. Se o tipo mudou de dono, escolha (ou crie) um grupo dele.
{% endhint %}

## Situações reais {#situacoes-reais}

- **O caminhão do transportador parceiro:** você contrata a Transportes Silva para as entregas grandes. Cadastra o tipo "Truck Silva" com o titular **Transportes Silva**, num grupo dela. No orçamento, quando a viagem é cotada num grupo dela, o frete daquela viagem sai do motor de frete da Silva.
- **O veículo que você comprou do fornecedor:** o caminhão que era da Silva agora é seu. Na edição do tipo, você troca o titular para **Sua empresa** — o tipo e os veículos dele passam para a sua frota — e escolhe um grupo seu.

## Próximo passo {#proximo-passo}

Volte para [Frota](frota.md) para a visão geral, ou veja [Grupos da frota](frota-grupos.md) e [Fornecedores de frete](../parcerias/fornecedores-de-frete.md).
