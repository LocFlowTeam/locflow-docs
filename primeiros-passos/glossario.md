---
icon: book
description: Os termos do LocFlow em uma linha — orçamento, movimento, frete por rota, fatura, canal, crédito e mais. Consulte sempre que bater dúvida.
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
| **Pendente (aguardando aprovação)** | Pré-etapa do funil: uma **política** do Motor de Orçamento (ex.: frete acima de um limite) deixou o pedido congelado até o aval de um responsável. **Não é o mesmo que "Em aberto"** — só depois de aprovado o orçamento entra no funil. |
| **Em aberto** | Criado, ainda sem ação. |
| **Em negociação** | Enviado ao cliente, aguardando resposta. |
| **Pré-reservado** | "Segurar" o aluguel antes de confirmar (opcional, só locação). Você decide na [Operação do Orçamento](../configuracoes/motores-operacionais.md#operacao-do-orcamento) se essa etapa entra no seu funil — desligada, a negociação vai direto para reservado. |
| **Reservado** | Aluguel confirmado — o **ganho** da locação; estoque bloqueado. |
| **Vendido** | Venda confirmada — o **ganho** da venda. |
| **Perdido** | Não fechou; pode ser reaberto. |
| **Cancelado** | Cancelado **depois** de ganho (já havia compromissos). |
| **Finalizado** | Operação concluída de ponta a ponta — entregue (e, na locação, retirada e conferida de volta). |

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
| **Janela de bloqueio de uso** | O período de **uso exclusivo** do cliente — quando o uso começa e termina. |
| **Turnaround** | O preparo (limpeza, conferência, retorno) **depois** que o item volta, antes de ficar disponível de novo. |
| **Bloqueio de estoque** | A janela total em que o item fica indisponível para outro cliente: **uso + turnaround**. |

→ Detalhes em [Duração, cobrança e bloqueio de uso](../orcamentos/duracao-e-bloqueio.md).

## Logística (estados do material) {#logistica-estados}

| Termo | O que é |
| --- | --- |
| **A separar → Separado** | Fila de **separação** no galpão (preparar o material). |
| **Saiu para entrega → Entregue** | O material a caminho do cliente e entregue. |
| **Saiu para retirada → Retirado** | Buscar o material de volta (locação). |
| **A conferir → Conferido** | Fila de **conferência** na devolução (checar estado/avarias). |
| **Roteiro** | Conjunto de paradas (entregas/retiradas) organizado para o dia. |
| **Parada** | Um ponto de entrega ou retirada dentro do roteiro. |
| **Sob demanda** | Despachar **uma** entrega na hora, sem planejar antes. |
| **Comprovação (POD)** | Prova de entrega/retirada: foto, vídeo, assinatura. |
| **Desatualizado (defasado)** | Um movimento ficou **velho** no roteiro porque o pedido mudou depois; vira pendência para o operador e trava o motorista até o ajuste. |

→ Comece por [Visão geral da logística](../logistica/visao-geral.md).

## Frete {#frete}

| Termo | O que é |
| --- | --- |
| **Rota Estimada** | O trecho que o motor mede para cobrar o frete, no **pior cenário** (veículo dedicado só àquele pedido). |
| **Frete por rota (não por viagem)** | Cada valor do motor é aplicado a **cada** Rota Estimada — um aluguel típico tem 4 rotas (ida e volta de entrega e de retirada). |

→ Detalhes em [Motor de Frete: como calcula](../configuracoes/motor-de-frete.md).

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

## Pessoas e acesso {#pessoas-acesso}

| Termo | O que é |
| --- | --- |
| **Papel** | O que a pessoa **vê e faz** (permissões). Ex.: Motorista, Separador. |
| **Função** | O **cargo** na operação (Vendedor, Motorista…). |
| **Competência** | A **habilidade** ligada à função (Dirigir veículos, Vender orçamentos, Separação, Conferência, Operar logística). |
| **Responsável pela operação** | Quem está **por trás** daquela operação (ex.: quem executa a rota) — descoberto pelo sistema, sem você nomear. |

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
| **Capacidade** | Como o LocFlow avalia se a carga **cabe** no veículo: **contagem** (quantos de cada produto cabem — os kits entram diluídos nos seus produtos) ou **volumétrica** (volume do baú × cubagem da carga), usada quando não há limite de contagem. |
| **Baú fechado** | A chave que confirma uma carroceria cubável e **libera** a estratégia volumétrica. |
| **Vistoria** | Checklist do veículo antes de rodar. |

→ Créditos em [Minha assinatura e créditos](../configuracoes/assinatura-e-creditos.md); capacidade em [Especificações: capacidade](../cadastros/frota-capacidade.md).

## Próximo passo {#proximo-passo}

Veja como tudo se conecta em [O ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md).
