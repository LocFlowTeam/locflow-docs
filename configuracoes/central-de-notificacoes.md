---
icon: bell
description: Avise as pessoas certas, na hora certa. Defina o que dispara cada aviso, quem recebe e com que destaque — e prévia de como ele chega.
---

# Central de Notificações

A **Central de Notificações** avisa as pessoas certas, na hora certa, sobre o que acontece no seu negócio — de um valor a favor do cliente a uma parada pulada na rota. Você define **quais avisos** sua organização recebe, **quem** recebe cada um e **com que destaque** — e ainda vê uma **prévia de como o aviso chega** antes de salvar.

{% hint style="info" %}
As notificações são da **organização**, não de um usuário específico. Quem decide para quem cada aviso vai é o **canal** (quem recebe + como). Cada pessoa vê, no próprio **sino**, só os avisos destinados a ela (veja [Vendo e gerenciando os avisos recebidos](#avisos-recebidos)).
{% endhint %}

## Como cada notificação funciona

Toda notificação tem quatro partes:

| Parte | O que é |
| --- | --- |
| **Acionador** | O que dispara o aviso: um **evento** (ex.: a equipe saiu do galpão) ou uma **data** — antes dela ("3 dias antes do vencimento") ou depois ("vencida há 3 dias"). |
| **Canal** | Para onde o aviso vai. Cada aviso aponta para um **canal**, que define **quem recebe** e **como** o aviso é distribuído. Veja [Canais de notificação](canais-de-notificacao.md). |
| **Nível de atenção** | Quanto o aviso deve **interromper** quem recebe (ver abaixo). |
| **Ação rápida (opcional)** | Um botão de atalho para resolver, dentro do próprio aviso — ex.: "Abrir a fatura", "Ver no roteiro". |

### Responsável pela operação

Alguns avisos miram **quem está por trás daquela operação**, sem você precisar nomear ninguém — o sistema descobre na hora. Como diz a própria tela:

> O **responsável pela operação** é descoberto automaticamente — sem precisar nomear ninguém.

Na **logística**, é **quem está executando a rota** (o condutor). Em outros casos seria, por exemplo, quem vende o orçamento. Nem todo aviso tem um responsável "por trás" — quando tem, ele aparece como opção de canal.

## Níveis de atenção {#niveis-de-atencao}

O nível descreve **quanto a notícia deve interromper** quem recebe — e isso define **como** o aviso chega. São três:

| Nível | Como chega |
| --- | --- |
| **Crítico** | **Modal que interrompe** a tela + som (se a pessoa ativou) + fica no sino. Exige olhar agora. |
| **Importante** | **Aviso discreto no topo** + fica no sino. Bom ver logo, sem travar o trabalho. |
| **Informativo** | **Só conta no sino**, sem interromper. Você confere quando quiser. |

{% hint style="warning" %}
Avisos **críticos** miram um público **estreito** (a pessoa diretamente envolvida — ex.: quem está executando a rota), para não interromper quem não tem a ver com aquilo.
{% endhint %}

### A prévia "Como o aviso chega" {#previa-como-o-aviso-chega}

Ao abrir um aviso, no rodapé do detalhe há uma **prévia ao vivo** com o título **COMO O AVISO CHEGA**. Ela é um **espelho visual** do nível escolhido — muda na hora, conforme você troca de nível:

- **Crítico** → mostra o **modal que interrompe**, com os botões "Fechar" e a ação rápida (se houver).
- **Importante** → mostra o **aviso discreto** (um cartão no topo) com a ação como link.
- **Informativo** → mostra só o **sino** com o aviso na lista.

É a forma mais rápida de entender o efeito antes de salvar: você troca o nível, olha a prévia e decide.

## Padrão de fábrica × o ajuste da sua organização {#padrao-x-override}

Cada aviso já vem com um **padrão de fábrica**: um nível e um canal sugeridos pelo LocFlow (ex.: "Reembolso ou crédito resolvido" chega como **Importante** para **toda a organização**). Você não precisa configurar nada para começar — o padrão já funciona.

Quando você **muda o nível** ou **troca o canal** de um aviso, está criando um **ajuste da sua organização** que passa a valer **por cima** do padrão. Enquanto você não mexe, o padrão de fábrica é o que vale.

{% hint style="info" %}
**Voltar ao padrão:** para retornar ao comportamento de fábrica de um aviso, basta reescolher o nível/canal originais (mostrados como sugestão na lista). O ajuste da sua organização só existe enquanto você o mantém diferente do padrão.

Nos avisos com **lembretes por data**, toque em **Restaurar padrão** no editor de lembretes para voltar aos valores de fábrica — 1 dia antes do evento (aluguel) e 7 dias antes do vencimento (venda) no *Acompanhamento de orçamento em aberto*; 3, 10 e 30 dias de atraso na *Parcela vencida há X dias*. Deixar a lista **vazia** mantém o aviso por data **desligado**.
{% endhint %}

## Ligar, desligar e ajustar um aviso {#configurando}

Você chega à configuração por **Ajustes › Notificações › Central de Notificações** — na mesma seção de Ajustes fica o item **Canais de Notificação**. Os avisos ficam **agrupados por módulo** (Cobrança, Logística, Orçamento, **Parceria**, **Financeiro** e **Estoque**), com **busca** e um contador de quantos estão ligados em cada grupo. Escolha um aviso para configurá-lo:

1. **Ligar ou desligar** o aviso (o interruptor no topo do detalhe).
2. **Escolher o nível de atenção** (Crítico / Importante / Informativo) — com a prévia atualizando ao vivo.
3. **Escolher o canal** (quem recebe e como). Toque no canal para trocar, ou use **Gerenciar canais** para editar a pool e o roteamento — e reaproveite o mesmo canal em vários avisos.

No topo da tela há uma **legenda dos níveis** (cartões "Crítico / Importante / Informativo") para consulta rápida.

{% hint style="info" %}
As preferências de **som** e **pop-up** não ficam aqui — são **pessoais**, na tela **Preferências**: toque no seu **avatar** (no topo) › **Preferências**, ou no atalho **Preferências** no alto de Ajustes. O link no rodapé de cada aviso também leva para lá. A configuração desta página é da **organização**. Veja [Preferências pessoais](minha-conta.md#preferencias-pessoais).
{% endhint %}

### Alterações não salvas (o aviso ao sair) {#alteracoes-nao-salvas}

A página **só aplica suas mudanças quando você salva**. Enquanto houver ajustes pendentes:

- aparece o sinal **"● Alterações não salvas"** (no computador) ou a barra **"Você tem alterações não salvas"** com o botão **Salvar** (no celular);
- se você tentar **sair, voltar ou trocar de tela**, o LocFlow pergunta **"Salvar alterações?"** — *"Você ajustou notificações que ainda não foram salvas."* — e deixa **salvar** ou **descartar** (voltando à última versão salva).

Depois de salvar, aparece a confirmação **"Salvo"** (e o aviso de pendência some). Esse aviso evita que um ajuste importante se perca por um toque distraído.

## "Em breve": avisos que ainda estão chegando {#em-breve}

Alguns avisos aparecem numa seção **"Em breve"**, recolhida no fim da lista, com o selo **Disponível em breve**. Eles são **só para visualização**: você consegue abrir e entender o que farão, mas **não dá para ligá-los nem ajustá-los ainda** — o interruptor e a edição ficam desativados. Conforme cada recurso fica pronto (pagamento online, mensagens ao cliente), o aviso sai do "Em breve" e passa a ser configurável.

## O que você pode ser avisado (catálogo) {#catalogo}

> A coluna **Status** mostra o que já está disponível e o que está **Em breve** (só visualização). Um caso à parte: o aviso *Aguardando aprovação* **já dispara** hoje, mas a **tela para configurá-lo** ainda não chegou — por isso o rótulo *"Já avisa · ajuste em breve"*.

### Cobrança

| Notificação | Quando avisa | Canal padrão | Nível padrão | Status |
| --- | --- | --- | --- | --- |
| Reembolso ou crédito resolvido | Um valor a favor do cliente virou crédito, vale ou reembolso | Toda a organização | Importante | Disponível |
| Cobrança órfã com pagamento a resolver | Um orçamento foi encerrado antes da reserva com o **sinal já pago**, e o valor não pôde virar crédito nem devolução sozinho — alguém precisa resolver à mão. Atalho: **Abrir a fatura** | Toda a organização | Importante | Disponível |
| Pagamento confirmado | O cliente pagou um valor online | Toda a organização | Importante | Em breve |
| Parcela a vencer | Faltam alguns dias para o vencimento | — | Informativo | Em breve |
| **Parcela vencida há X dias** | A parcela passou do vencimento e continua em aberto — 3, 10 e 30 dias depois, por padrão | Quem cuida do financeiro | Importante | Disponível |

#### Como funciona o "Parcela vencida há X dias" {#parcela-vencida}

Este aviso era só uma promessa — ficava na seção **Em breve**, sem poder ser ligado. Agora ele funciona: **toda manhã**, cada parcela que passou do vencimento e **continua em aberto** vira um aviso para quem cuida do dinheiro, com **o cliente**, **o valor que falta receber**, **desde quando** e o atalho **Abrir a fatura**. Na prática, o aviso chega assim:

> **Parcela vencida há 10 dias**
> Maria Souza está com R$ 1.200,00 em aberto desde 05/08/2026 (orçamento ORC-142). Abra a fatura para cobrar ou registrar o pagamento.

Ele sai pelo canal **Quem cuida do financeiro** — quem tem a competência *Pagar contas* (e quem tem a função "Todas"). Não há "responsável" por uma dívida: o lembrete é da organização. Para estreitar o público, conceda a competência só a quem cuida do dinheiro, ou troque o canal do aviso.

**Você decide em quantos dias de atraso quer ser lembrado.** O padrão são **três lembretes — 3, 10 e 30 dias** —, e cada organização monta os seus na **mesma tela** do acompanhamento de orçamento: abra o aviso e, no bloco **Quando lembrar**, use **Adicionar lembrete** para incluir quantos quiser, cada um de **1 a 90 dias** depois do vencimento. **Restaurar padrão** devolve os três de fábrica.

{% hint style="info" %}
**Lista vazia desliga o lembrete sem desligar o aviso.** Apague todos os lembretes e a tela diz: *"Nenhum lembrete — você não será avisado por atraso."* O aviso continua ligado (e configurado) — ele só não tem mais nenhuma data para disparar. Para silenciá-lo de vez, use o interruptor no topo.
{% endhint %}

**Cada lembrete chega uma vez por parcela.** Rodar o dia de novo não repete o aviso, e 3, 10 e 30 dias não colidem entre si — são três cobranças diferentes da mesma parcela, e cada uma acontece uma vez só. **Reagendar o vencimento também não reabre um lembrete já dado**: o aviso é do atraso, não do dia em que o sistema passou.

**Só o que é dívida entra:**

| Parcela | Entra no lembrete? |
| --- | --- |
| **Pendente** | Sim — é o caso comum. |
| **Aguardando conferência** | **Sim.** O dinheiro da rua ainda não foi conferido; até lá, a dívida existe. |
| **Congelada** | **Sim.** É dinheiro parado esperando alguém decidir — exatamente o que o lembrete existe para lembrar. |
| **Paga** | Não. |
| **Cancelada** | Não. |
| Qualquer parcela de uma **cobrança cancelada** | Não — cobrar por ela seria pedir um dinheiro que a organização já decidiu não cobrar. |

### Logística

| Notificação | Quando avisa | Canal padrão | Nível padrão | Status |
| --- | --- | --- | --- | --- |
| Saída do galpão | A equipe saiu para iniciar a rota | Operadores logísticos | Informativo | Disponível |
| Chegada ao galpão | A equipe retornou ao fim do roteiro | Operadores logísticos | Informativo | Disponível |
| Desvio da rota | Uma parada foi pulada durante a execução | Operadores logísticos | Importante | Disponível |
| Entrega ou retirada concluída | A equipe concluiu uma parada | Operadores logísticos | Informativo | Disponível |
| Roteiro precisa de ajuste | O pedido de uma parada mudou (datas, itens ou quem leva) e o roteiro planejado ficou desatualizado | Operadores logísticos | Importante | Disponível |
| Roteiro ajustado em execução | O operador ajustou um roteiro que já estava em andamento | Responsável pela operação | Crítico | Disponível |
| Condutor do roteiro trocado em execução | O operador trocou o motorista de um roteiro com a rota na rua — avisa quem **assumiu** (o aviso abre a execução) e quem **deixou** de ser o responsável, dizendo se ele segue na equipe como ajudante. Quem só entra ou sai como acompanhante não é avisado | Responsável pela operação | Crítico | Disponível |
| Atendimento na loja (retirada/devolução) | O cliente retirou ou devolveu os itens presencialmente na loja | Responsável pela loja | Informativo | Disponível |
| Movimentos do dia sem roteiro | Toda manhã, quando há entregas ou retiradas com data para hoje (ou atrasadas) que ainda não foram incluídas em um roteiro | Operadores logísticos | Importante | Disponível |

Entenda a fundo o aviso **"Roteiro precisa de ajuste"** (e por que o condutor não recebe a mudança crua) em [Quando um pedido muda depois de fechado](../logistica/quando-um-pedido-muda.md).

### Orçamento

| Notificação | Quando avisa | Canal padrão | Nível padrão | Status |
| --- | --- | --- | --- | --- |
| Acompanhamento de orçamento em aberto | Faltam X dias para a data do evento (aluguel) ou para o vencimento do orçamento — e o orçamento ainda está em aberto, em negociação ou pré-reservado | Responsável pela operação (o vendedor do orçamento) | Importante | Disponível |
| Reserva automática não concluída | O **sinal** de uma pré-reserva foi pago, mas a reserva automática não pôde ser concluída — por exemplo, porque o estoque ficou indisponível — e precisa de ação manual. Atalho: **Abrir orçamento** | Toda a organização | Importante | Disponível |
| Aguardando aprovação | Um orçamento fica congelado esperando um aval — por exemplo, quando o frete passa de um limite e pede aprovação manual | Aprovadores de orçamento | Importante | Já avisa · ajuste em breve |

{% hint style="info" %}
**Sobre o "Aguardando aprovação": o aviso já dispara.** Quando um orçamento congela esperando aprovação (um frete acima do limite, por exemplo), quem pode **vender orçamentos** já é avisado na hora — pelo canal **Aprovadores de orçamento** — para decidir. O que ainda está chegando é só a **tela de configuração** deste aviso: por ora você **não consegue ligá-lo/desligá-lo nem trocar o canal ou o nível** por aqui (ele aparece esmaecido, em "Em breve", na lista de configuração). Ou seja: **já avisa hoje**, só ainda **não é ajustável**. Assim que a configuração ficar pronta, ele sai do "Em breve".
{% endhint %}

#### Como funciona o "Acompanhamento de orçamento em aberto"

Em vez de avisar quando o orçamento é **criado**, este aviso lembra o **vendedor responsável** de **retomar o contato com o cliente** quando a decisão está chegando — enquanto o orçamento **ainda está em jogo**: **em aberto, em negociação ou pré-reservado** (ou seja, ainda não foi **ganho** nem **descartado**, como perdido ou cancelado). **Você define os lembretes**: uma lista de "**X dias antes**", onde cada lembrete aponta para uma data de referência do orçamento:

- **Aluguel** — conte a partir da **data do evento** (recomendado: quando a data se aproxima, há mais chance de fechar) **ou** do **vencimento do orçamento**.
- **Venda** — conte a partir do **vencimento do orçamento**.

Pode ter **vários** lembretes (ex.: *1 dia antes do evento* **e** *5 dias antes do vencimento*). O padrão, se você não mexer, é **1 dia antes do evento** (aluguel) e **7 dias antes do vencimento** (venda). Cada lembrete chega ao **vendedor responsável** daquele orçamento, com um atalho para **abrir o orçamento**. O LocFlow confere os lembretes **todos os dias** automaticamente — você não precisa fazer nada além de configurá-los. Deixar a lista **vazia** desliga o aviso por data.

### Parceria {#avisos-de-parceria}

Este é, de longe, o maior grupo — e faz sentido: quando outra empresa entra na operação, **você deixa de ver com os próprios olhos** o que está acontecendo, e o aviso vira o seu par de olhos. Ele existe tanto para quem **repassa** quanto para quem **executa**; o mesmo aviso muda de destinatário conforme o seu lado da parceria.

Os que mais mudam o seu dia:

| Notificação | Quando avisa | Canal padrão | Nível padrão |
| --- | --- | --- | --- |
| Repasse recebido (reserva) | Você recebeu um pedido para executar | Responsável pela operação | Importante |
| Repasse aceito pelo parceiro | O parceiro topou executar o pedido que você repassou | Responsável pela operação | Importante |
| Repasse recusado pelo parceiro | O parceiro recusou, com o motivo — a operação volta para você | Responsável pela operação | Importante |
| Prazo de aceite do repasse estourou | O parceiro não respondeu a tempo e a operação voltou para você | Responsável pela operação | Importante |
| Parceiro desistiu da reserva | Ele já tinha aceitado e desistiu, com o motivo | Responsável pela operação | Importante |
| **Parceiro concluiu a entrega ou retirada** | O parceiro **cumpriu** uma parada da operação que você repassou | Responsável pela operação | Informativo |
| **Parceiro não cumpriu a entrega ou retirada** | O parceiro **pulou** uma parada, com o motivo informado por ele | Responsável pela operação | **Importante** |
| A operação repassada mudou | O orçamento de um pedido já repassado foi editado | Responsável pela operação | Importante |
| Reserva no galpão do parceiro não confirmada | O material não conseguiu ser reservado no estoque da parceira | Responsável pela operação | Importante |
| Acordo aguardando aprovação / Acordo ativado | Um acordo espera a outra parte, ou passou a valer | Responsável pela operação · Toda a organização | Importante |
| Parceiro revogou o acordo | Ele saiu de um acordo já ativo | Toda a organização | Importante |
| Proposta de parceria recebida · Parceria encerrada | Alguém propôs (ou rompeu) o vínculo entre as duas organizações | Toda a organização | Importante |
| Repasse pago | Um repasse foi pago ao parceiro | Responsável pela operação | Informativo |
| Repasse manual aguarda sua confirmação | Para o **parceiro**: a organização declarou ter pago o repasse dele **por fora** do sistema — ele confirma o recebimento ou contesta | Responsável pela operação | Importante |
| Repasse manual confirmado | Para quem **repassou**: o parceiro confirmou o recebimento do repasse pago por fora — a taxa da plataforma daqueles repasses passa a ser devida | Toda a organização | Importante |
| Repasse manual contestado | Para quem **repassou**: o parceiro nega ter recebido o pagamento declarado, com o motivo — o saldo volta a contar como devido | Toda a organização | Importante |
| Taxa da plataforma quitada | Confirma o pagamento da taxa da plataforma dos repasses pagos por fora | Toda a organização | Informativo |

{% hint style="success" %}
**Os dois que valem ligar primeiro** são o *Parceiro concluiu* e o *Parceiro não cumpriu*. Quem responde ao cliente é **você**, não o parceiro — e antes eles a única forma de descobrir uma entrega frustrada era o telefone do cliente tocando. O "não cumpriu" chega como **Importante** e traz o **motivo** que o parceiro informou em campo.
{% endhint %}

A lista completa do módulo é maior que esta tabela (acordos, prazos, penalidades de reputação, cancelamentos, frete alterado, e as versões "parceria interna" de cada um) — abra o grupo **Parceria** na tela para vê-la inteira. Para entender o que cada aviso representa no negócio, comece por [Rede de Parceiros: a visão](../parcerias/visao-geral.md).

### Financeiro {#avisos-do-financeiro}

| Notificação | Quando avisa | Canal padrão | Nível padrão |
| --- | --- | --- | --- |
| Nota fiscal recusada | A SEFAZ ou a prefeitura **recusou** uma nota emitida pelo sistema. O motivo vem no aviso; a correção e o reenvio acontecem na Central de notas | Toda a organização | Importante |
| Nota fiscal presa no envio | Uma nota ficou aguardando o provedor fiscal e o sistema desistiu de conferir sozinho, depois de várias tentativas — alguém precisa verificar a situação dela | Toda a organização | Importante |
| Lançamento cancelado com nota fiscal ativa | Uma conta a receber foi cancelada, mas a nota fiscal dela **segue autorizada** — verifique se a nota também precisa ser cancelada | Toda a organização | Importante |
| Fatura do cartão fechou | A fatura de um cartão de crédito da empresa fechou: o total do ciclo está definido e o vencimento se aproxima. Atalho: **Ver faturas** | Quem cuida do financeiro | Importante |
| Fatura do cartão a vencer | A fatura de um cartão **vence hoje** e ainda tem saldo em aberto. Atalho: **Ver faturas** | Quem cuida do financeiro | **Crítico** |

Os avisos fiscais só disparam para quem emite notas pela [Integração Fiscal](integracao-fiscal.md). Os de cartão vão para quem tem a competência *Pagar contas* — no canal [Quem cuida do financeiro](canais-de-notificacao.md#canais-padrao) dá para estreitar o público ou escolher nomes. Veja como as faturas do cartão funcionam em [Cartões](../financeiro/cartoes.md).

### Estoque {#avisos-de-estoque}

| Notificação | Quando avisa | Canal padrão | Nível padrão |
| --- | --- | --- | --- |
| Item na sua bancada de manutenção | Um item entrou na bancada e ganhou responsável. Os itens são distribuídos **em rodízio** entre os operadores de manutenção do galpão, para o trabalho ficar parelho — e o aviso vai para quem recebeu. Atalho: **Abrir a bancada** | Responsável pela operação | Importante |

Veja o que acontece na bancada em [Manutenção: o desfecho do reparo](../estoque/manutencao.md).

{% hint style="info" %}
Esta lista cresce com o tempo. Se há um aviso que faria diferença para a sua operação, fale com o suporte.
{% endhint %}

## Vendo e gerenciando os avisos recebidos {#avisos-recebidos}

Toque no **sino** (no topo) para abrir as **suas** notificações. No alto há três abas: **Todas**, **Não lidas** (com a contagem) e **Novidades**.

A lista não separa os avisos por módulo, e sim pelo que eles pedem de você — em três grupos:

| Grupo | O que entra | Ordem |
| --- | --- | --- |
| **Precisa de ação** | Avisos **não lidos** de nível **Crítico** ou **Importante** | Os mais urgentes primeiro |
| **Para saber** | Avisos **não lidos** de nível **Informativo** | Os mais recentes primeiro |
| **Lidas** | Tudo o que você já leu ou resolveu | Os mais recentes primeiro |

Cada aviso ocupa **uma linha**, com o ícone do módulo pintado na **cor do nível** — o olho lê "vermelho na logística" antes de ler qualquer palavra. Tocar na linha **só abre o detalhe**: no computador ele aparece ao lado da lista; no celular, numa folha.

**Ler é um gesto seu.** O aviso sai de "Precisa de ação" ou "Para saber" quando você toca em **Marcar como lida** ou quando abre a **ação** dele (por exemplo, *Abrir a fatura*), que já conta como lido. Para limpar tudo de uma vez, use **Marcar todas como lidas**. **Nada some** — o que foi lido vai para o grupo **Lidas**, e o histórico permanece.

{% hint style="info" %}
**E a aba Novidades?** Ela não traz avisos da sua operação: mostra **o que está mudando no LocFlow** — cada pedido de melhoria numa trilha de cinco etapas (*Na fila → Em desenvolvimento → Em testes → Lançando → No ar*), que também serve de filtro. Veja [Novidades do LocFlow](../ajuda/novidades-do-sistema.md).
{% endhint %}

## Situações reais

- **"Abro o sino e não sei por onde começar."** Comece pelo grupo **Precisa de ação**: são os avisos críticos e importantes que você ainda não leu, os mais urgentes no topo. O resto é recado, em **Para saber**.
- **"Uma nota fiscal foi recusada e eu só descobri dias depois."** Confira se o aviso **Nota fiscal recusada** (grupo **Financeiro**) está ligado e se o canal dele alcança quem emite as notas.
- **"Quero ver como um alerta vai aparecer antes de ligar."** Abra o aviso, troque entre os níveis e olhe a prévia **COMO O AVISO CHEGA** — ela mostra o modal, o aviso discreto ou o sino conforme o nível.
- **"Mudei o nível de um aviso e me arrependi."** Tente sair sem salvar: o LocFlow pergunta **"Salvar alterações?"** e deixa **descartar**, voltando à última versão salva. Ou reescolha o nível original para voltar ao padrão.
- **"Os operadores estão sendo interrompidos por um aviso pouco urgente."** Baixe o nível dele para **Informativo** (só conta no sino) ou troque o canal para um público mais estreito — e salve.
- **"Esse aviso aqui está apagado e não consigo mexer."** Ele está na seção **Em breve**: é só visualização, ainda não dá para ligar/ajustar.
- **"Estou cobrando atraso na mão, cliente por cliente."** Abra **Parcela vencida há X dias** e confira os lembretes em **Quando lembrar**. Sem mexer, você já é avisado aos 3, 10 e 30 dias de atraso, com o valor em aberto e o atalho para a fatura.
- **"Meu time reclama que o aviso de atraso é demais."** No mesmo bloco, tire os lembretes que não usa (ou deixe só um). Lista vazia desliga o lembrete e mantém o aviso configurado, pronto para você voltar atrás.
- **"Configurei o aviso, mas não sei se ele chega a alguém."** Abra o **canal** que o aviso usa (em **Gerenciar canais**) e toque em **Testar canal**: um aviso de teste sai na hora para quem o canal alcança — no sino e no celular — e a folha mostra o resultado pessoa por pessoa. Veja [Testar um canal](canais-de-notificacao.md#testar-um-canal).

## Próximo passo

- [Canais de notificação](canais-de-notificacao.md) — crie e edite **quem recebe** cada aviso (toda a organização, por competência, o responsável da operação) e **como** (todo o grupo ou rodízio) — e **teste** um canal para confirmar quem ele alcança.
- [Colaboradores e acessos](colaboradores-e-acessos.md) — atribua **competências** às funções para que os canais por competência entreguem só a quem deve.
- [Minha conta e preferências](minha-conta.md#preferencias-pessoais) — o **som** e o **pop-up** de cada pessoa, que não dependem desta página.
