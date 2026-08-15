---
icon: book
description: Os termos do LocFlow em uma linha — orçamento, movimento, frete por viagem, fatura, canal, crédito e mais. Consulte sempre que bater dúvida.
---

# Glossário do LocFlow

Os termos que você vê pelo sistema, explicados em uma linha. Bateu dúvida em alguma tela? Volte aqui — e siga o link para a página que aprofunda.

## Negócio {#negocio}

| Termo | O que é |
| --- | --- |
| **Bem móvel / item** | O que você aluga ou vende (mobília, estrutura, tenda, som, veículo…). |
| **Locação** | Aluguel: o item vai e **volta**. |
| **Venda** | O item sai em **definitivo** (sem retorno). |
| **Contato** | Um cliente — ou possível cliente — pessoa física ou jurídica. |
| **Produto** | Um item do seu catálogo, com preço de aluguel e/ou venda. |
| **Kit** | Um pacote de produtos vendido/alugado como um conjunto. |
| **Galpão** | A base de onde seus itens saem e para onde voltam. É também o **balcão** de atendimento — onde o cliente retira/devolve presencialmente (hoje, no mesmo endereço do galpão). |

## Orçamento (estados) {#orcamento-estados}

| Termo | O que é |
| --- | --- |
| **Pendente (aguardando aprovação)** | Pré-etapa do funil: uma **política** deixou o pedido congelado até o aval de um responsável — frete acima do limite, **desconto acima do teto** ou frete de fornecedor. **Não é o mesmo que "Em aberto"** — só depois de aprovado o orçamento entra no funil. |
| **Em aberto** | Criado, ainda sem ação. |
| **Em negociação** | Enviado ao cliente, aguardando resposta. |
| **Pré-reservado** | "Segurar" o aluguel antes de confirmar (opcional, só locação). Você decide na [Operação do Orçamento](../configuracoes/motores-operacionais.md#operacao-do-orcamento) se essa etapa entra no seu funil — desligada, a negociação vai direto para reservado. |
| **Reservado** | Aluguel confirmado — o **ganho** da locação; estoque bloqueado. |
| **Vendido** | Venda confirmada — o **ganho** da venda. |
| **Perdido** | Não fechou; pode ser reaberto. |
| **Cancelado** | Cancelado **depois** de ganho (já havia compromissos). |
| **Finalizado** | Operação concluída de ponta a ponta — entregue (e, na locação, retirada e conferida de volta). |
| **Vencido (fora da validade)** | Passou a **data de validade** da proposta. **Não é um estado do funil** — o orçamento continua no estado em que estava, mas fica **impedido de avançar** até você renovar a validade ou criar um novo. Veja [Quando o orçamento vence](../orcamentos/acompanhando-e-fechando.md#quando-o-orcamento-vence). |

## Movimentos e janelas {#movimentos-janelas}

| Termo | O que é |
| --- | --- |
| **Movimento logístico** | Cada deslocamento dos seus itens: a **entrega** (saída) e, na locação, a **retirada** (retorno). |
| **Forma de operação** | Como sua locadora opera: **Só balcão** (cliente retira/devolve no galpão), **Só rota** (equipe entrega/retira) ou **Mista**. Define o padrão dos movimentos no orçamento e oculta do menu o que você não usa — sem bloquear (a exceção abre em "Operação avançada"). Configurada no [Motor de Logística](../configuracoes/motores-operacionais.md#motor-de-logistica). |
| **Janela** | A data + a faixa de horário em que um movimento deve acontecer. |
| **Galpão de origem** | De onde a carga **sai** para aquele movimento — o LocFlow ranqueia seus galpões por proximidade do destino. |
| **Raio (máximo) de atendimento** | A distância máxima, a partir do galpão, que ele cobre; um destino fora do raio fica indisponível para aquele galpão. |
| **Intervalo mínimo logístico** | O tempo de folga que sua operação precisa entre os movimentos; o LocFlow recua o início da janela por ele e avisa quando a janela fica apertada. |

→ Detalhes em [Movimentos, janelas e galpão de origem](../orcamentos/movimentos-e-janelas.md).

## Duração e bloqueio (locação) {#duracao-bloqueio}

| Termo | O que é |
| --- | --- |
| **Período de cobrança** | Por **quantas locações** o cliente paga (×1 por padrão; pode ser por diária). |
| **Multiplicador de cobrança** | O número que multiplica o valor dos itens conforme o período de cobrança (ex.: ×3). |
| **Operação** | O vai e volta real do material: da hora em que ele **sai** do galpão até a hora em que **volta**. É a base do bloqueio. |
| **Janela de bloqueio de uso** | O período em que o item fica reservado a um cliente e indisponível para os outros: a **operação mais a folga**. |
| **Política de bloqueio** | A escolha, no Motor de Estoque, entre **Mínimo justo** (sem folga) e **Com folga** (recomendada). Só decide a folga — a base é sempre a operação. |
| **Folga de equipe** | Minutos extras de bloqueio quando **você** entrega e recolhe; cobre trânsito e imprevisto de rota. Padrão: 60 min de cada lado. |
| **Folga de cliente** | Minutos extras de bloqueio quando **o cliente** retira e devolve no galpão; cobre o cliente que atrasa ou remarca. |
| **Preparo** | O tempo de conferência, limpeza e manutenção **depois** que o item volta, antes de contar como disponível de novo. |
| **Data de Liberação** | A data em que o item volta a contar como disponível: o retorno **mais** o preparo. |

{% hint style="info" %}
Regra que o sistema cobra: **o bloqueio cobre a operação, e a operação cobre o evento**. Se um orçamento sair disso, o LocFlow avisa e pede correção antes de seguir.
{% endhint %}

→ Detalhes em [Duração, cobrança e bloqueio de uso](../orcamentos/duracao-e-bloqueio.md).

## Valores: acréscimos e descontos {#valores}

| Termo | O que é |
| --- | --- |
| **Acréscimo** | Tudo que **soma** ao orçamento e não é item: mão de obra, montagem, desmontagem, layout, outros. É uma **lista** — você lança quantos precisar, cada um com o seu texto e valor (R$ ou % **sobre o total dos itens**). |
| **Taxa de serviço** | A porcentagem padrão do [Motor de Orçamento](../configuracoes/motor-de-orcamento.md#taxa-de-servico) que já nasce lançada como **um acréscimo de mão de obra** em todo orçamento novo. |
| **Desconto avulso** | O desconto digitado **só naquele orçamento**, na hora da negociação. Não vira regra e pode repetir. |
| **Desconto tabelado** | O desconto que veio de uma **regra do catálogo**. Leva o selo *Tabelado* e a mesma regra não entra duas vezes no mesmo pedido. |
| **Regra de desconto** | O desconto cadastrado uma vez em **Ajustes › Regras de Desconto**, com condição e base — o sistema o **sugere** sozinho quando cabe. Veja [Regras de desconto](../configuracoes/regras-de-desconto.md). |
| **Condição** | *Quando* o desconto vale: **sem condição** (quem decide é o vendedor), **por valor do orçamento** ou **por quantidade** de um item. |
| **Base de incidência** | *Sobre qual valor* o desconto morde: **o total** (itens + acréscimos + frete), **os itens** ou **o item** que ativou a condição. A mesma porcentagem vale valores bem diferentes em cada base. |
| **Desconto proporcional aos kits** | A sugestão **automática**: quando os produtos avulsos do carrinho formam kits do seu catálogo, o LocFlow oferece a economia do combo como desconto, e o valor se recalcula sozinho quando o carrinho muda. |
| **Teto de desconto** | O quanto o vendedor abate **sozinho**. Acima dele o orçamento nasce **congelado aguardando aprovação**. *Sem teto* = nada trava; *teto 0%* = tudo trava. |

{% hint style="info" %}
Descontos **nunca se aplicam em cascata**: todos partem do valor original. 10% + 10% abatem 20%, não 19% — e a ordem em que você lança não muda o total.
{% endhint %}

→ Detalhes em [Valores: acréscimos, frete e descontos](../orcamentos/valores.md).

## Logística (estados do material) {#logistica-estados}

| Termo | O que é |
| --- | --- |
| **A separar → Separado** | Fila de **separação** no galpão (preparar o material). |
| **Saiu para entrega → Entregue** | O material a caminho do cliente e entregue. |
| **Saiu para retirada → Retirado** | Buscar o material de volta (locação). |
| **A conferir → Conferido** | Fila de **conferência** na devolução (checar estado/avarias). |
| **Roteiro** | Conjunto de paradas (entregas/retiradas) organizado para o dia. |
| **Parada** | Um ponto de entrega ou retirada dentro do roteiro. |
| **Planejar entrega/retirada** | Ação rápida do pedido que abre o planejamento do roteiro com aquele movimento já selecionado — o jeito de despachar na hora, sem montar a rota do dia antes. |
| **Comprovação (POD)** | Prova de entrega/retirada: foto, vídeo, assinatura. Quando a sua empresa exige, **sem ela o registro não fecha**. |
| **Dispensa de evidência** | Fechar um registro **sem a prova** que a política exigia, escrevendo um **motivo obrigatório** que fica carimbado no registro. É uma válvula para quem lança o que já aconteceu (retaguarda, balcão) e depende de uma **permissão dedicada** — motorista e parceiro externo **não a têm**, justamente porque existem para produzir a prova. |
| **Desatualizado (defasado)** | Um movimento ficou **velho** no roteiro porque o pedido mudou depois. Ele fica **só de leitura** e trava quem está na rua até alguém **ressincronizar** a parada com o pedido atual. Num pedido **repassado a um parceiro**, quem ressincroniza é **o parceiro**, não você — veja [O pedido já estava com um parceiro](../logistica/efeitos-na-parceria.md). |

→ Comece por [Visão geral da logística](../logistica/visao-geral.md).

## Frete {#frete}

| Termo | O que é |
| --- | --- |
| **Rota Estimada** | O trajeto de **ida e volta** de um movimento que o motor mede para cobrar o frete, no **pior cenário** (veículo dedicado só àquele pedido). |
| **Viagem** | A unidade de cálculo do frete: um movimento (a **entrega** ou a **retirada**), com a **ida e a volta contando como uma coisa só**. |
| **Frete por viagem** | Cada valor do motor é aplicado a **cada viagem** — o valor fixo e a carga contam 1× por viagem; km e tempo já somam a ida e a volta. Um aluguel típico tem **2 viagens** (a entrega e a retirada). |
| **Detentor** | O titular de uma ficha de frota, de um motor de frete e de uma porção do frete: a sua **organização** ou um **fornecedor de frete**. Cada detentor cobra pela **tabela dele**. Veja [Fornecedores de frete](../parcerias/fornecedores-de-frete.md#detentor). |
| **Transportadora** | Quem leva uma porção da carga — a sua organização ou um fornecedor. No cálculo do frete, é o mesmo que **detentor**. |
| **Composição do frete** | Como o valor final é montado: o **custo** de cada porção (cotado pelo motor de quem transporta) somado, mais o **repasse** ao cliente. Veja [Valores](../orcamentos/valores.md#composicao-do-frete). |
| **Repasse (frete)** | Quanto do frete você **cobra do cliente** — pode ser igual, menor ou maior que o custo. Nada a ver com o **repasse da parceria** (o pedido e o dinheiro que vão para um parceiro): veja [Rede de Parceiros](#rede-de-parceiros). |
| **Margem (no frete)** | A diferença entre o que você cobra do cliente (o repasse) e o **custo** do transporte. |
| **Estratégia de alocação** | Como o LocFlow **recomenda** repartir a carga entre as transportadoras: **Menor valor ao cliente**, **Melhor aproveitamento** ou **Montar manualmente**. Veja [Motor de Frete por detentor](../configuracoes/motor-de-frete-detentor.md#estrategia-de-alocacao). |
| **Divisão de movimento** | Repartir a carga de um mesmo movimento entre veículos (e transportadoras) diferentes — cada **porção** com o seu preço. |

→ Detalhes em [Motor de Frete: como calcula](../configuracoes/motor-de-frete.md) e [Motor de Frete por detentor](../configuracoes/motor-de-frete-detentor.md).

## Cobrança {#cobranca}

| Termo | O que é |
| --- | --- |
| **Fatura** | A cobrança do pedido; nasce automática ao ganhar o orçamento e **espelha** o orçamento. |
| **Parcela** | Uma divisão da fatura, com vencimento próprio. É **atômica** (não existe "meia paga": pagamento parcial **desdobra** a parcela). |
| **Baixa manual** | Registrar um recebimento feito por fora (dinheiro, pix, maquininha). |
| **Pagamento online** | Link de pagamento (PIX/cartão/boleto) com baixa automática, em tempo real. |
| **Recebedor** | A conta da sua locadora que **recebe** os valores das cobranças online. |
| **Validação (KYC)** | Checagem de identidade exigida por lei, feita pelo responsável via link, antes de liberar o recebedor. |
| **Saldo a favor do cliente** | Valor que sobra a favor do cliente (ex.: edição que reduz o total depois de já pago). |
| **Crédito / vale-locação** | Esse saldo a favor virando crédito reaproveitável na **próxima locação**, sem operação bancária. |
| **Reembolso** | Esse saldo a favor sendo **devolvido** ao cliente (estorno ou transferência). |

→ Comece por [Faturas e parcelas](../cobranca/faturas-e-parcelas.md).

## Rede de Parceiros {#rede-de-parceiros}

Quando você faz negócio junto com outra operação, o LocFlow reparte o pedido em **linhas de responsabilidade**: um lado cuida do cliente e do dinheiro, o outro cuida do material na rua. Quase todo termo desta seção sai daí.

| Termo | O que é |
| --- | --- |
| **Vendedor** | O lado **dono do cliente**: fez o orçamento, emite a fatura e responde pela relação comercial. |
| **Parceiro logístico** | O lado que **executa**: entrega, retira e cuida do material — e, quando o acordo permite, recebe do cliente na porta. |
| **Linha logística** | O pedaço da operação que passa a ser do parceiro quando você repassa: o roteiro, o plano de movimentos (dividir, juntar, remarcar), a entrega, a retirada e o balcão daquele pedido. |
| **Linha comercial e de cobrança** | O pedaço que continua **seu**, sempre: o cliente, o orçamento, o preço final, a fatura e a relação de crédito. Não muda de dono — nem quando o parceiro recebe o dinheiro na porta. |
| **Parceiro externo** | Uma pessoa ou empresa **convidada por link**, que trabalha **dentro da sua conta** com um papel fixo de parceiro. Veja [Parceiro Logístico Externo](../parcerias/parceiro-logistico-externo.md). |
| **Parceria interna (org↔org)** | Duas organizações LocFlow de verdade, cada uma na sua conta, ligadas por um **vínculo**. |
| **Vínculo** | O "sim" entre duas organizações, que abre a porta para vocês montarem acordos. **Aceitar um vínculo concede algo:** a outra parte passa a poder usar o seu **motor de frete publicado**, os seus **galpões** e o seu **preço de tabela** como sugestão ao montar um acordo — e o que ela derivar fica guardado lá, mesmo que o acordo não feche. Dá para desligar essa sugestão no **Perfil de parceria** sem romper o vínculo. |
| **Acordo de parceria** | Os termos do trabalho conjunto: quais itens, por qual preço, quando o parceiro recebe, quem paga o quê. Só vale depois do aceite dos **dois** lados. |
| **Repasse (parceria)** | Duas coisas com o mesmo nome: o **ato** de entregar um pedido já ganho a um parceiro, e o **valor** que você deve a ele por ter executado. |
| **Saldo devedor do repasse** | O repasse **ao contrário**. Se quem ficou com o dinheiro do cliente foi o parceiro, não é você que deve a ele — **é ele que deve a você** (a sua margem mais a taxa da plataforma). Ele vê *"A pagar à organização"*; você vê *"A receber de parceiros"*. |
| **Taxa da plataforma** | **8% fixos** (iguais em qualquer plano) sobre o **total da operação** — itens + mão de obra + frete − descontos — e só sobre o que o cliente **efetivamente pagou**. O acordo decide como esses 8% se dividem entre as partes; o padrão é 8% no vendedor e 0% no parceiro. **O teto é por orçamento**: a mesma venda nunca é taxada duas vezes, mesmo que passe por dois parceiros. |
| **Modelo de pagamento (gatilho)** | *Quando* o parceiro recebe e *quanto*. Ao **montar** o acordo ele aparece como **"Como você paga o parceiro"**; ao **revê-lo depois**, o mesmo bloco se chama **"Quando você paga"**. Do lado de quem executa, os dois momentos dizem **"Quando você recebe"**. Há três atalhos prontos — *Pago pelo que ele fez*, *Só quando o cliente pagar*, *Confio, pago adiantado* — e um caminho **Do meu jeito** para o ajuste fino. Veja [Acordos de parceria](../parcerias/acordos-de-parceria.md#gatilho-de-pagamento). |
| **Cobrança na rua** | A permissão, combinada no acordo, de o **parceiro receber do cliente no ponto de entrega**. A fatura, a razão e a relação com o cliente continuam suas — ele age como **coletor**, não como dono do crédito. Vale hoje só com o **parceiro externo**; entre duas organizações, quem recebe do cliente continua sendo você. E a coleta é **tudo ou nada**: ou ele fecha a cobrança inteira, ou o caminho é o seu PIX. Veja [Cobrança na rua](../parcerias/cobranca-na-rua.md). |
| **Coletor** | Quem de fato **ficou com o dinheiro** do cliente naquela operação: você ou o parceiro. É esse fato — e não o que está escrito no acordo — que decide para que lado o repasse corre. |
| **Cobertura parcial** | Itens daquela operação que o acordo **não traduz** para o catálogo da parceira: ela não vai fornecê-los. Aparece como faixa âmbar no comparativo e no aceite, **antes** do repasse. **Avisa, não bloqueia.** |

{% hint style="warning" %}
**"Repasse" quer dizer duas coisas no LocFlow.** No **frete**, é quanto do transporte você cobra do cliente. Na **parceria**, é o pedido (e o dinheiro) que vai para o parceiro. Se você chegou aqui de uma tela de frete, o termo é o [outro](#frete).
{% endhint %}

{% hint style="info" %}
**O que o parceiro vê do seu negócio.** Ele vê o **preço ao cliente dos itens que estão no acordo** — sem esse número, "você recebe 70% do valor" não significa nada — e a **divisão da taxa da plataforma** combinada ali (a fatia dele e a sua). Quando o acordo permite cobrança na rua, vê também **quanto o cliente deve** daquele pedido e pode gerar o **seu** PIX para mostrar na porta. Ele **não** vê o resto da sua carteira de cobranças, os seus outros clientes e orçamentos, nem como o preço final foi montado (descontos, histórico). Detalhes em [Rede de Parceiros: a visão](../parcerias/visao-geral.md).
{% endhint %}

→ Comece por [Rede de Parceiros: a visão](../parcerias/visao-geral.md); a conta do dinheiro está em [O dinheiro da parceria](../parcerias/dinheiro-da-parceria.md).

## Pessoas e acesso {#pessoas-acesso}

| Termo | O que é |
| --- | --- |
| **Papel** | O que a pessoa **vê e faz** (permissões). Ex.: Motorista, Separador. |
| **Função** | O **cargo** na operação (Vendedor, Motorista…). |
| **Competência** | A **habilidade** ligada à função (Dirigir veículos, Vender orçamentos, Separação, Conferência, Operar logística, Atendimento no balcão). |
| **Responsável pela operação** | Quem está **por trás** daquela operação (ex.: quem executa a rota) — descoberto pelo sistema, sem você nomear. |
| **Colaborador × parceiro** | O **colaborador** é da sua equipe e você o convida em **Colaboradores**. O **parceiro externo** é gente de fora e entra por outro caminho — o convite da **Rede de Parceiros**. O papel de parceiro **não aparece** na lista de papéis do convite de colaborador. Veja [Entrando na rede](../parcerias/entrando-na-rede.md). |

## Notificações {#notificacoes}

| Termo | O que é |
| --- | --- |
| **Canal** | Para onde um aviso vai: **quem recebe** (pool) + **como** (todos ou rodízio). |
| **Pool** | De onde saem os destinatários: organização, competência, responsável pela operação, cliente. |
| **Rodízio** | Distribui 1 a 1, revezando (ex.: leads entre vendedores). |
| **Nível de atenção** | Quanto o aviso interrompe: **Crítico** (modal + som), **Importante** (toast), **Informativo** (só o sino). |

→ Detalhes em [Canais de notificação](../configuracoes/canais-de-notificacao.md).

## Configuração e frota {#configuracao-frota}

| Termo | O que é |
| --- | --- |
| **Motor** | Uma regra da sua operação que o sistema segue sozinho (frete, cobrança, logística, estoque, orçamento). |
| **Crédito (moeda de mapa)** | A "moeda" que cobre o custo dos recursos de **mapa do Google** (geocodificar, traçar e otimizar rota); pino e onboarding são grátis. |
| **Classe / Especificação / Veículo** | Como a frota é organizada: tipo → ficha técnica → o veículo com placa. |
| **Fornecedor de frete** | Uma **transportadora terceira** que você cadastra e gerencia por inteiro (ela **não tem login**) para terceirizar o transporte de um pedido. Veja [Fornecedores de frete](../parcerias/fornecedores-de-frete.md). |
| **Frota-espelho** | As **fichas de veículo** que você cria no seu sistema atribuídas a um fornecedor — é o que permite a ele cotar frete sem ter acesso ao app. Veja [Fornecedores de frete](../parcerias/fornecedores-de-frete.md#frota-espelho). |
| **Capacidade** | Como o LocFlow avalia se a carga **cabe** no veículo: **contagem** (quantos de cada produto cabem — os kits entram diluídos nos seus produtos) ou **volumétrica** (volume do baú × cubagem da carga, pelo fator de cubagem de cada item), usada quando não há limite de contagem. |
| **Fator de cubagem** | O **volume efetivo (m³)** que um item (produto ou kit) ocupa numa carga, **considerando o empilhamento** — empírico, aferido na prática. Base da estratégia volumétrica. Não pode passar do volume das dimensões da peça; o kit tem fator próprio (não é a soma das peças). |
| **Baú fechado** | A chave que confirma uma carroceria cubável e **libera** a estratégia volumétrica. |
| **Vistoria** | Checklist do veículo antes de rodar. |

→ Créditos em [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md); capacidade em [Especificações: capacidade](../cadastros/frota-capacidade.md).

## Próximo passo {#proximo-passo}

Veja como tudo se conecta em [O ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md).
