---
title: Minha Área
parent: Módulos
nav_order: 2
---

# Minha Área

A **Minha Área** é o espaço de autoatendimento para condôminos e síndicos. Os serviços da sua unidade ficam organizados em duas abas: **Solicitar Documentos e Serviços** (emitir e solicitar documentos, extrato da unidade e negociação de dívida) e **Meus Documentos** (baixar os documentos que você emitiu ou recebeu).

> Porteiros não têm acesso a este módulo.

---

## Como acessar

Clique em **Minha Área** no menu lateral (desktop) ou no menu inferior (mobile). O acesso está disponível para condôminos e síndicos. Se você é síndico e também mora no condomínio, verá aqui os dados da sua própria unidade.

---

## Aba "Solicitar Documentos e Serviços"

Reúne tudo o que o condômino pode **emitir, solicitar ou acessar** sobre a própria unidade. No computador aparece como uma lista; no celular, como cartões.

![Aba "Solicitar Documentos e Serviços" no computador — lista com Nada Consta, Quitação Anual (IR) com seletor de ano, Declaração de Débitos/Residência e Certidão de Quitação com cadeado Pro, Solicitar documento (Outros) e Extrato da Unidade, cada item com sua ação à direita](/assets/screenshots/102-minha-area-solicitar-lista.png)

No celular, os mesmos itens aparecem como cartões empilhados:

![Aba "Solicitar Documentos e Serviços" no celular — os documentos e serviços em cartões](/assets/screenshots/103-minha-area-solicitar-cards.png)

### Emitir documento na hora

Alguns documentos são gerados automaticamente, na hora, a partir dos dados da sua unidade:

| Documento | Para que serve | Plano |
|---|---|---|
| **Nada Consta** | Comprova que a unidade está sem débitos | Básico |
| **Quitação Anual (IR)** | Demonstrativo anual de pagamentos para o Imposto de Renda (você escolhe o ano) | Básico |
| **Declaração de Débitos** | Relação dos débitos em aberto da unidade | Pro |
| **Declaração de Residência** | Comprova o vínculo da unidade com o condomínio | Pro |
| **Certidão de Quitação (venda)** | Atesta quitação para escritura/venda do imóvel | Pro |

Clique em **Emitir** e o PDF é baixado na hora. Na Quitação Anual (IR), o seletor mostra apenas os anos em que há lançamentos da sua unidade. Documentos do plano **Pro** aparecem com cadeado quando o condomínio está no Básico. Se a unidade tiver débitos vencidos, o Nada Consta e a Certidão de venda não são emitidos — o app oferece a Declaração de Débitos no lugar.

Todo documento emitido traz um **código de verificação** e um **QR Code**: qualquer pessoa (banco, cartório) confere a autenticidade na página pública **v3rcondo.com.br/verificar**, sem ver seus dados financeiros.

<!-- TODO captura: página /verificar com um documento válido -->

### Solicitar documento ao síndico (Outros)

Precisa de um documento personalizado que o app não gera automaticamente? Clique em **Solicitar** no item "Outros", descreva o que precisa (e anexe uma referência, se quiser). O síndico recebe o pedido, produz o documento e anexa o PDF — que aparece para você na aba **Meus Documentos**. Você acompanha o status e pode cancelar enquanto o pedido estiver "aguardando o síndico".

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

## Aba "Meus Documentos"

Lista todos os documentos da sua unidade para baixar — tanto os **automáticos** que você emitiu quanto os **manuais** que o síndico entregou. Cada item mostra o tipo, a data, o **código de verificação** e um botão para **baixar** (ou re-baixar) o PDF. Pedidos ainda em andamento aparecem com o status: *aguardando síndico*, *em análise*, *concluído* ou *recusado* (com o motivo).

<!-- TODO captura: aba "Meus Documentos" com o histórico de emissões/solicitações -->

---

## Perguntas frequentes

**Não vejo nenhuma cobrança no meu extrato. O que pode ser?**
Pode ser que o síndico ainda não tenha vinculado sua unidade aos lançamentos financeiros. Entre em contato com a administração pelo módulo **Fale com o Síndico**.

**Posso ver o extrato de outras unidades?**
Não. Cada condômino visualiza apenas os lançamentos da sua própria unidade.

**O extrato está incorreto. Como corrijo?**
O extrato reflete os lançamentos registrados pelo síndico. Em caso de divergência, entre em contato pela função **Fale com o Síndico**.
