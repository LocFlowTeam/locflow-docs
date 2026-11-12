---
icon: hourglass-half
description: O material que saiu da bancada avaliado, mas sem destino decidido — como ele chega à quarentena, quem decide e como os números do estoque o contam.
---

# Quarentena: o material que espera uma decisão

Na bancada de manutenção, nem toda peça tem resposta óbvia. A solda tem uma trinca fina — compromete ou não? O tecido manchou — ainda dá para alugar? Quem está com a ferramenta na mão nem sempre tem a alçada para decidir se aquilo vai para o lixo ou para a venda de usados. A **quarentena** existe para isso: **separar em vez de arriscar**, e deixar a decisão para quem pode tomá-la.

A tela fica em **Estoque › Quarentena** — *"Separado, esperando decisão"*.

## Como o material chega aqui

Pela [bancada de manutenção](manutencao.md). Ao concluir o reparo de um lote, quem avalia escolhe a saída **Separar em quarentena** e escreve o **motivo** — obrigatório, porque é a única coisa que o próximo leitor vai ter (*"Trinca fina na solda — não sei dizer se compromete"*). *Quem decide o destino vê esta frase na tela Quarentena.*

Não há botão de "criar" na Quarentena: ela é uma **fila de trabalho**, formada pelo que sai da bancada.

## Enquanto espera

| Pergunta | Resposta |
| --- | --- |
| Pode ser prometido a um pedido? | **Não.** Ele não conta como disponível |
| Ainda está em reparo? | **Não.** Já saiu da bancada |
| Continua no meu patrimônio? | **Sim.** Está separado, não removido |
| Conta no "no local"? | **Sim.** Ele está no galpão — conta no local e no "ao todo" |

No [Painel de Estoque](painel.md), esse material aparece na coluna **Quarentena** e no filtro **Em quarentena** da lista de Itens, e na linha de fatos da Visão geral (*"… 2 em quarentena · …"*).

{% hint style="warning" %}
**Na contagem, não conte o que está em quarentena.** Ao conferir a contagem, o que está separado não entra: ele já saiu do saldo da prateleira quando foi para a bancada. Contá-lo junto faria você "achar" sobra que não existe.
{% endhint %}

## A fila

* Duas abas: **Em quarentena** (com a quantidade) e **Resolvidos**.
* **O mais antigo primeiro.** Aqui o tempo parado é decisão que ninguém tomou — por isso o que espera há mais tempo fica no topo. Cada item diz há quanto tempo espera e quem o separou.
* Com mais de um galpão, chips filtram por local.

## Decidir o destino

Toque num item da fila e use **Decidir o destino**. As unidades saem da quarentena por uma de três portas:

| Decisão | O que acontece |
| --- | --- |
| **Voltar ao estoque** | Avaliado e aprovado — o material volta ao disponível |
| **Descartar** | Sem conserto — baixa permanente do patrimônio. Pede **O que aconteceu?** e permite **cobrar o cliente pelo descarte** |
| **Reclassificar** | Serve para outro uso — por exemplo, sai do aluguel e vira venda usada. Pede **Para onde vai?** |

**A decisão pode ser parcial.** Dez unidades separadas não precisam do mesmo destino: se 3 delas são sucata e as outras 7 podem voltar, informe em **Quantas unidades decidir agora?** e decida em dois passes, cada um com a sua quantidade. O item só sai da fila quando a última unidade tiver destino.

Cada decisão abre na mesma janela das outras operações: o cabeçalho na cor da saída, o lote como contexto, a prévia do que vai acontecer (*"3 unidades saem do patrimônio"*) e o botão que diz por escrito o que falta (*"Descreva o que aconteceu"*, *"Escolha um destino diferente de onde está"*). **Voltar** nunca trava.

## Quem separa não decide

A quarentena separa **quem avalia** de **quem decide**:

| Papel pronto | O que pode fazer |
| --- | --- |
| **Operador de Manutenção** | Manda material para a quarentena. Vê a fila, mas não decide o destino |
| **Encarregado de Manutenção** | Tudo o que o operador faz e mais: devolve ao estoque, descarta e reclassifica o que está em quarentena |

Se você vê a fila mas nenhum botão de decisão, não é defeito: descartar e reclassificar **mexem no patrimônio**, e quem administra a conta define quem faz isso. Veja [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md).

{% hint style="info" %}
**Não achou a Quarentena no menu?** Ela fica guardada enquanto não há nada esperando decisão, e aparece sozinha quando alguém separa material. Para mostrá-la mesmo vazia, use **Personalizar** no menu.
{% endhint %}

{% hint style="success" %}
**Por que isso te faz faturar mais:** sem a quarentena, a peça duvidosa voltava ao estoque "por via das dúvidas" — e ia parar no evento de um cliente — ou ficava esquecida numa ordem aberta. Separada e com motivo escrito, ela chega a quem decide, e o material bom volta a render.
{% endhint %}

## Próximo passo

Veja de onde o material vem em [Manutenção: o desfecho do reparo](manutencao.md), como os números o contam em [O estoque de agora e a previsão](posicao-e-previsao.md#agora) e o que cada decisão registra em [Cada movimentação, em detalhe](posicao-e-previsao.md#movimentacoes).
