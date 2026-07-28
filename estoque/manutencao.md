---
icon: wrench
description: O que fazer quando um item volta do reparo — voltar ao estoque, descartar com motivo (e cobrar o cliente) ou reclassificar para outro tipo de estoque, com conclusão parcial.
---

# Manutenção: o desfecho do reparo

Nem todo item que sai para o conserto volta do mesmo jeito. A cadeira pode voltar boa, pode voltar sem conserto possível, ou pode voltar servindo só para outra coisa — a almofada muito usada, por exemplo, não vale mais alugar, mas ainda dá para vender como usada. O LocFlow trata os três casos como **desfechos** diferentes de uma mesma remessa em reparo, escolhidos direto da bancada, na hora em que o item volta.

## Enquanto o item está em reparo

Quando você manda [bens móveis](../primeiros-passos/glossario.md) para o conserto, eles saem do **disponível** — ninguém consegue prometer esse item para um orçamento novo enquanto ele está na oficina. Mas o item continua **seu**: ele segue contando no seu patrimônio, só não pode ser alugado nem vendido até voltar.

{% hint style="info" %}
Se você informou uma **previsão de volta** ao enviar a remessa, o item volta a contar como disponível a partir daquela data — mesmo antes de alguém concluir a manutenção manualmente. Sem previsão, ele fica indisponível até você mesmo encerrar o reparo, item por item.
{% endhint %}

Para mandar um item (ou vários de uma vez) para o reparo, veja [Operar vários itens de uma vez](operar-varios-itens.md).

## Três desfechos possíveis quando o item volta {#tres-desfechos}

Cada remessa em reparo aparece como uma ordem, com a quantidade que ainda está na bancada. Para cada uma, você escolhe o que aconteceu:

<table><thead><tr><th width="180">Desfecho</th><th>O que acontece</th></tr></thead><tbody><tr><td><strong>Voltar ao estoque</strong></td><td>O reparo deu certo. O item some da bancada e volta a contar como disponível — o desfecho de sempre.</td></tr><tr><td><strong>Descartar</strong></td><td>O reparo não compensou (a almofada rasgou de vez, a peça empenou). O item sai do seu patrimônio ali mesmo — sem precisar voltar ao estoque bom para, só depois, dar baixa.</td></tr><tr><td><strong>Reclassificar</strong></td><td>O item ainda serve, mas não para o que servia antes. Ele passa direto para outro tipo de estoque — o caso clássico é a cadeira muito usada saindo do aluguel para a venda de usados.</td></tr></tbody></table>

### Descartar exige um motivo — e pode virar cobrança

Ao descartar, o LocFlow pede um **motivo** (obrigatório, por escrito — "estrutura empenada, sem conserto viável"). Esse motivo fica registrado no extrato do estoque.

Se você tem permissão para emitir cobranças, aparece a opção de **cobrar o cliente pelo prejuízo** no mesmo passo: escolha o contato e o valor, e o LocFlow gera uma cobrança avulsa — normalmente pelo valor de reposição do item. É opcional; sem marcar, o descarte só dá baixa, sem gerar nenhuma cobrança.

{% hint style="warning" %}
**A baixa vale mesmo se a cobrança falhar.** Descartar o item é definitivo assim que você confirma — o LocFlow não espera a cobrança para isso. Se a cobrança não puder ser gerada, o app avisa que o descarte foi registrado mas a cobrança falhou, para você gerá-la manualmente em Cobranças. Nunca fica em dúvida se o item saiu do patrimônio: ele saiu.
{% endhint %}

### Reclassificar pede o destino — e o destino precisa ter preço

Ao reclassificar, você escolhe para onde o item vai: **Aluguel**, ou **Venda** numa condição (Novo, Seminovo ou Usado). O destino precisa ser **diferente** de onde o item já estava, e o produto **precisa ter preço configurado** naquele destino — se a condição escolhida ainda não tem preço cadastrado, o LocFlow recusa a reclassificação até você cadastrar (veja [Catálogo: produtos](../cadastros/catalogo-produtos.md)). O motivo aqui é opcional.

## Cada opção só aparece com a permissão certa

Você só vê o botão do desfecho que pode de fato usar:

- **Voltar ao estoque** pede a permissão de encerrar manutenção.
- **Descartar** pede, além dessa, a permissão de dar baixa no estoque.
- **Reclassificar** pede, além da primeira, a permissão de ajustar estoque.

Sem nenhuma delas, a tela avisa que falta permissão para encerrar lotes de manutenção — em vez de mostrar um botão cinza que terminaria em erro. Fale com quem administra os acessos da sua locadora para liberar o que faltar (veja [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md)).

## A conclusão pode ser parcial

Você não precisa dar o mesmo destino para a remessa inteira. Dos **10** itens que foram para o reparo, **6** podem voltar boas ao estoque e **4** podem ser descartadas — em dois passes separados, cada um com a quantidade certa. A ordem só desaparece da bancada quando a última unidade recebe um desfecho; até lá, ela continua ali, mostrando quanto ainda falta decidir.

{% hint style="success" %}
**Por que isso te faz faturar mais:** sem esse fluxo, o item ruim precisaria voltar ao estoque bom só para alguém lembrar de tirá-lo depois — um passo a mais, uma chance a mais de esquecer e vender (ou alugar) algo quebrado. Descartar ou reclassificar na hora do reparo fecha o ciclo num só passo, com o motivo registrado e, quando cabe, o prejuízo já cobrado do cliente.
{% endhint %}

## Próximo passo

Veja o que cada movimentação do estoque registra — inclusive as geradas por um descarte ou reclassificação de manutenção — em [Posição e previsão de estoque](posicao-e-previsao.md#movimentacoes). Para mandar vários itens ao reparo de uma vez, veja [Operar vários itens de uma vez](operar-varios-itens.md).
