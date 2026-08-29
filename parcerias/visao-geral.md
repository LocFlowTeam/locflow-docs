---
icon: handshake
description: A porta da Rede de Parceiros — venda mais sem frota própria ou execute para quem vende, num espaço de trabalho separado da sua operação.
---

# Rede de Parceiros: a visão

**Onde fica:** no **alternador de espaço de trabalho** — o seletor **Operação ↔ Rede de Parceiros** no topo do menu lateral (telas largas) ou na aba **Menu** (celular).

Nenhuma operação de locação cresce sozinha. Uma hora você fecha um pedido longe demais para a sua estrutura; outra hora sobra caminhão e falta venda. A **Rede de Parceiros** existe para os dois lados dessa moeda: **vender mais sem ter frota e galpão próprios** — repassando a execução a quem tem — e **executar para quem vende** — recebendo pedidos de outras operações e ganhando por eles.

Os papéis têm nome: quem é dono do cliente e do orçamento é o **vendedor**; quem entrega, retira e cuida do material é o **parceiro logístico**. A mesma organização pode ser um num pedido e outro no seguinte.

{% hint style="info" %}
**Parceiro não é colaborador.** Quem trabalha no dia a dia da sua organização — com papel e permissões que você define — é um [colaborador](../configuracoes/colaboradores-e-acessos.md). O parceiro é gente **de fora**: outra operação, com quem você combina termos para fazer negócio junto.
{% endhint %}

## As linhas de responsabilidade {#linhas-de-responsabilidade}

Esta é **a ideia que organiza todo o resto**. Vale a pena gastar dois minutos aqui: ela explica por que certos botões somem quando você repassa um pedido, e por que outros aparecem para o parceiro.

Um pedido em parceria não é dividido em "metade sua, metade dele". Ele é dividido em **linhas de responsabilidade** — e cada linha tem **um dono só**:

| Linha | De quem é | O que ela inclui |
| --- | --- | --- |
| **Linha logística** | **Parceiro logístico** | Entregar, retirar, cuidar do material, montar e executar o roteiro, **planejar os movimentos** — e, quando o acordo permite, **receber o cliente na porta**. |
| **Linha comercial** | **Vendedor** | O cliente é dele, o orçamento é dele, o preço ao cliente é dele. |
| **Linha de cobrança** | **Vendedor** | A fatura é dele, a relação de crédito com o cliente é dele, a cobrança é dela. |

A regra prática que cai disso: **quem é dono da linha manda nela, e o outro não mexe.**

{% hint style="warning" %}
**Sumiu o botão de dividir/consolidar/reatribuir o movimento de um pedido que eu repassei?** Sumiu de propósito, e essa é a consequência mais visível das linhas. Depois que o parceiro **aceita** o repasse, o **plano de movimentos daquele pedido passa a ser dele** — inclusive dividir, consolidar, reatribuir e ressincronizar. Você também deixa de poder **marcar manualmente** a operação como entregue ou retirada.

O motivo é concreto: aquele plano é o que o roteiro **dele** executa. Fechar o movimento pela sua tela desfechava, de forma irreversível, a folha que o motorista dele ainda ia cumprir — e ele chegava ao cliente com a entrega já dada como feita.

Você não fica no escuro: o detalhe da reserva passa a mostrar **o andamento da rota do parceiro**, e você é **avisado** quando ele conclui (ou pula) a entrega. Veja [Depois do aceite](repassando-um-pedido.md#execucao).
{% endhint %}

### Interno e externo: mesma responsabilidade, capacidade diferente {#interno-e-externo}

Um erro comum é achar que o parceiro **externo** (o convidado) é "meio parceiro" e o **interno** (a outra organização) é "parceiro de verdade". Não é assim. Os dois carregam a **mesma linha logística** — **os dois roteirizam**, os dois executam, os dois respondem pelo material.

O que muda entre eles é **capacidade**, não responsabilidade:

| | Parceiro externo | Parceiro interno (org↔org) |
| --- | --- | --- |
| **Responsabilidade** | Linha logística, inteira | Linha logística, inteira |
| **Roteiriza** | Sim | Sim |
| **Estoque próprio no sistema** | Não — o material sai do **seu** galpão | Sim — o material sai do **galpão dela** |
| **Mapa, créditos de rota, verificação de presença** | Usa a estrutura da sua conta | Tem a própria |
| **Onde os dados dele vivem** | Dentro da **sua** conta | Na **conta dela** |

{% hint style="info" %}
**Uma diferença honesta que ainda existe:** o **balcão** (o cliente que retira e devolve no galpão, com conferência na hora) hoje só é operado pelo parceiro **externo**. O parceiro interno ainda não alcança essa tela. É uma fatia que falta, não uma decisão de produto — e não muda de quem é a responsabilidade.
{% endhint %}

## Um espaço de trabalho só para a rede {#espaco-de-trabalho}

Parceria é um assunto diferente do dia a dia — aqui você não atende cliente, você se conecta a outras empresas. Por isso a Rede vive num **espaço de trabalho próprio**, separado da Operação: o menu da locadora fica limpo, e o que é rede fica junto do que é rede. Ao alternar, até a cor muda — a Rede tem o seu **acento visual (magenta)**, para você sempre saber onde está.

No celular, a barra de baixo mostra quatro atalhos: **Início** (o hub da Rede) · **Descobrir** · **Acordos** · **Menu**. O **Menu** abre a lista completa, organizada por **intenção** — o que você quer fazer, não o tipo de dado:

| Grupo | O que tem dentro |
| --- | --- |
| **Descobrir & Conectar** | Descobrir parceiros · Vínculos · Meu perfil público · Minha reputação |
| **Operar** | Avaliações de parceria · Acordos · Parceiros externos |
| **Financeiro da rede** | Meus Ganhos · Repasses · Conta de recebimento |

{% hint style="info" %}
**E o dinheiro?** **Repasses** (vendedor) e **Meus Ganhos** (parceiro) são dinheiro de verdade da sua operação — vivem no **Financeiro**, com um selo **"Rede"**, e aparecem no espaço da Rede como atalhos fixos. Um assunto, dois caminhos até ele.
{% endhint %}

## Os dois níveis de parceria {#dois-niveis}

A Rede tem dois níveis, pensados para dois momentos:

* **Parceria externa** — o parceiro é uma pessoa **convidada por link** que trabalha **dentro da sua conta**, com um papel fixo e restrito de parceiro. Ideal para o motorista ou a transportadora que não usa (ainda) um sistema próprio.
* **Parceria interna (org↔org)** — as **duas partes são organizações LocFlow de verdade**, cada uma na sua conta, conectadas por um **vínculo** de parceria (uma propõe, a outra aceita). Os acordos internos casam os dois catálogos **item a item**, e o estoque de quem executa entra na jogada de verdade.

| | Parceria externa | Parceria interna (org↔org) |
| --- | --- | --- |
| **Quem é o parceiro** | Uma pessoa convidada por link | Outra organização LocFlow |
| **Conta própria** | Não — trabalha dentro da **sua** conta | Sim — cada lado na sua |
| **O que ele enxerga** | As operações repassadas a ele e os preços do acordo | A própria operação inteira; da sua, o que você repassa e os preços do acordo |
| **Catálogo e estoque** | Os **seus** | Os **dela** — itens mapeados pelo acordo, estoque reservado no galpão dela |
| **Como começa** | Link de convite | Perfil público → propor parceria → vínculo aceito |
| **Para quem** | Autônomo, motorista, transportadora sem sistema | Duas empresas estabelecidas |

{% hint style="success" %}
**Um nível leva ao outro.** O parceiro externo que cresce e cria a própria organização pode **promover** o acordo para org↔org — e a [reputação](reputacao-e-boas-praticas.md) acumulada **carrega junto**, sem recomeçar do zero. Veja [Entrando na rede](entrando-na-rede.md).
{% endhint %}

## O que o parceiro vê (e o que ele não vê) {#o-que-o-parceiro-ve}

Esta é a pergunta que todo dono de locadora faz antes de aceitar a primeira parceria — e ela merece resposta direta, sem promessa bonita que se desfaz no primeiro repasse.

**O parceiro vê o preço ao cliente dos itens que estão no acordo.** Isso é decisão de produto, não descuido: o acordo diz "você recebe R$ 300 por esta mesa" e o seu cliente paga R$ 500 por ela — sem o R$ 500, a frase "você recebe 60%" não significa nada, e o parceiro estaria assinando um combinado que não consegue avaliar. Um acordo é uma negociação entre duas empresas; negociação com um lado cego não é negociação.

| O parceiro **vê** | O parceiro **não vê** |
| --- | --- |
| O preço ao cliente **dos itens do acordo** e o repasse dele em cada um | Os **seus outros clientes** e a sua carteira |
| A operação repassada a ele: itens, quantidades, endereços, datas, nome do contato | Os **seus outros orçamentos** — mesmo os do mesmo cliente |
| **Quanto ele ganha** naquela operação — bruto, taxa e líquido | O **total** da operação (a soma final do pedido), a menos que o acordo o autorize a cobrar na rua |
| A **divisão da taxa da plataforma** no acordo de vocês: a fatia dele e a sua, lado a lado | **Quanto a plataforma faturou em reais** na operação inteira, e o que ela ganha nos acordos que não são o dele |
| A fatura do cliente **apenas** quando o acordo o autoriza a [cobrar na rua](cobranca-na-rua.md) — aí ele vê quanto o cliente deve e pode gerar o **seu** PIX daquela parcela | Como o seu preço final se formou: descontos aplicados, histórico comercial, negociação |
| | A fatura do cliente, quando **não** há cobrança na rua — só o sinal de "está paga ou em aberto" |

{% hint style="info" %}
**A régua para lembrar:** o parceiro enxerga **o negócio que ele está fazendo com você** — inteiro, para poder decidir. Ele não enxerga **o seu negócio**.
{% endhint %}

## Fornecedores de frete: um caso à parte {#fornecedores-de-frete}

Antes de qualquer parceria, existe o jeito mais simples de usar estrutura de fora: o **fornecedor de frete**. É a transportadora terceira que **você cadastra e gerencia por inteiro** — a frota dela, as regras de preço dela — e que **não tem login** no LocFlow: quem opera tudo é você, e ela aparece como opção na composição do frete do orçamento.

Como ela não é uma operação independente — é um **cadastro** de terceiro que a sua operação usa —, essa página vive em **Cadastros Base › Fornecedores**, junto de Contatos e Catálogo, e não no espaço da Rede. Detalhes em [Fornecedores de frete](fornecedores-de-frete.md).

## O mapa da seção {#mapa-da-secao}

| Página | Em uma frase |
| --- | --- |
| [Entrando na rede](entrando-na-rede.md) | Como começar: convidar um parceiro externo pelo link, montar o perfil público, descobrir organizações, propor e encerrar o vínculo. |
| [Acordos de parceria](acordos-de-parceria.md) | Os termos do trabalho conjunto — itens e preços, quando e quanto se paga, prazos de aceite e desistência, frete e cobrança na rua. |
| [Repassando um pedido](repassando-um-pedido.md) | O passo a passo de repassar um pedido ganho: esboço grátis, comparativo de candidatos, aceite ou recusa, e o que muda na execução. |
| [O dinheiro da parceria](dinheiro-da-parceria.md) | Como o valor se reparte entre vendedor e parceiro — a conta do repasse, a taxa de plataforma e os caminhos da liquidação. |
| [Cobrança na rua](cobranca-na-rua.md) | Quando o acordo permite ao parceiro receber o cliente na porta — o que ele vê, como o dinheiro volta e as regras que protegem os dois lados. |
| [Estoque na parceria](estoque-na-parceria.md) | Num pedido repassado a uma organização parceira, de onde sai o material — e o que reserva e libera o estoque dela. |
| [Reputação e boas práticas](reputacao-e-boas-praticas.md) | Como a confiança é medida na rede — avaliações, selos, índice de confiabilidade — e o que ela cobra **dos dois lados**. |
| [Parceiro Logístico Externo](parceiro-logistico-externo.md) | O convidado que executa dentro da sua conta: o papel restrito, o galpão dele e o recebedor do repasse. |
| [Fornecedores de frete](fornecedores-de-frete.md) | Transportadoras sem login que você precifica e aciona na composição do frete. |

## Próximo passo {#proximo-passo}

- Vai trabalhar com alguém de fora pela primeira vez? Comece por [Entrando na rede](entrando-na-rede.md).
- Só precisa de caminhão para uma entrega? [Fornecedores de frete](fornecedores-de-frete.md) resolve sem parceria formal.
- Já tem parceiro e quer repassar um pedido? Vá direto a [Repassando um pedido](repassando-um-pedido.md).
- Dúvida em algum termo? Consulte o [glossário](../primeiros-passos/glossario.md).
