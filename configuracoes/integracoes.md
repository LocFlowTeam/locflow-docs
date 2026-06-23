---
icon: plug
description: O hub de integrações do LocFlow — pagamento online, sincronização em nuvem, fiscal (em breve) e domínio próprio, com o status de cada uma.
---

# Integrações

As **integrações** conectam o LocFlow a serviços de fora para você **receber pagamentos**, **guardar uma cópia dos seus documentos**, **emitir notas** e usar **o seu próprio endereço** nos links. Cada uma é **opcional**, tem a sua tela e funciona por conta própria — você liga só o que precisa.

Esta página é o **hub**: mostra o que cada integração faz e em que **estado** ela está. O passo a passo de cada uma fica na sua página dedicada (links abaixo).

## O que tem aqui

Em **Ajustes → Integrações** você encontra quatro cartões. O cartão já mostra um **selo de estado** para você saber, de relance, o que está ligado:

| Integração | Para que serve | Estado típico |
| --- | --- | --- |
| **Pagamento online** | O cliente paga por um link (PIX, boleto, cartão) e a fatura baixa sozinha | Disponível |
| **Sincronização em Nuvem** | Cópia automática dos seus documentos e comprovantes no seu Google Drive | Disponível |
| **Fiscal / NF-e** | Emitir notas fiscais (NFSe, NFe de venda, NF de remessa) | **Em breve** |
| **Domínio personalizado** | Link de pagamento com o seu próprio endereço e a sua marca | Disponível (planos superiores) |

{% hint style="info" %}
**O selo de cada cartão é honesto.** Ele reflete a situação real da sua conta — por exemplo, **Inativo** quando você ainda não começou, **Ativo** quando está tudo pronto, ou **Em breve** para o que ainda não foi liberado. Veja a tabela completa em [Estados das integrações](#estados-das-integracoes).
{% endhint %}

## Pagamento online <a id="pagamento-online"></a>

Conecta a sua organização a um **recebedor** — a conta da sua locadora que vai receber os valores — para que as cobranças virem **link de pagamento** com PIX, boleto e cartão, e o dinheiro caia na **sua conta bancária**. Quando o cliente paga, a fatura se atualiza sozinha, em tempo real. Serve igual para **locação** e para **venda** de bens móveis.

É um **cadastro guiado** (recebedor, dados e validação de identidade) e, depois de aprovado, você acompanha **saldo e transferências** pela própria tela.

{% hint style="success" %}
**Por que vale a pena:** quanto mais fácil pagar, mais gente paga — e mais cedo. Com o link pronto no fechamento, você recebe mais rápido e para de correr atrás de comprovante.
{% endhint %}

Veja o passo a passo completo — recebedor, validação, métodos e recebíveis — em [Pagamento online](../cobranca/pagamento-online.md).

## Sincronização em Nuvem <a id="sincronizacao-em-nuvem"></a>

Espelha os seus **documentos** (PDFs gerados) e **comprovantes** — incluindo as **provas de entrega** da logística — para o **seu próprio Google Drive**. É uma **cópia de segurança** na sua conta: você é o dono dos arquivos, e eles ficam organizados numa pasta **LocFlow** (com subpastas para Documentos e Provas logísticas).

Você conecta a sua conta Google uma vez; depois disso, **novos arquivos são enviados sozinhos**, de tempos em tempos. A qualquer momento você pode acompanhar quantos estão **pendentes** e **sincronizados**, ver a última sincronização e **forçar uma agora**.

{% hint style="info" %}
**Os arquivos são seus, e não saem da sua cota do LocFlow.** A cópia vai para o **seu** Google Drive (que já vem com espaço gratuito), então não pesa no seu plano do LocFlow. Se um dia você desconectar, **o que já foi enviado continua no seu Drive** — só param os envios novos até reconectar.
{% endhint %}

Veja como conectar e acompanhar em [Sincronização em Nuvem](sincronizacao-em-nuvem.md).

## Fiscal / NF-e <a id="fiscal-nfe"></a>

A emissão de notas fiscais está **em construção**. A ideia é você escolher quais notas pretende emitir e seguir um passo a passo para habilitar:

| Tipo de nota | O que é |
| --- | --- |
| **NFSe** | Nota Fiscal de Serviço |
| **NFe de Venda** | Nota Fiscal eletrônica de venda |
| **NF de Remessa de Bens** | Para a movimentação de itens (saída e retorno) |

{% hint style="info" %}
**Em breve.** A tela já existe como **pré-visualização**: você seleciona os tipos de nota e ela mostra o roteiro que será necessário (dados da empresa, prefeitura e certificado, no caso da NFSe). Mas a **emissão ainda não está ativa** — nada é emitido por enquanto. Quando entrar no ar, esta página ganha o passo a passo completo.
{% endhint %}

{% hint style="warning" %}
Quando a parte fiscal for liberada, ela será um **adicional do contrato** — habilitada nos planos que a incluírem. Aqui só sinalizamos a previsão; a disponibilidade fica em **Ajustes → Minha assinatura**.
{% endhint %}

## Domínio personalizado <a id="dominio-personalizado"></a>

Faz o link de pagamento usar **o seu próprio endereço** (ex.: `pagamento.suaempresa.com.br`) em vez do endereço padrão do LocFlow — mais confiança e profissionalismo na hora de cobrar. É um recurso dos **planos superiores** e tem página própria.

{% hint style="info" %}
Mesmo sem o domínio próprio, o seu **endereço oficial LocFlow** já funciona e fica ativo para sempre, sem custo. O domínio personalizado é um endereço **a mais**, com a sua marca.
{% endhint %}

Veja como configurar (incluindo os registros de DNS) em [Domínio personalizado](dominio-personalizado.md).

## Estados das integrações <a id="estados-das-integracoes"></a>

O selo no cartão (e dentro da tela de cada integração) resume a situação em uma palavra. Os principais:

| Integração | Selos possíveis | Quando aparece |
| --- | --- | --- |
| **Pagamento online** | Inativo · Em validação · Recusado · Ativo | De "ainda não cadastrado" a "recebendo". Detalhes em [Pagamento online](../cobranca/pagamento-online.md). |
| **Sincronização em Nuvem** | Inativo · Ativo · Reconectar · Indisponível | **Reconectar** = o acesso ao Drive expirou ou foi revogado. **Indisponível** = ainda não habilitada na sua conta. |
| **Fiscal / NF-e** | Em breve | Pré-visualização; emissão ainda não liberada. |
| **Domínio personalizado** | Inativo · Pendente · Ativo | **Pendente** = você informou o endereço e falta a verificação do DNS concluir. |

{% hint style="info" %}
Puxe a tela de Integrações para baixo para **atualizar os selos** — útil depois de concluir um cadastro ou uma autorização que você terminou no navegador.
{% endhint %}

### Algumas coisas se concluem no navegador, não no app

Conectar o **pagamento online** (validação de identidade) e o **Google Drive** (autorização da conta) podem te levar a uma tela no **navegador** para concluir com segurança. Depois de terminar lá, **volte ao app e atualize** — o selo muda quando o LocFlow confirma.

{% hint style="warning" %}
**No celular, a compra e a troca de plano não acontecem dentro do app.** Por regra das lojas (Google Play e App Store), assinar, fazer upgrade ou comprar créditos é feito na **versão web** do LocFlow — no app você apenas **vê o status** e é orientado a concluir no painel. Isso vale para a assinatura; **receber dos seus clientes** pelo pagamento online continua normal no app.
{% endhint %}

## Por porte

| Porte | Por onde começar |
| --- | --- |
| **Autônomo / MEI** | Ligue só o **Pagamento online** com PIX — é o que mais muda o seu caixa. O resto pode esperar. |
| **Médio** | Some a **Sincronização em Nuvem** para ter backup automático dos comprovantes e provas de entrega, sem pensar no assunto. |
| **Grande** | Combine **pagamento online + domínio personalizado** (sua marca no link) e a **nuvem**; acompanhe os selos para garantir que nada caiu (ex.: "Reconectar"). |

## Situações reais <a id="situacoes-reais"></a>

* **Quero receber por PIX.** Ative o **Pagamento online**, conclua o cadastro do recebedor e a validação; depois de aprovado, o link da fatura já oferece PIX (e boleto/cartão, se você ligar).
* **Quero um backup dos comprovantes.** Conecte a **Sincronização em Nuvem**: seus PDFs e provas de entrega passam a ser copiados para o seu Google Drive sozinhos.
* **O selo da nuvem virou "Reconectar".** O acesso ao Drive expirou — abra a tela e reconecte; o que já foi enviado continua lá.
* **Preciso emitir nota.** Por enquanto, a emissão fiscal está **em breve** — a tela mostra o roteiro, mas ainda não emite. Acompanhe esta página.

## Próximo passo <a id="proximo-passo"></a>

* Configure recebimentos em [Pagamento online](../cobranca/pagamento-online.md).
* Faça backup dos seus arquivos em [Sincronização em Nuvem](sincronizacao-em-nuvem.md).
* Use a sua marca no link em [Domínio personalizado](dominio-personalizado.md).
* Em dúvida com um termo? Consulte o [Glossário](../primeiros-passos/glossario.md).
