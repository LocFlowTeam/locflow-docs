---
icon: address-book
description: Sua agenda de clientes — cadastre uma vez, reaproveite em todo orçamento e complete os dados só quando a operação pedir.
---

# Contatos

O módulo de **Contatos** é a sua agenda dentro do LocFlow: seus clientes (e possíveis clientes), pessoas físicas ou jurídicas. Cada [contato](../primeiros-passos/glossario.md) que você cadastra fica disponível para ser **reaproveitado** em qualquer orçamento — você digita os dados uma vez e nunca mais precisa redigitar nome, celular ou endereço.

{% hint style="success" %}
**Por que isso te faz faturar mais:** uma base de clientes organizada é uma base que **recompra**. Quando todo cliente já está cadastrado, com canal de contato e histórico, fazer follow-up vira questão de minutos — e cliente que você consegue chamar de volta é cliente que aluga (ou compra) de novo.
{% endhint %}

## O que é um contato {#o-que-e-um-contato}

Um contato representa **uma pessoa ou empresa** com quem você se relaciona — o seu cliente, ou um possível cliente. O cadastro é enxuto de propósito: para começar, basta o nome e **um canal de contato** (celular ou e-mail). O resto é opcional e você completa quando precisar.

```mermaid
flowchart TD
    C[Contato] --> P[Perfil]
    C --> K[Contato / canal]
    C --> E[Endereço]
    P --> PF[Pessoa física<br/>CPF]
    P --> PJ[Pessoa jurídica<br/>CNPJ]
    K --> CEL[Celular + WhatsApp]
    K --> EM[E-mail]
```

### Perfil: pessoa física ou jurídica {#perfil-pessoa-fisica-ou-juridica}

| Tipo | Documento | Campos extras |
| --- | --- | --- |
| **Pessoa física** | CPF | Nome completo |
| **Pessoa jurídica** | CNPJ | Razão social, Nome fantasia, Inscrição estadual (IE), Contribuinte ICMS |

O **documento (CPF/CNPJ) é opcional** no cadastro — você pode salvar um contato só com o nome e o telefone. A obrigatoriedade do documento aparece mais adiante, quando a operação realmente exige (por exemplo, na emissão fiscal ou na cobrança online). Para uma empresa, ao informar a IE você ainda marca se ela é **Contribuinte ICMS**.

### Canal de contato: celular, WhatsApp e e-mail {#canal-de-contato}

- **Celular** — ao preencher, surge a pergunta **"Este número é WhatsApp?"**. Marque sim quando for o caso; isso ajuda a equipe a saber por onde falar com o cliente.
- **E-mail** — usado para envio de proposta e comunicação.
- Se o cliente realmente não tem um dos canais, há os atalhos **"Não possui celular"** e **"Não possui e-mail"**.

{% hint style="info" %}
O cadastro pede **ao menos um canal**: celular **ou** e-mail. Sem um meio de contato, você não consegue dar follow-up — por isso o sistema garante esse mínimo.
{% endhint %}

### Endereço {#endereco}

O endereço fica em **"Editar mais informações"** (junto de CPF/CNPJ e demais dados opcionais). Você informa o **CEP** e o sistema **completa logradouro, bairro e cidade automaticamente** — depois é só ajustar número e complemento. Dá ainda para classificar o **tipo do local** (Residencial ou Condomínio); em condomínio, o complemento (bloco, torre ou apartamento) passa a ser pedido para que a entrega chegue certo.

Esse endereço não é decorativo: ele é reaproveitado no orçamento como **endereço de entrega** (veja [mais abaixo](#reaproveitar-no-orcamento)).

### O estágio de funil (categoria) {#estagio-de-funil}

Todo contato tem um **estágio de funil**, que o LocFlow calcula sozinho a partir das reservas fechadas:

| Estágio | O que significa |
| --- | --- |
| **Contato qualificado (lead)** | Ainda não fechou nenhuma reserva. É o registro mínimo para acompanhar antes da primeira locação ou venda. |
| **Cliente ativo** | Já fechou ao menos uma reserva com você. |
| **Cliente fidelizado** | Tem duas ou mais reservas fechadas — recorrência e fidelidade. |

Você não precisa mexer nisso no cadastro: o estágio **evolui automaticamente** conforme o cliente fecha pedidos. Apenas na **edição** de um contato é possível fixar o estágio manualmente — o seletor traz a opção **Automático** (recomendada) ou um estágio fixo. Como diz a própria ajuda da tela: *"Automático = derivado das reservas fechadas. Fixe manualmente só em exceções (ex.: VIP)."*

## Criar, buscar e filtrar {#criar-buscar-filtrar}

### Criar um contato {#criar-um-contato}

Na lista de contatos, toque no botão **+** para abrir o cadastro. Preencha o **Nome** e um canal (celular ou e-mail) e salve — só isso já cria o contato. Precisa de mais dados (CPF/CNPJ, endereço)? Abra **"Editar mais informações"** e complete. Para uma empresa, troque o perfil para **Pessoa Jurídica** e o rótulo do nome muda para **Razão Social**.

{% hint style="info" %}
Começou a digitar e precisou sair? O LocFlow guarda um **rascunho** do cadastro e oferece retomar depois — você não perde o que já tinha preenchido.
{% endhint %}

### Buscar e filtrar na lista {#buscar-e-filtrar}

A lista tem uma **busca inteligente** no topo: digite nome, documento, parte do telefone ou e-mail e os resultados se ajustam. Quando a base cresce, a lista é **paginada** (você escolhe quantos por página e navega entre as páginas). Tocar em um contato abre a **ficha** com Perfil, Contato e Endereço; o lápis leva direto para a edição. Em telas largas (no computador), a lista vira uma **tabela** ao lado da ficha — você seleciona um contato à esquerda e lê os detalhes à direita.

```mermaid
flowchart LR
    L[Lista de contatos] --> B[Busca / paginação]
    B --> F[Ficha do contato]
    F --> ED[Editar]
    L --> N[Novo contato +]
```

## Completar dados na hora certa {#completar-dados-sob-demanda}

Como o cadastro pode nascer enxuto, vai haver momentos em que a operação **exige um dado que ainda falta** — por exemplo, gerar uma cobrança online costuma pedir CPF/CNPJ e e-mail do pagador; certos métodos de pagamento pedem também o telefone ou o endereço.

Quando isso acontece, o LocFlow **não te manda voltar ao cadastro inteiro**. Ele abre uma janela curta — **"Completar dados do contato"** — que mostra **apenas o que falta** e nada mais. Você preenche só aquilo, confirma, e o sistema **continua de onde você parou**.

- A janela busca os dados **mais recentes** do contato ao abrir e pede só os campos ausentes (documento, e-mail, telefone e/ou endereço, conforme a ação exigir).
- O botão de confirmar **carrega a próxima ação junto** — por exemplo, "Salvar e gerar PIX" ou "Salvar e habilitar" um método. Em um toque você completa o dado e já segue.
- Se nada estiver faltando, a janela avisa: *"Os dados do contato já estão completos. Pode continuar."*
- Salvar ali **preserva todo o resto** da ficha — você só acrescenta o que faltava, não reescreve o cadastro.

{% hint style="success" %}
**Por que é melhor assim:** você cadastra rápido no começo e só enriquece a ficha **quando há motivo real** para isso. O dado entra no momento em que vale a pena — não como uma barreira logo na primeira digitação.
{% endhint %}

## Quem pode criar, editar e excluir {#permissoes}

O acesso aos contatos é controlado por **permissões** do colaborador (definidas em [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md)). Cada uma libera uma ação específica:

| Permissão | O que libera |
| --- | --- |
| **Listar contatos** | Ver a lista de contatos. |
| **Visualizar contato** | Abrir a ficha de um contato. |
| **Criar contato** | Cadastrar novos contatos (botão **+**). |
| **Editar contato** | Alterar dados de um contato existente (o lápis). |
| **Excluir contato** | Enviar um contato para a lixeira. |

{% hint style="info" %}
Sem a permissão de **criar**, o botão **+** não fica disponível. Sem a de **visualizar**, tocar num contato avisa que falta acesso. Assim cada pessoa da equipe enxerga e mexe só no que faz parte do trabalho dela.
{% endhint %}

## Excluir um contato (lixeira) {#exclusao-lixeira}

Excluir um contato é uma ação **reversível**: em vez de apagar de vez, o LocFlow **envia o contato para a lixeira**. A intenção é proteger você de perder um cliente por engano — o registro sai da lista do dia a dia, mas continua recuperável.

- **Excluir** (lixeira) — exige a permissão de **excluir contato**; o contato é removido da lista corrente.
- **Excluir permanentemente** — uma ação à parte, mais restrita, para tirar o contato da lixeira de vez. É irreversível e fica reservada a perfis com esse acesso específico.

{% hint style="warning" %}
Mande para a lixeira em vez de apagar de vez sempre que houver dúvida. Cliente excluído por engano pode estar ligado a um histórico que você ainda vai querer consultar.
{% endhint %}

## Reaproveitar no orçamento {#reaproveitar-no-orcamento}

Aqui está o ganho real da base de contatos: ao [criar um orçamento](../conceitos/ciclo-de-um-pedido.md), você **seleciona um contato já cadastrado** em vez de redigitar tudo. Os dados do cliente entram no pedido na hora — e o **endereço do contato** vira opção de entrega.

No orçamento, o endereço de entrega pode ser:

| Opção | Quando usar |
| --- | --- |
| **Endereço do contato** | Entrega no endereço já cadastrado na ficha do cliente. |
| **Endereço salvo** | Um endereço recorrente que você guardou (ex.: um galpão de cliente). |
| **Endereço exclusivo** | Um endereço só daquele pedido (ex.: um evento pontual). |

Se o contato ainda **não tem endereço** quando você escolhe "Endereço do contato", o LocFlow te leva direto para completar o endereço dele e **volta para o orçamento** com o dado preenchido — sem você se perder no caminho. Da mesma forma, dá para **criar um contato novo** no meio do orçamento e retornar com ele já selecionado. Veja mais em [Endereços e endereços salvos](../orcamentos/enderecos.md).

## Situações reais {#situacoes-reais}

- **Cliente recorrente:** o Buffet do Marcos alugou mesas com você há dois meses. Hoje ele liga pedindo de novo. Você busca "Marcos" na lista, o contato aparece com celular, WhatsApp e endereço — em segundos você abre um orçamento já com tudo preenchido. Como ele já tem reservas fechadas, aparece como **Cliente ativo** (ou **fidelizado**, se for a segunda vez).
- **Lead que ainda não fechou:** um possível cliente pediu cotação pelo WhatsApp. Você cadastra só **nome + celular (WhatsApp)** e manda a proposta. Ele entra como **Contato qualificado (lead)** — e fica na sua lista para o follow-up.
- **Faltou o CPF na hora da cobrança:** você vai gerar um link de pagamento e o método pede CPF e e-mail do cliente. Em vez de abrir o cadastro inteiro, a janela **"Completar dados do contato"** pede só esses dois campos; você preenche, toca em **"Salvar e gerar PIX"** e a cobrança segue na sequência.
- **Empresa com nota fiscal:** uma construtora vai alugar andaimes e precisa de nota. Você cadastra como **Pessoa Jurídica**, com CNPJ, Razão Social, Nome fantasia e IE — pronto para a operação fiscal quando ela exigir.

{% hint style="success" %}
**Filosofia por porte:** quem está começando cadastra só nome e telefone e segue em frente. Quem cresceu vai preenchendo documento, endereço e dados fiscais — e o sistema pede cada um **só quando a operação precisa**. O cadastro **abstrai para o pequeno e revela para o grande**: você nunca é obrigado a preencher o que não usa.
{% endhint %}

## Próximo passo {#proximo-passo}

Veja como o contato entra no fluxo em [O ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md), entenda quem pode o quê em [Colaboradores e acessos](../configuracoes/colaboradores-e-acessos.md), ou tire dúvidas em [Onde tirar dúvidas](../primeiros-passos/onde-tirar-duvidas.md).
