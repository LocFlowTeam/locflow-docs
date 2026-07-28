---
icon: people-arrows
description: Você mexeu num pedido que já tinha sido repassado — e agora? Delta por delta: quem é avisado, quem ajusta a rota, o que acontece com o repasse e o que você não pode mais fazer.
---

# O pedido já estava com um parceiro

**Onde fica:** o estado do repasse aparece na linha **"Repasse a parceiro"** das ações do orçamento e no detalhe em **Rede de Parceiros › Reservas em parceria**. É lá que você acompanha o efeito de qualquer mudança feita no pedido.

A pergunta que esta página responde é literal:

> *"Eu fui lá no orçamento e mudei alguma coisa — só que eu já tinha passado isso pro sistema de parceria. E daí, o que que vai acontecer?"*

A resposta curta: **depende do que você mudou**, e em nenhum caso a mudança fica em silêncio. A resposta longa é o resto da página.

{% hint style="warning" %}
**Leia isto antes de editar.** Repassar não é "pedir um favor": é passar uma **linha de responsabilidade** a outra empresa, que já reservou material, alocou motorista e montou rota em cima do que você mandou. Quando o pedido muda, o combinado dos dois lados muda junto — e algumas mudanças **devolvem a decisão ao parceiro**.
{% endhint %}

## O que muda de dono quando você repassa {#o-que-muda-de-dono}

O acordo divide a operação em **linhas de responsabilidade**:

| Linha | De quem é | O que inclui |
| --- | --- | --- |
| **Logística** | **Parceiro** (interno ou externo) | Entregar, retirar, cuidar do material — e **o plano de movimentos**: como a carga se divide em viagens, em que rota entra, em que ordem. |
| **Comercial e cobrança** | **Você (vendedor)** | O cliente é seu, o orçamento é seu, a fatura é sua, o preço é seu. |

**Parceiro interno e externo têm a mesma responsabilidade** — os dois roteirizam, os dois executam. O que muda entre eles é **capacidade** (mapa, créditos, verificação de presença), nunca responsabilidade.

## Quatro coisas que você deixa de poder fazer {#o-que-voce-nao-faz-mais}

Depois que o parceiro assume, o LocFlow **barra o vendedor** nos atos que reescreveriam o plano que o parceiro está executando:

* **dividir** um movimento em viagens;
* **consolidar** viagens de volta num movimento só;
* **reatribuir** uma viagem a outra rota;
* **concluir a entrega ou a retirada** avançando o status logístico à mão.

A mensagem é explícita: *"Este movimento pertence a um orçamento repassado a «parceiro» — o parceiro cuida da logística dele, inclusive do plano de movimentos."*

{% hint style="info" %}
**Por que isso é bom para você.** O caminho de maior estrago era justamente o antigo: o vendedor marcava "entregue" pelo painel enquanto o motorista do parceiro ainda estava na rua — e "entregue" não volta atrás. Agora quem fecha o movimento é quem esteve na porta do cliente.
{% endhint %}

E o que você **continua** podendo fazer: editar o pedido, mudar datas, itens, endereço, frete, cancelar, reverter o ganho, acompanhar tudo pelo detalhe da reserva. A linha comercial continua inteira nas suas mãos.

## Quem recebe o aviso {#quem-recebe-o-aviso}

Numa operação da sua própria equipe, quem é avisado de uma mudança é o **seu operador logístico**. Numa operação **repassada e viva**, não: o aviso vai ao **lado logístico** — o parceiro externo ou a organização parceira — e a sua central **fica de fora**.

Não é esquecimento; é a regra: **avisa-se quem pode ajustar o plano.** O roteiro é do parceiro (na parceria interna, ele nem existe na sua conta) — mandar o alerta para a sua central seria um aviso sem ação possível.

| Aviso | Quem recebe | Quando |
| --- | --- | --- |
| **"A operação repassada mudou"** | O parceiro logístico (ou toda a organização parceira) | Mudou data, horário, endereço, itens ou quem desloca. |
| **"O frete de uma operação repassada mudou"** | O mesmo | Você mexeu no frete cobrado do cliente. |
| **"Repasse cancelado"** | O mesmo | Você cancelou ou reverteu o pedido e o repasse dele morreu. |

{% hint style="success" %}
**O parceiro é avisado mesmo quando ainda não há roteiro.** A janela entre "ele aceitou" e "ele montou a rota" é exatamente aquela em que o vendedor mexe no pedido. Se o aviso dependesse de existir um roteiro para ficar desatualizado, ele descobriria a mudança na porta do cliente — com a data velha, o endereço velho e a carga velha.
{% endhint %}

## Mudar a data, o horário ou o endereço {#data-e-endereco}

O efeito é o mesmo de sempre, só que do outro lado: o movimento ganha uma versão nova, **o roteiro do parceiro fica desatualizado** e as paradas afetadas ficam **bloqueadas** para a equipe dele até que ele ajuste a rota.

**O que você precisa fazer:** nada além de salvar a edição — e, se a mudança for grande ou em cima da hora, **avisar o parceiro por fora também**. O sistema entrega o alerta; a conversa continua sendo sua.

{% hint style="warning" %}
**Editar um endereço SALVO atinge pedidos repassados também.** Se o destino do pedido é um endereço salvo e alguém corrige esse endereço no cadastro (ou arrasta o pino dele), o destino muda para todos os pedidos ganhos que apontam para ali — inclusive os que já estão nas mãos de um parceiro, inclusive os que já têm rota montada. Veja [Editar um endereço salvo depois](../orcamentos/enderecos.md#editar-endereco-salvo).
{% endhint %}

## Mudar os itens devolve a decisão ao parceiro {#itens-revogam-o-aval}

Este é o efeito mais caro — e o mais invisível, se você não souber que ele existe.

O parceiro aceitou **aquele** pedido: 100 cadeiras, aquela janela, aquele valor de repasse. Se você muda para 60 (ou para 140), **o que ele aceitou deixou de existir**. Então:

* a operação **volta ao estado "aguardando a decisão do parceiro"**, agora com o pedido real na tela dele;
* **ele continua cuidando da entrega enquanto decide** — a posse operacional não fica no limbo;
* **o pagamento segura** até o novo aval: nenhum valor novo é reconhecido enquanto a decisão está aberta;
* se ele **recusar**, a operação volta para você — possivelmente em cima da hora, e a rota que ele havia montado é desfeita.

{% hint style="danger" %}
**Nunca "só ajuste rapidinho" os itens de um pedido repassado.** Fale com o parceiro antes. Do lado dele, o pedido volta à mesa de decisão — e uma recusa a dois dias do evento devolve para o seu colo uma operação que você já tinha dado como resolvida.
{% endhint %}

### Duas exceções, de propósito {#excecoes-do-aval}

Há dois casos em que o aval **não** é revogado — e é bom conhecê-los, porque a diferença vai aparecer como conversa entre as partes:

| Situação | O que acontece | Por quê |
| --- | --- | --- |
| **O acordo não está ativado** (foi cancelado, revogado ou está em renegociação) | O aval é mantido; o LocFlow registra a divergência para conciliação. | Não se pede um aval novo contra um acordo que as partes já não estão praticando. |
| **A janela de aceite já fechou** (o marco da operação passou) | O aval é mantido; a diferença vira **acerto entre vocês**. | Revogar aqui **apagaria o direito de quem já executou**: ele não teria como reaceitar, e o trabalho feito ficaria sem pagamento. |

Nos dois casos a regra é a mesma: **o sistema não apaga direito de quem trabalhou**. A diferença entre o combinado e o pedido final vocês acertam conversando.

### Encolher o pedido: o que se reescreve e o que não volta {#encolher-o-pedido}

Reduzir itens de um pedido repassado não é só logística — é dinheiro que já foi reconhecido.

**Exemplo.** Pedido de **R$ 10.000,00** ao cliente, repasse combinado de **R$ 3.000,00**. A entrega aconteceu e o sistema já reconheceu **R$ 3.000,00** ao parceiro. Aí o cliente devolve metade do material e você reduz o pedido: o repasse devido cai para **R$ 1.800,00**.

| O que estava assim | O que acontece |
| --- | --- |
| Fatias de repasse **ainda pendentes** (dinheiro que não andou) | São **canceladas** e regravadas no valor certo, no ponto certo do direito. |
| A **taxa da plataforma** da fatia corrigida | Recalculada respeitando o **teto por orçamento** — a soma das taxas daquele pedido nunca passa dos 8% do valor atual. Veja [O teto por orçamento](../parcerias/dinheiro-da-parceria.md#teto-da-taxa). |
| Repasse **já liquidado**, ou preso numa **quitação PIX em aberto** | **Não é desfeito.** Fica registrado que sobrou valor reconhecido acima do direito. |

{% hint style="warning" %}
**Reduzir um pedido já pago ao parceiro gera uma conversa, não um estorno automático.** O LocFlow não puxa de volta dinheiro que já saiu — nem tenta. Ele acerta o que ainda dá para acertar, deixa registrado o que sobrou, e o acerto do excedente é entre vocês dois. Combine antes de reduzir.
{% endhint %}

## O frete não acompanha o repasse {#frete-congelado}

O frete que o parceiro recebe é um **termo congelado no aval**. Mexer no frete que você cobra do cliente **não mexe nele**.

**Exemplo.** O cliente mudou para um bairro mais distante e você sobe o frete de **R$ 300,00** para **R$ 500,00**. O cliente paga R$ 500,00; a sua fatura sobe. O parceiro continua recebendo exatamente o frete que ele aceitou.

O que o sistema faz é **não deixar isso passar em silêncio**: ele avisa o parceiro de que a viagem foi **reprecificada** e **em que sentido** (subiu ou desceu) — **sem o valor**, porque o preço ao cliente é a sua linha comercial. Um frete que **cai** também avisa: reduzir em silêncio o que ele já aceitou seria tão errado quanto.

{% hint style="info" %}
**Para o novo frete valer entre vocês, é preciso repassar de novo.** Um re-repasse pede um **aval novo** sobre os termos novos — é o único caminho legítimo para mudar o que foi combinado. Sem isso, você acha que "ajustou o frete" e ele acha que vai receber mais: é assim que nasce uma discussão no fim do mês.
{% endhint %}

## Cancelar ou reverter um pedido repassado {#cancelar-repassado}

Valem todas as travas de [Reverter o ganho e cancelar](quando-um-pedido-muda.md#reverter-e-cancelar) — e mais o que é próprio da parceria:

* a **reserva de parceria é encerrada** e o parceiro é avisado;
* os **repasses ainda em aberto são cancelados** — e o que estava no gateway (quitação PIX aberta, cobrança com divisão na fonte) é encerrado antes, para não deixar dinheiro se movendo por uma operação que morreu;
* o parceiro recebe um aviso nominal de **"Repasse cancelado"**, com o valor que saiu dos ganhos dele — porque quem perdeu o dinheiro não fez nada de errado e merece a explicação;
* na parceria interna, o **estoque espelhado** no galpão dele é liberado;
* o **roteiro que ele havia montado** é desfeito (rota já **em campo** não é tocada: o motorista é avisado e o operador resolve à mão).

{% hint style="danger" %}
**Cancelar em cima da hora pode custar a sua reputação na rede.** Se o parceiro **já tinha aceitado** e o cancelamento acontece **fora da janela de desistência** do acordo (padrão: 24 horas antes da operação), **você** leva a penalidade — a mesma régua que pune o parceiro que desiste tarde. A rede só funciona se for justa nos dois sentidos.
{% endhint %}

**Como não ser penalizado injustamente:** ao cancelar, **escolha da lista o motivo que descreve um ato do cliente**, quando for o caso. Hoje são cinco — *desistência do evento*, *mudança de data*, *preço* (o cliente contestou o valor depois de fechar), *achou outro fornecedor* e *inadimplência* —, e qualquer um deles isenta você. Reputação mede **conduta**, não azar: cancelamento causado pelo cliente não conta contra você.

A regra é essa e nada além dela: **isenta o que está na lista e descreve o cliente**. Escrever o motivo à mão, em texto livre, **não** isenta — por mais bem explicado que esteja, o sistema não tem como classificar uma frase. E *"voltar para negociação"*, que nem pede motivo, também não isenta.

{% hint style="warning" %}
**"Voltar para negociação" penaliza por padrão.** Esse caminho não pede motivo nenhum — então o sistema não tem como saber que a culpa foi do cliente. Se o negócio caiu por um ato do cliente, prefira **Cancelar com o motivo certo**.
{% endhint %}

## Renegociar ou encerrar o acordo com uma entrega em curso {#acordo-em-curso}

E se o que mudou não foi o pedido, mas a **relação**?

| O que já foi | O que acontece |
| --- | --- |
| Solicitações que **ainda aguardavam** a decisão do parceiro | São **canceladas automaticamente** — o convite morre com o acordo. Se ele já tinha montado uma rota antes de aceitar, ela é desmontada, e o responsável de cada pedido é avisado de que a operação voltou para ele. |
| Operações que ele **já aceitou** | **Sobrevivem.** Compromisso assumido é compromisso: ele executa ou desiste pelo caminho normal. |
| O **pagamento** dessas operações aceitas | **Continua acontecendo.** Quem manda na liquidação é o **aval da reserva**, não o status vivo do acordo. Ninguém trabalha de graça porque o acordo acabou no meio. |
| **Rota já em campo** | **Preservada**, com aviso ao motorista. |

O que o acordo encerrado **deixa** de fazer é repartir o dinheiro na fonte: dali em diante a obrigação nasce como **saldo a pagar** no razão, que ainda é corrigível — em vez de sair repartida automaticamente no pagamento do cliente.

**Encerrar o vínculo** com uma organização parceira vai um passo além: além de encerrar os acordos entre vocês (nos **dois** sentidos — os que você repassa a ela e os que ela repassa a você), ele **fecha o acesso dela ao que ela ainda não tinha assumido**. Ela mantém a visão apenas das operações que já aceitou; o resto some. Tentar repassar algo novo devolve:

> *"A parceria com esta organização foi encerrada — não é possível repassar operações novas por este acordo. As operações que ela já aceitou seguem valendo."*

Os termos completos estão em [Acordos de parceria](../parcerias/acordos-de-parceria.md#vigencia).

## A ordem importa: roteirize depois de repassar {#ordem-importa}

Um efeito colateral na direção contrária, que você vai encontrar mais cedo ou mais tarde: **certos estados do roteiro impedem o repasse**.

| A tela recusa quando... | Mensagem | O que fazer |
| --- | --- | --- |
| O movimento já está num roteiro que **agrupa pedidos de outros donos** | *"Este orçamento está no roteiro X, que agrupa movimentos de outros donos. Replaneje o roteiro… antes de repassar."* | Tire o movimento daquela rota (ou isole-o num roteiro só dele) e repasse depois. |
| Alguma viagem tem o **frete fixado a outra transportadora** | *"Uma das viagens deste orçamento tem o frete fixado a outra transportadora e não pode ser repassada a este parceiro."* | Refaça o frete sem a fixação (ou com a frota do parceiro) — veja [a composição do frete](../orcamentos/valores.md#composicao-do-frete). |

{% hint style="success" %}
**A regra prática:** se você já sabe que vai repassar, **repasse antes de roteirizar**. Deixa a rota para quem vai rodá-la — que é justamente o parceiro.
{% endhint %}

## E o que o parceiro vê do seu pedido {#o-que-o-parceiro-ve}

Uma dúvida que costuma aparecer junto: *"se eu mudo o pedido, o parceiro passa a ver o quê?"*

Ele vê **a operação dele** — o que entregar, onde, quando, os itens **do acordo** com os preços do acordo, o que ele ganha e o frete dele. E, quando o acordo permite que ele **receba do cliente na porta**, ele também vê **quanto o cliente deve à sua organização** — que é o número que ele cobra, e nunca se confunde com o repasse dele (a tela mostra os dois separados).

O que ele **não** vê: o resto da sua carteira, os seus outros clientes, os seus outros orçamentos, como o seu preço final foi composto (descontos, histórico comercial) e a sua fatura completa quando não há cobrança na rua. Detalhes em [O que o parceiro vê do seu dinheiro](../parcerias/dinheiro-da-parceria.md#o-que-o-parceiro-ve) e em [Cobrança na rua](../parcerias/cobranca-na-rua.md#o-que-ele-ve).

{% hint style="info" %}
**Se o acordo permite cobrança na rua, editar o pedido muda o que ele cobra na porta.** O valor que aparece para ele é o que o cliente deve **agora** — então acrescentar itens depois do aceite aumenta o que ele vai coletar, e reduzir diminui. Vale checar o combinado antes de mexer perto da data. Veja [Cobrança na rua](../parcerias/cobranca-na-rua.md).
{% endhint %}

## Situações reais {#situacoes-reais}

**"Mudei a entrega de sexta para sábado e não avisei ninguém."**
O parceiro recebeu *"A operação repassada mudou"* e o roteiro dele ficou desatualizado — as paradas afetadas travam até ele ajustar. A sua central **não** recebeu nada, porque não é ela que ajusta aquela rota. Ligue para ele assim mesmo: o alerta chega, a antecedência é sua.

**"Reduzi de 100 para 60 cadeiras e o repasse voltou a 'aguardando parceiro'."**
Correto. O que ele aceitou eram 100 cadeiras. Enquanto ele decide, ele continua cuidando da entrega e nenhum valor novo é reconhecido. Se ele aceitar, segue tudo; se recusar, a operação volta para você.

**"Subi o frete e o parceiro reclamou que não recebeu a diferença."**
Ele está certo: o frete dele foi congelado no aceite. Se a viagem ficou mais cara de verdade, o caminho é **repassar de novo** com os termos novos e pedir o aval dele.

**"O cliente desistiu na véspera e eu cancelei — e levei uma penalidade."**
Cancelamento fora da janela de desistência, depois do aceite, penaliza o vendedor por padrão. Se a causa foi o cliente, escolha **um dos motivos que descrevem o cliente** — desistência do evento, mudança de data, preço, achou outro fornecedor ou inadimplência — e aí não há penalidade. Motivo escrito à mão não isenta.

**"Encerrei a parceria e o pedido que ele já tinha aceitado continuou lá."**
É o desenho: compromisso assumido sobrevive, e continua sendo pago. O que morre é o **novo** — repasses novos por aquele acordo, e o acesso dele ao resto.

## Próximo passo {#proximo-passo}

- [Quando um pedido muda depois de fechado](quando-um-pedido-muda.md) — o mesmo assunto na operação da sua própria equipe.
- [Repassando um pedido](../parcerias/repassando-um-pedido.md) — o ciclo do repasse, do envio ao desfecho.
- [O dinheiro da parceria](../parcerias/dinheiro-da-parceria.md) — como o repasse é apurado, pago e cobrado.
- [Acordos de parceria](../parcerias/acordos-de-parceria.md) — os termos que decidem tudo acima.
- [Reputação e boas práticas](../parcerias/reputacao-e-boas-praticas.md) — o que pesa (e o que não pesa) no seu índice.
