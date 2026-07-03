---
title: Inadimplência e Acordos
parent: Módulos
nav_order: 3.5
---

# Inadimplência e Acordos

O módulo de Inadimplência reúne, por unidade, tudo o que está em atraso no condomínio e as ferramentas para recuperar esses valores — incluindo **acordos de parcelamento** e **notificação extrajudicial**.

{: .note }
> **Quem acessa**
>
> A Inadimplência é uma área do **síndico** — o condômino não a enxerga. **Visualizar** os inadimplentes está disponível no plano **Básico**. As **ações de recuperação** (fechar acordos, emitir notificação extrajudicial e liberar a negociação pelo próprio condômino) fazem parte do plano **Pro**. Quem está nos 30 dias grátis usa tudo.

<!-- print: inad-visao-01 — Tela de Inadimplência: lista de unidades devedoras com totais (desktop) -->

## Como a dívida aparece

A tela lista as **unidades devedoras** e, dentro de cada uma, os lançamentos vencidos e ainda não pagos. É a partir daqui que você fecha um acordo com um devedor.

{: .note }
> Uma unidade que fechou um acordo **sai desta lista** enquanto o acordo estiver em dia — a dívida não sumiu, ela está "em acordo". Se o acordo for descumprido ou cancelado, a dívida **volta a aparecer** aqui (veja mais abaixo).

## Fechar um acordo de parcelamento

Um acordo transforma uma ou mais dívidas vencidas de uma unidade em um parcelamento, com um desconto opcional.

**Passo a passo:**

1. Na unidade devedora, abra a opção de **novo acordo**.
2. **Selecione as dívidas** que entram na negociação.
3. Defina o **número de parcelas** (de 1 a 36) e, se quiser, um **desconto**.
4. Confira o resumo e confirme.

<!-- print: inad-acordo-criar-01 — Assistente de novo acordo: seleção de dívidas, parcelas e desconto (desktop) -->

**O que o sistema faz ao criar o acordo:**

- As dívidas originais **não são apagadas nem quitadas** — passam para o estado "em acordo" e **saem da lista de inadimplência**.
- São criadas as **parcelas novas** (com o valor já com desconto), que passam a ser o que o condômino deve pagar.
- É gerado um **PDF do acordo** com **atestação eletrônica** (quem fez o acordo, o vínculo com a unidade e a data), para registro.

{: .tip }
> Um acordo pode ser iniciado por você (síndico) ou pelo **próprio condômino**, pela negociação self-service — veja a seção "Negociação pelo próprio condômino".

## Acompanhar e receber as parcelas

Conforme o condômino paga, você registra o pagamento de cada parcela. O acordo mostra quantas parcelas já foram pagas e quantas faltam.

<!-- print: inad-acordo-parcelas-01 — Detalhe de um acordo ativo com parcelas pagas e pendentes (desktop) -->

Quando a **última parcela é paga**, o acordo é marcado como **Concluído** e as dívidas originais são **quitadas** de vez. Fim feliz: nada mais fica pendente para aquela unidade em relação a essas dívidas.

## Quando uma parcela atrasa

Um atraso pontual (uma parcela vencida e ainda não paga) **não** encerra o acordo — ele continua **Ativo**. É a situação normal de "está um pouco atrasado, mas o acordo segue de pé".

## Quando o acordo é descumprido (quebra automática)

Se a unidade acumular **2 parcelas vencidas e não pagas**, o sistema marca o acordo como **Quebrado automaticamente** (uma verificação roda todo dia). Nesse momento:

- O condômino **perde o desconto** da negociação e volta a dever o **valor original cheio**.
- **Tudo o que ele já pagou é abatido** — nada do que entrou é perdido.
- As parcelas que ainda não tinham sido pagas **deixam de existir**.
- As dívidas originais **voltam a aparecer na inadimplência**, já com o valor certo.
- Você recebe uma **notificação** (no aplicativo e por e-mail, com a identidade do seu condomínio) avisando que o acordo foi quebrado.

**Exemplo prático:**

> Uma unidade devia **R$ 1.000**. Foi fechado um acordo com **20% de desconto** = **R$ 800 em 8 parcelas de R$ 100**. O condômino pagou **3 parcelas (R$ 300)** e parou. Na segunda parcela vencida sem pagamento, o acordo **quebra**: ele perde o desconto (volta a dever os **R$ 1.000**), o sistema abate os **R$ 300** já pagos, e a unidade **reaparece na inadimplência devendo R$ 700**. Os R$ 300 que ele pagou continuam registrados normalmente, nas datas em que foram pagos.

{: .warning }
> **Perder o desconto é intencional.** O desconto é o incentivo para o acordo ser cumprido. Se o acordo é descumprido, a base de cálculo volta a ser a dívida cheia — mas sempre creditando o que já foi pago.

## Cancelar um acordo manualmente

Você também pode **cancelar** um acordo ativo a qualquer momento. O efeito é o mesmo da quebra automática, com o crédito correto: as dívidas originais voltam para a inadimplência e **tudo o que já foi pago é abatido**, sem duplicar valores.

<!-- print: inad-acordo-cancelar-01 — Diálogo de cancelamento de acordo com aviso de crédito das parcelas pagas (desktop) -->

{: .note }
> **O que você já recebeu continua registrado.** Quebrar ou cancelar um acordo **não reescreve meses já fechados** — cada pagamento que o condômino fez permanece lançado na data em que entrou. A conta do que ele ainda deve é sempre: **dívida original cheia menos o total já pago**.

## Os status de um acordo

| Status | O que significa |
|---|---|
| **Ativo** | Acordo em andamento; parcelas sendo pagas (pode haver atraso pontual). |
| **Concluído** | Todas as parcelas foram pagas; as dívidas originais foram quitadas. |
| **Quebrado** | Acumulou 2 parcelas vencidas sem pagamento; a dívida voltou (cheia, menos o pago). |
| **Cancelado** | Encerrado manualmente pelo síndico; a dívida voltou (cheia, menos o pago). |

<!-- print: inad-acordo-status-01 — Lista de acordos mostrando os diferentes selos de status, com destaque no "Quebrado" (desktop) -->

## Negociação pelo próprio condômino

Quando essa opção está ativa (plano Pro), o **condômino** pode propor e fechar o parcelamento da própria dívida, sem depender de você iniciar. O acordo resultante segue exatamente as mesmas regras descritas acima — inclusive a quebra automática por descumprimento.

---

## Roteiro de capturas *(pendente — sessão autenticada do síndico)*

As telas abaixo precisam ser capturadas logado como síndico, num condomínio de **demonstração** (sem dados pessoais reais), viewport **desktop**, e salvas em `docs-publicos/assets/screenshots/` com estes nomes:

| Arquivo | Tela / o que precisa aparecer |
|---|---|
| `inad-visao-01.png` | Tela de Inadimplência: lista de unidades devedoras com totais. |
| `inad-acordo-criar-01.png` | Assistente de novo acordo: seleção de dívidas + nº de parcelas + campo de desconto. |
| `inad-acordo-parcelas-01.png` | Detalhe de um acordo **Ativo** com parcelas pagas e pendentes. |
| `inad-acordo-cancelar-01.png` | Diálogo de cancelamento de acordo (com o aviso de que as parcelas pagas serão creditadas). |
| `inad-acordo-status-01.png` | Lista de acordos exibindo os selos de status, com o **Quebrado** visível. |

Depois de capturadas, os marcadores `<!-- print: ... -->` no texto são substituídos pelas imagens.
