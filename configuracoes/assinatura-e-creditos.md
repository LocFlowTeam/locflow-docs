---
icon: coins
description: Seu plano, o ciclo de cobrança e o status; o direito de arrependimento; e os créditos — o que consome e o que é grátis.
---

# Minha assinatura e créditos

Em **Minha assinatura** você acompanha duas coisas separadas, em abas diferentes da mesma tela:

* **Plano & faturas** — o seu **contrato com o LocFlow**: em que plano você está, o ciclo de cobrança e o status.
* **Créditos** — a sua **carteira**, usada por serviços externos do app, como mapas e a Flo.

São coisas distintas. Mexer numa não mexe na outra.

{% hint style="info" %}
A **assinatura do LocFlow** (o que você paga *para usar o sistema*) não tem nada a ver com as cobranças que **você emite para os seus clientes** por locação ou venda. Para receber dos seus clientes, veja [Pagamento online](../cobranca/pagamento-online.md).
{% endhint %}

## A assinatura é comprada na web {#assinatura-na-web}

Pelas regras das lojas de aplicativos (Google Play e App Store), **comprar, trocar de plano e comprar créditos só acontece no navegador**, no painel web do LocFlow. No celular essas telas são **apenas para acompanhar** — você vê plano, status, faturas e saldo, mas a compra em si é feita na web.

{% hint style="warning" %}
No app, ao tentar uma ação de compra você verá um aviso explicando isso. No Android aparece o botão **"Gerenciar no painel web"** (que leva à área da sua conta). No iPhone, a mensagem é mais neutra e orienta falar com o administrador da conta. Em qualquer caso: **abra o navegador para comprar ou trocar de plano.**
{% endhint %}

## Plano & faturas {#plano-e-faturas}

É o seu contrato com o LocFlow. Aqui você vê o plano, o **ciclo de cobrança** (mensal ou anual) e o **status** atual.

### Os planos por nível {#planos-por-nivel}

O LocFlow tem planos de diferentes **níveis** — do mais enxuto, para quem está começando, aos mais completos, para operações maiores. Quanto maior o nível, mais limites de uso e mais recursos liberados (alguns recursos premium, como o [Domínio personalizado](dominio-personalizado.md), só aparecem a partir de certo plano).

{% hint style="info" %}
A escolha de qual plano cabe na sua operação é assunto da página de planos no site. Aqui na ajuda a gente só explica **como funciona** a tela — sem nomes nem valores, que mudam com o tempo.
{% endhint %}

### O status do contrato {#status-do-contrato}

O selo ao lado do plano mostra em que pé está a sua assinatura:

| Status | O que significa |
| --- | --- |
| **Em teste** | Período gratuito para experimentar. **Sem cobrança** até o teste acabar. |
| **Ativo** | Contrato em vigor, cobrado a cada ciclo. Tudo certo. |
| **Pagamento pendente** | Falta concluir o pagamento para o plano começar a valer. |
| **Em carência** | Houve um problema com o pagamento; atualize o método para não perder acesso. |
| **Inadimplente** | Há fatura em atraso. Quite para destravar o plano e voltar ao normal. |
| **Cancelado** | A cobrança recorrente foi encerrada. Dá para **reativar** quando quiser. |

### Período de teste (trial) {#periodo-de-teste}

Durante o teste você usa o LocFlow à vontade, **sem nenhuma cobrança**. Em **Meu contrato**, a tela mostra quantos dias faltam e até quando o teste vai — por exemplo, *"Faltam 12 dias de teste grátis · até 20/10/2026"* — e a data da **Próxima cobrança**. Depois que o teste vira plano pago, essa linha passa a dizer **Próxima renovação**.

{% hint style="info" %}
Em **Meus limites**, o teste aparece como **"Sem cobrança agora"**: *"Você está em teste grátis: não há nada a pagar por enquanto. A LocFlow cobre os custos até o teste terminar — use o plano com calma. Quando o teste acabar, passam a valer os valores do contrato."*
{% endhint %}

{% hint style="warning" %}
**No teste, os créditos são de cortesia.** A carteira começa com uma quantidade de **créditos de cortesia** que **não se renova** — e, durante o teste, não dá para comprar mais. Assinar um plano libera a franquia mensal completa e a compra de créditos. Veja [Sua carteira e o saldo](#carteira-e-saldo).
{% endhint %}

### Faturas, limites e troca de plano {#faturas-e-limites}

Ainda na aba **Plano & faturas**, conforme a permissão do seu usuário, você encontra:

* **Meu contrato** — plano, status, ciclo e datas do período.
* **Minhas faturas** — histórico, vencimentos e pagamento das faturas do LocFlow.
* **Meus limites** — o uso do mês contra as cotas do seu plano (mês a mês).
* **Editar contrato** — trocar de plano (sempre na web). Com faturas em aberto, a troca fica bloqueada até a quitação.
* **Zona de perigo** — o **cancelamento** do contrato.

{% hint style="info" %}
**Cancelar o contrato** encerra a cobrança recorrente na hora, mas a sua organização e os perfis continuam no LocFlow — é só **reativar** quando quiser voltar a operar.
{% endhint %}

### Direito de arrependimento (7 dias) {#arrependimento-cdc}

Se você acabou de assinar e mudou de ideia, o **Código de Defesa do Consumidor** garante o **arrependimento em até 7 dias**. Na seção **Meu contrato**, em *"Reembolso por arrependimento"*, o LocFlow consulta se você ainda está no prazo e mostra:

* o **valor estimado do reembolso integral** da cobrança inicial;
* **quantos dias faltam** para encerrar o prazo e a data final.

Ao solicitar, a cobrança inicial é **estornada por inteiro**, a assinatura é encerrada e o contrato fica cancelado. O estorno em si segue os prazos do seu **banco / operadora do cartão**.

{% hint style="info" %}
A entrada é discreta e só consulta o prazo quando você toca nela. Se o prazo já passou (ou não se aplica), a própria tela explica o motivo.
{% endhint %}

## Créditos {#creditos}

Alguns recursos que usam **serviços externos** consomem **créditos** — por exemplo, mapas, a assistente Flo e a emissão de notas fiscais. Os créditos cobrem o custo desses serviços. Seu plano já vem com uma **franquia mensal**; se precisar de mais, você compra (na web).

```mermaid
flowchart LR
    F[Franquia do mês<br/>inclusa no plano] --> S[Saldo da carteira]
    C[Créditos comprados] --> S
    S --> M[Recursos de mapa]
    S --> I[Assistente Flo]
    S --> N[Notas fiscais<br/>em produção]
```

### O que consome crédito {#o-que-consome}

O consumo acontece quando o LocFlow precisa chamar um serviço externo. O app sinaliza essas ações
antes ou mostra o custo logo depois.

| Ação | Consome? |
| --- | --- |
| Calcular o **endereço no mapa** (geocodificação) de um galpão ou no cálculo de frete | Sim |
| **Traçar a rota** real do roteiro | Sim |
| **Otimizar a rota** (melhor ordem das paradas) — cobra **por parada** | Sim |
| Mostrar o pino no cadastro / no onboarding | **Não** (é gratuito) |
| Enviar uma mensagem ou responder às perguntas da **Flo** | Sim — o custo varia e aparece na conversa |
| Gerar a resposta falada da Flo em **Ouvir** | Pode consumir — o app avisa antes |
| **Conversar por voz** com a Flo (no navegador) | Sim — cobrada **por minuto**, com o tempo e o custo à vista na tela |
| Abrir a tela sugerida, revisar ou salvar sem enviar nova mensagem à Flo | **Não gera um novo turno da Flo** |
| Emitir uma **nota fiscal em produção** pela [Integração Fiscal](integracao-fiscal.md#creditos) | Sim — por nota emitida |
| Emitir uma nota de **teste** (homologação) | **Não** |

{% hint style="info" %}
Recursos que consomem crédito ficam **sinalizados na própria tela**, para você não ser pego de surpresa. Na Flo, cada resposta mostra o custo abaixo da mensagem, e **Ouvir** avisa quando precisa gerar um áudio. Cálculos e resultados são **reaproveitados** quando possível, evitando cobrar de novo pela mesma coisa.
{% endhint %}

### Sua carteira e o saldo {#carteira-e-saldo}

A aba **Créditos** mostra a sua carteira com o **saldo total disponível**, separado em:

* **Franquia do mês** — quanto ainda resta da franquia inclusa no plano (ex.: *"80 de 200"*). Durante o teste grátis, esta linha se chama **Créditos do teste grátis** e mostra os créditos de cortesia.
* **Comprados** — créditos que você comprou e que não expiram com o mês.

O consumo gasta primeiro o que faz sentido para o seu saldo; a franquia **renova no próximo ciclo**. Saldos grandes aparecem de forma compacta (ex.: *"12,3 K"*), para você ler sem uma parede de números.

O saldo atualiza **em tempo real**: assim que um recurso consome, o **Extrato** registra.

{% hint style="info" %}
**No teste grátis**, no lugar da compra aparece o aviso: *"Durante o teste grátis, sua organização conta com N créditos de cortesia — quando acabarem, eles não se renovam. Assine um plano para liberar a franquia mensal completa e a compra de créditos."*
{% endhint %}

### Uso da Flo {#uso-da-flo}

Logo abaixo do saldo, o cartão **Uso da Flo** responde à pergunta seguinte: *quanto a Flo gastou?*

* **Hoje** — quantos créditos a Flo usou de **meia-noite a meia-noite** (no fuso da organização) contra o **limite diário** — por exemplo, *"40 de 100 hoje"*. Perto do fim, a barra avisa; quando acaba, a Flo para até a meia-noite: *"O limite de hoje acabou. A Flo volta à meia-noite."* Entram na conta as mensagens, as respostas faladas e as conversas por voz.
* **No mês** — quanto a Flo usou no mês e quanto resta na sua carteira.
* **Ajustar limite** *(para quem administra)* — **Do plano**, **Personalizado** ou **Sem limite**.
* **Ver por pessoa** — o uso de cada pessoa; quem pode, libera ali quem ficou sem conversas por voz.

O limite diário existe para proteger o saldo de um dia fora da curva — ele não impede o uso normal. O cartão só aparece para quem tem acesso ao uso. Mais sobre a Flo em [Conheça a Flo](../flo/conheca-a-flo.md).

### Comprar créditos {#comprar-creditos}

Comprar créditos é feito **na web** (lembra do aviso lá em cima). Quando você compra, escolhe entre:

* **Avulso** — paga só pelo que precisa, ajustando a quantidade.
* **Pacotes** — leve mais por menos; quanto maior o pacote, maior a **economia** (aparece um selo de desconto).

{% hint style="info" %}
A compra depende de **permissão** (gerenciar o contrato). No app, em vez dos botões de compra, aparece o aviso para concluir no painel web.
{% endhint %}

### Extrato {#extrato}

No **Extrato** você confere cada movimentação, com data e descrição:

* **Entradas** (verde, com `+`) — compras e a renovação da franquia do mês.
* **Saídas** (com `−`) — cada consumo de mapa, da Flo ou de nota fiscal. As mensagens e respostas faladas aparecem como **Assistente Flo**; a chamada de voz, como **Conversa por voz com a Flo**; e cada nota emitida em produção, como **Emissão de nota fiscal**.

Achou um gasto estranho? O Extrato mostra exatamente **o que consumiu, quando e quanto**.

{% hint style="success" %}
**Por que isso vale a pena:** a **otimização de rota** acerta a melhor ordem das paradas e o traçado real. Numa operação com várias entregas no dia, isso é menos quilômetro rodado, menos combustível e mais entregas por motorista — um consumo pequeno de crédito que se paga rápido.
{% endhint %}

## Situações reais {#situacoes-reais}

* **Vou testar antes de pagar.** Durante o teste, use à vontade — sem cobrança. Ao final, escolha o plano (no navegador, pela página **Plano & faturas**).
* **Os créditos do teste acabaram.** Os créditos de cortesia não se renovam e, no teste, não dá para comprar mais: assine um plano para liberar a franquia mensal e a compra.
* **A Flo parou de responder no meio da tarde.** Provavelmente o **limite diário** da Flo acabou. Veja o cartão **Uso da Flo** na aba Créditos: quem administra pode ajustar o limite; senão, a Flo volta à meia-noite.
* **Me arrependi logo depois de assinar.** Dentro de 7 dias, abra *"Reembolso por arrependimento"* em **Meu contrato**: a tela mostra o prazo e o valor do estorno integral.
* **Acabou a franquia no fim do mês.** Fez muitas otimizações de rota ou usou bastante a Flo e a franquia acabou? Compre créditos (na web) e siga operando; a franquia renova no próximo ciclo.
* **Estou no celular e quero trocar de plano.** No app é só acompanhar. Abra o **painel web** no navegador para trocar de plano ou comprar créditos.
* **Conferir um consumo.** Abra o **Extrato** — cada linha mostra o que consumiu, quando e quanto.

## Próximo passo {#proximo-passo}

* Use bem os créditos de rota em [Planejando o roteiro](../logistica/planejando-o-roteiro.md).
* Veja como conversar, revisar sugestões e controlar custos em [Conheça a Flo](../flo/conheca-a-flo.md).
* Veja os recursos premium ligados ao plano em [Domínio personalizado](dominio-personalizado.md).
* Para receber dos seus clientes (que é outra coisa), veja [Pagamento online](../cobranca/pagamento-online.md).
* Em dúvida? Veja [onde tirar dúvidas](../primeiros-passos/onde-tirar-duvidas.md).
