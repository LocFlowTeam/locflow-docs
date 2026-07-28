---
icon: layer-group
description: Confira a contagem, mande para reparo ou transfira vários itens de uma vez — com o limite de 25 por vez e o que acontece quando uma linha não passa.
---

# Operar vários itens de uma vez

Depois de um evento, raramente você mexe em um item só: volta a bandeja inteira, e cada peça precisa ser conferida, mandada para o reparo ou levada para outro galpão. Fazer isso um a um é onde o tempo se perde — e onde alguém esquece de registrar o último.

No **Estoque → Itens**, cada linha tem uma **caixinha de seleção**. Marque os [bens móveis](../primeiros-passos/glossario.md) que quer mexer e toque em **Operar**.

## O que dá para fazer em lote

<table><thead><tr><th width="220">Operação</th><th>O que ela faz</th></tr></thead><tbody><tr><td><strong>Conferir contagem</strong></td><td>Você digita quanto contou de cada item; o sistema corrige o saldo pela diferença.</td></tr><tr><td><strong>Enviar para reparo</strong></td><td>Manda a remessa para a oficina. Os itens saem do disponível até alguém <a href="manutencao.md">concluir o reparo</a> — voltando ao estoque, sendo descartados ou reclassificados.</td></tr><tr><td><strong>Transferir entre galpões</strong></td><td>Despacha tudo para o mesmo destino. O material sai daqui na hora e entra lá quando alguém confirmar a chegada.</td></tr></tbody></table>

{% hint style="info" %}
**A avaria continua item a item.** Ela é a exceção, quase sempre de uma peça só, e cada uma tem seu motivo e pode virar cobrança do cliente — decisões que pedem atenção individual. Registrar avarias em série convidaria ao erro caro.
{% endhint %}

## O limite: 25 itens por vez

Você pode selecionar até **25 itens** de uma vez. Ao chegar lá, o contador muda para **"25 de 25 — o máximo por vez"**, e as caixinhas dos itens não escolhidos ficam apagadas até você desmarcar algum.

Se você usar a caixinha **"todos"** com mais de 25 itens na tela, o LocFlow marca os 25 primeiros e **avisa quantos ficaram de fora** — nunca marca em silêncio o galpão inteiro.

{% hint style="warning" %}
**Por que existe esse limite.** Uma operação em lote é aplicada com **um toque** e mexe no seu estoque de verdade. Vinte e cinco itens é o quanto ainda dá para **conferir com os olhos** antes de mandar; desfazer é caro, porque cada correção volta como outra operação. O limite existe para proteger você do toque distraído, não para atrapalhar o trabalho.
{% endhint %}

Precisa mexer em mais? Opere estes 25, e depois selecione os próximos — a seleção se esvazia sozinha quando você fecha a folha.

## Um item pode virar mais de uma linha

Ao abrir a folha, você verá **uma linha por lote**, não por produto. Um mesmo item guardado em dois galpões (ou vendido em duas condições — novo e seminovo) aparece separado, porque são estoques diferentes: você decide quanto sai de cada um.

Por isso a folha às vezes mostra mais linhas do que itens selecionados. É esperado.

## Quando uma linha não passa

O envio é **parcial de propósito**. Se uma linha for recusada — não há material suficiente no galpão, ou há um pedido confirmado que precisa daquele item durante o reparo —, as **outras continuam valendo**.

O que aconteceu fica visível na própria folha:

- as linhas que entraram **somem** da lista;
- as recusadas **ficam**, com o número que você digitou e o **motivo** logo abaixo.

Assim você corrige só o que precisa, sem recomeçar a conferência do zero.

{% hint style="success" %}
**Se a internet cair no meio.** Pode tentar de novo sem medo: o LocFlow reconhece o reenvio e **não registra duas vezes** o que já tinha entrado. É por isso que a mensagem diz "tente de novo" em vez de prometer que nada foi alterado — quando a resposta se perde, ninguém pode garantir o que chegou do outro lado, mas duplicar não vai.
{% endhint %}

## O que cada folha pergunta

- **Contagem** — quanto você contou. A diferença aparece na hora, em verde quando bate, e em vermelho quando falta.
- **Reparo** — uma **previsão de volta** para a remessa inteira (é um caminhão só indo para a oficina). Sem previsão, o material fica indisponível até você concluir o reparo.
- **Transferência** — **para onde vai**. O destino começa vazio de propósito: ele decide para onde o material segue fisicamente. Escolhido o galpão, os itens que já estão lá saem da folha sozinhos.

Em todas, tocar no número ao lado do campo preenche o lote inteiro — o caso comum é levar tudo.

## Próximo passo

Entenda o que cada número da tela significa em [Posição e previsão de estoque](posicao-e-previsao.md), o que acontece quando o item volta do reparo em [Manutenção: o desfecho do reparo](manutencao.md), e a regra que impede reserva dupla em [Galpões e disponibilidade](galpoes-e-disponibilidade.md).
