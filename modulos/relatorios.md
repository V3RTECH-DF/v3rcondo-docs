---
title: Relatórios
parent: Módulos
nav_order: 13
---

O módulo de Relatórios oferece uma visão analítica da situação financeira e das compras do condomínio. São cinco abas: Fluxo de Caixa, Projeção (Forecast), Gastos por Categoria, Inadimplência e Compras e Serviços.

![Aba Fluxo de Caixa com gráfico de barras agrupadas e tabela de resumo mensal](/assets/screenshots/67-relatorios-fluxo-caixa.png)

{: .note }
> **Disponível para condôminos**
>
> O módulo de Relatórios está disponível para **síndicos e condôminos**. A aba Inadimplência exibe dados resumidos para condôminos, sem identificar individualmente os inadimplentes.

{: .warning }
> **Recursos exclusivos do Plano Pro**
>
> A exportação em PDF/XLSX, o Relatório Mensal com IA e a aba **Projeção (Forecast)** são recursos exclusivos do **plano Pro**.

## Fluxo de Caixa

Exibe a evolução financeira mensal no período selecionado.

**Filtros:** período de início e fim (mês/ano) e conta bancária. Por padrão, exibe os últimos 6 meses considerando todas as contas.

**Gráfico:** barras agrupadas por mês mostrando Receitas (verde escuro) e Despesas (vermelho), com linha de Saldo Acumulado sobreposta.

**Resumo Mensal:** tabela com as colunas Mês, Receitas, Despesas, Saldo do Mês e Acumulado.

{: .note }
> **Entendendo os números do Fluxo de Caixa**
>
> **Saldo do mês** é a diferença simples entre receitas e despesas daquele mês. Um mês com mais despesas do que receitas terá saldo do mês negativo.
>
> **Saldo acumulado** é a soma progressiva dos saldos mensais ao longo do período selecionado. Ele mostra se o condomínio está construindo ou consumindo reservas ao longo do tempo. É possível ter um mês positivo e ainda assim ver o acumulado negativo — isso acontece quando meses anteriores com deficit foram grandes o suficiente para não serem recuperados pelo mês atual.
>
> **O que entra como receita e despesa?** Apenas lançamentos do tipo receita e despesa são considerados. Transferências entre contas do próprio condomínio são excluídas — do contrário, uma transferência inflaria receitas e despesas ao mesmo tempo sem representar nenhuma movimentação real de dinheiro.
>
> **O que não entra?** Lançamentos futuros (com data de vencimento à frente) aparecem no Financeiro mas não afetam o Fluxo de Caixa até que sejam pagos e registrados com data de pagamento. O Fluxo de Caixa reflete apenas o que foi efetivamente movimentado.

## Projeção (Forecast) *(plano Pro)*

Projeta a situação financeira do condomínio para os próximos meses com base no histórico de lançamentos pagos e nas recorrências financeiras ativas.

{: .note }
> **Disponível apenas para síndicos**
>
> A aba Projeção é exibida somente para o **síndico**. Condôminos não têm acesso a essa aba.

![Aba Projeção (Forecast) com cartões de resumo, alerta de saldo negativo e gráficos de barras e linha](/assets/screenshots/73-relatorios-forecast.png)

**Período de projeção:** selecione via caixa de seleção no topo da aba. O padrão é **6 meses**.

| Opção | Período projetado |
|---|---|
| 1 mês | 1 mês a partir do mês atual |
| 3 meses | 3 meses a partir do mês atual |
| Próximos 6 meses | 6 meses a partir do mês atual |
| Próximos 12 meses | 12 meses a partir do mês atual |
| Até o final do semestre | Do mês atual até o final do semestre vigente |
| Até o final do ano | Do mês atual até dezembro |

![Seletor de período da Projeção com as opções disponíveis](/assets/screenshots/74-relatorios-forecast-periodo.png)

**Cartões de resumo:** três indicadores principais no topo.

- **Saldo Atual** — saldo real nas contas bancárias do condomínio, idêntico ao exibido no módulo Financeiro.
- **Saldo Projetado** — estimativa do saldo ao final do período, considerando receitas e despesas esperadas mês a mês.
- **Variação** — diferença entre o Saldo Projetado e o Saldo Atual (valor positivo em verde, negativo em vermelho).

**Gráfico de barras:** barras agrupadas por mês mostrando Receitas projetadas (verde) e Despesas projetadas (vermelho) para cada mês do período.

**Gráfico de linha:** evolução do Saldo Acumulado mês a mês, partindo do Saldo Atual. A linha fica vermelha se o saldo projetado ficar negativo em algum mês do período.

**Alerta de saldo negativo:** quando a projeção indica saldo negativo em algum mês, um banner de aviso é exibido informando em qual mês isso ocorre.

{: .warning }
> **Histórico mínimo necessário**
>
> O sistema exige um número mínimo de meses com dados para gerar a projeção. Se não houver histórico suficiente, a aba exibe uma mensagem informando quantos meses ainda faltam.

{: .note }
> **Entendendo a Projeção (Forecast)**
>
> **De onde vêm os números projetados?**
>
> Para cada categoria financeira, o sistema escolhe automaticamente a melhor fonte de dados disponível:
>
> - Se a categoria tem **histórico de lançamentos pagos**, calcula a média mensal dos valores efetivamente pagos e usa esse número como estimativa para os próximos meses.
> - Se a categoria **não tem histórico** mas possui uma **recorrência financeira ativa** (por exemplo, uma mensalidade de serviço de portaria cadastrada em Financeiro → Recorrências), usa o valor nominal da recorrência.
> - Se não há nem histórico nem recorrência, a categoria não contribui para a projeção.
>
> **Por que usar a média dos pagamentos e não dos lançamentos?**
>
> Porque lançamentos em aberto não representam dinheiro que entrou ou saiu de fato. Se o condomínio tem inadimplência crônica — por exemplo, taxa mensal lançada como R$ 5.000 mas recebendo apenas R$ 3.500 — a projeção de receita refletirá os R$ 3.500 efetivamente recebidos, não os R$ 5.000 esperados. Isso torna a estimativa mais conservadora e realista.
>
> **O que o Saldo Projetado representa?**
>
> É o saldo atual das contas bancárias somado ao resultado acumulado de todas as receitas e despesas estimadas mês a mês ao longo do período escolhido. Não é uma promessa — é uma estimativa baseada no comportamento histórico do condomínio.
>
> **Limitações importantes**
>
> - Não considera inadimplência *futura* que ainda não ocorreu
> - Não considera eventos imprevistos: obras emergenciais, multas, reajustes de contrato
> - Não captura sazonalidade atípica (meses com despesas excepcionais distorcem a média)
> - Quanto maior o período projetado, menor a precisão da estimativa
>
> Use o Forecast como apoio à tomada de decisão — por exemplo, para antecipar a necessidade de convocar uma assembleia de aprovação de taxa extra.

## Gastos por Categoria

Mostra como as despesas (ou receitas) estão distribuídas entre as categorias financeiras.

**Filtros:** período e tipo (Despesas, Receitas ou Ambos).

**Gráfico:** pizza com a participação percentual de cada categoria no total do período.

**Detalhamento:** tabela com Categoria, Total e %, ordenada do maior para o menor valor.

![Aba Gastos por Categoria com gráfico pizza e tabela de detalhamento](/assets/screenshots/68-relatorios-categorias.png)

## Inadimplência

Identifica receitas com vencimento passado e ainda não pagas.

**Visão do síndico:** no topo, um card em destaque mostra o **Total Inadimplente** e a quantidade de lançamentos vencidos. As unidades inadimplentes são listadas de forma colapsável — ao expandir uma unidade, o síndico vê cada lançamento vencido com descrição, valor, data de vencimento e dias em atraso. Quando não há inadimplência, o sistema exibe "Nenhuma inadimplência encontrada".

![Aba Inadimplência com card de total e listagem de unidades colapsáveis](/assets/screenshots/75-inadimplencia-overview.png)

![Unidade expandida exibindo os lançamentos vencidos individuais](/assets/screenshots/76-inadimplencia-expandida.png)

**Visão do condômino:** por privacidade, condôminos não visualizam dados que identifiquem individualmente quem está inadimplente. A aba exibe apenas um painel com indicadores agregados:

- **Total de unidades** do condomínio
- **Unidades adimplentes** — quantidade e percentual
- **Unidades inadimplentes** — quantidade e percentual
- **Valor total em aberto** — soma de todos os lançamentos vencidos

{: .note }
> **Entendendo a Inadimplência**
>
> **O que o sistema considera como inadimplente?**
>
> Um lançamento é considerado inadimplente quando cumpre duas condições ao mesmo tempo: é do tipo **receita** e tem data de vencimento **no passado** sem registro de pagamento. Lançamentos com vencimento futuro, mesmo que ainda não pagos, não entram na inadimplência — eles ainda estão dentro do prazo.
>
> **Qual a diferença entre inadimplência e lançamento em aberto?**
>
> Um lançamento em aberto é qualquer receita sem data de pagamento registrada, independente do vencimento. A inadimplência é o subconjunto dos lançamentos em aberto cujo prazo já venceu. Em outras palavras: toda inadimplência é um lançamento em aberto, mas nem todo lançamento em aberto é inadimplência.
>
> **Como os "dias em atraso" são calculados?**
>
> É a diferença em dias corridos entre a data de vencimento do lançamento e a data de hoje. Um lançamento vencido há 10 dias mostra "10 dias em atraso", independente de feriados ou fins de semana.
>
> **Por que condôminos não veem os nomes dos inadimplentes?**
>
> Por privacidade. Expor individualmente quem está em atraso poderia gerar conflitos internos no condomínio. Os indicadores agregados (percentual de unidades adimplentes, valor total em aberto) permitem que todos acompanhem a saúde financeira coletiva sem identificar ninguém.

### Notificação Extrajudicial *(plano Pro, síndico)*

A aba Inadimplência exibe os lançamentos vencidos agrupados por unidade. Ao expandir uma unidade, o síndico vê os débitos individuais e pode selecionar quais incluir em uma notificação extrajudicial.

**Notificação individual:** expanda uma unidade, marque os lançamentos desejados e clique em **Notificar**. Um painel abre com as opções de prazo, observações e canal de envio.

![Modal de notificação individual com seleção de lançamentos, prazo e canal de envio](/assets/screenshots/91-inadimplencia-modal-individual.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

**Notificação em lote:** marque várias unidades com as caixas de seleção e clique em **Notificar selecionadas**. O sistema emite uma notificação por unidade na mesma operação.

![Modal de notificação em lote com resumo das unidades selecionadas](/assets/screenshots/92-inadimplencia-modal-lote.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

**Canais disponíveis:**

| Canal | O que acontece |
|---|---|
| E-mail | PDF enviado como anexo ao e-mail do condômino responsável |
| E-mail + Telegram | PDF enviado por e-mail e aviso no Telegram |
| Apenas baixar PDF | PDF gerado para download — nenhuma notificação enviada ao condômino |

**O documento PDF** contém cabeçalho com logo e dados do condomínio, dados do notificado (nome, unidade, CPF se cadastrado), tabela de débitos com descrição, vencimento, valor e dias em atraso, prazo para regularização, cláusula legal e assinatura do síndico. Um **código de referência** de 8 caracteres é gerado por notificação para rastreamento.

**Histórico:** abaixo da listagem de inadimplentes, todas as notificações emitidas ficam registradas com data, canal, unidade e código de referência, com botão de download do PDF. Notificações emitidas em lote aparecem agrupadas.

![Histórico de notificações extrajudiciais com datas, canais e botões de download](/assets/screenshots/93-inadimplencia-historico.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

{: .note }
> **Responsável pela unidade**
>
> Apenas o condômino designado como **responsável** pela unidade recebe a notificação. O responsável é definido na aba Inadimplência (ao expandir a linha da unidade) ou em **Configurações → Condôminos**. O sistema garante sempre um único responsável por unidade — ao remover um condômino que é responsável, a transferência é obrigatória antes de confirmar.

### Acordos de Parcelamento *(plano Pro, síndico)*

Quando uma unidade possui débitos em aberto, o síndico pode formalizar um **Acordo de Parcelamento** diretamente na aba Inadimplência — sem precisar contato externo ou documentos manuais. O acordo gera parcelas como lançamentos financeiros e um PDF com cláusula jurídica pronto para assinatura.

**Como criar um acordo:**

Clique em **Gerar Acordo** ao lado da unidade desejada. Um assistente de três passos será aberto:

**Passo 1 — Débitos:** selecione quais lançamentos vencidos farão parte do acordo. O total selecionado é calculado em tempo real.

**Passo 2 — Condições:** configure o acordo:

| Campo | Descrição |
|---|---|
| **Desconto (%)** | Percentual de desconto sobre o total; use valor negativo para acréscimo |
| **Nº de parcelas** | De 1 a 36 parcelas |
| **Datas de vencimento** | Sugeridas automaticamente com base no dia de vencimento configurado; editáveis individualmente |
| **Categoria** | Categoria financeira para as parcelas geradas |
| **Advogado / OAB** | Opcionais — aparecem no PDF se preenchidos |
| **Observações** | Campo livre opcional |

**Passo 3 — Confirmação:** prévia com a tabela de parcelas (número, vencimento, valor) e o total acordado destacado. Clique em **Confirmar e Gerar Acordo** para criar o acordo.

**O que acontece após a criação:**

- Os lançamentos originais são marcados como "Em acordo" e deixam de aparecer na lista de inadimplência e nos indicadores financeiros enquanto o acordo estiver ativo.
- As parcelas são criadas como novos lançamentos de receita e aparecem normalmente no Financeiro e no Fluxo de Caixa.
- Um card de acordo aparece abaixo dos lançamentos da unidade, com referência, status, total acordado e progresso (X/N parcelas pagas).

**Gerenciar um acordo:**

Expanda o card do acordo para ver a tabela de parcelas. Para cada parcela pendente (enquanto o acordo estiver ativo), o botão **Marcar como pago** registra o pagamento.

- Quando **todas as parcelas** são pagas, o sistema marca automaticamente o acordo como **Concluído** e registra o pagamento dos lançamentos originais.
- O botão **Baixar PDF** gera o documento do acordo com cabeçalho V3RCondo, identificação das partes (condomínio, síndico, condômino com CPF), tabela de débitos originais, desconto/acréscimo, tabela de parcelas, advogado (se informado) e cláusula jurídica.
- O botão **Cancelar Acordo** desfaz o acordo: os lançamentos originais retornam à lista de inadimplência e as parcelas não pagas são excluídas.

| Status | Significado |
|---|---|
| **Ativo** | Acordo em vigor; parcelas em andamento |
| **Concluído** | Todas as parcelas foram pagas |
| **Cancelado** | Acordo cancelado; débitos originais restaurados |

{: .note }
> **Parcelas de acordo no Financeiro**
>
> As parcelas geradas pelo acordo aparecem na listagem do Financeiro como lançamentos normais de receita. Quando pagas, contribuem para os totais de entradas do período. Os débitos originais, enquanto "Em acordo", ficam ocultos dos indicadores para evitar dupla contagem.

{: .warning }
> **Cancelamento é irreversível**
>
> Ao cancelar um acordo, as parcelas ainda não pagas são excluídas permanentemente. Os lançamentos originais voltam à inadimplência com seus valores e vencimentos originais.

### Negociar dívida *(plano Pro, condômino)*

Condôminos também podem propor um acordo de parcelamento de forma autônoma, sem precisar acionar o síndico. A seção **Negociar dívida** aparece em **Minha Área** quando o condômino possui lançamentos vencidos e o condomínio está no plano Pro.

**Como funciona:**

1. O condômino seleciona quais débitos em atraso quer incluir no acordo (todos são marcados por padrão)
2. Escolhe o número de parcelas — as opções respeitam os parâmetros configurados pelo síndico (máximo de parcelas e valor mínimo por parcela)
3. O sistema exibe o preview em tempo real:

| Item | Descrição |
|---|---|
| Dívida selecionada | Soma dos débitos marcados |
| Multa | Percentual definido pelo síndico aplicado sobre o total |
| Juros estimados | Juros de mora mensais × meses de atraso de cada lançamento |
| **Total acordado** | Dívida + multa + juros |
| Valor por parcela | Total acordado ÷ número de parcelas |

4. O condômino lê e confirma o texto de compromisso:

    > "Ao confirmar, você reconhece a dívida descrita acima e se compromete a pagar as parcelas nas datas indicadas. O descumprimento de qualquer parcela implica vencimento antecipado do saldo total, sujeito à cobrança integral com multa, juros e honorários."

5. Clica em **Confirmar Acordo** — o sistema gera o acordo e as parcelas automaticamente

Após a confirmação, os acordos aparecem abaixo da seção com referência, status e progresso de parcelas. O PDF do acordo pode ser baixado diretamente por ali.

{: .note }
> **Parâmetros do acordo self-service**
>
> O síndico configura os parâmetros (multa, juros, máximo de parcelas, valor mínimo por parcela) em **Configurações → Cobranças → Parâmetros de Acordo Self-Service**. Se não configurados, o sistema usa os valores padrão: 2% de multa, 1% de juros ao mês, até 12 parcelas, mínimo de R$ 50,00 por parcela.

## Compras e Serviços

Reúne duas visões analíticas:

**Compras por Período:** tabela com todas as compras no período filtrado — título, categoria, status, data, fornecedor aprovado e valor aprovado.

**Comparativo de Orçamentos:** selecione uma compra específica para ver uma tabela comparativa com todos os orçamentos recebidos.

![Aba Compras com tabela de compras por período e comparativo de orçamentos](/assets/screenshots/70-relatorios-compras.png)

## Relatório Mensal com IA *(plano Pro)*

O V3RCondo gera automaticamente um relatório executivo mensal com análise de inteligência artificial, consolidando dados financeiros, solicitações, tarefas e compras do período.

**Geração automática:** todo dia 2 de cada mês, o relatório do mês anterior é gerado automaticamente e enviado por e-mail para todos os síndicos. O arquivo também fica disponível no módulo **Documentos**, categoria Relatórios.

**Geração manual:** clique em **Gerar Relatório com IA** e selecione o período:

| Opção | Descrição |
|---|---|
| Mês anterior | Mês anterior completo |
| Mês atual | Do início do mês até hoje |
| Mês específico | Escolha mês e ano |
| Ano anterior | Ano anterior completo |
| Ano atual | De janeiro até hoje |

Após confirmar, o relatório é gerado em segundo plano e enviado por e-mail em instantes. O PDF também é salvo automaticamente no módulo Documentos.

![Modal de seleção de período para geração do Relatório Mensal com IA](/assets/screenshots/71-relatorios-ia-modal.png)

## Exportação *(plano Pro)*

Todas as abas oferecem os botões **PDF** e **XLSX** no canto superior direito. Os arquivos exportados incluem o nome do condomínio, o período filtrado e a data de geração.

![Botões de exportação PDF e XLSX disponíveis em todas as abas de Relatórios](/assets/screenshots/72-relatorios-exportar.png)
