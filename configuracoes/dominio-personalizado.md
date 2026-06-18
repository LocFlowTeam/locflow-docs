# Domínio personalizado

Por padrão, o link de pagamento que você envia ao cliente usa o endereço oficial do LocFlow. Com o **domínio personalizado**, esse link passa a usar **o seu próprio endereço** — por exemplo:

| | Endereço do link |
| --- | --- |
| **Padrão** | `pagamento.locflow.com.br/sua-empresa/orc1` |
| **Com domínio próprio** | `pagamento.suaempresa.com.br/orc1` |

O cliente paga numa página com **a sua marca** — mais confiança e profissionalismo na hora de receber.

{% hint style="info" %}
**Recurso premium.** O domínio personalizado faz parte dos planos superiores. Veja a disponibilidade em **Ajustes → Minha assinatura**. Mesmo sem ele, seu **endereço oficial LocFlow** já funciona e continua ativo para sempre — gratuito.
{% endhint %}

## Antes de começar

Você vai precisar de:

* Um **domínio próprio** já registrado (ex.: `suaempresa.com.br`), em um provedor como **Registro.br**, GoDaddy, Hostinger, Cloudflare, entre outros.
* Acesso ao **painel de DNS** desse provedor (onde você gerencia o domínio).
* Escolher um **subdomínio dedicado** para o pagamento — recomendamos `pagamento.suaempresa.com.br`.

{% hint style="warning" %}
Use sempre um **subdomínio** (`pagamento.suaempresa.com.br`), **nunca** o domínio raiz pelado (`suaempresa.com.br`). O raiz costuma já estar em uso pelo seu site e não é aceito aqui.
{% endhint %}

## Passo a passo

1. No app, abra **Ajustes → Integrações → Domínio personalizado**.
2. Digite o endereço que você quer usar (ex.: `pagamento.suaempresa.com.br`) e toque em **Começar configuração**.
3. O LocFlow vai mostrar **um ou mais registros de DNS** para você criar — normalmente um **CNAME** (e, às vezes, um **TXT** de verificação). Cada registro tem um **Nome** e um **Valor**; toque para **copiar**.
4. Abra o **painel de DNS** do seu provedor de domínio e **crie esses registros exatamente como mostrados** (veja abaixo como).
5. Volte ao app e toque em **Já configurei — verificar**.
6. Aguarde a confirmação. Quando tudo estiver pronto, o estado muda para **Domínio ativo** e seus links já passam a usar o seu endereço.

{% hint style="info" %}
A **propagação do DNS** pode levar de alguns **minutos a algumas horas** — é normal. Você pode fechar o app e voltar depois: o LocFlow verifica sozinho de tempos em tempos e ativa assim que o domínio estiver pronto. Não precisa configurar nada de certificado/HTTPS: o LocFlow cuida disso automaticamente, sem custo extra.
{% endhint %}

## Como criar o registro no seu provedor

O passo 4 acontece **fora do LocFlow**, no painel de quem cuida do seu domínio. O nome das telas muda de provedor para provedor, mas o caminho é sempre parecido:

1. Entre no painel do seu provedor de domínio e procure por **"DNS"**, **"Zona DNS"** ou **"Gerenciar registros"**.
2. Clique em **adicionar registro**.
3. Preencha com os dados que o LocFlow mostrou:
   * **Tipo:** `CNAME` (ou `TXT`, conforme o registro).
   * **Nome / Host:** o que aparece no campo **Nome** (ex.: `pagamento`).
   * **Valor / Destino / Aponta para:** o que aparece no campo **Valor**.
4. Salve. Repita para cada registro que o LocFlow listou.

{% hint style="warning" %}
Copie e cole **exatamente** o que o app mostra (sem espaços a mais). Um caractere trocado impede a verificação. Em caso de dúvida sobre onde colar, o suporte do seu provedor de domínio ajuda — esse é um procedimento comum.
{% endhint %}

## Perguntas frequentes

**Ainda não tenho um domínio. Preciso?**\
Só para usar o domínio próprio. Sem ele, seu **endereço oficial LocFlow** já funciona normalmente — você não fica sem cobrar.

**O link antigo para de funcionar?**\
Não. O endereço oficial continua ativo. O domínio próprio é um endereço **a mais**, com a sua marca.

**Posso trocar o domínio depois?**\
Pode. É só informar o novo endereço e refazer a verificação. O anterior é desativado automaticamente.

**Tem custo de certificado de segurança (HTTPS)?**\
Não. O cadeado de segurança é emitido e renovado pelo LocFlow, sem custo extra para você.
