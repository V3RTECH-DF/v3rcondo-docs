---
title: Relatórios
parent: Módulos
nav_order: 13
---

# Relatórios

O módulo de Relatórios oferece uma visão analítica da situação financeira e das compras do condomínio. São seis abas: Fluxo de Caixa, Projeção (Forecast), Gastos por Categoria, Compras e Serviços, **Prestação de Contas** e **Relatório de Gestão**.

![Aba Fluxo de Caixa com gráfico de barras agrupadas e tabela de resumo mensal](/assets/screenshots/67-relatorios-fluxo-caixa.png)

{: .note }
> **A Inadimplência mudou de lugar.** Devedores por unidade, **acordos de parcelamento** e **notificação extrajudicial** deixaram de ser uma aba de Relatórios e agora têm **módulo próprio** — item **Inadimplência** na barra lateral. Veja [Inadimplência e Acordos](inadimplencia.md).

{: .note }
> **Disponível para condôminos**
>
> O módulo de Relatórios está disponível para **síndicos e condôminos** — algumas abas são exclusivas do síndico (indicado em cada seção).

{: .warning }
> **Recursos exclusivos do Plano Pro**
>
> A exportação em PDF/XLSX e a aba **Projeção (Forecast)** são recursos exclusivos do **plano Pro**.

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

## Compras e Serviços

Reúne duas visões analíticas:

**Compras por Período:** tabela com todas as compras no período filtrado — título, categoria, status, data, fornecedor aprovado e valor aprovado.

**Comparativo de Orçamentos:** selecione uma compra específica para ver uma tabela comparativa com todos os orçamentos recebidos.

![Aba Compras com tabela de compras por período e comparativo de orçamentos](/assets/screenshots/70-relatorios-compras.png)

## Prestação de Contas

A Prestação de Contas é o **documento financeiro formal** do condomínio, em regime de caixa, que o síndico gera e pode **publicar para os condôminos**. Reúne o resultado do período (receitas, despesas e transferências), a movimentação por conta, a inadimplência e os comprovantes anexados.

**Geração:** escolha o período — **Mês** ou **Ano** — e clique em **Gerar prestação**. Antes de gerar, o síndico pode anexar **documentos complementares** (atas, ofícios, planilhas em PDF/imagem) com um rótulo. O documento é montado em segundo plano e o síndico é avisado por e-mail quando fica pronto.

**Publicação:** depois de pronta, a prestação pode ser **publicada** — a partir daí os condôminos passam a vê-la e baixá-la (na aba e em **Minha Área**). O síndico pode despublicar ou excluir a qualquer momento.

{: .note }
> **Comprovantes anexados**
>
> Quando há comprovantes vinculados aos lançamentos do período, eles são reunidos em um único PDF junto com a prestação, cada um identificado por descrição, data e valor.

## Relatório de Gestão *(síndico)*

O Relatório de Gestão é um documento **gerencial, exclusivo do síndico**, com o panorama operacional de todos os módulos do condomínio no período: indicadores (receitas, despesas, saldo, unidades, inadimplência), **Destaques e Pontos de Atenção**, inadimplência por unidade, compras/obras e resumos de tarefas, solicitações, visitantes, assembleias, reservas, documentos, mural e membros.

**Geração:** escolha o período — **Mês**, **Ano** ou **Intervalo personalizado** — e clique em **Gerar relatório**. O documento é montado em segundo plano e o síndico é avisado por e-mail quando o PDF fica pronto; ele aparece na lista **Relatórios gerados** com o botão **Baixar PDF**.

![Aba Relatório de Gestão com seletor de período e lista de relatórios gerados](/assets/screenshots/77-relatorio-gestao-aba.png)

### Análise por IA

Quando a análise por IA está habilitada na plataforma, o Relatório de Gestão traz, logo após os indicadores, um **Resumo Executivo** e **comentários por seção** gerados por inteligência artificial — interpretando os números do período (saldo, inadimplência, pontos críticos) em linguagem gerencial e indicando onde vale a pena agir.

![Resumo Executivo gerado por IA no Relatório de Gestão, com atribuição do provedor e aviso de revisão](/assets/screenshots/78-relatorio-gestao-ia.png)

*Imagem ilustrativa, com dados de um condomínio de teste.*

{: .note }
> **Como funciona a análise por IA**
>
> - A IA recebe **apenas indicadores agregados** do período — nunca nomes, unidades ou dados individuais.
> - O rodapé do bloco indica **qual provedor** gerou a análise (ex.: Google Gemini, OpenAI ou Anthropic Claude).
> - É **best-effort**: se a IA estiver indisponível no momento, o relatório é gerado **normalmente, sem a seção de análise**, e o síndico é avisado por e-mail.
> - O conteúdo é um apoio à leitura dos números — **revise sempre antes de qualquer decisão**, conforme o aviso exibido no próprio documento.

## Exportação *(plano Pro)*

Todas as abas oferecem os botões **PDF** e **XLSX** no canto superior direito. Os arquivos exportados incluem o nome do condomínio, o período filtrado e a data de geração.

![Botões de exportação PDF e XLSX disponíveis em todas as abas de Relatórios](/assets/screenshots/72-relatorios-exportar.png)
