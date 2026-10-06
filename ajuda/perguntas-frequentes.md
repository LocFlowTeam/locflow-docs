---
icon: comments
description: Respostas rápidas para as dúvidas mais comuns do dia a dia — orçamento, pré-reserva, separação, pagamento, papéis, créditos, Flo, nota fiscal, segurança e a Rede de Parceiros.
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

É um **acerto comercial** antes de confirmar de vez — útil quando o cliente está quase fechando, por exemplo esperando o sinal. Vale **só para locação** e é opcional. Atenção: a pré-reserva **não bloqueia estoque** — enquanto o pedido está pré-reservado, os itens continuam disponíveis para outros clientes; o bloqueio começa no **Reservado**. Veja os estados no [Glossário](../primeiros-passos/glossario.md), o caminho completo no [Ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md) e os detalhes em [Acompanhando e fechando](../orcamentos/acompanhando-e-fechando.md).

## O que acontece quando um orçamento vence? {#orcamento-vence}

Todo orçamento tem uma **validade** (padrão 7 dias, ajustável no Motor de Orçamento e em cada orçamento). Passado o prazo, ele fica **vencido**: continua no funil onde estava, mas **não avança** — ao tentar reservar, vender ou reabrir, o LocFlow pede para você **renovar a validade** ou **criar um orçamento novo**, porque preços e regras podem ter mudado. Se o cliente não vai voltar, marque como **Perdido**. "Vencido" **não é um novo estado** do catálogo, é uma condição sobre o orçamento. Veja [Quando o orçamento vence](../orcamentos/acompanhando-e-fechando.md#quando-o-orcamento-vence).

## Como o cliente paga pelo link? Preciso configurar algo antes?

Para gerar PIX e boleto e receber na sua conta, é preciso ativar a **integração de pagamento** (via Pagar.me) — um cadastro guiado. Depois disso, todo link de fatura já oferece o pagamento online. Veja [Integrações](../configuracoes/integracoes.md) e [Pagamento online](../cobranca/pagamento-online.md).

## Convidei alguém e o convite expirou. E agora?

Sem problema: o convite tem prazo de validade. Em **Colaboradores → Convites pendentes**, gere um novo link e reenvie. Como o link é a credencial, mande só para a pessoa certa. Detalhes em [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md).

## O que são os créditos e o que consome crédito?

Créditos são a "moeda" do que tem custo por uso:

* recursos de **mapa** — localizar endereço, **traçar a rota** e **otimizar o roteiro**;
* a **emissão de notas fiscais** em produção (as notas de teste não consomem);
* a **Flo** — mensagens, respostas faladas e **conversa por voz** (cobrada por minuto). O custo aparece na própria conversa, e a Flo tem um **limite diário** que renova à meia-noite.

Seu plano inclui uma **franquia mensal**; se acabar, dá para comprar mais (pelo navegador). **No teste grátis**, valem **créditos de cortesia** que não se renovam — e, durante o teste, não dá para comprar mais: o caminho é assinar um plano. Acompanhe o saldo, o extrato e o cartão **Uso da Flo** em [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md#creditos).

## Não consigo concluir a entrega sem a foto. Como resolvo? {#evidencia-obrigatoria}

Se a sua empresa configurou que aquele tipo de movimento **exige comprovação**, o LocFlow não fecha o registro sem ela — nem na rua, nem no lançamento retroativo, nem na loja. Isso é de propósito: a prova de entrega é o que te defende numa discussão com o cliente.

Quando a foto é **impossível** (você está lançando ontem no escritório, o cliente foi embora, o celular falhou), existe a **dispensa de evidência**: você escreve o **motivo** no próprio card daquele atendimento e o registro fecha — com o motivo carimbado junto, para quem for auditar depois.

{% hint style="warning" %}
A dispensa depende de uma **permissão dedicada**, que **motorista e parceiro externo não têm** — eles estão em campo justamente para produzir a prova. Se o botão não aparece para você, é isso: peça a quem faz a retaguarda para lançar, ou fale com quem administra a conta.
{% endhint %}

## Por que não consigo reservar este orçamento? {#nao-consigo-reservar}

Três motivos aparecem com mais frequência:

* **A sua operação exige algo da cobrança antes.** No [Gatilho da reserva](../configuracoes/motores-operacionais.md#gatilho-da-reserva), com **Exigir cobrança gerada** falta gerar a cobrança do orçamento; com **Exigir sinal pago**, o pedido espera em pré-reservado e o pagamento do sinal reserva sozinho.
* **O orçamento venceu.** Fora da validade ele não avança — renove a validade ou crie um novo (veja [acima](#orcamento-vence)).
* **Ele está aguardando aprovação.** Uma política (frete acima do limite, desconto acima do teto) congelou o pedido até o aval de um responsável. Veja [Aprovação de orçamentos](../orcamentos/aprovacao.md).

## Como começo a emitir nota fiscal? {#emitir-nota-fiscal}

Em **Ajustes › Integrações › Integração Fiscal**, um assistente guiado credencia a sua empresa. O caminho tem quatro marcos: **credenciar**, enviar o **certificado digital**, emitir uma **nota de teste** (sem valor fiscal e sem custo) e **ativar a emissão em produção**. Depois disso, cada nota emitida em produção consome créditos. Veja [Integração Fiscal](../configuracoes/integracao-fiscal.md).

## Como ligo a verificação em duas etapas? E como exijo de toda a equipe? {#verificacao-em-duas-etapas}

Para a **sua** conta: em **Minha Conta › Segurança › Verificação em duas etapas**, toque em **Configurar autenticador**, escaneie o QR code num aplicativo autenticador (como o Google Authenticator) e digite o **código de 6 números**.

Para **todo mundo**: quem administra vai em **Ajustes › Empresa e equipe › Perfil da Empresa**, no bloco **Verificação em duas etapas da equipe**, e toca em **Exigir da equipe**. Avise a equipe antes — quem não tiver o aplicativo vai precisar dele na próxima entrada. Veja [Verificação em duas etapas](../configuracoes/verificacao-em-duas-etapas.md).

## Excluí um contato ou um colaborador por engano. Dá para voltar? {#excluido-por-engano}

Dá. Contatos, colaboradores e roteiros excluídos vão para a **Lixeira**, em **Ajustes › Conta e segurança › Lixeira**. Ali, **Restaurar** devolve o item como estava; **Excluir de vez** apaga para sempre. Cada botão depende de uma permissão do seu papel. Veja [Lixeira](../configuracoes/lixeira.md).

## A Flo disse que o limite de hoje acabou. O que eu faço? {#limite-da-flo}

A Flo tem um **limite diário de créditos**, que protege o saldo de um dia fora da curva e **renova à meia-noite** (no fuso da organização). Você tem dois caminhos:

* **Quem administra a conta** toca em **Ajustar limite** e sobe o número — ou tira o limite;
* ou esperar a meia-noite. Quem não administra é orientado a pedir o aumento a quem administra.

Comprar créditos não libera o limite do dia. Se a mensagem falar que os **créditos acabaram** (e não o limite de hoje), aí o problema é o saldo: **Comprar créditos**, pelo navegador — ou, no teste grátis, assinar um plano.

Acompanhe o gasto no cartão **Uso da Flo**. Veja [Conheça a Flo](../flo/conheca-a-flo.md#limite-diario).

## Onde vejo o que está mudando no LocFlow? {#novidades}

No **sino**, na aba **Novidades**: cada melhoria aparece numa trilha de cinco etapas — da fila até **No ar**. Veja [Novidades do LocFlow](novidades-do-sistema.md).

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

**Se o acordo permite cobrança na rua**, o parceiro recebe do cliente na porta **em seu nome** (a fatura e a relação com o cliente continuam suas) e declara o recebimento no app dele. A partir daí passam a existir **duas contas, de sentidos opostos**, sobre o mesmo pedido — uma não substitui a outra:

| Conta | Quem paga a quem |
| --- | --- |
| **A devolução** | **Ele paga a você** o que recebeu do cliente — o valor inteiro da cobrança que ele fechou. |
| **O repasse do acordo** | **Você continua pagando a ele** o que foi combinado, no momento que o acordo combinou — como em qualquer pedido. Receber na porta não adia nem cancela o repasse dele. |

A taxa da plataforma entra **uma vez só** por pedido. Hoje são **dois PIX separados**: ele quita a devolução pelo botão **Quitar via PIX**, e você paga o repasse dele do jeito de sempre. Ele acompanha o que deve em **Repasses a pagar**, no valor *"A pagar à organização"* (em **Meus Ganhos** aparece o aviso de que há valor a repassar); você acompanha em **Financeiro › Repasses**, na seção *"Quem me paga"*.

{% hint style="warning" %}
**A coleta é tudo ou nada.** O parceiro só pode declarar o recebimento se ele **fechar a cobrança inteira** daquele pedido. Recebeu só uma parte? O caminho é o **PIX do vendedor** — que, aliás, é sempre o melhor: o dinheiro cai já repartido, sem sobrar saldo para ninguém acertar depois.
{% endhint %}

**Se o acordo não permite**, o parceiro não consegue registrar esse recebimento — o app dele avisa para mostrar o **PIX do vendedor** ao cliente. Cobrança na rua vale hoje apenas para o **parceiro externo** (o convidado que trabalha dentro da sua conta); na parceria entre duas organizações, quem recebe do cliente continua sendo você.

→ [Cobrança na rua](../parcerias/cobranca-na-rua.md) · [Quando o parceiro recebe do cliente](../parcerias/dinheiro-da-parceria.md#repasse-inverso)

### Encerrei a parceria e o pedido continua com o parceiro. Por quê? {#encerrei-e-o-pedido-continua}

Porque **compromisso assumido é compromisso**. Encerrar a parceria corta o futuro, não o que já foi combinado:

| O que acontece | Ao encerrar |
| --- | --- |
| Os **acordos** entre as duas partes | Cancelados — **nos dois sentidos**, inclusive os em que você era o parceiro dela |
| Repassar um pedido **novo** | Bloqueado, mesmo pelos acordos que estavam ativos |
| Solicitações que só **aguardavam resposta** | Encerradas — a operação volta para você, e o responsável é avisado |
| O que o parceiro **já aceitou** | **Continua valendo** — ele executa e continua sendo pago |
| O acesso dele aos seus dados (roteirização, atendimento na loja, cliente, situação da cobrança) | Cortado, exceto no que ele já assumiu |

Ou seja: o pedido que "continua lá" é um pedido que o parceiro já tinha aceitado antes de você encerrar. Se você quer tirá-lo de fato daquela operação, o caminho é **desfazer aquele repasse** especificamente — e aí valem as regras de desistência do acordo.

→ [Acordos de parceria](../parcerias/acordos-de-parceria.md#vigencia)

### Apareceu que a rota está "desatualizada". O que fazer? {#rota-desatualizada}

Significa que o **pedido mudou depois** de o roteiro ter sido planejado — a data da entrega, os itens, o endereço, quem leva. A parada fica **só de leitura** e trava quem está na rua, de propósito: é melhor parar do que entregar a versão errada do pedido.

Para destravar, alguém precisa **ressincronizar** aquela parada com o pedido atual. Quem faz isso:

* pedido **seu**, roteiro seu → o seu operador de logística;
* pedido **repassado a um parceiro** → **o parceiro**. O plano de movimentos é dele desde o repasse, e por isso a correção também é. Se a mudança foi grande, avise-o.

→ [Quando um pedido muda depois de fechado](../logistica/quando-um-pedido-muda.md) · [O pedido já estava com um parceiro](../logistica/efeitos-na-parceria.md#data-e-endereco)

### Sou o parceiro. Preciso ter frota e galpão cadastrados? {#parceiro-precisa-de-frota}

Se você é o **parceiro convidado por link**: sim, e é rápido. Você cadastra a **sua própria frota** dentro da conta de quem te convidou — tipos de veículo e veículos com placa que são **seus** e só você enxerga — e o **Meu galpão**, que é o endereço de onde as suas viagens partem (é dele que sai o cálculo do frete do repasse). Nada disso se mistura com a frota de quem te convidou.

Se você é uma **organização parceira** (parceria org↔org), o que pesa é o **estoque**: o material sai do **seu** galpão, e sem galpão cadastrado o sistema não reserva nada — o pedido chega marcado como sem cobertura, e quem corrige é você.

→ [Parceiro Logístico Externo](../parcerias/parceiro-logistico-externo.md#minha-logistica) · [Estoque na parceria](../parcerias/estoque-na-parceria.md)
