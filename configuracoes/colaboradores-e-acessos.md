---
icon: users
description: Cadastre a equipe em passos, conceda acesso por link e organize papéis, funções, CNH e o veículo do dia a dia de cada colaborador.
---

# Colaboradores e acessos

Quando você está sozinho, o LocFlow faz tudo por você — com acesso total. Conforme a equipe chega, a pergunta vira "**quem pode fazer o quê?**". Aqui você cadastra pessoas, define o que cada uma acessa e organiza as habilidades da operação.

Antes de continuar, vale entender a ideia por trás disso em [Papéis, funções e competências](../conceitos/papeis-funcoes-competencias.md) — é o conceito que esta tela coloca em prática.

{% hint style="success" %}
**Valor:** cada pessoa enxerga só o que usa. O motorista abre o app e vê **a rota dele** — não o financeiro nem o catálogo. Você delega sem medo, evita erro e ganha tempo: dar acesso a alguém é mandar **um link** pelo WhatsApp.
{% endhint %}

## Cadastrar é diferente de dar acesso

São duas coisas separadas, e essa é a primeira escolha que muda tudo:

* **Cadastrar** registra a pessoa na sua equipe — com nome, funções e dados como a CNH. Ela aparece na lista, mas **não entra** no sistema.
* **Dar acesso** gera o **convite** (um link) para essa pessoa fazer login e usar o app ou o navegador.

Você pode fazer as duas coisas de uma vez (no cadastro guiado, basta dizer que a pessoa terá login) ou só cadastrar agora e **conceder acesso depois**, quando quiser. É comum cadastrar o time inteiro de uma vez e ir liberando o acesso conforme cada um começa.

<a id="cadastro-guiado"></a>

## Cadastro guiado em 4 passos

Toque no **+** na aba **Pessoas** para abrir o **Novo colaborador**. Ele é um assistente que vai te guiando — você avança em **Continuar** e pode **Voltar** a qualquer momento sem perder o que já preencheu.

```mermaid
flowchart LR
    A[1. Pessoa<br/>nome] --> B[2. Funcoes<br/>+ CNH se dirige]
    B --> C[3. Acesso<br/>login ou so cadastro]
    C --> D[4. Revisao<br/>e link do convite]
```

| Passo | O que você define |
| --- | --- |
| **1. Pessoa** | O **nome** do colaborador. Só isso para começar. |
| **2. Funções** | O que ela faz na operação (dirigir, vender, separar…). Se uma função pede **dirigir**, aparece um bloco para a **CNH**. |
| **3. Acesso** | Vai ter login? Se **sim**, você escolhe **onde** ela usa (app ou navegador), o **e-mail** (opcional) e os **papéis**. Se **não**, fica só cadastrada. |
| **4. Revisão** | Um resumo de tudo. Se houver login, o **link do convite** aparece pronto para copiar ou enviar. |

{% hint style="info" %}
Você só consegue avançar quando o passo está completo: no passo 1, o nome; no passo 3 (com login), pelo menos um papel marcado e o e-mail válido, se preenchido. Os outros passos são livres.
{% endhint %}

### O atalho inteligente dos papéis

No passo 3, o LocFlow já **sugere os papéis** com base nas funções que você marcou — por exemplo, escolheu a função de dirigir, ele propõe o papel **Motorista**. A sugestão vem pré-marcada; você ajusta à vontade. E ele também já **pré-seleciona o dispositivo**: quem dirige tende a usar o **app no celular**; os demais, o **navegador** (você pode trocar).

## Conceder acesso a quem já está cadastrado

Para uma pessoa que está em **Sem acesso**, toque em **Conceder acesso →** no card dela. Aqui você não repete o cadastro — só decide o acesso:

* **Papéis** — marque um ou mais (veja [as permissões de cada um](#papeis-prontos)).
* **Onde vai usar** — app no celular ou navegador no computador.
* **E-mail** (opcional) — vincula o convite, como no cadastro.

Toque em **Gerar convite e enviar**: o link nasce na hora, pronto para copiar e mandar.

<a id="convidar-e-mandar-link"></a>

## Convidar é mandar um link

No LocFlow você **não define a senha** da pessoa, e informar o e-mail é **opcional**. O convite gera um **link** — e esse link É a credencial. Você manda por WhatsApp, e-mail ou qualquer app, e quem recebe entra direto.

```mermaid
flowchart LR
    A[Voce concede acesso] --> B[LocFlow gera o link]
    B --> C[Voce envia<br/>WhatsApp / email]
    C --> D[Pessoa abre o link]
    D --> E[Aceita e ja entra<br/>com os papeis certos]
```

Quem aceita pode entrar pelo navegador, sem instalar nada, ou pelo app LocFlow se já tiver instalado — e cai direto na tela de aceitar, sem o cadastro de empresa nova.

### Onde a pessoa vai usar (app ou navegador)

No convite você escolhe **como o link se comporta ao ser aberto**, com a pergunta *"Como [nome] vai usar a LocFlow?"*:

| Opção | Para quem | Por quê |
| --- | --- | --- |
| **Aplicativo no celular** | Motoristas e equipe de campo | Entregas, separação e rotas se fazem na rua, no celular. |
| **Navegador no computador** | Escritório / administrativo | Orçamentos, cobrança e relatórios pedem tela maior. |

Não é uma trava — é só por onde o link abre primeiro. A pessoa continua podendo usar os dois.

### O e-mail vinculado (camada extra)

Informar o **e-mail** no convite **o vincula àquela pessoa**: só quem entrar autenticado com esse e-mail consegue aceitar — se outra pessoa abrir o link, o LocFlow avisa *"Este convite é para fulano@… Entre com essa conta para aceitar."* É uma camada extra de segurança para o link não cair em mãos erradas. Deixou em branco? Qualquer um com o link aceita.

**E tem um efeito prático:** com o e-mail preenchido, **o LocFlow envia o convite por e-mail sozinho** — você não precisa copiar e mandar. O link continua disponível na tela para você reenviar por WhatsApp se quiser.

{% hint style="info" %}
Como o link é a credencial, **trate-o como uma senha**: mande só para a pessoa certa. O convite tem **prazo de validade**; se expirar, é só gerar outro. Convites enviados ficam visíveis em **Convites pendentes**, com o link para **copiar de novo** a qualquer momento.
{% endhint %}

<a id="papeis-prontos"></a>

## Papéis prontos (você não monta do zero)

O LocFlow já vem com um papel para cada cargo. No convite, basta marcar. O **papel** controla o que a pessoa **acessa** no sistema:

| Papel | Para quem | O que enxerga |
| --- | --- | --- |
| **Administrador** | Sócio ou braço direito | Praticamente tudo. Só fica de fora o que **encerra a conta**: apagar a organização e mexer no contrato de assinatura (cancelar, trocar de plano, pedir reembolso) — isso continua exclusivo do dono. Ele **vê** plano, consumo e faturas normalmente |
| **Operador / Atendente** | Gestão e dia a dia | Orçamentos, frota, roteiros, equipe |
| **Motorista** | Quem roda a rota | Só os roteiros atribuídos a ele |
| **Separador** | Galpão (ida) | A fila *A separar → Separado* |
| **Conferente** | Galpão (volta) | A fila *A conferir → Conferido* |
| **Operador de Balcão** | Loja física (as duas pontas) | O [balcão](../logistica/balcao.md) — entrega **e** recebe do cliente, e pode registrar **em lote** |

{% hint style="info" %}
O **dono** entra como acesso total — por isso, quem está sozinho nem percebe que papéis existem. Eles só aparecem quando você convida a primeira pessoa.
{% endhint %}

{% hint style="warning" %}
**Procurando o papel de "Parceiro"? Ele não está aqui — e não deveria estar.** Parceiro é gente **de fora**, não da sua equipe, e por isso entra por outro caminho: **Rede de Parceiros → convidar parceiro**. O papel dele é fixo (você não escolhe nem edita) e dá acesso **só aos pedidos que você repassar a ele**. Veja [Entrando na rede](../parcerias/entrando-na-rede.md) e [Parceiro Logístico Externo](../parcerias/parceiro-logistico-externo.md).
{% endhint %}

<a id="dispensar-evidencia"></a>

### Uma permissão que vale conhecer: dispensar a evidência

Se a sua empresa exige **comprovação** (foto, vídeo, assinatura) para fechar uma entrega, retirada ou atendimento de balcão, o LocFlow **não fecha o registro sem ela**. Só que nem sempre a prova é possível: quem lança no escritório o que aconteceu ontem não tem como fotografar o passado.

Para esses casos existe a **dispensa de evidência** — fechar o registro escrevendo um **motivo obrigatório**, que fica gravado junto e aparece na [auditoria](historico-de-auditoria.md). É uma permissão **separada**, e a distribuição dela tem uma lógica:

| Quem tem | Por quê |
| --- | --- |
| **O dono** e o **Administrador** | Têm, junto com todo o resto da gestão — o Administrador recebe tudo, menos o que encerra ou cobra a conta |
| **Operador / Atendente** | É a retaguarda: lança o que já aconteceu, sem ter como voltar no tempo e fotografar |
| **Operador de Balcão** | Já registrava vários atendimentos de uma vez; a permissão só dá nome ao que ele fazia |
| **Motorista** e **Parceiro Externo** | **Não têm** — e não é esquecimento. Eles estão no ponto da entrega justamente para **produzir** a prova; dar a eles a chave de pular a prova esvaziaria a política. No caso do parceiro externo isso nem é configurável: o papel dele é fixo |

{% hint style="info" %}
Se você personalizar um papel, pense duas vezes antes de incluir essa permissão em quem trabalha em campo. Ela não é um atalho de conveniência — é uma exceção que fica registrada com nome, hora e motivo.
{% endhint %}

### Vários papéis na mesma pessoa

No mesmo convite você pode marcar **mais de um papel**. É comum: um colaborador que **dirige a rota** e também **confere o material na volta** recebe *Motorista* + *Conferente*. Ao aceitar, todos os papéis marcados são atribuídos de uma vez — sem precisar de dois convites.

Antes de convidar, você pode tocar no ícone de **olho** ao lado de cada papel para ver **exatamente quais permissões** ele inclui.

<a id="cnh-do-motorista"></a>

## A CNH do motorista (avisa, nunca bloqueia)

Quando você escolhe uma função que **exige dirigir**, aparece um bloco de **CNH**. Você informa:

* **Número** da habilitação;
* **Categoria(s)** — **A**, **B**, **C**, **D** ou **E** (pode marcar mais de uma);
* **Validade**.

A regra de ouro: **a CNH nunca trava o cadastro**. Você pode concluir sem ela ou com ela vencida — o LocFlow só **avisa**.

{% hint style="warning" %}
Sem CNH válida, fica **pendente** para a pessoa dirigir rotas. Você ainda pode concluir o cadastro.
{% endhint %}

A CNH é considerada **regularizada** quando tem categoria informada e **validade futura**. Se a validade já passou, o aviso fica mais forte: *"CNH vencida — precisa de renovação. Fica pendente para dirigir rotas até a validade ser atualizada."* É uma pendência que aparece no card da pessoa (veja [Pendências](#pendencias)) — ela não some sozinha, mas também não impede você de seguir trabalhando.

<a id="veiculo-padrao"></a>

## O veículo padrão do condutor

Para quem **dirige**, a ficha do colaborador (em **Editar**) traz um campo de **Veículo padrão**: o veículo que essa pessoa usa no dia a dia. Você busca pela **placa** e seleciona.

Para que serve? Para **adiantar o seu trabalho**: ao atribuir ou executar um roteiro com esse colaborador, o LocFlow já **infere** o veículo dele — você não precisa escolher toda vez. É opcional, aparece **só para quem dirige**, e dá para **limpar** quando quiser (tocando no **X** ao lado).

{% hint style="info" %}
O veículo padrão é uma **sugestão**, não uma amarra: no roteiro você pode trocar para outro veículo da [frota](../cadastros/frota.md) sempre que precisar.
{% endhint %}

## Personalizar um papel ou função

Os papéis prontos resolvem a maioria dos casos. Quando a sua operação pede algo sob medida, você personaliza — sem perder o original:

* **Personalizar um papel:** parte de um papel do sistema (ex.: *Atendente*) e ajusta as permissões, criando uma cópia só da sua organização. Também dá para **criar um papel do zero** pelo link "Criar papel personalizado".
* **Criar uma função nova:** funções dizem **o que a pessoa sabe fazer** (competências). Você pode criar funções próprias ou personalizar as do sistema.

Tudo isso fica na aba **Funções & Papéis**, que mostra as duas camadas lado a lado: **Funções** (operacional) e **Papéis** (acesso). Itens do sistema aparecem com a etiqueta *Sistema*; os seus, com *Personalizado*.

### As competências (o que a pessoa sabe fazer)

A **função** reúne competências. Elas não dão acesso a telas — dizem **habilidade**, e é por elas que a logística sabe quem pode fazer cada tarefa. As competências do LocFlow são:

| Competência | Habilita | Observação |
| --- | --- | --- |
| **Dirigir Veículos** | Conduzir veículos da frota | Depende de CNH válida (mas não bloqueia o cadastro) |
| **Vender Orçamentos** | Emitir e conduzir orçamentos (aluguel ou venda) | — |
| **Operar Logística** | Operar roteiros, entregas e retiradas | — |
| **Separação** | Separar e preparar o material para envio | — |
| **Conferência** | Conferir o material no retorno ao galpão | — |
| **Atendimento no balcão** | Atender o cliente presencialmente no balcão — as retiradas e devoluções no galpão | — |

{% hint style="info" %}
Papel e função são **eixos diferentes**: o papel libera **o que a pessoa vê**; a função registra **o que ela sabe fazer**. Um *Motorista* tem o papel de motorista (vê só a rota dele) e a função de motorista (competência *Dirigir Veículos*, que pede CNH).
{% endhint %}

## Quem já está cadastrado

A aba **Pessoas** lista a equipe e os convites, e você filtra por três grupos (cada um com a contagem ao lado):

* **Com acesso** — quem já tem login ativo.
* **Sem acesso** — colaboradores cadastrados que ainda não entram no sistema. Use **Conceder acesso** para enviar o convite.
* **Convites pendentes** — convites enviados aguardando o aceite (com link para copiar de novo).

A busca encontra por **nome ou e-mail**. Em cada pessoa você ajusta **funções e CNH** em **Editar funções e CNH →** e vê eventuais **pendências**.

<a id="pendencias"></a>

### As pendências do colaborador

Quando algo importante falta, o card da pessoa mostra um aviso âmbar com a **pendência** — por exemplo, um motorista sem CNH cadastrada ou com a CNH vencida. Se houver mais de uma, ele resume a quantidade.

A pendência **não impede** a pessoa de existir no sistema nem você de trabalhar; ela é um **lembrete visível** do que regularizar. No caso da CNH, basta abrir a ficha, preencher os dados e salvar — o aviso vira **ok**.

## Situações reais

* **Convidar um motorista.** Você contratou um motorista. Em **Pessoas → +**, escreva o nome, marque a função de **dirigir** e informe a **CNH** (ou conclua sem ela e regularize depois). No passo de acesso, deixe o papel **Motorista** sugerido, escolha **app no celular** e gere o link. Toque em **Copiar link** e mande no WhatsApp — ele abre, aceita e já vê **só os roteiros atribuídos a ele**.
* **Pessoa que faz duas coisas.** Seu ajudante de galpão também sai para conferir devoluções. No passo de acesso, marque **Separador** e **Conferente** juntos — um link só.
* **Cadastrar agora, liberar depois.** Você está montando o time, mas alguns só começam mês que vem. No passo de acesso, escolha **Só cadastro**. Eles ficam em **Sem acesso**, e você toca em **Conceder acesso →** no dia que cada um entrar.
* **CNH vencendo.** O sistema mostra a pendência de CNH vencida no card do motorista. Abra **Editar funções e CNH →**, atualize a **validade** e salve. O aviso some.

{% hint style="warning" %}
As opções desta tela dependem das **permissões** do seu usuário. Se você não vê "criar papel" ou "personalizar", seu perfil não tem esse acesso — fale com quem administra a conta.
{% endhint %}

## Próximo passo

* Entenda o modelo por trás disso em [Papéis, funções e competências](../conceitos/papeis-funcoes-competencias.md).
* Cadastre os veículos da equipe em [Frota](../cadastros/frota.md).
* Veja como tudo se encaixa no [Ciclo de um pedido](../conceitos/ciclo-de-um-pedido.md).
* Em dúvida com um termo? Consulte o [Glossário](../primeiros-passos/glossario.md) ou veja [onde tirar dúvidas](../primeiros-passos/onde-tirar-duvidas.md).
