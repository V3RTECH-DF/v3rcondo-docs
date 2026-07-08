---
title: Inadimplência e Acordos
parent: Módulos
nav_order: 3.5
---

# Inadimplência e Acordos

O módulo de **Inadimplência** reúne, por unidade, tudo o que está em atraso no condomínio e as ferramentas para recuperar esses valores — **acordos de parcelamento** e **notificação extrajudicial**.

{: .note }
> **Onde fica e quem acessa**
>
> A Inadimplência tem **item próprio na barra lateral** (logo abaixo de Financeiro) — não fica mais dentro de Relatórios. A página tem **duas abas: Inadimplentes** e **Acordos**.
>
> É uma área de gestão: o **síndico** opera tudo; **Conselho Fiscal** e **Contador** entram em **modo leitura** (veem devedores e acordos, mas não operam); o **condômino comum não acessa** — ele acompanha só a própria dívida e os próprios acordos na **Minha Área**.
>
> **Visualizar** os inadimplentes está no plano **Básico**. As **ações de recuperação** (fechar acordos, emitir notificação extrajudicial e liberar a negociação pelo próprio condômino) são do plano **Pro**. Nos 30 dias grátis tudo fica liberado.

![Módulo Inadimplência com as abas Inadimplentes e Acordos, e a lista de unidades devedoras](/assets/screenshots/inad-visao-01.png)

## Aba Inadimplentes

### Como a dívida aparece

A aba **Inadimplentes** lista as **unidades devedoras** e, dentro de cada uma, os lançamentos vencidos e ainda não pagos. No topo, um card mostra o **Total Inadimplente** e a quantidade de lançamentos vencidos. É a partir daqui que você notifica um devedor ou fecha um acordo.

{: .note }
> **O que conta como inadimplência?** Um lançamento entra quando é do tipo **receita**, tem vencimento **no passado** e **não** foi pago. Lançamentos com vencimento futuro, mesmo em aberto, ainda estão no prazo e não entram.

{: .note }
> Uma unidade que fechou um acordo **sai desta lista** enquanto o acordo estiver em dia — a dívida não sumiu, está "em acordo". Se o acordo for descumprido ou cancelado, a dívida **volta a aparecer** aqui. O acordo em si você acompanha na aba **Acordos** (veja abaixo).

### Notificar devedores (notificação extrajudicial) *(Pro)*

Ao expandir uma unidade, você vê os débitos individuais e pode emitir uma **notificação extrajudicial** — um PDF formal de cobrança.

- **Individual:** expanda a unidade, marque os lançamentos e clique em **Notificar**. Abre um painel com prazo, observações e canal de envio.
- **Em lote:** marque várias unidades e use **Notificar em lote** — uma notificação por unidade, na mesma operação.

![Modal de notificação individual com seleção de lançamentos, prazo e canal de envio](/assets/screenshots/91-inadimplencia-modal-individual.png)

*Dados pessoais fictícios, apenas ilustrativos.*

**Canais:**

| Canal | O que acontece |
|---|---|
| E-mail | PDF enviado ao e-mail do condômino responsável |
| E-mail + Telegram | PDF por e-mail e aviso no Telegram |
| Apenas baixar PDF | PDF gerado para download — nada é enviado ao condômino |

O **PDF** traz o cabeçalho com logo e dados do condomínio, os dados do notificado, a tabela de débitos (descrição, vencimento, valor, dias em atraso), o prazo para regularização, a cláusula legal e um **código de referência** para rastreio. Todas as notificações emitidas ficam no **Histórico**, ao fim da lista, com botão de download.

{: .note }
> **Responsável pela unidade.** Só o condômino designado **responsável** pela unidade recebe a notificação. O responsável é definido ao expandir a unidade ou em **Configurações → Condôminos** — sempre um único por unidade.

## Fechar um acordo de parcelamento *(Pro)*

Um acordo transforma uma ou mais dívidas vencidas de uma unidade em um parcelamento, com desconto opcional. Comece pela aba **Inadimplentes**, na unidade devedora.

**Passo a passo:**

1. Na unidade devedora, clique em **Gerar Acordo**.
2. **Selecione as dívidas** que entram na negociação.
3. Defina o **número de parcelas** (de 1 a 36) e, se quiser, um **desconto**.
4. Confira o resumo e confirme.

![Assistente de novo acordo: seleção das dívidas vencidas que entram na negociação](/assets/screenshots/inad-acordo-criar-01.png)

**O que o sistema faz ao criar o acordo:**

- As dívidas originais **não são apagadas nem quitadas** — passam para o estado "em acordo" e **saem da lista de inadimplência**.
- São criadas as **parcelas novas** (já com o desconto), que passam a ser o que o condômino deve pagar.
- É gerado um **PDF do acordo** com **atestação eletrônica** (quem fez o acordo, o vínculo com a unidade e a data).

{: .tip }
> Um acordo pode ser iniciado por você (síndico) ou pelo **próprio condômino**, pela negociação self-service — veja "Negociação pelo próprio condômino".

## Aba Acordos — todos os acordos num lugar só

A aba **Acordos** lista **todos** os acordos do condomínio, com filtro por status. Cada item mostra a **unidade** e o **responsável**, o selo de status, a data, o progresso das parcelas e o valor. É aqui que você acompanha, registra pagamentos, baixa o PDF e cancela acordos.

![Aba Acordos: lista consolidada de todos os acordos do condomínio, com selos de status e filtro](/assets/screenshots/inad-acordo-status-01.png)

{: .note }
> **Por que esta aba existe.** Antes, o acordo só aparecia grudado na unidade dentro da lista de inadimplência. Quando o acordo cobria **toda** a dívida da unidade, ela saía da lista e o acordo "sumia" da sua visão. Agora, **todo acordo fica sempre visível e gerenciável aqui** — inclusive os que já quitaram a dívida inteira da unidade.

### Acompanhar e receber as parcelas

Conforme o condômino paga, você **registra o pagamento** de cada parcela (expanda o acordo → **Marcar como pago**). O acordo mostra quantas parcelas já foram pagas e quantas faltam.

![Detalhe de um acordo ativo com uma parcela paga e as demais pendentes](/assets/screenshots/inad-acordo-parcelas-01.png)

Quando a **última parcela é paga**, o acordo é marcado como **Concluído** e as dívidas originais são **quitadas** de vez.

### Quando uma parcela atrasa

Um atraso pontual (uma parcela vencida e ainda não paga) **não** encerra o acordo — ele continua **Ativo**. É o "está um pouco atrasado, mas o acordo segue de pé".

### Quando o acordo é descumprido (quebra automática)

Se a unidade acumular **2 parcelas vencidas e não pagas**, o sistema marca o acordo como **Quebrado automaticamente** (uma verificação roda todo dia). Nesse momento:

- O condômino **perde o desconto** e volta a dever o **valor original cheio**.
- **Tudo o que ele já pagou é abatido** — nada do que entrou é perdido.
- As parcelas ainda não pagas **deixam de existir**.
- As dívidas originais **voltam a aparecer na inadimplência**, com o valor certo.
- Você recebe uma **notificação** (app + e-mail, com a identidade do condomínio).

**Exemplo prático:**

> Uma unidade devia **R$ 1.000**. Acordo com **20% de desconto** = **R$ 800 em 8 parcelas de R$ 100**. O condômino pagou **3 parcelas (R$ 300)** e parou. Na segunda parcela vencida sem pagamento, o acordo **quebra**: perde o desconto (volta a dever **R$ 1.000**), o sistema abate os **R$ 300** já pagos, e a unidade **reaparece devendo R$ 700**. Os R$ 300 continuam registrados nas datas em que foram pagos.

{: .warning }
> **Perder o desconto é intencional.** O desconto é o incentivo para o acordo ser cumprido. Descumprido, a base volta a ser a dívida cheia — sempre creditando o que já foi pago.

### Cancelar um acordo manualmente

Você pode **cancelar** um acordo ativo a qualquer momento (expanda o acordo → **Cancelar Acordo**). O efeito é o mesmo da quebra automática, com o crédito correto: as dívidas originais voltam para a inadimplência e **tudo o que já foi pago é abatido**, sem duplicar valores.

![Diálogo de cancelamento de acordo com o aviso de que as parcelas já pagas serão creditadas](/assets/screenshots/inad-acordo-cancelar-01.png)

{: .note }
> **O que você já recebeu continua registrado.** Quebrar ou cancelar um acordo **não reescreve meses já fechados** — cada pagamento fica lançado na data em que entrou. O que ele ainda deve é sempre: **dívida original cheia menos o total já pago**.

### Os status de um acordo

| Status | O que significa |
|---|---|
| **Ativo** | Acordo em andamento; parcelas sendo pagas (pode haver atraso pontual). |
| **Concluído** | Todas as parcelas foram pagas; as dívidas originais foram quitadas. |
| **Quebrado** | Acumulou 2 parcelas vencidas sem pagamento; a dívida voltou (cheia, menos o pago). |
| **Cancelado** | Encerrado manualmente pelo síndico; a dívida voltou (cheia, menos o pago). |

## Negociação pelo próprio condômino *(Pro)*

Quando essa opção está ativa, o **condômino** pode propor e fechar o parcelamento da própria dívida pela **Minha Área**, sem depender de você iniciar. Ele seleciona os débitos, escolhe o número de parcelas (dentro dos limites que você definiu), vê o preview (dívida + multa + juros = total acordado) e confirma um termo de compromisso. O acordo resultante segue exatamente as mesmas regras acima — inclusive a quebra automática por descumprimento.

{: .note }
> **Parâmetros do self-service.** Você configura multa, juros, máximo de parcelas e valor mínimo por parcela em **Configurações → Cobranças & Acordos**. Sem configurar, o padrão é 2% de multa, 1% de juros ao mês, até 12 parcelas e mínimo de R$ 50,00 por parcela.
