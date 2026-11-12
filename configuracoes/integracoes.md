---
icon: plug
description: O hub de integrações do LocFlow — pagamento online, emissão de notas fiscais, sincronização em nuvem e domínio próprio, com o status de cada uma.
---

# Integrações

As **integrações** conectam o LocFlow a serviços de fora para você **receber pagamentos**, **emitir notas fiscais**, **guardar uma cópia dos seus documentos** e usar **o seu próprio endereço** nos links. Cada uma é **opcional**, tem a sua tela e funciona por conta própria — você liga só o que precisa.

Esta página é o **hub**: mostra o que cada integração faz e em que **estado** ela está. O passo a passo de cada uma fica na sua página dedicada (links abaixo).

## O que tem aqui

Em **Ajustes › Integrações** você encontra quatro itens. Cada um já mostra um **selo de estado** para você saber, de relance, o que está ligado:

| Item em Ajustes | Para que serve | Disponibilidade |
| --- | --- | --- |
| **Integração de Pagamento** | O cliente paga por um link (PIX, boleto, cartão) e a fatura baixa sozinha | Todos os planos |
| **Integração Fiscal** | Emitir notas fiscais de dentro do LocFlow: NFS-e, NF-e de venda e NF-e de remessa | Todos os planos (a NF-e de venda é do plano **Pro**) |
| **Domínio Personalizado** | Link de pagamento com o seu próprio endereço e a sua marca | Plano **Pro** |
| **Sincronização em Nuvem** | Cópia automática dos seus documentos e comprovantes no seu Google Drive | Todos os planos |

{% hint style="info" %}
**O selo de cada item é honesto.** Ele reflete a situação real da sua conta — por exemplo, **Inativo** quando você ainda não começou, **Homologação** quando a emissão de notas ainda está em teste, **Ativo** quando está tudo pronto. Veja a tabela completa em [Estados das integrações](#estados-das-integracoes).
{% endhint %}

{% hint style="warning" %}
Cada item só aparece para quem tem a **permissão** de configurá-lo — em geral, o dono e o **Administrador**. Se você não encontra uma integração, fale com quem administra a conta.
{% endhint %}

## Pagamento online <a id="pagamento-online"></a>

No app, o item se chama **Integração de Pagamento**. Ele conecta a sua organização a um **recebedor** — a conta da sua locadora que vai receber os valores — para que as cobranças virem **link de pagamento** com PIX, boleto e cartão, e o dinheiro caia na **sua conta bancária**. Quando o cliente paga, a fatura se atualiza sozinha, em tempo real. Serve igual para **locação** e para **venda** de bens móveis.

É um **cadastro guiado** (recebedor, dados e validação de identidade) e, depois de aprovado, você acompanha **saldo e transferências** pela própria tela.

{% hint style="success" %}
**Por que vale a pena:** quanto mais fácil pagar, mais gente paga — e mais cedo. Com o link pronto no fechamento, você recebe mais rápido e para de correr atrás de comprovante.
{% endhint %}

Veja o passo a passo completo — recebedor, validação, métodos e recebíveis — em [Pagamento online](../cobranca/pagamento-online.md).

## Sincronização em Nuvem <a id="sincronizacao-em-nuvem"></a>

Espelha os seus **documentos** (PDFs gerados), **comprovantes** — incluindo as **provas de entrega** da logística — e as **notas fiscais** (com o XML) para o **seu próprio Google Drive**. É uma **cópia de segurança** na sua conta: você é o dono dos arquivos, e eles ficam organizados numa pasta **LocFlow** **dividida por módulo** (Orçamentos, Cobranças, Logística, Estoque e Contábil), com o código do orçamento no nome de cada arquivo — pesquise por ele no Drive e ache tudo de um pedido de uma vez.

Você conecta a sua conta Google uma vez; depois disso, **novos arquivos são enviados sozinhos**, de tempos em tempos. A qualquer momento você pode acompanhar quantos estão **pendentes** e **sincronizados**, ver a última sincronização e **forçar uma agora**.

{% hint style="info" %}
**Os arquivos são seus, e não saem da sua cota do LocFlow.** A cópia vai para o **seu** Google Drive (que já vem com espaço gratuito), então não pesa no seu plano do LocFlow. Se um dia você desconectar, **o que já foi enviado continua no seu Drive** — só param os envios novos até reconectar.
{% endhint %}

Veja como conectar e acompanhar em [Sincronização em Nuvem](sincronizacao-em-nuvem.md).

## Integração Fiscal (notas fiscais) <a id="fiscal-nfe"></a>

A **Integração Fiscal** emite as suas notas **de verdade, dentro do LocFlow** — a nota sai do próprio orçamento, com os dados do cliente, dos itens e dos valores que você já preencheu, sem redigitar nada em outro sistema.

| Tipo de nota | Para quê | Plano |
| --- | --- | --- |
| **NFS-e** | A nota de serviço da locação | Todos os planos |
| **NF-e de remessa** | Acompanha os bens móveis que **saem** para o cliente e **voltam** — sem venda, regulariza o transporte | Todos os planos |
| **NF-e de venda** | A nota de produto, quando o item sai **em definitivo** | **Pro** |
| **MDF-e** | Manifesto de transporte das notas de um roteiro | **Em breve** |

Você cadastra a empresa e o **certificado digital A1** uma vez, num assistente guiado. A integração começa **em homologação** — o ambiente de teste, em que as notas **não têm valor fiscal** e **não consomem créditos** — e, com uma nota de teste autorizada, você **ativa a emissão em produção**: a partir daí cada nota sai valendo.

{% hint style="success" %}
**Primeiro é teste.** Ninguém precisa "mexer com a Receita" no escuro: dá para errar à vontade na homologação e só ligar a produção quando estiver seguro.
{% endhint %}

Depois de ativa, as notas ficam no menu **Fiscal › Notas Fiscais** (a [Central de notas](../fiscal/central-de-notas.md)), onde você emite, acompanha, baixa o PDF e o XML e cancela.

{% hint style="info" %}
**Quem configura e quem emite são pessoas diferentes.** Configurar a integração (empresa, certificado, virar para produção) é de quem administra a conta. Emitir notas é de quem tem a permissão fiscal — o papel **Operador / Atendente** já nasce emitindo NFS-e e NF-e de remessa. Quem só opera notas e encontra a integração desligada vê, no lugar do botão **Configurar**, o pedido: *"Peça a um administrador da organização para configurar a integração fiscal."*
{% endhint %}

O passo a passo completo — tipos de nota, NFS-e Nacional ou Municipal, certificado, numeração, do teste à produção — está em [Integração Fiscal](integracao-fiscal.md). Para entender qual nota cabe em cada operação, veja [Nota fiscal na locação](../conceitos/nota-fiscal-na-locacao.md) e [Nota fiscal na venda](../conceitos/nota-fiscal-na-venda.md).

## Domínio personalizado <a id="dominio-personalizado"></a>

Faz o link de pagamento usar **o seu próprio endereço** (ex.: `pagamento.suaempresa.com.br`) em vez do endereço padrão do LocFlow — mais confiança e profissionalismo na hora de cobrar. É um recurso dos **planos superiores** e tem página própria.

{% hint style="info" %}
Mesmo sem o domínio próprio, o seu **endereço oficial LocFlow** já funciona e fica ativo para sempre, sem custo. O domínio personalizado é um endereço **a mais**, com a sua marca.
{% endhint %}

Veja como configurar (incluindo os registros de DNS) em [Domínio personalizado](dominio-personalizado.md).

## Estados das integrações <a id="estados-das-integracoes"></a>

O selo no item de Ajustes (e dentro da tela de cada integração) resume a situação em uma palavra. Os principais:

| Integração | Selos possíveis | Quando aparece |
| --- | --- | --- |
| **Integração de Pagamento** | Inativo · Em validação · Recusado · Bloqueado · Ativo | De "ainda não cadastrado" a "recebendo". **Recusado** = o cadastro foi reprovado — corrigir os dados e reenviar resolve. **Bloqueado** = uma conta que já existia foi suspensa — reenviar dados não muda nada; fale com o suporte para regularizar. Detalhes em [Pagamento online](../cobranca/pagamento-online.md). |
| **Integração Fiscal** | Inativo · Em credenciamento · Homologação · Ativo · Suspenso | **Em credenciamento** = cadastro iniciado, falta concluir. **Homologação** = notas de teste, sem valor fiscal. **Ativo** = emitindo em produção. **Suspenso** = a emissão está parada; abra a tela da integração para ver o que falta. Detalhes em [Integração Fiscal](integracao-fiscal.md#estados). |
| **Sincronização em Nuvem** | Inativo · Ativo · Reconectar · Indisponível | **Reconectar** = o acesso ao Drive expirou ou foi revogado. **Indisponível** = ainda não habilitada na sua conta. |
| **Domínio Personalizado** | Inativo · Pendente · Ativo | **Pendente** = você informou o endereço e falta a verificação do DNS concluir. |

{% hint style="info" %}
Para ver o estado mais recente, abra a integração e **puxe a tela dela para baixo**: ela consulta de novo a situação — útil depois de concluir um cadastro ou uma autorização que você terminou no navegador. O selo da lista de Ajustes é lido quando a tela de Ajustes abre.
{% endhint %}

### Algumas coisas se concluem no navegador, não no app

Conectar o **pagamento online** (validação de identidade) e o **Google Drive** (autorização da conta) podem te levar a uma tela no **navegador** para concluir com segurança. Depois de terminar lá, **volte ao app e atualize** — o selo muda quando o LocFlow confirma.

{% hint style="warning" %}
**No celular, a compra e a troca de plano não acontecem dentro do app.** Por regra das lojas (Google Play e App Store), assinar, fazer upgrade ou comprar créditos é feito na **versão web** do LocFlow — no app você apenas **vê o status** e é orientado a concluir no painel. Isso vale para a assinatura; **receber dos seus clientes** pelo pagamento online continua normal no app.
{% endhint %}

## Por porte

| Porte | Por onde começar |
| --- | --- |
| **Autônomo / MEI** | Ligue só o **Pagamento online** com PIX — é o que mais muda o seu caixa. Se você emite nota, credencie a **Integração Fiscal** (MEI emite a NFS-e pelo padrão nacional). O resto pode esperar. |
| **Médio** | Some a **Integração Fiscal**, para a nota sair do próprio orçamento, e a **Sincronização em Nuvem**, para ter backup automático dos comprovantes, das provas de entrega e das notas (PDF e XML), sem pensar no assunto. |
| **Grande** | Combine **pagamento online + domínio personalizado** (sua marca no link), a **emissão fiscal** e a **nuvem**; acompanhe os selos para garantir que nada caiu (ex.: "Reconectar" ou "Suspenso"). |

## Situações reais <a id="situacoes-reais"></a>

* **Quero receber por PIX.** Ative o **Pagamento online**, conclua o cadastro do recebedor e a validação; depois de aprovado, o link da fatura já oferece PIX (e boleto/cartão, se você ligar).
* **Quero um backup dos comprovantes.** Conecte a **Sincronização em Nuvem**: seus PDFs e provas de entrega passam a ser copiados para o seu Google Drive sozinhos.
* **O selo da nuvem virou "Reconectar".** O acesso ao Drive expirou — abra a tela e reconecte; o que já foi enviado continua lá.
* **Preciso emitir nota.** Abra **Ajustes › Integrações › Integração Fiscal** e siga o assistente. Comece emitindo uma nota de teste (em homologação, sem valor fiscal) e, quando ela for autorizada, ative a produção. O passo a passo está em [Integração Fiscal](integracao-fiscal.md).
* **O certificado digital está vencendo.** A tela da Integração Fiscal mostra até quando ele vale (*"Válido até…"*). Compre o novo certificado A1 e envie o arquivo no cartão **Renovar certificado A1**, na mesma tela — sem refazer o cadastro.

## Próximo passo <a id="proximo-passo"></a>

* Configure recebimentos em [Pagamento online](../cobranca/pagamento-online.md).
* Emita notas fiscais pelo LocFlow em [Integração Fiscal](integracao-fiscal.md).
* Faça backup dos seus arquivos em [Sincronização em Nuvem](sincronizacao-em-nuvem.md).
* Use a sua marca no link em [Domínio personalizado](dominio-personalizado.md).
* Em dúvida com um termo? Consulte o [Glossário](../primeiros-passos/glossario.md).
