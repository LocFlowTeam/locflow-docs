---
icon: boxes-stacked
description: Num pedido repassado a uma parceira, de onde sai o material — a tradução pelo acordo, a reserva no galpão dela e o que libera o estoque.
---

# Estoque na parceria

Quando você repassa um pedido a uma organização parceira, uma pergunta prática decide tudo: **de onde sai o material?** A resposta do LocFlow é direta — **do estoque dela**. Esta página mostra como isso acontece sozinho, sem planilha paralela e sem telefonema para "confirmar se tem".

{% hint style="info" %}
Esta página é sobre a **parceria interna** — quando as duas partes são organizações LocFlow de verdade, conectadas por um vínculo e um [acordo de parceria](acordos-de-parceria.md). No **parceiro externo** (o convidado que trabalha dentro da sua conta), nada disto se aplica: ele não tem estoque no sistema, e o material continua saindo do **seu** galpão, como em qualquer pedido. Veja [Parceiro Logístico Externo](parceiro-logistico-externo.md).
{% endhint %}

## O essencial {#o-essencial}

No momento em que a parceira **aceita** a solicitação de repasse, o material do pedido passa a ser **responsabilidade dela**:

```mermaid
flowchart LR
    A[Parceira aceita o repasse] --> B[LocFlow traduz os itens<br/>pelo mapeamento do acordo]
    B --> C[Reserva no galpão dela<br/>mais perto da entrega]
    C --> D[Seu estoque não move]
```

* O LocFlow **traduz** os itens: cada bem móvel do **seu** catálogo vira o item correspondente do catálogo **dela**, pelo mapeamento item-a-item definido no acordo.
* A quantidade é **reservada no galpão dela mais próximo do endereço de entrega** — como se ela mesma tivesse fechado aquele pedido.
* O **seu estoque não move**. Você vendeu; quem separa, entrega e recolhe o material é a parceira, com os itens dela.

É por isso que a parceria interna escala: você pode fechar um pedido numa cidade onde não tem um único item em prateleira — o material existe do lado de lá, e o sistema cuida de reservá-lo.

## O guard no aceite: sem estoque, sem aceite {#guard-no-aceite}

Aceitar um pedido sem ter o material seria assinar um problema. Por isso o aceite tem uma **trava de disponibilidade**: no momento em que a parceira tenta aceitar, o LocFlow confere se há estoque disponível **na janela da operação** para todos os itens traduzidos.

| Situação do item na parceira | O que acontece no aceite |
| --- | --- |
| **Disponível** na janela | Aceite segue normalmente. |
| **Sem estoque** para a data | O aceite é **barrado**, com a lista exata do que falta. |
| **Nunca cadastrado** no estoque dela | **Não barra** — o aceite passa, com um **aviso**. |
| **Sem par no acordo** (cobertura parcial ou zero) | **Não barra** — mas ela é avisada, antes de aceitar, de **quantos itens da operação ela não fornece**. |

{% hint style="warning" %}
**Kit só passa inteiro.** Se o pedido tem um kit, a trava exige disponibilidade de **todos os componentes**. Faltou um componente na janela, o kit conta como indisponível — e o aceite é barrado do mesmo jeito.
{% endhint %}

A distinção do "nunca cadastrado" é proposital: uma parceira que ainda não usa o controle de estoque do LocFlow não fica impedida de trabalhar — ela só perde a proteção da trava para aqueles itens. O aviso existe justamente para lembrar que, ali, a conferência voltou a ser manual.

## Ter estoque e ter o item no acordo são coisas diferentes {#cobertura}

Este é o ponto que mais confunde, e vale separar bem:

| Pergunta | Nome | Quem resolve |
| --- | --- | --- |
| *O acordo traduz este item para o catálogo dela?* | **Cobertura** | O **vendedor**, mapeando o item no acordo |
| *Ela tem esse item livre na data?* | **Disponibilidade** | A **parceira**, no estoque dela |

Um item **sem par no acordo** simplesmente **não existe** para o razão dela: ele não é traduzido, não é reservado e **não vai ser fornecido por ela** — mesmo que ela tenha dez unidades na prateleira. A responsabilidade por aquele pedaço da carga continua sendo sua.

Por isso a cobertura tem os seus próprios avisos, com **causas que pedem ações opostas**:

| Aviso | O que significa | Quem corrige |
| --- | --- | --- |
| **Cobertura parcial** — *"3 itens desta operação não estão mapeados no acordo com este parceiro"* | Parte da carga não tem par. | **Você**, no acordo. O aviso leva direto lá. |
| **Nenhum item mapeado** | O acordo não traduz nada desta carga. | **Você**, no acordo. |
| **Parceira sem galpão de estoque** | Ela não tem onde reservar nada. | **Ela**. O aviso **não** oferece atalho para o acordo — não há nada errado lá. |

{% hint style="info" %}
**A cobertura avisa, não bloqueia** — a mesma doutrina do "estoque não cadastrado". A lacuna quase sempre é um item novo que ninguém casou ainda, e barrar esconderia isso atrás de um "candidato indisponível". O aviso aparece **nas duas pontas**: no seu comparativo, antes de repassar, e no detalhe da reserva dela, antes de aceitar.
{% endhint %}

## Você vê tudo isso antes de repassar {#disponibilidade-antes-de-repassar}

Não é preciso esperar o aceite para descobrir que faltava material. No **comparativo de repasse** — a tela em que você escolhe para qual parceira mandar o pedido — cada candidata interna já aparece com a situação para a data da operação:

* **Disponível** — o acordo traduz a carga inteira e ela tem o material na janela; caminho livre.
* **Cobertura parcial / nenhum item mapeado / sem galpão** — ela pode aceitar, mas você já sabe **o que ela não leva**, e com um toque vai ao acordo consertar.
* **Sem estoque para a data** — a candidata aparece **desabilitada**: repassar seria convidá-la a um aceite que a trava vai barrar.
* **Estoque não cadastrado** — ela pode aceitar, mas você vê o **aviso** de que a disponibilidade não foi conferida pelo sistema.

Assim a decisão de quem executa já nasce informada — e corrigir no comparativo custa infinitamente menos do que corrigir no galpão, na véspera.

## Quando a reserva no galpão dela não se confirma {#espelho-nao-confirmado}

Quase sempre o espelho funciona. Mas existe um caso em que ele **não** acontece — e ele é perigoso justamente porque, sem aviso, os dois lados achariam que está tudo coberto: a reserva já foi aceita, o **seu** estoque já foi liberado, e **o razão dela não segurou nada**.

Isso acontece quando há um impedimento permanente do lado de lá:

* a parceira **não tem galpão** de estoque cadastrado;
* o produto traduzido **não existe** no estoque dela;
* o item **não tem par** no acordo.

{% hint style="warning" %}
**Os dois lados são avisados, com destaque de importante:**

* para quem repassou: **"Reserva no galpão do parceiro não confirmada"** — a operação parece coberta, mas o estoque dele não segurou nada;
* para a parceira: **"Operação aceita que seu estoque não cobre"**.

Recebeu um desses? Não deixe para o dia da entrega. Ou o material é conferido à mão entre vocês, ou a lacuna é fechada no acordo (mapeamento) ou no estoque dela (galpão e produto cadastrados).
{% endhint %}

## Devolução, desistência e cancelamento {#devolucao-e-liberacoes}

A reserva no estoque da parceira acompanha o ciclo do pedido do começo ao fim:

| O que aconteceu | Efeito no estoque da parceira |
| --- | --- |
| **Cliente devolveu** o material (locação) | Os itens **voltam ao estoque dela**, seguindo o desfecho normal da devolução. |
| Parceira **recusou**, **desistiu**, o prazo de aceite **expirou** ou o repasse foi **cancelado** | A reserva espelhada é **liberada** — os itens voltam a ficar disponíveis para outros pedidos dela. |
| Material **já entregue** ao cliente | Só volta com a **devolução real** — cancelar o vínculo no papel não teletransporta item que está na casa do cliente. |

{% hint style="success" %}
**Nada fica preso à toa.** Toda saída de cena do repasse — recusa, desistência, expiração, cancelamento — devolve a disponibilidade na hora. A parceira nunca fica com estoque travado por um pedido que não vai acontecer.
{% endhint %}

## Por porte {#por-porte}

| Se você é… | O que muda para você |
| --- | --- |
| **Autônomo / micro** | Nada a configurar: repassou, a parceira aceitou, o material é problema dela — e o sistema confirma que ela tem. |
| **Médio** | Use a **cobertura e a disponibilidade** no comparativo para escolher a parceira certa por data, não só por preço — e mantenha o mapeamento do acordo em dia conforme o seu catálogo cresce. |
| **Grande / rede** | O espelho por galpão mais próximo da entrega vira logística de verdade: cada pedido repassado reserva onde faz sentido operar, sem ninguém abrir planilha. |

## Próximo passo {#proximo-passo}

* O mapeamento item-a-item que faz a tradução vive no [acordo de parceria](acordos-de-parceria.md).
* Como o seu próprio estoque reserva e libera: [Galpões e disponibilidade](../estoque/galpoes-e-disponibilidade.md) e [Posição e previsão de estoque](../estoque/posicao-e-previsao.md).
* Ainda não conhece os dois modelos de parceria? Comece pela [visão geral](visao-geral.md).
