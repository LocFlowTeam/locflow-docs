---
icon: wrench
description: A bancada de manutenção e as quatro saídas de um lote em reparo — voltar ao estoque, descartar com motivo (e cobrar o cliente), reclassificar ou separar em quarentena —, com conclusão parcial.
---

# Manutenção: o desfecho do reparo

Nem todo item que sai para o conserto volta do mesmo jeito. A cadeira pode voltar boa, pode voltar sem conserto possível, pode voltar servindo só para outra coisa — a almofada muito usada não vale mais alugar, mas ainda dá para vender como usada — ou pode deixar dúvida em quem avaliou. O LocFlow trata esses casos como **saídas** diferentes de um mesmo lote em reparo, escolhidas direto da **bancada**, na hora em que o item volta.

## Enquanto o item está em reparo

Quando você manda [bens móveis](../primeiros-passos/glossario.md) para o conserto, eles saem do **disponível** — ninguém consegue prometer esse item para um orçamento novo enquanto ele está na oficina. Mas o item continua **seu**: ele segue contando no seu patrimônio, só não pode ser alugado nem vendido até voltar. Só o que está **disponível** pode ir para o reparo: material reservado para um pedido continua onde está.

{% hint style="info" %}
Se você informou uma **previsão de volta** ao mandar a remessa, o item volta a contar como disponível a partir daquela data — mesmo antes de alguém concluir a manutenção. Sem previsão, ele fica indisponível até você mesmo encerrar o reparo.
{% endhint %}

Para mandar um item para o reparo, use **Enviar para reparo** — na ficha do item, no **Operar** do [Painel de Estoque](painel.md) ou na própria tela de Manutenção. Para mandar vários de uma vez (com a previsão de volta da remessa inteira), veja [Operar vários itens de uma vez](operar-varios-itens.md).

## A bancada

A bancada fica em **Estoque › Manutenção** — *"O que está na bancada agora"*. Cada envio vira um **lote**, com a quantidade que ainda está no conserto.

* **O mais antigo vem primeiro.** A bancada não é um extrato: no topo fica o que está parado há mais tempo, não o que chegou por último.
* O lote que **passou da previsão** do conserto fura a fila e ganha o **selo vermelho**.
* Passando de **15 dias parado**, o lote ganha o **selo âmbar** — é material que a operação já esqueceu.
* Cada lote tem um **responsável**. Quem manda material para a bancada pode trocá-lo em **Trocar**.

Abrir o lote e escolher a saída basta. Marcar os serviços feitos, tirar a foto de antes e a de depois e escrever uma observação **ajudam você a conferir** antes de encerrar — mas **nenhuma delas trava** a saída do material, e essas anotações não ficam arquivadas no lote. O que fica registrado de verdade é o motivo do descarte, da reclassificação e da quarentena, que vai para o histórico do estoque.

## Quatro saídas para o lote {#quatro-saidas}

No lote, toque em **Concluir reparo** — *"Diga o que foi feito e para onde as unidades vão"* — e escolha a saída:

<table><thead><tr><th width="200">Saída</th><th>O que acontece</th></tr></thead><tbody><tr><td><strong>Voltar ao estoque</strong></td><td>O reparo deu certo. O item sai da bancada e volta a contar como disponível — a saída de sempre.</td></tr><tr><td><strong>Descartar</strong></td><td>O reparo não compensou (a almofada rasgou de vez, a peça empenou). O item sai do seu patrimônio ali mesmo — sem precisar voltar ao estoque bom para, só depois, dar baixa.</td></tr><tr><td><strong>Reclassificar</strong></td><td>O item ainda serve, mas não para o que servia antes. Ele passa direto para outro tipo de estoque — o caso clássico é a cadeira muito usada saindo do aluguel para a venda de usados.</td></tr><tr><td><strong>Separar em quarentena</strong></td><td>Quem avaliou ficou em dúvida e não tem alçada para decidir. O item sai da bancada, continua fora do disponível e fica separado até alguém com alçada decidir o destino. Veja <a href="quarentena.md">Quarentena</a>.</td></tr></tbody></table>

Cada saída abre na mesma janela: o cabeçalho na cor da saída, o lote como contexto, a prévia do que vai acontecer (*"3 unidades saem do patrimônio · 2 unidades continuam na bancada"*) e um botão que diz por escrito o que falta enquanto estiver travado. Se o seu acesso só permite uma saída, ela já vem escolhida. **Voltar** nunca trava.

### Descartar exige um motivo — e pode virar cobrança

Ao descartar, o LocFlow pergunta **O que aconteceu?** (obrigatório, por escrito — *"Estrutura empenada, sem conserto viável"*). Esse motivo fica registrado no histórico do estoque.

Se você tem permissão para emitir cobranças, aparece a opção **Cobrar o cliente pelo descarte**: escolha o cliente e o valor, e o LocFlow gera uma cobrança avulsa — normalmente pelo valor de reposição do item. É opcional; sem marcar, o descarte só dá baixa.

{% hint style="warning" %}
**A baixa vale mesmo se a cobrança falhar.** Descartar o item é definitivo assim que você confirma — o LocFlow não espera a cobrança para isso. Se a cobrança não puder ser gerada, o app avisa que o descarte foi registrado mas a cobrança falhou, para você gerá-la manualmente em Cobranças. Nunca fica em dúvida se o item saiu do patrimônio: ele saiu.
{% endhint %}

### Reclassificar pede o destino

Ao reclassificar, você escolhe **Para onde vai?** — **Aluguel**, ou **Venda** numa condição (**Novo**, **Seminovo** ou **Usado**). O destino precisa ser **diferente** de onde o item já estava. O motivo aqui é opcional.

O destino **não precisa ter preço** no catálogo: onde o material fica separado é um fato do galpão. Se o produto não tem preço avulso naquele destino, ele aparece no painel com o selo **sem preço avulso** — informação, não pendência.

### Separar em quarentena pede o motivo

O **Motivo** é obrigatório (*"Trinca fina na solda — não sei dizer se compromete"*): quem decide o destino vê essa frase na tela Quarentena. Lá, alguém com alçada devolve ao estoque, descarta ou reclassifica.

## Cada saída depende do que você pode fazer

Você só vê a saída que pode de fato usar:

- **Voltar ao estoque** pede a permissão de encerrar manutenção.
- **Descartar** pede, além dessa, a permissão de dar baixa no estoque.
- **Reclassificar** pede, além da primeira, a permissão de ajustar estoque.
- **Separar em quarentena** pede, além da primeira, a permissão de pôr material em quarentena.

Nos papéis prontos, a diferença é clara: o **Operador de Manutenção** devolve ao estoque e pode separar em quarentena; o **Encarregado de Manutenção** também descarta e reclassifica — e é quem decide o destino do que está em quarentena. Descartar e reclassificar **mexem no patrimônio**, e não são decisão de quem está com a ferramenta na mão.

Se aparece só **Voltar ao estoque**, não é defeito nem botão desligado — as outras saídas simplesmente não fazem parte do seu acesso. Fale com quem administra os acessos da sua locadora para liberar o que faltar (veja [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md)).

## A conclusão pode ser parcial

Você não precisa dar o mesmo destino para o lote inteiro. Dos **10** itens que foram para o reparo, **6** podem voltar bons ao estoque e **4** podem ser descartados — em dois passes separados, cada um com a quantidade certa. O lote só desaparece da bancada quando a última unidade recebe um destino; até lá, ele continua ali, mostrando quanto ainda falta decidir.

{% hint style="info" %}
**Não achou a Manutenção no menu?** Ela fica guardada enquanto a bancada está vazia e aparece sozinha quando há material em reparo. Para mostrá-la mesmo assim, use **Personalizar** no menu.
{% endhint %}

{% hint style="success" %}
**Por que isso te faz faturar mais:** sem esse fluxo, o item ruim precisaria voltar ao estoque bom só para alguém lembrar de tirá-lo depois — um passo a mais, uma chance a mais de esquecer e vender (ou alugar) algo quebrado. Descartar, reclassificar ou separar na hora do reparo fecha o ciclo num só passo, com o motivo registrado e, quando cabe, o prejuízo já cobrado do cliente.
{% endhint %}

## Próximo passo

Veja o que acontece com o material separado em [Quarentena](quarentena.md), o que cada movimentação do estoque registra — inclusive as geradas por um descarte ou reclassificação de manutenção — em [Cada movimentação, em detalhe](posicao-e-previsao.md#movimentacoes), e como mandar vários itens ao reparo de uma vez em [Operar vários itens de uma vez](operar-varios-itens.md).
