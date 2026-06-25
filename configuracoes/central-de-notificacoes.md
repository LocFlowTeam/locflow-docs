---
icon: bell
description: Avise as pessoas certas, na hora certa. Defina o que dispara cada aviso, quem recebe e com que destaque — e prévia de como ele chega.
---

# Central de Notificações

A **Central de Notificações** avisa as pessoas certas, na hora certa, sobre o que acontece no seu negócio — de um valor a favor do cliente a uma parada pulada na rota. Você define **quais avisos** sua organização recebe, **quem** recebe cada um e **com que destaque** — e ainda vê uma **prévia de como o aviso chega** antes de salvar.

{% hint style="info" %}
As notificações são da **organização**, não de um usuário específico. Quem decide para quem cada aviso vai é o **canal** (quem recebe + como). Cada pessoa vê, na própria Central, só os avisos destinados a ela.
{% endhint %}

## Como cada notificação funciona

Toda notificação tem quatro partes:

| Parte | O que é |
| --- | --- |
| **Acionador** | O que dispara o aviso: um **evento** (ex.: a equipe saiu do galpão) ou uma **data** (ex.: "3 dias antes do vencimento"). |
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
{% endhint %}

## Ligar, desligar e ajustar um aviso {#configurando}

Você chega à configuração por **Ajustes → Central de Notificações** (atalho direto) ou por **Ajustes → Motores → Central de Notificações**. Os avisos ficam **agrupados por módulo** (Cobrança, Logística, Orçamento), com **busca** e um contador de quantos estão ligados em cada grupo. Escolha um aviso para configurá-lo:

1. **Ligar ou desligar** o aviso (o interruptor no topo do detalhe).
2. **Escolher o nível de atenção** (Crítico / Importante / Informativo) — com a prévia atualizando ao vivo.
3. **Escolher o canal** (quem recebe e como). Toque no canal para trocar, ou use **Gerenciar canais** para editar a pool e o roteamento — e reaproveite o mesmo canal em vários avisos.

No topo da tela há uma **legenda dos níveis** (cartões "Crítico / Importante / Informativo") para consulta rápida.

{% hint style="info" %}
As preferências de **som** e **pop-up** não ficam aqui — são **pessoais**, em **Ajustes → Conta → Notificações e avisos**. A configuração desta página é da **organização**.
{% endhint %}

### Alterações não salvas (guard de saída) {#alteracoes-nao-salvas}

A página **só aplica suas mudanças quando você salva**. Enquanto houver ajustes pendentes:

- aparece o sinal **"● Alterações não salvas"** (no computador) ou a barra **"Você tem alterações não salvas"** com o botão **Salvar** (no celular);
- se você tentar **sair, voltar ou trocar de tela**, o LocFlow pergunta **"Salvar alterações?"** — *"Você ajustou notificações que ainda não foram salvas."* — e deixa **salvar** ou **descartar** (voltando à última versão salva).

Depois de salvar, aparece a confirmação **"Salvo"** (e o aviso de pendência some). Esse guard evita que um ajuste importante se perca por um toque distraído.

## "Em breve": avisos que ainda estão chegando {#em-breve}

Alguns avisos aparecem numa seção **"Em breve"**, recolhida no fim da lista, com o selo **Disponível em breve**. Eles são **só para visualização**: você consegue abrir e entender o que farão, mas **não dá para ligá-los nem ajustá-los ainda** — o interruptor e a edição ficam desativados. Conforme cada recurso fica pronto (lembretes por data, pagamento online, mensagens ao cliente), o aviso sai do "Em breve" e passa a ser configurável.

## O que você pode ser avisado (catálogo) {#catalogo}

> A coluna **Status** mostra o que já está disponível e o que está **Em breve** (só visualização).

### Cobrança

| Notificação | Quando avisa | Canal padrão | Nível padrão | Status |
| --- | --- | --- | --- | --- |
| Reembolso ou crédito resolvido | Um valor a favor do cliente virou crédito, vale ou reembolso | Organização | Importante | Disponível |
| Pagamento confirmado | O cliente pagou um valor online | Organização | Importante | Em breve |
| Parcela a vencer | Faltam alguns dias para o vencimento | — | Informativo | Em breve |
| Parcela vencida | A parcela passou da data de vencimento | — | Importante | Em breve |

### Logística

| Notificação | Quando avisa | Canal padrão | Nível padrão | Status |
| --- | --- | --- | --- | --- |
| Saída do galpão | A equipe saiu para iniciar a rota | Organização | Informativo | Disponível |
| Chegada ao galpão | A equipe retornou ao fim do roteiro | Organização | Informativo | Disponível |
| Desvio da rota | Uma parada foi pulada durante a execução | Organização | Importante | Disponível |
| Entrega ou retirada concluída | A equipe concluiu uma parada | Organização | Informativo | Disponível |
| Roteiro precisa de ajuste | O pedido de uma parada mudou (datas, itens ou quem leva) e o roteiro planejado ficou desatualizado | Operadores logísticos | Importante | Disponível |
| Roteiro ajustado em execução | O operador ajustou um roteiro que já estava em andamento | Responsável pela operação | Crítico | Disponível |
| Atendimento no balcão (retirada/devolução) | O cliente retirou ou devolveu os itens presencialmente no balcão | Organização | Informativo | Disponível |
| Movimentos do dia sem roteiro | Toda manhã, quando há entregas ou retiradas com data para hoje (ou atrasadas) que ainda não foram incluídas em um roteiro | Operadores logísticos | Importante | Disponível |

Entenda a fundo o aviso **"Roteiro precisa de ajuste"** (e por que o condutor não recebe a mudança crua) em [Quando um pedido muda depois de fechado](../logistica/quando-um-pedido-muda.md).

### Orçamento

| Notificação | Quando avisa | Canal padrão | Nível padrão | Status |
| --- | --- | --- | --- | --- |
| Novo orçamento para follow-up | Um orçamento foi criado e entra na fila de follow-up | Vendedores | Importante | Disponível |
| Follow-up de lead | Lembrete para retomar o contato antes de uma data do orçamento | — | Importante | Em breve |
| Orçamento prestes a expirar | Faltam alguns dias para o fim da validade | — | Importante | Em breve |
| Aguardando aprovação | Um orçamento ou frete precisa de aprovação manual | — | Importante | Em breve |

{% hint style="info" %}
Esta lista cresce com o tempo. Se há um aviso que faria diferença para a sua operação, fale com o suporte.
{% endhint %}

## Vendendo e gerenciando os avisos recebidos

Toque no **sino** (no topo) para abrir a Central de avisos recebidos. Eles ficam **agrupados por módulo**, com o número de não-lidos, **ordenados por urgência e horário** — os novos e os antigos juntos, para você ter o histórico completo. Cada aviso mostra o **nível** e a **hora** em que foi emitido; o **botão de ação** fica em destaque quando é novo e discreto depois. **Nada some** — o histórico permanece.

## Situações reais

- **"Quero ver como um alerta vai aparecer antes de ligar."** Abra o aviso, troque entre os níveis e olhe a prévia **COMO O AVISO CHEGA** — ela mostra o modal, o aviso discreto ou o sino conforme o nível.
- **"Mudei o nível de um aviso e me arrependi."** Tente sair sem salvar: o LocFlow pergunta **"Salvar alterações?"** e deixa **descartar**, voltando à última versão salva. Ou reescolha o nível original para voltar ao padrão.
- **"Os operadores estão sendo interrompidos por um aviso pouco urgente."** Baixe o nível dele para **Informativo** (só conta no sino) ou troque o canal para um público mais estreito — e salve.
- **"Esse aviso aqui está apagado e não consigo mexer."** Ele está na seção **Em breve**: é só visualização, ainda não dá para ligar/ajustar.

## Próximo passo

- [Canais de notificação](canais-de-notificacao.md) — crie e edite **quem recebe** cada aviso (toda a organização, por competência, o responsável da operação) e **como** (todos ou rodízio).
- [Colaboradores e acessos](colaboradores-e-acessos.md) — atribua **competências** às funções para que os canais por competência entreguem só a quem deve.
- [Motores operacionais](motores-operacionais.md) — onde a Central de Notificações vive, junto dos demais motores da organização.
