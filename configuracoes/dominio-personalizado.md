# Domínio personalizado

Com o **domínio personalizado**, o LocFlow passa a usar **o seu próprio endereço** em duas pontas da sua operação — tudo com a sua marca:

| Onde | O que é | Endereço com domínio próprio |
| --- | --- | --- |
| **Painel** | Onde **você e sua equipe** acessam o sistema | `painel.suaempresa.com.br` |
| **Pagamento** | Onde **o seu cliente** paga a cobrança | `pagamento.suaempresa.com.br` |

Em vez do endereço padrão do LocFlow, sua equipe entra no sistema pelo **seu** domínio e o cliente paga numa página com a **sua** marca — mais confiança e profissionalismo de ponta a ponta.

{% hint style="info" %}
**Recurso premium.** O domínio personalizado faz parte dos planos superiores — veja a disponibilidade em **Ajustes → Minha assinatura**. Mesmo sem ele, seus **endereços oficiais LocFlow** já funcionam e continuam ativos para sempre, gratuitos.
{% endhint %}

Você pode configurar **as duas pontas ou só uma** — cada uma é independente.

## Antes de começar

Você vai precisar de:

* Um **domínio próprio** já registrado (ex.: `suaempresa.com.br`), em um provedor como **Registro.br**, GoDaddy, Hostinger, Cloudflare, entre outros.
* Acesso ao **painel de DNS** desse provedor (onde você gerencia o domínio).
* Escolher um **subdomínio dedicado** para cada ponta — recomendamos `painel.suaempresa.com.br` e `pagamento.suaempresa.com.br`.

{% hint style="warning" %}
Use sempre um **subdomínio** (`painel.` / `pagamento.` na frente), **nunca** o domínio raiz pelado (`suaempresa.com.br`). O raiz costuma já estar em uso pelo seu site e não é aceito aqui.
{% endhint %}

## Passo a passo

Em **Ajustes → Integrações → Domínio personalizado** você verá uma seção para o **Painel** e outra para a **Página de pagamento**. O processo é o mesmo nas duas — faça para a(s) que quiser:

1. Na seção desejada, digite o endereço (ex.: `painel.suaempresa.com.br`) e toque em **Começar configuração**.
2. O LocFlow vai mostrar **um ou mais registros de DNS** para criar — normalmente um **CNAME** (e, às vezes, um **TXT** de verificação). Cada registro tem um **Nome** e um **Valor**; toque para **copiar**.
3. Abra o **painel de DNS** do seu provedor de domínio e **crie esses registros exatamente como mostrados** (veja abaixo como).
4. Volte ao app e toque em **Já configurei — verificar**.
5. Quando ficar pronto, o estado muda para **Ativo** ✅. A partir daí, aquele endereço já é o seu.

{% hint style="info" %}
A **propagação do DNS** pode levar de alguns **minutos a algumas horas** — é normal. Você pode fechar o app e voltar depois: o LocFlow verifica sozinho de tempos em tempos e ativa assim que o domínio estiver pronto. Não precisa mexer em certificado/HTTPS: o LocFlow cuida disso automaticamente, sem custo extra.
{% endhint %}

## Como criar o registro no seu provedor

O passo 3 acontece **fora do LocFlow**, no painel de quem cuida do seu domínio. O nome das telas muda de provedor para provedor, mas o caminho é sempre parecido:

1. Entre no painel do seu provedor de domínio e procure por **"DNS"**, **"Zona DNS"** ou **"Gerenciar registros"**.
2. Clique em **adicionar registro**.
3. Preencha com os dados que o LocFlow mostrou:
   * **Tipo:** `CNAME` (ou `TXT`, conforme o registro).
   * **Nome / Host:** o que aparece no campo **Nome** (ex.: `painel` ou `pagamento`).
   * **Valor / Destino / Aponta para:** o que aparece no campo **Valor**.
4. Salve. Repita para cada registro que o LocFlow listou — e para cada superfície (painel e pagamento), se for usar as duas.

{% hint style="warning" %}
Copie e cole **exatamente** o que o app mostra (sem espaços a mais). Um caractere trocado impede a verificação. Em caso de dúvida sobre onde colar, o suporte do seu provedor de domínio ajuda — esse é um procedimento comum.
{% endhint %}

## Perguntas frequentes

**Preciso configurar as duas pontas?**\
Não. Painel e pagamento são independentes — configure só a que fizer sentido para você, ou as duas.

**Ainda não tenho um domínio. Preciso?**\
Só para usar o domínio próprio. Sem ele, seus **endereços oficiais LocFlow** já funcionam normalmente.

**O endereço antigo para de funcionar?**\
Não. Os endereços oficiais continuam ativos. O domínio próprio é um endereço **a mais**, com a sua marca.

**Posso trocar o domínio depois?**\
Pode. É só informar o novo endereço e refazer a verificação. O anterior é desativado automaticamente.

**Tem custo de certificado de segurança (HTTPS)?**\
Não. O cadeado de segurança é emitido e renovado pelo LocFlow, sem custo extra para você.