---
icon: truck
description: Transportadoras terceiras sem login — o conceito de detentor, a frota-espelho, o motor de frete do fornecedor e o encaixe na composição do frete.
---

# Fornecedores de frete

Um dia a entrega é longe demais, ou chega mais carga do que a sua frota dá conta. Em vez de recusar o pedido, você aciona uma **transportadora parceira** para fazer o transporte. No LocFlow, essas transportadoras são os seus **fornecedores de frete**: terceiros que você cadastra, precifica e usa dentro dos orçamentos — como se fossem uma extensão da sua operação.

**Onde fica:** menu da organização → **Cadastros Base** → **Fornecedores**, junto de Contatos, Catálogo e Orçamentos. Ele mora ali por um motivo simples: o fornecedor é um **cadastro** de terceiro que a sua operação usa — como um contato ou um produto —, e não uma operação independente. Por isso não fica no espaço da [Rede de Parceiros](visao-geral.md), que é para parcerias entre empresas que se conectam de verdade.

## Uma tela só para todos os fornecedores {#tela-unica}

**Fornecedores** é a tela única de quem presta serviço ou fornece para a sua operação. Ela lista, juntos, os fornecedores criados no **financeiro** (nos lançamentos), os **contatos com o papel Fornecedor** e as **transportadoras de frete** — cada um dizendo de onde veio. A busca encontra por nome, CPF/CNPJ ou celular, e o recorte **Ativos · Inativos · Todos** muda o que aparece.

Cada fornecedor pode ganhar uma **categoria**, pela natureza do que ele fornece:

| Categoria | O que significa |
| --- | --- |
| **Direto** | Participa da entrega ao cliente. |
| **Indireto** | Suporte e infraestrutura da operação. |
| **Estratégico** | Difícil de substituir. |

Opcionalmente, você também marca a posição dele na **Matriz de Kraljic** (o impacto financeiro × o risco de ficar sem ele), que dá o quadrante: **Rotineiro**, **Gargalo**, **Alavancado** ou **Estratégico**. Tudo é opcional: **"Sem categoria"** é um estado visível e filtrável, e nada disso bloqueia pagamento. Os quatro cartões no topo contam os fornecedores por categoria e filtram com um toque — o de **"Sem categoria"** é a sua fila de trabalho.

{% hint style="info" %}
**Quem vê a tela, e o que é do plano Pro.** A tela aparece para quem tem a permissão do cadastro de fornecedores **ou** a do financeiro. O que é recurso do plano **Pro** é o cadastro do fornecedor em **Parceiros**: os serviços que ele presta (entre eles o **Frete**), a frota-espelho e o motor de frete dele — tudo o que esta página explica daqui para baixo. Sem ele, a tela continua listando e categorizando as fichas do financeiro. Se você não vê o campo **Detentor** na sua [frota](../cadastros/frota.md), é porque o seu plano ainda não o inclui, não é um erro. Para liberar, veja [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md).
{% endhint %}

{% hint style="info" %}
**Não achou o item no menu?** Em organizações que fizeram o cadastro inicial mais recente, **Fornecedores** começa guardado e aparece sozinho quando você cadastra o primeiro fornecedor — ou quando você o traz de volta em **Personalizar**, no menu.
{% endhint %}

## Onde isso se encaixa {#onde-se-encaixa}

O fornecedor de frete é o jeito **mais simples** de trabalhar com um transporte de fora — e é bem diferente de uma parceria de verdade. Vale entender o quadro antes de mergulhar nos detalhes.

Aqui, o fornecedor é um terceiro que **você gerencia por inteiro**. Você cadastra a empresa dele, monta a **frota** dele dentro do sistema, configura o **motor de frete** dele — e ele **não tem login**. Quem opera tudo é você. Por isso ele vive nos **Cadastros Base**: é uma ficha que a sua operação consulta, não uma operação independente que decide alguma coisa.

{% hint style="info" %}
**Quer um parceiro de verdade, com conta própria?** Isso existe — e é outra coisa. Na [Rede de Parceiros](visao-geral.md) você convida um **parceiro logístico externo** (com acesso próprio, que aceita e executa os pedidos que você repassa) ou conecta a sua organização a **outra organização LocFlow** (parceria org ↔ org, com acordos, divisão automática de ganhos e reputação). O fornecedor de frete continua sendo a escolha certa quando você só quer **cotar e pagar um transporte**, sem envolver a outra parte no sistema.
{% endhint %}

## O conceito de detentor {#detentor}

Este é o conceito que amarra tudo. No LocFlow, **cada tipo de veículo da frota, cada motor de frete e cada composição de frete tem um titular** — o que chamamos de **detentor**. E o detentor só pode ser uma de duas coisas:

| Detentor | O que significa |
| --- | --- |
| **Própria organização** | O padrão. O tipo de veículo, o motor e a cobrança são **seus** — a sua frota, as suas regras de preço. |
| **Fornecedor de frete** | O titular é um **terceiro cadastrado**. O tipo de veículo representa um veículo *dele*, e o preço vem do motor de frete *dele*. |

Pense no detentor como o **eixo** que conecta as três coisas: a **frota** (de quem é o veículo), o **motor de frete** (de quem é a regra de preço) e a **composição do frete** no orçamento (quem, afinal, transporta e cobra). Todo tipo de veículo que você cria já nasce com um detentor — a sua organização, salvo se você escolher um fornecedor.

{% hint style="success" %}
**Por que isso importa.** Graças ao detentor, o mesmo orçamento pode comparar o **seu** custo de frete com o de **vários fornecedores** lado a lado, cada um com o seu preço — e você escolhe quem leva a carga. É o que transforma "terceirizar frete" numa decisão de um toque, sem planilha por fora.
{% endhint %}

## Cadastrar um fornecedor {#cadastrar}

Na tela **Fornecedores**, toque no botão **+** (o **Novo fornecedor**). O cadastro tem duas etapas:

1. **Quem é** — os dados da pessoa ou da empresa, na mesma tela de cadastro de contato, com o papel **Fornecedor** já marcado. É lá que ficam documento, telefone e endereço.
2. **O que ele faz para você** — os serviços que esse fornecedor presta. É aqui que mora a parte importante (veja [Serviços prestados](#servicos)).

Na lista, quem presta frete ganha o selo **"Presta frete"** — o atalho visual para saber quem já está pronto para cotar transporte.

{% hint style="info" %}
**Só tem o financeiro?** Sem a permissão do cadastro de fornecedores — ou sem o plano que inclui o fornecedor de frete —, o **+** cria só a ficha do fornecedor no financeiro, o suficiente para lançar despesas. Serviços e frete ficam com quem cadastra fornecedores.
{% endhint %}

### O que dá para fazer com cada fornecedor {#acoes}

Toque num fornecedor para abrir as ações dele — cada uma aparece para quem tem a permissão certa:

| Ação | O que faz |
| --- | --- |
| **Categorizar** | Escolhe a categoria (e, se quiser, o quadrante). Num fornecedor que ainda não tem ficha no financeiro, categorizar **cria** essa ficha. |
| **Editar ficha** | Ajusta os dados da ficha do financeiro. |
| **Serviços e frete em Parceiros** | Abre os serviços que ele presta — é ali que se marca o **Frete**. |
| **Ver contato** | Abre o cadastro dele em Contatos. |
| **Arquivar** / **Reativar** | Tira a ficha do seletor de despesas novas — o histórico fica — ou a traz de volta. |
| **Cancelar em Parceiros** | Deixa de oferecê-lo em novos serviços e o tira das opções de frete. |

### Cancelar (sem perder histórico) {#cancelar}

Quando um fornecedor deixa de trabalhar com você, use **Cancelar em Parceiros**. O app confirma com clareza:

{% hint style="warning" %}
*"Deseja cancelar "Transportadora Silva" em Parceiros? Ele deixa de ser oferecido em novos serviços (e sai do pool de frete, se prestava frete). O histórico é preservado, e a ficha do financeiro continua."*
{% endhint %}

Cancelar é um **arquivamento**, não um apagão. O fornecedor **sai das escolhas** de novos orçamentos, mas **todo o histórico é preservado**: os fretes que ele já fez, os valores que cobrou, os orçamentos onde entrou. E a ficha dele no financeiro continua lá, para as despesas. Você não perde rastro de nada — só deixa de oferecê-lo daqui para frente.

## Serviços prestados: Frete é a chave {#servicos}

No cadastro, em **O que ele faz para você**, os serviços aparecem como **chips** que você marca ou desmarca. E há um serviço especial: o **Frete**. Ao marcá-lo, o próprio chip explica o efeito: *"Habilita frota e motor de frete próprios."*

Marcar o chip **Frete** é o que **torna o fornecedor elegível ao motor de frete** — ou seja, o que o habilita a cotar transporte nos seus orçamentos. Sem esse serviço marcado, o fornecedor até existe no cadastro, mas **não entra na composição do frete**: ele não tem preço de transporte para oferecer.

Os outros serviços (como **Mão de obra** ou **Montagem**) existem para você organizar o que o fornecedor faz, mas **não disparam** o mecanismo de frete. Só o **Frete** faz isso. Por isso o app dá um destaque sutil ao chip de Frete — é o que muda o jogo.

## A frota-espelho do fornecedor {#frota-espelho}

Aqui está o passo que muita gente pergunta: *"Se o fornecedor não tem login, como ele cota um preço?"*

A resposta é a **frota-espelho**. Para um fornecedor conseguir cotar, você cria, dentro da sua própria [Frota](../cadastros/frota.md#detentor), **tipos de veículo atribuídos a ele** — usando o mesmo catálogo de veículos (a mesma base FIPE) que você usa para os seus carros. Ao criar um tipo de veículo, o campo **Detentor** deixa você escolher: **Própria organização** (o padrão) ou um dos seus fornecedores de frete.

```mermaid
flowchart LR
    F[Fornecedor de frete] --> E["Tipo de veículo<br/>(detentor = fornecedor)"]
    E --> M["Motor de frete<br/>do fornecedor"]
    M --> C["Composição do frete<br/>no orçamento"]
```

Assim, cada fornecedor ganha os **tipos de veículo** que representam a frota dele no seu sistema. Você descreve os veículos dele uma vez, e eles passam a existir como opção de transporte — sem o fornecedor precisar tocar em nada.

{% hint style="info" %}
**O detentor é escolhido na criação do tipo de veículo.** Ao editar um tipo existente, com o acesso certo, também é possível **trocar o detentor** — o que move o tipo (e os veículos ligados a ele) de um titular para outro. Os detalhes de como cadastrar e atribuir tipos de veículo estão em [Frota](../cadastros/frota.md#detentor).
{% endhint %}

## Cada fornecedor tem o seu motor de frete {#motor-do-fornecedor}

Ter a frota-espelho é metade do caminho. A outra metade é o **preço**: quanto esse fornecedor cobra pelo transporte.

Para isso, **cada fornecedor tem o seu próprio Motor de Frete** — um conjunto de regras de preço separado do seu. As viagens atribuídas aos tipos de veículo de um fornecedor são cobradas pelas **regras dele**, não pelas suas. É o que permite que a sua frota e a de um fornecedor apareçam no mesmo orçamento com **preços diferentes**, cada um justo com quem transporta.

A mecânica de configuração é a mesma do seu motor — os mesmos perfis, gatilhos e cobranças. Só muda o **titular**. Veja como montar o motor de um fornecedor em [Motor de frete por detentor](../configuracoes/motor-de-frete-detentor.md).

## Elegibilidade: fornecedor sem motor fica bloqueado {#elegibilidade}

Um fornecedor só é **elegível** para transportar de fato quando tem **motor de frete ativo**. Faz sentido: sem regras de preço, não há como saber quanto o transporte dele custa — e uma viagem sem preço não pode entrar num orçamento.

O LocFlow protege você disso **na hora de dividir a carga**. Quando você monta a composição do frete e vai escolher o tipo de veículo de cada viagem, um fornecedor **sem motor de frete ativo** aparece com um **cadeado** e a marca **"sem motor de frete"** — e **não pode ser selecionado**. O app explica o motivo ali mesmo, para você não escolher uma opção que sairia sem valor.

{% hint style="warning" %}
**Como destravar.** Se um fornecedor aparece bloqueado, é porque falta configurar o **motor de frete dele**. Configure o motor (com pelo menos uma cobrança válida) e ele passa a ser selecionável na divisão. Onde tudo isso aparece no orçamento — a composição do frete, a divisão entre transportadoras e o repasse ao cliente — está em [Valores: acréscimos, frete e descontos](../orcamentos/valores.md#composicao-do-frete).
{% endhint %}

## Como tudo se conecta {#como-se-conecta}

Juntando as peças, o caminho de um fornecedor de frete é este:

1. **Cadastre** o fornecedor e marque o serviço **Frete**.
2. **Crie a frota-espelho** dele — tipos de veículo com o **Detentor** apontando para o fornecedor.
3. **Configure o motor de frete** dele, com as regras de preço que ele cobra.
4. No **orçamento**, ele passa a aparecer na **composição do frete**, ao lado da sua própria frota, com o preço dele.
5. Você **escolhe** quem transporta — um só ou vários, dividindo as viagens — e define **quanto repassa** ao cliente.

Pule a etapa 3 e o fornecedor fica **bloqueado** na divisão. As três primeiras etapas são o preparo; a partir daí, é decisão de orçamento.

## Por porte {#por-porte}

| Se você é… | Como os fornecedores entram |
| --- | --- |
| **Autônomo / micro** | Provavelmente nem precisa: você usa a sua própria frota (ou frete manual). Fornecedores fazem sentido quando você começa a **terceirizar** entregas. |
| **Médio** | Um ou dois fornecedores para as entregas que a sua frota não cobre — longas, ou em dias de pico. Você compara o custo deles com o seu e escolhe o melhor por pedido. |
| **Grande / muitas filiais** | Uma rede de transportadoras, cada uma com a sua frota-espelho e o seu motor. O orçamento vira uma cotação automática entre várias opções, com repasse e margem controlados. |

## Situações reais {#situacoes-reais}

- **Entrega distante:** chega um pedido para uma cidade a 300 km. A sua frota não vale a pena. Você tem a "Transportadora Silva" cadastrada, com frota-espelho e motor — no orçamento, ela aparece com o preço dela e você fecha o frete com ela num toque.
- **Dia de pico:** cinco entregas no mesmo sábado, três caminhões seus. Você divide a carga: duas viagens ficam com a sua frota e três com um fornecedor, cada porção cobrada pela precificação de quem a leva.
- **Fornecedor novo, ainda sem preço:** você cadastrou a transportadora e criou os tipos de veículo dela, mas ainda não montou o motor dela. Ao tentar usá-la, ela aparece com **cadeado** e "sem motor de frete". Você configura o motor e ela destrava.
- **Transportadora que saiu:** um fornecedor parou de atender. Você o **cancela** — ele some dos novos orçamentos, mas os fretes antigos que ele fez continuam no histórico, intactos para os seus relatórios.

## Próximo passo {#proximo-passo}

- Entenda o quadro maior das parcerias em [Parcerias: a visão](visao-geral.md).
- Monte a **frota-espelho** de um fornecedor em [Frota](../cadastros/frota.md#detentor).
- Configure o **preço** dele em [Motor de frete por detentor](../configuracoes/motor-de-frete-detentor.md).
- Veja o fornecedor entrar no orçamento em [Valores: acréscimos, frete e descontos](../orcamentos/valores.md#composicao-do-frete).
- Precisa liberar o recurso? Veja [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md).
- Dúvida em algum termo? Consulte o [glossário](../primeiros-passos/glossario.md).
