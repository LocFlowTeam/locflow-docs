# Plano de Documentação Pública do LocFlow — Fonte da Verdade das Regras de Negócio (locação E venda)

> Proposta para aprovação do dono. Repositório: `locflow-docs` (GitBook, publicado em `docs.locflow.com.br`). Princípio orientador do dono, fielmente: **a documentação deve ser a fonte da verdade de TODAS as regras de negócio que locação e venda de bens móveis pedem — abrangente, didática, fácil, bem organizada, tela a tela, sem nada de fora, com profundidade progressiva** (quanto mais o locador se aprofunda, mais conceito aparece, passo a passo), aproveitando as trilhas de leitura e o onboarding que já existem.

---

## 1. Diagnóstico

Foram cruzados **14 módulos** do app contra a documentação existente.

**Volume mapeado (somando o JSON):**
- **Telas mapeadas:** ~169 telas (Acesso 9, Setup 10, Painel/Calendário/Notif/Ajuda 5, Contatos 2, Produtos 9, Kits 6, Frota 10, Orçamentos 14, Cobrança 9, Logística 9, Estoque 5, Motores 11, Central de Notificações 6, Colaboradores 11, Horários/Modelos/Identidade 14, Assinatura/Integrações/Conta 15).
- **Textos de ajuda contextual ("?", InfoHint, CartãoDica, AjudaIcone, banners verbatim) achados:** ~218 (destaques: Motores 28, Horários/Modelos 44, Central de Notificações 17, Assinatura/Integrações 19, Orçamentos 15, Frota 14, Logística 14, Cobrança 14, Produtos 11, Setup 8, Contatos 7).
- **Conceitos de negócio catalogados:** ~250 (somatório das listas de cobertura).

**Veredito de cobertura atual (qualitativo, ponderado pelos módulos):**

| Faixa | Situação |
|---|---|
| **Bem coberto (~35%)** | Núcleo conceitual já maduro: funil/estados de orçamento, faturas/parcelas/desdobramento, separação, conferência, POD, defasagem (`quando-um-pedido-muda` é exemplar), domínio personalizado, identidade visual, central de notificações (núcleo), papéis/funções/competências (núcleo), bloqueio de estoque + folgas. |
| **Parcial (~30%)** | Conceito existe mas falta a regra precisa ou o comportamento de tela: natureza única do orçamento, recebedor/KYC (3 de 7 estados), galpão no mapa, fila de cobranças, vistoria/capacidade da frota (modelo antigo), aprovação inline vs por regra. |
| **Ausente (~35%)** | Telas/fluxos inteiros sem nenhuma página: Painel + Calendário logístico, Motor de Frete de cálculo (rota estimada, por-rota-não-por-viagem, perfis, gatilhos, versionamento, simulador), Sincronização em Nuvem (Drive), Programa de Parceiros/split, Minha conta + Preferências, página pública de pagamento `/pagar/:token`, jornada "Ver Logística" + eixo de responsabilidade, listagem/tela única de roteiro, histórico de preços de produto/kit, segregação de estoque por natureza+condição, designer de documentos (variáveis, ocultar-quando-vazio, kit agrupado, compositor logístico). |

**Achados críticos que exigem correção, não só adição:**
1. **Erro factual** — `conceitos/locacao-e-venda.md` afirma "no mesmo orçamento você combina itens de aluguel e de venda". O seletor de natureza prova que **a natureza é única e trocá-la apaga os itens**.
2. **Desatualização** — `configurando-sua-empresa.md` anuncia **6 passos com "Motores"**; hoje são **5 passos** e Motores saiu do onboarding. O passo 3 está descrito como "logo/cores", mas hoje é só fuso + horário comercial.
3. **Divergência** — `execucao-em-campo.md` diz "veículo é opcional para iniciar"; o preparo agora **exige veículo concreto ATIVO** (e virou wizard de 4 passos). *(Correção da auditoria: `planejando-o-roteiro.md` está OK — os "três caminhos" de veículo seguem válidos no PLANEJAMENTO; só a EXECUÇÃO mudou.)*
4. **Imprecisão/contradição** — `colaboradores-e-acessos.md` diz "você não cadastra e-mail"; na verdade o **e-mail é opcional e, se informado, trava o aceite**.
5. **Contradição potencial** — `criando-sua-conta.md` afirma "acesso imediato, não chega e-mail de confirmação"; o cadastro **pode exigir confirmação por e-mail**.

---

## 2. Princípios editoriais a preservar

Estes padrões já estão validados nas páginas existentes e são **invioláveis** em tudo que for escrito:

- **Tom "você"**, direto, sem jargão técnico de engenharia (nada de `CAT.PRODUTO.CRIAR`, `409`, `JWT`, `categoriaMatchInfo`, `Broadcast`). O efeito visível, não o mecanismo.
- **Terminologia: "bens móveis" / "itens", NUNCA "equipamentos"** — mesmo quando a copy do app usa "equipamento" (ex.: ajuda do valor de reposição/NF-e) ou "material". O LocFlow atende **locação E venda**: todo exemplo dá os dois lados (aluguel = duas pontas / pré-reserva+reserva; venda = uma ponta / vendido).
- **Frontmatter** com `icon` + `description` em toda página.
- **Callouts** `{% hint style="info|success|warning" %}` para conceitos não óbvios; **warning** para regras que custam dinheiro se ignoradas (ex.: frete por rota), **success** para "por que isso te faz faturar mais".
- **Tabelas** para estados/legendas e **mermaid** para fluxos e máquinas de estado.
- **Seções recorrentes**: "Situações reais", a tabela "Pequeno / médio / grande" (por porte), e "Próximo passo" com links relativos ao fim de cada página.
- **Recursos "em breve"** entram como bloco curto com callout (padrão de `galpoes-e-disponibilidade.md`), sem fixar preços/nomes de planos (catálogo de planos é mock de UI).
- **Cor âmbar como fio condutor pedagógico**: "âmbar = ação que você precisa resolver agora" — alinhado ao calendário (nível 4), à pilha "Pendente de informação" e aos avisos de formulário.

---

## 3. Modelo de profundidade progressiva

A regra do dono "quanto mais fundo, mais detalhe" vira **três camadas explícitas por tema**, marcadas no `description`/frontmatter e na ordem do SUMMARY:

| Camada | O que entra | Quem lê | Posição |
|---|---|---|---|
| **Essencial** | O que a tela faz, o conceito-chave, o caminho feliz. Sem fórmulas. | Todo locador, no 1º contato. | Topo da página / página-porta de cada módulo. |
| **Intermediário** | Regras de negócio, estados, exceções, "como destravar X". | Quem já opera e quer dominar. | Seções finais da página-porta OU página-filha dedicada. |
| **Avançado** | Fórmulas ("Para quem quer os números"), versionamento, permissões finas, mecânica interna visível, blocos do designer. | Operação madura / quem configura. | Página-filha avançada, aninhada no SUMMARY. |

**Como escala dentro de uma página:** abertura essencial → "Situações reais" → bloco intermediário → callout/bloco "Para quem quer os números" (avançado) no fim. Quando o tema é grande, **extrai-se uma página-filha** em vez de inchar a porta (ex.: Frota → `frota-capacidade` + `frota-vistoria`).

**Amarração nas trilhas existentes** (`trilhas-de-leitura.md`): cada nova página entra na trilha por **porte** e por **papel** já existente. Propostas concretas de atualização das trilhas:
- "Começando (sozinho)": acrescentar **O Painel (tela inicial)** logo após Configuração inicial.
- "Crescendo (com equipe)": acrescentar **Motor de Frete (essencial)** e **A jornada de um pedido na logística**.
- "Estruturada (galpão + frota)": acrescentar **Calendário logístico**, **Especificações: capacidade** e **Designer de documentos**.
- Por papel: **Financeiro** ganha "Emitindo a cobrança" e "A página de pagamento do cliente"; **Motorista** ganha "Execução em lote" e "Cobrança na rua".

**Fechar o loop (deep link app → doc):** o achado central do mapeamento é que vários módulos **não têm ajuda contextual nenhuma** (Acesso = 0 ajudas, Contatos = 7, Estoque = 1) — a doc pública é o único lugar onde o locador entende os estados sutis. Proposta: **cada botão "?" / AjudaIcone do app passa a apontar para o ancoramento (`#secao`) da página de doc correspondente** (deep link com fragmento). A doc deve ser escrita com **âncoras estáveis por microconceito** (ex.: `motor-de-frete.md#por-rota-nao-por-viagem`) para que o app linke direto. Isso é uma decisão a aprovar (§8) porque exige um pequeno trabalho no app (mapa ajuda→URL).

---

## 4. Arquitetura proposta da documentação (SUMMARY evoluído)

Resumo: **2 seções novas** ("Painel" e — opcional — separar "Conta e assinatura"), **~30 páginas novas**, **~22 páginas a melhorar**. Abaixo, o SUMMARY proposto com marcação de ação `[NOVA]`/`[MELHORAR]` e a camada de profundidade `(E/I/A)`. Páginas-filhas aninhadas para preservar a hierarquia do GitBook.

```markdown
# Resumo
* Bem-vindo ao LocFlow (README)

## Primeiros passos
* A filosofia do LocFlow
* Trilhas de leitura            [MELHORAR] (incluir novas páginas nas trilhas)
* Onde tirar dúvidas            [MELHORAR] (E) sessão de chat exclusiva, atalho ? global, suporte@/Instagram
* Criando sua conta             [MELHORAR] (E) login, senha mín.6, confirmação de e-mail, web-first
* Recuperar sua senha           [NOVA]     (E)
* Criando sua locadora (onboarding)        [NOVA] (I) web-first, trial x pago, CNPJ x CPF, 1 org/usuário
* Plano e pagamento inicial     [NOVA]     (A) catálogo mock, checkout só web
* Aceitando um convite          [NOVA]     (I) estados, e-mail vinculado, 1 org/usuário, gates de plataforma
* Configuração inicial          [MELHORAR] (E) corrigir 6→5 passos, remover Motores, linear/retomada
  * O setup passo a passo       [NOVA]     (I) os 5 passos com os textos de ajuda reais
  * Como o setup se comporta     [NOVA]    (A) retomada, web x nativo, ponte, adiar, celebração
* Glossário do LocFlow          [MELHORAR] (E) +org, trial, recebedor, KYC, rota estimada, etc.

## Conceitos essenciais
* O ciclo de um pedido
* Locação e venda               [MELHORAR] (E) CORRIGIR natureza única + reset ao trocar
* Papéis, funções e competências [MELHORAR] (A) fork, curinga *, sugestão de papel

## Painel                       [SEÇÃO NOVA]
* O Painel (sua tela inicial)   [NOVA]     (E) 5 cards, gating duplo, personalizar, banner rodapé
* Indicadores                   [NOVA]     (I) contratado x recebido, ganhos, conversão/perda, cancelamento
* O funil de vendas no painel   [NOVA]     (A) taxa de passagem, gargalo, fórmulas
* O card de Logística no painel [NOVA]     (I) 3 pilhas, pendente de informação, selo Rota/Balcão
* Calendário logístico          [NOVA]     (A) níveis 1-5, cores, ícones, fusos, fórmulas

## Cadastros
* Contatos                      [MELHORAR] (E) ficha enxuta do lead, doc opcional, listagem
  * Completar dados sob demanda [NOVA]     (I)
  * Funil, permissões e exclusão [NOVA]    (A)
* Catálogo: produtos            [MELHORAR] (E) valor de reposição (4 funções), SKU auto, fiscal, status
  * Estoque por natureza e condição [NOVA] (I) segregação + exemplo das 10 unidades
  * Histórico de preços e como reverter [NOVA] (I)
  * Catálogo da comunidade (em breve)  [bloco] (A)
* Catálogo: kits                [MELHORAR] (E) itens distintos x unidades, composição, status
  * Quando o kit aluga ou vende (elegibilidade e condições) [NOVA] (I)
  * Montando kits prontos (fluxo guiado em lote) [NOVA] (I)
  * Histórico de preços do kit  [NOVA]     (A)
* Frota                         [MELHORAR] (E) hierarquia, hub, classe, status, em-trânsito
  * Especificações: capacidade  [NOVA]     (I) estratégias em ordem, baú fechado, contagem, volumétrica
  * Especificações: vistoria    [NOVA]     (A) 5 gatilhos, modelos de checklist

## Orçamentos
* Criando um orçamento          [MELHORAR] (E) responsável PJ obrigatório, ponteiros p/ novas páginas
* Movimentos, janelas e galpão de origem [NOVA] (I) intervalo salvo x exclusivo, a-definir, proximidade
* Endereços e endereços salvos  [NOVA]     (E) (ou seção dentro de Movimentos — decisão §8)
* Valores: mão de obra, frete e descontos [NOVA] (I) frete por movimento, viagens, desconto por kits
* Duração, cobrança e bloqueio de uso (locação) [NOVA] (A) tríade cobrança/uso/estoque, multiplicador
* Acompanhando e fechando       [MELHORAR] (I) matriz documentos x status/natureza, jornada, dry-run
* Aprovação de orçamentos       [MELHORAR] (I) pré-aprovação inline x congelamento por regra

## Cobrança
* Cobranças: a lista e o que mostra [NOVA]  (E) busca, filtros, saldo do filtro, card
* Faturas e parcelas            [MELHORAR] (E) cobrança=fatura, congelada read-only, saldo, natureza
* Emitindo a cobrança           [NOVA]     (I) à vista/sinal/parcelado, D+X, editar parcelas
* Recebendo pagamentos          [MELHORAR] (I) editar vencimento, histórico de tentativas
* Pagamento online              [MELHORAR] (A) instrumento, pré-requisitos por método, recebedor 4 passos, KYC
* A página de pagamento do cliente [NOVA]  (A) /pagar/:token, tokenização, selos de confiança

## Logística
* Visão geral da logística      [MELHORAR] (E) 6 fases nomeadas, fase Finanças, status por fase
* A jornada de um pedido (Ver Logística) [NOVA] (I) eixo de responsabilidade, modal "como funciona"
* Acompanhando seus roteiros (listagem + tela única) [NOVA] (E) abas, filtro, estados, ao-vivo
* Planejando o roteiro          [MELHORAR] (I) corrigir veículo, galpão único, CNH, ver-trânsito
* Execução em campo             [MELHORAR] (A) wizard 4 passos, veículo obrigatório, gates, bolha, cobrar na rua
* Execução em lote (retroativa) [NOVA]     (A)
* Separação no galpão
* Conferência na devolução
* Quando um pedido muda         [MELHORAR] (I) banners verbatim

## Estoque
* Galpões e disponibilidade     [MELHORAR] (I/E) painel de estoque, mapa em 4 passos, limite por plano
                                            (disponibilidade locação x venda, agnóstico de natureza)

## Documentos e marca
* Modelos personalizados        [MELHORAR] (I) preview exemplo x real, permissões, modelo herdado
* Designer: blocos, variáveis e regras [NOVA] (A) variáveis, ocultar-quando-vazio, kit agrupado, logística
* Identidade visual

## Configurações
* Motores operacionais          [MELHORAR] (E) hub com 2 grupos, operação do orçamento, agendamento
  * Motor de Frete: como calcula [NOVA]    (E→I) rota estimada, por-rota, perfis, simulador, versões
  * Montando as cobranças do frete [NOVA]  (I) gatilhos, cobrar-por x critério, combinação, conflito
  * Motor de Frete avançado     [NOVA]     (A) regras, ações com ordem fixa, parâmetros, versionamento
  * Motor de Orçamento (corte + padrões) [NOVA] (I) valor mínimo versionado x taxa/validade/intervalo
* Central de Notificações       [MELHORAR] (E) override x padrão, prévia, em-breve, guard de saída
  * Canais de notificação       [NOVA]     (I) criar/editar/remover, desvínculo, badges
* Colaboradores e acessos       [MELHORAR] (E) cadastro 4 passos, conceder x convidar, pills, busca
  * (subseções) convite: link/plataforma/e-mail vinculado [MELHORAR] (I) — CORRIGIR e-mail
  * (subseção) CNH e pendências do colaborador [MELHORAR] (I) categorias, nunca bloqueia, veículo padrão
* Horários e sazonalidades      [MELHORAR] (I) GPS, sazonalidade que cruza o ano
* Minha assinatura e créditos   [MELHORAR] (I) reembolso CDC 7 dias, compra só web, status-only
* Sincronização em Nuvem (Drive) [NOVA]    (I)
* Integrações                   [MELHORAR] (E) incluir nuvem no hub, fiscal em construção
* Programa de Parceiros         [NOVA]     (A) split, funil de liberação, taxa de plataforma
* Domínio personalizado         [MELHORAR] (E) alinhar termo Enterprise
* Minha conta e preferências    [NOVA]     (E) excluir conta, preferências locais, perfil da empresa

## Ajuda
* Perguntas frequentes
```

---

## 5. Matriz de cobertura tela-a-tela

| Módulo | Telas | Ajudas | Cobertos | Parciais | Ausentes | Buracos mais críticos |
|---|---:|---:|---|---|---|---|
| Acesso e criação de conta | 9 | 0 | ~2 | ~9 | ~12 | onboarding web-first, CNPJ x CPF, e-mail vinculado, 1 org/usuário, recuperar senha, wizard de criação da locadora |
| Configuração inicial (setup) | 10 | 8 | 1 | ~7 | ~7 | **6→5 passos (erro)**, retomada, web x nativo, adiar, celebração, 8 textos de ajuda |
| Painel / Calendário / Notif / Ajuda | 5 | 22 | ~6 | ~10 | ~13 | **Painel inteiro, Calendário logístico inteiro**, indicadores, funil-fórmulas |
| Contatos | 2 | 7 | ~7 | ~4 | ~2 | **completar dados sob demanda**, permissões/lixeira, ficha enxuta do lead |
| Catálogo — produtos | 9 | 11 | ~10 | ~7 | ~4 | **estoque por natureza+condição**, **histórico de preços**, valor de reposição (4 funções) |
| Catálogo — kits | 6 | 2 | ~4 | ~5 | ~6 | **elegibilidade aluga/vende**, **produtos faltantes**, histórico de preços, status |
| Frota | 10 | 14 | ~9 | ~7 | ~3 | **capacidade por estratégias + baú fechado** (modelo antigo), **vistoria por 5 gatilhos** (obsoleta) |
| Orçamentos | 14 | 15 | ~6 | ~9 | ~13 | **natureza única (erro)**, movimentos/janelas (4+4 ajudas), duração/bloqueio de uso, valores/descontos |
| Cobrança | 9 | 14 | ~12 | ~9 | ~6 | **emitir cobrança** (à vista/sinal/parcelado/D+X), **página pública do cliente**, histórico de tentativas |
| Logística | 9 | 14 | ~14 | ~9 | ~7 | **Ver Logística + eixo de responsabilidade**, **listagem/tela única**, veículo obrigatório (divergência) |
| Estoque / galpões | 5 | 1 | ~12 | ~5 | ~2 | mapa em 4 passos, limite de galpões por plano, painel/hub de estoque |
| Motores operacionais | 11 | 28 | ~7 | ~6 | ~13 | **Motor de Frete de cálculo inteiro**, Motor de Orçamento (corte versionado) |
| Central de Notificações | 6 | 17 | ~16 | ~9 | ~4 | tela de Canais (criar/remover/desvínculo), override x padrão, prévia, guard de saída |
| Colaboradores / papéis | 11 | 2 | ~9 | ~9 | ~5 | **cadastro 4 passos**, **e-mail vinculado (correção)**, CNH detalhada, veículo padrão |
| Horários / Modelos / Identidade | 14 | 44 | ~12 | ~3 | ~10 | **designer: variáveis, ocultar-quando-vazio, kit agrupado, compositor logístico** |
| Assinatura / Integrações / Conta | 15 | 19 | ~7 | ~7 | ~9 | **Nuvem (Drive)**, **Programa de Parceiros**, **Minha conta**, reembolso CDC, recebedor 4 passos |

A garantia de "nada fica de fora" é esta matriz: cada conceito do mapeamento foi atribuído a uma página (§4) com camada de profundidade.

---

## 6. Os botões de ajuda como fonte (microconceitos sem doc — os mais valiosos)

Estes textos de ajuda do app são regras de negócio que **hoje só existem dentro do "?" e não na doc**. São a matéria-prima de maior valor.

- **Orçamentos (15 ajudas, só 1 documentada):** AjudaIcone Janela Logística (Movimento / Intervalo Salvo / Intervalo Exclusivo / Validações); InfoHints "a definir" (entrega/retirada/galpão); AjudaIcone Janela de bloqueio de uso (uso x turnaround + política atual); AjudaIcone Galpão por proximidade + estados de disponibilidade; InfoHint "Frete desativado"; Desconto proporcional aos kits (ativo/sugestão/bloqueio); InfoHint troca de natureza apaga itens.
- **Motores (28 ajudas):** "por rota, não por viagem" (R$500 fixo → R$2.000 em aluguel de 4 rotas); rota estimada (pior cenário); perfis Simples/Intermediário/Avançado; cobrar-por x usar-como-critério; primeira-compatível x acumuladora; ordem matemática fixa das ações; simulador local sem créditos; corte de orçamento.
- **Horários/Modelos (44 ajudas):** hints por bloco do designer (chips de variável, coluna de foto do item, total em destaque, "deixe em branco para a logo da org"); ocultar-quando-vazio; kit Normal x Agrupamento; compositor logístico ("Logística a definir.", mesmo local, horário condicional); banner "Modelo herdado do sistema"; "Usar minha localização" (fuso por GPS); sazonalidade que cruza o ano.
- **Central de Notificações (17):** prévia "Como o aviso chega"; override x padrão de fábrica + "voltar ao padrão"; seção "Em breve" read-only; alterações não salvas / guard de saída; remover canal desvincula de todos os avisos.
- **Frota (14):** "Baú fechado habilita a volumétrica"; estratégias avaliadas em ordem (a 1ª que reprova limita); 5 gatilhos de vistoria + frases-resumo; modelos de checklist com presets.
- **Setup (8):** subtítulo passo 1 (nome aparece em orçamentos/conversas/logs, pode ser apelido, admin irreversível); passo 2 (o que o Google importa, "não encontrou? pule"); passo 3 (horário afeta lembretes/relatórios/cobranças); passo 5 (1 item com preço de aluguel destrava o 1º orçamento); celebração ("daqui o sistema não guia mais").
- **Estoque (1, mas crítica):** "Como usar o mapa" em 4 passos + botão "Ver área de cobertura de entrega".
- **Logística (14):** chips MOTIVOS_FORA_GALPAO; SheetPularMovimento (OUTRO exige descrição); banners de defasagem verbatim; ModalPermissaoBolha; gate "Antes de começar a rota".

Diretriz: **citar esses textos verbatim em callouts** para o locador reconhecer a UI — usando-os como fonte de verdade de redação (já validados pelo dono no app).

---

## 7. Roadmap em ondas priorizadas

**Onda 0 — Correções de verdade (esforço baixo, prioridade máxima).** Risco de informação enganosa hoje no ar.
- Corrigir natureza única em `locacao-e-venda.md`; 6→5 passos + remover Motores em `configurando-sua-empresa.md`; veículo obrigatório em `execucao-em-campo.md` + 3-caminhos em `planejando-o-roteiro.md`; e-mail vinculado em `colaboradores-e-acessos.md`; confirmação de e-mail em `criando-sua-conta.md`.
- *Dependência:* nenhuma. Pode sair imediatamente.

**Onda 1 — Núcleo que traz dinheiro: orçamento → cobrança (esforço alto).** O coração do funil.
- Orçamentos: Movimentos/janelas, Valores/descontos, Duração/bloqueio de uso, Endereços salvos; melhorar Acompanhando (matriz de documentos).
- Cobrança: Lista de cobranças, Emitindo a cobrança, Página pública do cliente; aprofundar Pagamento online (recebedor 4 passos/KYC).
- *Dependência:* Onda 0 (natureza única) precede Orçamentos.

**Onda 2 — Logística ponta a ponta (esforço alto).**
- A jornada de um pedido (Ver Logística + eixo de responsabilidade); Acompanhando seus roteiros (listagem + tela única); melhorar Execução em campo (gates/bolha/cobrar na rua); Execução em lote; melhorar Visão geral (6 fases).
- *Dependência:* Onda 1 (matriz de documentos e movimentos do orçamento alimentam a jornada).

**Onda 3 — Painel e Motor de Frete (esforço alto, valor analítico/configuração).**
- Seção Painel (5 páginas, incluindo Calendário logístico com fórmulas); Motores: hub + Motor de Frete (essencial→avançado) + Motor de Orçamento.
- *Dependência:* funil/estados do orçamento (Onda 1) para o Painel; Horários para gatilhos de sazonalidade do frete.

**Onda 4 — Cadastros em profundidade (esforço médio).**
- Produtos: estoque por natureza+condição, histórico de preços, valor de reposição; Kits: elegibilidade, fluxo guiado, histórico; Frota: capacidade + vistoria; Contatos: completar dados sob demanda + avançado.
- *Dependência:* independente; pode rodar em paralelo às Ondas 2–3.

**Onda 5 — Conta, integrações e configuração fina (esforço médio).**
- Sincronização em Nuvem, Programa de Parceiros, Minha conta/preferências, melhorar Assinatura/Integrações; Central de Notificações + Canais; Designer de documentos; Horários (GPS/sazonalidade); Colaboradores (4 passos/CNH).
- *Dependência:* Pagamento online aprofundado (Onda 1) precede Programa de Parceiros.

**Onda 6 — Acesso/onboarding e fechamento das trilhas (esforço médio).**
- Criando sua locadora, Aceitando convite, Recuperar senha, Plano e pagamento inicial; Setup passo a passo + Como o setup se comporta; atualizar Trilhas de leitura e Glossário com tudo; revisar deep links app→doc.
- *Dependência:* última, pois consolida links para todas as páginas criadas.

---

## 8. Decisões — RESOLVIDAS pelo dono

1. **Deep link app → doc (fechar o loop): APROVADO.** Cada "?" do app passa a abrir a página de doc no microconceito (`#âncora`). A doc se integra ao próprio produto. Toda página deve ser escrita com **âncoras estáveis por microconceito**.
2. **Seção "Painel": delegado** ("veja a melhor forma"). Decisão de execução — posicionar logo após "Primeiros passos"/"Conceitos" para ser a primeira tela explicada.
3. **Endereços salvos: PÁGINA PRÓPRIA.** É um *conceito à parte* — um **tipo de origem de endereço** que o usuário seleciona para facilitar a criação do orçamento. A página explica os três caminhos (endereço do próprio cliente — ex.: residencial; **endereço salvo** recorrente — condomínios, chácaras onde já se foi; e **endereço exclusivo** digitado na hora) e vende a *facilidade* que o sistema traz ao reaproveitar endereços recorrentes.
4. **Granularidade: delegado** ("o desmembramento que achar melhor"), com a trava obrigatória do **perfil do locador** (ver §9): mais abstraído/simples para o pequeno (autônomo/MEI/micro), mais detalhe e flexibilidade conforme cresce.
5. **Recursos "em breve": documentar agora** com selo "em breve" + **resumo curto** (não aprofundar). Ex.: Empacotamento 3D — "estamos avaliando integrar a JettaCargo" (a confirmar). Programa de Parceiros, Fiscal/NFe, Recorrência, Catálogo da comunidade, **Fornecedores de serviços** (frete/mão de obra — no backlog) idem.
6. **Planos: mencionar levemente** (ex.: "Básico") **sem preços nem nomes comerciais** — preços vivem na página de marketing.
7. **Avançado "Para quem quer os números": INCLUIR tudo** — fórmulas e, crucialmente, **as referências/base** de onde foram tiradas (ex.: o artigo da fórmula de probabilidade de fechamento que varia com a taxa de cancelamento e os dias até o evento). O usuário avançado precisa enxergar que há base científica; mas é detalhe opt-in, ao fim da página, só para quem se interessa.
8. **Status "Pendente" — CORRIGIR o entendimento:** pendente **NÃO** é "em aberto". Um orçamento **pendente** é um que **não foi aprovado por causa de uma política configurável no Motor de Orçamento da organização** (ex.: "frete acima de R$ X exige aprovação manual"). Fica pendente até que alguém com a qualificação de aprovação aprove → só então vira **aberto**. É um **pré-funil**. Documentar assim em `aprovacao.md` e nas tabelas de status.
9. **Fornecedor: REMOVER a menção por ora** (alinhar à realidade do código). Fornecedores **de serviços** (frete, mão de obra, etc.) estão no backlog → entram só como "em breve".
10. **Glossário/ortografia de termos novos: APROVADO** ("veja a melhor forma"). Validar contra **convenção de mercado** e clareza; em caso de dúvida, **perguntar ao dono**. Sempre abstraindo para o usuário mais simples — inclusive mudando *como* apresentamos o termo a cada perfil para ele entender na prática.

---

## 9. Princípios REFORÇADOS pelo dono (invioláveis, valem para toda a doc)

- **O código é a fonte da verdade.** As regras de negócio foram sendo pensadas e codificadas direto (sem tempo de doc). Agora a doc precisa refletir **exatamente** o que o sistema faz hoje — nada de descrever intenção antiga. Quando houver dúvida, conferir no código, não na memória.
- **A filosofia do produto deve estar intrínseca em TODA página:** *abstrai para o pequeno, melhora para o médio, escala/personaliza/flexibiliza para o grande.* Os três perfis (autônomo/MEI/micro → médio → grande) são a lente de profundidade: o pequeno quer o conceito simplificado e abstraído; o grande quer controle, números e flexibilidade. A camada Essencial/Intermediário/Avançado (§3) é a materialização disso.
- **Referências e base** nos blocos avançados (§8.7) — citar de onde vêm as fórmulas, como sinal de credibilidade para o usuário avançado.
- **Deep-link app→doc** (§8.1) exige âncoras estáveis por microconceito em todas as páginas.