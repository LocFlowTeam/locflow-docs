---
icon: sliders
description: Configure uma vez as regras da sua operação — frete, orçamento, estoque, logística e cobrança — e o LocFlow segue o padrão sozinho.
---

# Motores operacionais

Um **motor** é uma regra da sua operação que o sistema segue sozinho. Em vez de decidir tudo manualmente a cada locação ou venda, você configura o padrão **uma vez** e o LocFlow aplica daí em diante — calculando o frete, sugerindo datas, reservando os itens, pedindo aprovação quando preciso.

Você encontra todos eles em **Ajustes › Motores**.

{% hint style="info" %}
Pense nos motores como o "piloto automático" da sua operação. Eles não tiram seu controle: você pode sempre ajustar caso a caso dentro de cada orçamento. O motor só define o **ponto de partida** — o que acontece quando ninguém mexe em nada.
{% endhint %}

## Os dois grupos do hub {#os-dois-grupos}

A tela de Motores separa tudo em **dois grupos**, porque eles funcionam de formas diferentes:

| Grupo | O que é | Como se edita |
| --- | --- | --- |
| **Cálculo de preços** | Motores que definem **quanto se cobra** — e que guardam **histórico de versões**. | Você prepara os ajustes, revisa e **publica** uma nova versão. As anteriores ficam registradas. |
| **Regras de operação** | Configuração **única** da operação (estoque, logística, aprovações, reembolso). | Editada direto na tela; vale sempre a configuração atual, sem histórico. |

A diferença existe porque preço é algo sensível: ao mudar como você cobra, é bom ter um **registro do que valia antes** (e poder revisar com calma antes de pôr no ar). Já uma regra de operação — como "exigir fatura antes de entregar" — é um liga-desliga: vale a escolha atual e pronto.

```mermaid
flowchart TB
    HUB[Ajustes › Motores] --> CALC[Cálculo de preços<br/>versionados]
    HUB --> OPER[Regras de operação<br/>configuração única]
    CALC --> FRT[Motor de Frete]
    CALC --> ORC[Motor de Orçamento]
    OPER --> EST[Motor de Estoque]
    OPER --> LOG[Motor de Logística]
    OPER --> OPO[Operação do Orçamento]
    OPER --> OPF[Operação do Frete]
    OPER --> OPC[Operação da Cobrança]
```

---

## Cálculo de preços {#calculo-de-precos}

São os motores **versionados**. Cada um abre com a sua **configuração em vigor** (a que vale hoje), e você pode preparar **ajustes não publicados** e só então **publicar** uma nova versão para toda a empresa. Veja [Versões e publicação](#versoes-e-publicacao).

### Motor de Frete {#motor-de-frete}

Define **como o frete é calculado** quando você usa o cálculo automático no orçamento. Em vez de digitar um valor à mão toda vez, você descreve as suas **cobranças** — situações que você sabe explicar ("para Sorocaba", "no fim de semana", "para entregas longas") com um valor associado ("R$ 500 fixo", "R$ 3 por km", "20% a mais") — e o motor aplica sozinho.

Ao abrir, você escolhe como prefere montar as regras, pelo perfil da sua operação:

| Perfil | Quando usar |
| --- | --- |
| **Tenho um método único de cobrança** | Uma cobrança que vale para todos os fretes. Mais fácil de configurar — é o caminho **mais comum**. |
| **Tenho vários métodos de cobrança** | Várias cobranças combinadas, uma por situação (município, distância, época do ano…). |
| **Quero montar regras manualmente** | Editor avançado, com condições e mais de uma ação por regra. |

> Você pode trocar de perfil depois. O app ainda oferece um **Simulador de frete** para testar cenários hipotéticos com as suas regras — cálculo local, **sem criar orçamentos**.

{% hint style="warning" %}
**O motor cobra por viagem.** O LocFlow calcula o frete sobre uma **Rota Estimada**, como se o veículo saísse do galpão só para aquele orçamento. Uma **viagem** é um movimento (a entrega ou a retirada), com a **ida e a volta contando como uma coisa só**. Um aluguel típico tem **2 viagens** (a entrega e a retirada). Por isso, valores e limites configurados aqui valem **por viagem**: uma cobrança de **R$ 500 fixo** somaria **R$ 1.000** ao frete final (2 × R$ 500). Quer cobrar R$ 500 no total? Configure **R$ 250 por viagem**.
{% endhint %}

Para cada variável numérica (km, kg, minutos…), você decide entre **cobrar por ela** (preço por unidade) ou **usá-la como critério** — cobrar só quando o valor estiver dentro de um mínimo, máximo ou faixa. Exemplo: gatilho "distância" + critério "entre 0 e 50 km" + valor "R$ 100 fixo + R$ 3 por km" = uma cobrança específica para viagens curtas.

> Onde isso aparece no dia a dia: no bloco **Valores** do orçamento, na aba **Frete automático**. Veja [Valores: mão de obra, frete e descontos](../orcamentos/valores.md#frete).

### Motor de Orçamento {#motor-de-orcamento}

Define o **valor mínimo de orçamento** (o "corte"): o total que toda proposta precisa atingir.

> "O corte de orçamento é o valor mínimo que o total do orçamento deve atingir. Se o valor final ficar abaixo desse limite, o sistema avisa o operador e não permite criar o orçamento até que o valor seja ajustado ou o corte revisado."

É uma trava contra propostas baixas demais — útil para padronizar margem quando há vários vendedores. Aqui você edita um único valor e **salva**; o salvamento já publica a nova versão.

{% hint style="info" %}
Não confunda: o **valor mínimo** é versionado e fica neste motor. Já **taxa de serviço, validade e intervalo mínimo logístico** são padrões operacionais (sem histórico) e ficam em **Operação do Orçamento** — há um atalho para eles dentro desta tela.
{% endhint %}

---

## Regras de operação {#regras-de-operacao}

São os motores **operacionais**: configuração única, editada direto na tela. Vale sempre o que estiver salvo.

### Motor de Estoque {#motor-de-estoque}

Define **quando os itens ficam reservados** ao cliente — ou seja, por quanto tempo um item fica indisponível quando entra num orçamento. É o que impede alugar o mesmo item para dois clientes no mesmo período.

São políticas de bloqueio à sua escolha — da mais fiel à mais flexível:

| Política | O que faz |
| --- | --- |
| **Pela entrega e retirada** | O item fica reservado do momento em que sai para a entrega até voltar na retirada. O cálculo mais fiel quando você agenda entrega e coleta. |
| **Apenas o período do evento** | Bloqueia só as datas do evento informadas no orçamento, sem considerar deslocamento. Bom quando o cliente retira e devolve no balcão. |
| **Cada orçamento define** | Não há regra fixa — em cada orçamento você informa o período de bloqueio manualmente. Útil quando cada locação é muito diferente da outra. |
| **Com folga antes e depois** | Bloqueia o período do evento e ainda reserva um tempo extra antes e depois. Use quando precisa de uma margem entre uma locação e a próxima. |

Esse motor tem uma página dedicada, porque ele se cruza com a forma como você **cobra** e **usa** o item. Veja [Duração, cobrança e bloqueio de uso](../orcamentos/duracao-e-bloqueio.md).

### Motor de Logística {#motor-de-logistica}

Define as **regras de entrega, retirada e provas**. Tem quatro blocos:

**Faturamento antes da logística.** O liga-desliga **"Exigir fatura emitida para iniciar a logística"**:

> "Controla se a logística (separar, preparar e enviar os itens) só pode começar depois que uma fatura for gerada para o orçamento. A fatura apenas registra uma cobrança em aberto para o cliente — ela não significa que o cliente já pagou. Para decidir, pergunte-se: você começa a preparar e entregar os itens mesmo sem ter gerado uma fatura de cobrança?"
>
> • Sim, entrego antes de cobrar → deixe desligado.
> • Não, só libero os itens depois de gerar a fatura → deixe ligado.

**Logística interna (galpão).** Define se existem etapas **dentro do galpão**. Vale para orçamentos **futuros**; os já em andamento não mudam.

* **Separação interna** (*A separar → Separado*) — ative se o material é separado/conferido no galpão antes de sair. Desligado, a logística começa direto na entrega/retirada.
* **Conferência na devolução** (*A conferir → Conferido*) — só para aluguel. Ative se, ao voltar, o material passa por conferência antes de finalizar.

> Locadores pequenos, com pouca variedade, costumam deixar as duas **desligadas**: separar e conferir é controle que cabe na cabeça, e ligar só criaria cliques. Conforme cresce, ligue a **Separação** primeiro (organiza o que preparar) e depois a **Conferência** (controle da volta, com provas). Veja [Separação no galpão](../logistica/separacao.md) e [Conferência na devolução](../logistica/conferencia.md).

**Requisitos de evidência.** O que a equipe precisa registrar **antes de concluir** cada entrega e retirada — separadamente. Cada item marcado vira **obrigatório**: o app não deixa concluir sem registrar. **Nada marcado = conclui com 1 toque**, sem prova. As provas vão da mais simples (foto e vídeo) à mais forte (código confirmado no WhatsApp do cliente, identificação de quem recebeu, localização confirmada). Comece com foto e vídeo; conforme os itens ficam mais caros, some provas mais fortes. Aqui você também define, em conjunto, a **prova exigida no balcão** — separadamente para a **retirada pelo cliente** e a **devolução pelo cliente** no galpão; é a mesma lógica, aplicada ao atendimento presencial em vez da rota. Veja [Balcão: retirada e devolução no galpão](../logistica/balcao.md).

**Agendamento padrão.** Uma sugestão de datas ao criar um orçamento: ao informar a data do evento, a entrega e a retirada são preenchidas automaticamente (e podem ser ajustadas). Você diz quantos dias **antes** do evento é a entrega e quantos dias **depois** é a retirada. Deixe em branco para não sugerir.

**Forma de operação.** Diz como a sua locadora costuma operar — e deixa o app já no formato dela:

* **Mista** *(padrão)* — você decide pedido a pedido. O menu mostra Roteirização e [Balcão](../logistica/balcao.md); ao criar um orçamento, os botões "Cliente retira / devolve no galpão" ficam livres. É o comportamento de sempre.
* **Só balcão** — o cliente sempre retira e devolve no galpão. O orçamento já nasce assim e a **Roteirização** some do menu. Comum em quem trabalha de portas abertas.
* **Só rota** — a equipe sempre entrega e retira. O **Balcão** some do menu.

> A ocultação é só para simplificar: a permissão continua a mesma, e o que sumiu volta na hora em que você troca a forma. E nada bloqueia a exceção — quando um pedido fugir do padrão, abra **"Operação avançada"** na seção de movimentos do orçamento e ajuste à mão.

### Operação do Orçamento {#operacao-do-orcamento}

Parâmetros padrão usados ao montar orçamentos — políticas internas, sem histórico:

* **Taxa de serviço** — um valor de referência que agiliza a criação. "Orçamentos com taxa diferente da configurada aqui ainda podem ser criados normalmente."
* **Validade do orçamento** — por quantos dias, a partir da criação, o orçamento permanece reservado. "Preços e políticas mudam com frequência; a validade evita orçamentos com regras antigas." É um padrão — o operador pode mudar em cada orçamento.
* **Pré-reserva** — no aluguel, a [pré-reserva](../painel/funil-de-vendas.md) é uma etapa **opcional** entre "Em negociação" e "Reservado" (segurar antes de confirmar). Aqui você decide se ela entra no seu funil: **Conforme o porte** (segue a sugestão — locador pequeno costuma não usar, médio/grande usa), **Ligada** ou **Desligada** (fixo, independente do porte). Desligada, o funil vai direto de negociação para reservado e a etapa some das telas; orçamentos que já estão pré-reservados continuam valendo.
* **Intervalo mínimo logístico** — toda entrega e retirada ocorre dentro de um intervalo de horários (não dá para garantir chegada no minuto exato). Este campo define a folga mínima entre o início e o fim de cada movimento. Se algum movimento ficar abaixo dela, o sistema alerta o operador, que precisa consentir com o risco para prosseguir.

### Operação do Frete {#operacao-do-frete}

Define **como o frete é aprovado e distribuído** — políticas internas que valem sobre o **valor final** do frete, independentemente de como ele foi calculado (o **cálculo** fica no Motor de Frete). A tela tem **três blocos**:

#### 1. Detentor da política {#operacao-frete-detentor}

Antes de tudo, você escolhe **de quem** é a política que está editando. No LocFlow, o frete pode ser da **própria organização** (você mesmo entrega) ou de um **fornecedor de frete** — uma transportadora parceira cadastrada, com a sua própria frota e o seu próprio cálculo. Cada um desses **detentores** tem a sua política de aprovação, e você as edita uma de cada vez, trocando o detentor aqui no topo.

{% hint style="info" %}
O seletor de detentor só aparece quando você tem **fornecedores de frete cadastrados** (e permissão + plano para isso). Sem fornecedores, a tela edita direto a política da **sua organização** — que é o caso mais comum. Para entender o frete por fornecedor, veja [Frete por fornecedor: o detentor da política](motor-de-frete-detentor.md).
{% endhint %}

#### 2. Aprovação do frete {#operacao-frete-aprovacao}

Diz **quando um frete precisa do aval de um responsável** antes do orçamento seguir. A tabela abaixo cobre a política da **própria organização** — os três modos disponíveis quando o detentor é você:

| Modo | O que faz |
| --- | --- |
| **Aprovação automática** *(recomendado)* | Todo frete calculado é aprovado na hora, sem revisão. |
| **Aprovar acima de um valor** | Aprova automaticamente até o limite que você define; acima dele, exige um responsável. |
| **Sempre exigir aprovação** | Todo frete aguarda um responsável com permissão para aprovar. |

**Qual usar?** Locador que entrega ele mesmo → **Automática** (zero atrito). Operação em crescimento → **Por valor** (controla só os fretes altos). Equipe com vários vendedores → **Sempre manual** (padroniza margem e evita erro de digitação).

Quando o detentor é um **fornecedor de frete**, aparece um **quarto modo**, exclusivo dele:

| Modo | O que faz |
| --- | --- |
| **Aguardar resposta do fornecedor** *(padrão de fornecedor)* | Todo frete deste fornecedor nasce **pendente**, aguardando a confirmação dele antes de seguir. É o padrão seguro — evita fechar um frete terceirizado que ninguém confirmou. |

> Quando um orçamento trava aguardando aprovação, ele vira **Pendente** — uma pré-etapa do funil. Veja [Aprovação de orçamentos](../orcamentos/aprovacao.md).

#### 3. Estratégia de alocação {#operacao-frete-estrategia}

Quando você tem **mais de um detentor de frete** (a sua organização e um ou mais fornecedores), o LocFlow precisa decidir **como distribuir a carga e qual transportadora recomendar**. Este bloco define o padrão — e, por ser uma decisão da organização inteira, ele só aparece na política da **sua organização** (fornecedores não têm estratégia própria).

| Estratégia | O que faz |
| --- | --- |
| **Menor valor ao cliente** *(padrão)* | Recomenda a opção mais barata — a que sai com o menor frete para o cliente. |
| **Melhor aproveitamento** | Recomenda o melhor encaixe da carga no veículo: menos folga e menos viagens. |
| **Montar manualmente** | Sem recomendação automática — você distribui a carga à mão em cada orçamento. |

{% hint style="info" %}
A estratégia é só um **padrão de partida**: em cada orçamento você pode trocar a distribuição na mão, na seção de movimentos.
{% endhint %}

### Operação da Cobrança {#operacao-da-cobranca}

Define o destino **padrão** de um valor a favor do cliente — quando uma edição reduz o total abaixo do que já foi pago, ou quando entra um pagamento a mais:

| Política | O que faz |
| --- | --- |
| **Crédito / vale-locação** *(recomendado)* | O valor vira crédito reaproveitável na próxima locação. Não exige operação bancária. |
| **Reembolso em dinheiro** | O valor é devolvido ao cliente em dinheiro (estorno ou transferência). |

O sistema **aplica esse padrão automaticamente e avisa a equipe**, que pode trocar a forma em cada caso.

---

## Versões e publicação {#versoes-e-publicacao}

Os motores de **Cálculo de preços** guardam histórico. Dentro de cada um você vê duas abas:

* **Em vigor** — a versão que vale hoje para toda a empresa.
* **Ajustes não publicados** — um rascunho onde você prepara mudanças com calma. Ele não afeta ninguém até ser publicado.

Quando estiver pronto, você **publica** — e o app confirma: *"Esta ação irá publicar e tornar a configuração ativa para toda a organização."* A partir daí, a nova versão entra em vigor e a anterior fica registrada no **histórico de versões** (acessível pelo link "Ver histórico de versões"). Se quiser recomeçar do que já está no ar, há a opção **"Descartar e igualar ao publicado"**.

{% hint style="info" %}
No **Motor de Orçamento**, como é um único valor, não há abas: você edita e **salva**, e o salvamento já publica a nova versão em um passo.
{% endhint %}

## Quem pode mexer {#permissoes}

{% hint style="warning" %}
As opções visíveis dependem das **permissões** do seu usuário. Ver, listar e editar motores são permissões distintas — algumas pessoas conseguem **consultar** sem poder **alterar**. Se não encontrar um motor, fale com quem administra a conta. Veja [Colaboradores e acessos](colaboradores-e-acessos.md).
{% endhint %}

Alguns recursos de motor podem estar disponíveis apenas em um **plano superior**. Quando for o caso, o app indica.

## Situações reais {#situacoes-reais}

* **"Meus orçamentos saem com frete errado."** Confira o **Motor de Frete**: lembre que os valores valem **por viagem** (cada movimento, ida e volta), não pelo orçamento inteiro. Use o **Simulador** para testar antes de publicar.
* **"A equipe começou a preparar um pedido que ainda não foi cobrado."** Em **Motor de Logística**, ligue **"Exigir fatura emitida para iniciar a logística"**.
* **"O mesmo item foi reservado para dois clientes."** Revise a política do **Motor de Estoque** — provavelmente está "apenas o período do evento" quando deveria ser "pela entrega e retirada" (ou com folga).
* **"Quero que fretes altos passem por mim antes de fechar."** Em **Operação do Frete**, escolha **Aprovar acima de um valor** e defina o limite.
* **"Um cliente pagou a mais e não sei o que fazer com o troco."** O **Operação da Cobrança** já decide o padrão (crédito ou dinheiro) e avisa a equipe.

## Próximo passo {#proximo-passo}

* [Duração, cobrança e bloqueio de uso](../orcamentos/duracao-e-bloqueio.md) — o Motor de Estoque em detalhe.
* [Valores: mão de obra, frete e descontos](../orcamentos/valores.md) — onde o Motor de Frete aparece no orçamento.
* [Aprovação de orçamentos](../orcamentos/aprovacao.md) — o que acontece quando a Operação do Frete trava um pedido.
* [Frete por fornecedor: o detentor da política](motor-de-frete-detentor.md) — como cada fornecedor de frete tem a sua própria política de aprovação.
* [Separação no galpão](../logistica/separacao.md) e [Conferência na devolução](../logistica/conferencia.md) — as etapas internas que o Motor de Logística liga.
* [Horários e sazonalidades](horarios-e-sazonalidades.md) — os horários comerciais que o cálculo de frete e o agendamento respeitam.
