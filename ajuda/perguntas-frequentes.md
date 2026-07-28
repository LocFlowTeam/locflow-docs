---
icon: comments
description: Respostas rápidas para as dúvidas mais comuns do dia a dia — orçamento, pré-reserva, separação, pagamento, papéis, créditos e a Rede de Parceiros.
---

# Perguntas frequentes

Respostas rápidas para as dúvidas mais comuns. Não achou a sua? Veja [onde tirar dúvidas](../primeiros-passos/onde-tirar-duvidas.md).

## Posso editar um orçamento depois de ganho?

Sim. O LocFlow reflete a mudança na fatura e na logística automaticamente — desde que a operação não tenha avançado demais. Itens já entregues não podem mais ser alterados; nesses casos, o recomendado é criar um novo orçamento.

## O que acontece com um valor a favor do cliente?

Ele é resolvido pela **política de cobrança** da sua locadora: vira **crédito/vale-locação** ou **reembolso em dinheiro**. Você define o padrão em [Motores operacionais](../configuracoes/motores-operacionais.md) e pode ajustar caso a caso.

## Como recebo pagamento online?

Gere o **link de pagamento** na fatura ou na parcela e envie ao cliente. A baixa é automática assim que o pagamento é confirmado. Veja [Pagamento online](../cobranca/pagamento-online.md).

## Por que não vejo uma tela ou um botão?

A maioria das telas depende das **permissões** do seu usuário. Se algo não aparece, provavelmente seu perfil não tem acesso àquele recurso — peça a quem administra a conta. Entenda o modelo em [Papéis, funções e competências](../conceitos/papeis-funcoes-competencias.md).

## Como adiciono pessoas à minha equipe?

Você convida por um **link**, e esse link já é a credencial — não pedimos senha. Marque um ou mais **papéis prontos** (Administrador, Motorista, Separador, Conferente…) e mande o link.

O **e-mail é opcional** e muda duas coisas quando você o preenche: o LocFlow **envia o convite por e-mail sozinho**, e só quem entrar com **aquela** conta consegue aceitar — o link deixa de servir para qualquer um. Deixou em branco? Você mesmo envia, e quem tiver o link aceita. Veja [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md).

## Os estados do orçamento são fixos? Posso usar nomes próprios?

Os estados são **um catálogo oficial** do LocFlow (Em aberto, Em negociação, Pré-reservado, Reservado, Vendido, Perdido, Cancelado, Finalizado) — eles não são renomeados, justamente para a operação inteira falar a mesma língua. Consulte o que cada um significa no [Glossário](../primeiros-passos/glossario.md).

## Preciso separar e conferir o material no galpão?

Não. **Separação** (na ida) e **conferência** (na volta) são **opcionais**: locadores pequenos costumam deixar as duas desligadas e ligar conforme a operação cresce. Você decide em [Motores operacionais](../configuracoes/motores-operacionais.md). Quando ligadas, veja [Separação no galpão](../logistica/separacao.md) e [Conferência na devolução](../logistica/conferencia.md).

## O que é "pré-reservar" um orçamento?

É **segurar** um aluguel antes de confirmar de vez — útil quando o cliente está quase fechando e você não quer que o item seja prometido a outra pessoa. Vale **só para locação** e é opcional. Veja os estados no [Glossário](../primeiros-passos/glossario.md) e o caminho completo no [Ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md).

## O que acontece quando um orçamento vence?

Todo orçamento tem uma **validade** (padrão 7 dias, ajustável no Motor de Orçamento e em cada orçamento). Passado o prazo, ele fica **vencido**: continua no funil onde estava, mas **não avança** — ao tentar reservar, vender ou reabrir, o LocFlow pede para você **renovar a validade** ou **criar um orçamento novo**, porque preços e regras podem ter mudado. Se o cliente não vai voltar, marque como **Perdido**. "Vencido" **não é um novo estado** do catálogo, é uma condição sobre o orçamento. Veja [Quando o orçamento vence](../orcamentos/acompanhando-e-fechando.md#quando-o-orcamento-vence).

## Como o cliente paga pelo link? Preciso configurar algo antes?

Para gerar PIX e boleto e receber na sua conta, é preciso ativar a **integração de pagamento** (via Pagar.me) — um cadastro guiado. Depois disso, todo link de fatura já oferece o pagamento online. Veja [Integrações](../configuracoes/integracoes.md) e [Pagamento online](../cobranca/pagamento-online.md).

## Convidei alguém e o convite expirou. E agora?

Sem problema: o convite tem prazo de validade. Em **Colaboradores → Convites pendentes**, gere um novo link e reenvie. Como o link é a credencial, mande só para a pessoa certa. Detalhes em [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md).

## O que são os créditos e o que consome crédito?

Créditos cobrem recursos que usam **mapas do Google** — como calcular endereço, **traçar a rota** e **otimizar o roteiro**. Seu plano inclui uma **franquia mensal**; se acabar, dá para comprar mais. Acompanhe o saldo e o extrato em [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md).

## Não consigo concluir a entrega sem a foto. Como resolvo? {#evidencia-obrigatoria}

Se a sua empresa configurou que aquele tipo de movimento **exige comprovação**, o LocFlow não fecha o registro sem ela — nem na rua, nem no lançamento retroativo, nem no balcão. Isso é de propósito: a prova de entrega é o que te defende numa discussão com o cliente.

Quando a foto é **impossível** (você está lançando ontem no escritório, o cliente foi embora, o celular falhou), existe a **dispensa de evidência**: você escreve o **motivo** no próprio card daquele atendimento e o registro fecha — com o motivo carimbado junto, para quem for auditar depois.

{% hint style="warning" %}
A dispensa depende de uma **permissão dedicada**, que **motorista e parceiro externo não têm** — eles estão em campo justamente para produzir a prova. Se o botão não aparece para você, é isso: peça a quem faz a retaguarda para lançar, ou fale com quem administra a conta.
{% endhint %}

## Rede de Parceiros {#rede-de-parceiros}

As dúvidas que mais aparecem quando você começa a repassar pedidos — ou a executar para quem vende. A seção completa começa em [Rede de Parceiros: a visão](../parcerias/visao-geral.md).

### O parceiro vê os meus preços? {#parceiro-ve-meus-precos}

**Vê o preço ao cliente dos itens que estão no acordo.** Não é um vazamento: é o que sustenta o combinado. Se o acordo diz "você recebe 70% do valor", sem o valor a frase não significa nada, e ninguém aceita trabalhar assim. Esse número aparece dos dois lados desde a proposta, inclusive no link do convite, antes de o parceiro sequer ter conta.

Junto com o preço, ele vê **a divisão da taxa da plataforma daquele acordo** — a fatia que fica com ele e a que fica com você, uma ao lado da outra. Pelo mesmo motivo: a taxa sai do bolso de alguém, e quem assina precisa saber de qual. O que fica fora da vista dele é **quanto a plataforma faturou em reais na operação inteira** e o que ela ganha nos acordos que não são o dele.

O que ele **não** vê:

* os seus **outros clientes** e os seus **outros orçamentos** — só existe para ele o que você repassou;
* **como o preço final foi montado**: descontos aplicados, histórico comercial, negociação;
* a sua **carteira de cobranças** — as faturas dos seus outros pedidos e o seu **link de pagamento** fora daquele orçamento.

Sobre a cobrança do pedido repassado, o recorte é mais fino do que "vê" ou "não vê", e depende de o acordo permitir [cobrança na rua](#cliente-pagou-ao-parceiro):

* **Sem cobrança na rua**, ele recebe só um sinal simples: *Pago* ou *Cobrança em aberto — com o vendedor* (e *cancelada*, quando for o caso). Sem valores, sem parcelas. É o mínimo para não entregar em cima de uma pendência sem saber.
* **Com cobrança na rua ligada** — e só depois de ele aceitar o repasse —, ele vê **quanto o cliente deve** daquele pedido e pode **gerar o PIX da parcela** para mostrar na porta. O PIX é o **seu**: o dinheiro cai na sua conta, como se o cliente tivesse pago pelo link.

{% hint style="info" %}
Um jeito curto de guardar: ele enxerga **o negócio que está fazendo com você** — inteiro, para poder decidir. Ele não enxerga **o seu negócio**.
{% endhint %}

### Por que não consigo mais mexer no roteiro que repassei? {#nao-consigo-mexer-no-roteiro}

Porque a **linha logística** passou a ser dele. Ao repassar um pedido, você entrega a execução inteira: montar o roteiro, **dividir** uma entrega em duas, **juntar** paradas, **remarcar** quem leva e **ressincronizar** uma parada que ficou desatualizada. Se você ainda pudesse reescrever esse plano, estaria mudando por baixo o roteiro que o parceiro já está rodando — foi exatamente o que passou a ser bloqueado.

O que **continua seu**: o cliente, o orçamento, o preço, a fatura e as etapas que acontecem **no seu galpão** (separar o material, por exemplo).

Isso vale para os **dois níveis** de parceria — o parceiro convidado por link e a organização parceira. Precisa mudar alguma coisa na entrega? Fale com o parceiro, ou desfaça o repasse e assuma a operação.

{% hint style="warning" %}
Pelo mesmo motivo, **avançar o status "na mão"** até *Entregue* ou *Retirado* deixou de ser possível num pedido repassado: aquele atalho fechava de uma vez todas as paradas pendentes — inclusive as que o roteiro do parceiro estava executando naquele momento, sem volta.
{% endhint %}

→ [O pedido já estava com um parceiro](../logistica/efeitos-na-parceria.md#o-que-voce-nao-faz-mais) · [Repassando um pedido](../parcerias/repassando-um-pedido.md#execucao)

### Repassei duas vezes o mesmo pedido. Paguei a taxa duas vezes? {#taxa-duas-vezes}

**Não.** A taxa da plataforma tem **teto por orçamento**: o cliente pagou uma vez, a plataforma cobra uma vez — não uma por intermediário.

Na prática, numa venda de **R$ 1.000** com taxa de 8%:

| Situação | Taxa total da plataforma |
| --- | --- |
| Você repassa ao parceiro A e ele executa | R$ 80 |
| O parceiro A não vai, você repassa ao B, que executa | **R$ 80** (não R$ 160) |

O que **não** tem teto por orçamento é o **direito de cada parceiro**: se o segundo fez o serviço inteiro, ele recebe o combinado dele por inteiro — quem executou tem direito ao que combinou.

{% hint style="info" %}
A taxa incide sobre o **total da operação** (itens + mão de obra + frete − descontos) e **só sobre o que o cliente pagou de verdade**. Cliente que pagou metade gera taxa sobre metade.
{% endhint %}

→ [O dinheiro da parceria](../parcerias/dinheiro-da-parceria.md#taxa-de-plataforma)

### O cliente pagou na mão do parceiro. E agora? {#cliente-pagou-ao-parceiro}

Depende do que o acordo combinou.

**Se o acordo permite cobrança na rua**, o parceiro é o **coletor** daquele pedido: ele recebe do cliente na porta em seu nome (a fatura e a relação com o cliente continuam suas) e declara o recebimento no app dele. A partir daí a conta **vira do avesso** — em vez de você dever a ele, **ele deve a você** a sua margem mais a taxa da plataforma, e quita por PIX. Ele acompanha isso em **Meus Ganhos**, no cartão *"A pagar à organização"*; você, em **Financeiro › Repasses**, como valor a receber daquele parceiro.

{% hint style="warning" %}
**A coleta é tudo ou nada.** O parceiro só pode declarar o recebimento se ele **fechar a cobrança inteira** daquele pedido. Recebeu só uma parte? O caminho é o **PIX do vendedor** — que, aliás, é sempre o melhor: o dinheiro cai já repartido, sem sobrar saldo para ninguém acertar depois.
{% endhint %}

**Se o acordo não permite**, o parceiro não consegue registrar esse recebimento — o app dele avisa para mostrar o **PIX do vendedor** ao cliente. Cobrança na rua vale hoje apenas para o **parceiro externo** (o convidado que trabalha dentro da sua conta); na parceria entre duas organizações, quem recebe do cliente continua sendo você.

→ [Cobrança na rua](../parcerias/cobranca-na-rua.md) · [O parceiro recebeu do cliente?](../parcerias/dinheiro-da-parceria.md#parceiro-recebeu-na-entrega)

### Encerrei a parceria e o pedido continua com o parceiro. Por quê? {#encerrei-e-o-pedido-continua}

Porque **compromisso assumido é compromisso**. Encerrar a parceria corta o futuro, não o que já foi combinado:

| O que acontece | Ao encerrar |
| --- | --- |
| Os **acordos** entre as duas partes | Cancelados — **nos dois sentidos**, inclusive os em que você era o parceiro dela |
| Repassar um pedido **novo** | Bloqueado, mesmo pelos acordos que estavam ativos |
| Solicitações que só **aguardavam resposta** | Encerradas — a operação volta para você, e o responsável é avisado |
| O que o parceiro **já aceitou** | **Continua valendo** — ele executa e continua sendo pago |
| O acesso dele aos seus dados (roteirização, balcão, cliente, situação da cobrança) | Cortado, exceto no que ele já assumiu |

Ou seja: o pedido que "continua lá" é um pedido que o parceiro já tinha aceitado antes de você encerrar. Se você quer tirá-lo de fato daquela operação, o caminho é **desfazer aquele repasse** especificamente — e aí valem as regras de desistência do acordo.

→ [Acordos de parceria](../parcerias/acordos-de-parceria.md#vigencia)

### Apareceu que a rota está "desatualizada". O que fazer? {#rota-desatualizada}

Significa que o **pedido mudou depois** de o roteiro ter sido planejado — a data da entrega, os itens, o endereço, quem leva. A parada fica **só de leitura** e trava quem está na rua, de propósito: é melhor parar do que entregar a versão errada do pedido.

Para destravar, alguém precisa **ressincronizar** aquela parada com o pedido atual. Quem faz isso:

* pedido **seu**, roteiro seu → o seu operador de logística;
* pedido **repassado a um parceiro** → **o parceiro**. O plano de movimentos é dele desde o repasse, e por isso a correção também é. Se a mudança foi grande, avise-o.

→ [Quando um pedido muda depois de fechado](../logistica/quando-um-pedido-muda.md) · [O pedido já estava com um parceiro](../logistica/efeitos-na-parceria.md#data-e-endereco)

### Sou o parceiro. Preciso ter frota e galpão cadastrados? {#parceiro-precisa-de-frota}

Se você é o **parceiro convidado por link**: sim, e é rápido. Você cadastra a **sua própria frota** dentro da conta de quem te convidou — especificações e veículos com placa que são **seus** e só você enxerga — e o **Meu galpão**, que é o endereço de onde as suas viagens partem (é dele que sai o cálculo do frete do repasse). Nada disso se mistura com a frota de quem te convidou.

Se você é uma **organização parceira** (parceria org↔org), o que pesa é o **estoque**: o material sai do **seu** galpão, e sem galpão cadastrado o sistema não reserva nada — o pedido chega marcado como sem cobertura, e quem corrige é você.

→ [Parceiro Logístico Externo](../parcerias/parceiro-logistico-externo.md#minha-logistica) · [Estoque na parceria](../parcerias/estoque-na-parceria.md)
