---
title: Minha Área
parent: Módulos
nav_order: 2
---

# Minha Área

A **Minha Área** é o espaço de autoatendimento para condôminos e síndicos. Nela você encontra os serviços disponíveis para a sua unidade: extrato financeiro, negociação de dívidas, acompanhamento de acordos e, em breve, solicitação de documentos.

> Porteiros não têm acesso a este módulo.

---

## Como acessar

Clique em **Minha Área** no menu lateral (desktop) ou no menu inferior (mobile). O acesso está disponível para condôminos e síndicos. Se você é síndico e também mora no condomínio, verá aqui os dados da sua própria unidade.

---

## Serviços disponíveis

![Hub Minha Área com cards de Extrato da Unidade e Solicitar Documentos](/assets/screenshots/96-minha-area-hub.png)

### Extrato da Unidade

Consulte o histórico completo de cobranças da sua unidade — taxas de condomínio, taxas extras e outros lançamentos.

![Extrato da Unidade com filtro por ano, cards de resumo, tabela de lançamentos e botões de exportação](/assets/screenshots/97-minha-area-extrato.png)

*Os dados financeiros apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

O cabeçalho da página exibe o nome e o CPF do condômino designado como **responsável pela unidade** (quando configurado pelo síndico). Essa informação também aparece no PDF exportado, facilitando o uso como comprovante formal ou para a declaração de imposto de renda.

**O que você encontra:**

- **Filtro por ano** — selecione o exercício desejado ou visualize todos os lançamentos de uma vez
- **Resumo financeiro** com quatro totalizadores:
  - Total cobrado no período
  - Total pago (em verde)
  - Em aberto — lançamentos ainda dentro do prazo
  - Em atraso — lançamentos vencidos sem pagamento
- **Tabela detalhada** com competência, descrição, valor, vencimento, data de pagamento e status
- **Exportação em CSV** — baixe o extrato para usar em planilhas ou na declaração de imposto de renda. Disponível para todos os planos
- **Exportação em PDF** *(plano Pro)* — gera um documento formal com cabeçalho do condomínio, identificação do responsável pela unidade, tabela de resumo e listagem completa dos lançamentos. No plano Básico, o botão aparece com cadeado e mensagem explicativa

**Status dos lançamentos:**

| Status | Significado |
|--------|-------------|
| Pago | Pagamento registrado pelo síndico |
| Pendente | Ainda dentro do prazo de vencimento |
| Em atraso | Prazo vencido sem registro de pagamento |

---

### Negociar dívida *(plano Pro)*

{: .note }
> **Disponível apenas no plano Pro**
>
> Esta seção aparece somente para condomínios no plano Pro e apenas quando há lançamentos de inadimplência vencidos vinculados à sua unidade.

Condôminos com débitos em atraso podem iniciar um acordo de parcelamento diretamente pelo app, sem precisar contatar o síndico. Basta acessar **Minha Área → Negociar dívida** quando a seção estiver disponível.

**Como funciona o fluxo:**

1. **Selecione os débitos** — a tabela lista os lançamentos vencidos elegíveis com checkbox para seleção individual. Marque os débitos que deseja incluir no acordo.
2. **Confira o cálculo automático** — com base nos parâmetros definidos pelo síndico, o sistema calcula a multa (%) sobre o total selecionado e os juros de mora mensais (%) proporcionais ao tempo de atraso de cada lançamento.
3. **Escolha o número de parcelas** — o seletor exibe as opções disponíveis. Opções que resultariam em parcelas abaixo do valor mínimo configurado pelo síndico aparecem desabilitadas.
4. **Revise o resumo financeiro:**

    | Campo | Descrição |
    |---|---|
    | Dívida selecionada | Soma dos lançamentos marcados |
    | Multa | Percentual aplicado sobre a dívida |
    | Juros estimados | Calculado por mês de atraso de cada lançamento |
    | Total acordado | Soma de dívida + multa + juros |
    | Valor por parcela | Total acordado dividido pelo número de parcelas |

5. **Confirme o acordo** — leia o aviso legal de reconhecimento da dívida e clique em **Confirmar Acordo**. O síndico recebe uma notificação por e-mail e Telegram com os detalhes do acordo.

{: .warning }
> **Antes de confirmar**
>
> Ao confirmar o acordo você reconhece formalmente a dívida e se compromete com o parcelamento. O acordo não pode ser desfeito pelo condômino após a confirmação — apenas o síndico pode cancelá-lo pelo módulo Financeiro.

---

### Meus acordos *(plano Pro)*

Exibe todos os acordos de parcelamento existentes para a sua unidade — tanto os iniciados pelo próprio condômino quanto os criados pelo síndico.

![Seção Meus acordos com accordion expandido mostrando tabela de parcelas e botão Baixar PDF](/assets/screenshots/98-minha-area-acordos.png)

*Os dados financeiros apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

Cada acordo aparece em um card com as informações principais: valor total, número de parcelas, status e data de criação. O botão **Baixar PDF** está disponível em cada card para salvar o comprovante do acordo.

{: .note }
> **Ações disponíveis apenas para o síndico**
>
> Os botões de cancelar acordo e marcar parcelas como pagas não aparecem nesta visão — essas ações são exclusivas do síndico, acessíveis pelo módulo Financeiro.

---

### Solicitar Documentos *(em breve)*

Em breve você poderá solicitar documentos diretamente pelo app — como declaração de quitação, declaração de residência e outros. Acompanhe as novidades nas próximas versões.

---

## Perguntas frequentes

**Não vejo nenhuma cobrança no meu extrato. O que pode ser?**
Pode ser que o síndico ainda não tenha vinculado sua unidade aos lançamentos financeiros. Entre em contato com a administração pelo módulo **Fale com o Síndico**.

**Posso ver o extrato de outras unidades?**
Não. Cada condômino visualiza apenas os lançamentos da sua própria unidade.

**O extrato está incorreto. Como corrijo?**
O extrato reflete os lançamentos registrados pelo síndico. Em caso de divergência, entre em contato pela função **Fale com o Síndico**.
