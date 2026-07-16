---
title: Financeiro
parent: Módulos
nav_order: 3
---

# Financeiro

O módulo Financeiro centraliza toda a gestão financeira do condomínio — receitas, despesas, contas bancárias e conciliação com extratos.

![Módulo Financeiro com cards de resumo, saldos por conta e lista de lançamentos](/assets/screenshots/13-financeiro-lista.png)

## Visão geral *(síndico)*

A tela principal exibe cinco cards de resumo no topo:

- **Saldo Acumulado Projetado** — saldo inicial das contas bancárias + todos os lançamentos pagos anteriores ao mês atual + saldo projetado do mês atual
- **Saldo do Mês** — resultado líquido do período filtrado
- **Entradas do Mês** — total de receitas recebidas no período
- **Saídas do Mês** — total de despesas pagas no período
- **Pendentes** — lançamentos com vencimento passado e ainda não pagos

A seção **Saldos por Conta** mostra o saldo atual de cada conta bancária cadastrada. Um card de **Saldo Total** consolida todas as contas.

{: .tip }
> **O saldo não bate com o banco?**
>
> Cada conta tem um botão de lupa 🔍 que abre o **[Caça-diferenças](caca-diferencas.md)** — ele descobre onde está a diferença entre o saldo do app e o do extrato, mesmo sem importar o arquivo. Veja o capítulo dedicado.

## Filtros

| Filtro | Descrição |
|---|---|
| **Período** | Filtra por mês/ano. "Todos" exibe o histórico completo |
| **Tipo** | Receita, Despesa, Transferência ou Todos |
| **Status** | Todos, Pagos, Pendentes, Futuros ou Recorrentes |
| **Categoria** | Filtra por categoria financeira cadastrada |

{: .tip }
> **Filtro por Transferência**
>
> Selecione **Transferência** no filtro Tipo para visualizar exclusivamente as movimentações entre contas. Os filtros Receita e Despesa excluem automaticamente as transferências dos seus totais.

![Filtros disponíveis no módulo Financeiro](/assets/screenshots/14-financeiro-filtros.png)

## Registrar um lançamento *(síndico)*

Clique em **+ Novo Lançamento** e preencha:

![Formulário de novo lançamento](/assets/screenshots/15-financeiro-form-vazio.png)

1. **Tipo** — Receita ou Despesa
2. **Descrição** — nome do lançamento (obrigatório)
3. **Categoria** — classificação do lançamento
4. **Unidade** — identifica a unidade devedora; exibido apenas quando a categoria selecionada é do tipo inadimplência (obrigatório nesse caso)
5. **Conta** — conta bancária vinculada
6. **Valor** — valor em reais (obrigatório)
7. **Data de Vencimento** — obrigatório
8. **Competência** — mês/ano de referência do lançamento (padrão: mês do vencimento). Obrigatório para categorias de inadimplência
9. **Marcar como pago** — ative se o lançamento já foi liquidado
10. **Observações** — campo livre
11. **Comprovante** — PDF, imagem ou ZIP até 10 MB

![Formulário de lançamento preenchido, pronto para salvar](/assets/screenshots/16-financeiro-form-preenchido.png)

{: .tip }
> **Editar ou excluir**
>
> Para editar um lançamento, clique no ícone de lápis. Para excluir, clique no ícone de lixeira e confirme.

## Lançamentos parcelados *(síndico)*

Para despesas que devem ser pagas em várias parcelas — como uma reforma, equipamento ou compra de grande valor — ative o toggle **Parcelado** no formulário de novo lançamento.

![Formulário com toggle Parcelado ativado mostrando Nº de parcelas, data da 1ª parcela e tabela de prévia com valor e vencimento de cada parcela](/assets/screenshots/financeiro-parcelado-drawer.png)

Configure:

- **Nº de parcelas** — quantidade total de parcelas (mínimo 2)
- **1ª parcela** — data de vencimento da primeira parcela

O sistema exibe uma **tabela de prévia** com as parcelas geradas, calculando automaticamente:

- O **valor de cada parcela** a partir do total dividido pelo número de parcelas. A última parcela absorve eventuais diferenças de arredondamento centesimal
- As **datas de vencimento** mensais a partir da data da 1ª parcela

Os valores são **editáveis individualmente** — clique no campo de valor de qualquer linha para ajustá-la. A linha de rodapé mostra a **Soma das parcelas** e o **Total** informado em tempo real; se houver divergência, a soma aparece em vermelho.

Ao salvar, o sistema cria **N lançamentos independentes**, cada um com o badge **Parcela X/N** na lista do Financeiro.

![Lista do Financeiro mostrando lançamento com badge "Parcela 1/3" identificando a primeira de um conjunto parcelado](/assets/screenshots/financeiro-parcelas-lista.png)

{: .note }
> **Excluir um parcelamento**
>
> Ao excluir uma parcela, o sistema oferece três opções: excluir **apenas esta parcela**, excluir **todas as parcelas pendentes** (não pagas) ou excluir **todo o parcelamento** (incluindo as já pagas).

{: .warning }
> **Parcelado e Recorrente são exclusivos**
>
> Os modos **Parcelado** e **Lançamento recorrente** não podem ser usados ao mesmo tempo. Ao ativar um, o outro é ocultado automaticamente.

## Lançamentos recorrentes *(síndico — plano Pro)*

Para despesas ou receitas que se repetem — como taxa de condomínio ou seguro — ative o toggle **Lançamento recorrente** no formulário. Configure:

- **Periodicidade** — mensal, bimestral, trimestral, semestral ou anual
- **Data de início** — quando a recorrência começa
- **Data de fim** — opcional; deixe em branco para recorrência indefinida

O sistema gerará automaticamente os lançamentos futuros.

![Toggle de lançamento recorrente ativado com campos de periodicidade expandidos](/assets/screenshots/17-financeiro-form-recorrente.png)

## Transferências entre contas *(síndico)*

Registre movimentações entre duas contas bancárias do mesmo condomínio — por exemplo, da conta corrente para o fundo de reserva.

Clique em **+ Transferência** e preencha:

1. **Conta de origem** — de onde sai o valor (obrigatório)
2. **Conta de destino** — para onde vai o valor (obrigatório)
3. **Valor** — obrigatório
4. **Data** — data da transferência (obrigatório)
5. **Descrição** — campo livre opcional
6. **Categoria** — classifique a transferência (ex: Fundo de Reserva). Categorias de transferência são gerenciadas em **Configurações → Categorias → Financeiro**
7. **Comprovante** — anexe um arquivo como registro (opcional)

![Drawer de nova transferência com campos de contas, valor, data, categoria, descrição e comprovante](/assets/screenshots/89-financeiro-transferencia-drawer.png)

A operação é **atômica**: o sistema registra automaticamente um débito na conta de origem e um crédito na conta de destino de forma simultânea. Na listagem, transferências aparecem com o badge **Transferência** e o ícone ⇄. Se houver comprovante, um ícone de clipe permite visualizá-lo diretamente.

{: .warning }
> **Totais de receita e despesa**
>
> Transferências **não afetam** os cards de Entradas e Saídas do mês, nem os relatórios financeiros — elas representam movimentação interna entre contas, não variação no patrimônio do condomínio.

{: .note }
> **Excluir uma transferência**
>
> Ao excluir uma transferência, ambos os lançamentos (débito e crédito) são removidos automaticamente.

## Importar extrato bancário *(síndico — plano Pro)*

O V3RCondo aceita extratos nos formatos **OFX** (padrão da maioria dos bancos) e **CSV** genérico.

Para importar:

1. Clique em **Importar extrato**

![Tela de importação de extrato bancário](/assets/screenshots/18-financeiro-importar-extrato.png)

2. Selecione a **conta bancária de destino**
3. Faça o upload do arquivo OFX ou CSV
4. Revise as correspondências encontradas:
    - **Conciliado automaticamente** — mesmo valor + data ≤ 3 dias
    - **Aguarda confirmação** — mesmo valor + data 4–7 dias
    - **Novo lançamento** — sem correspondência; decida importar ou ignorar
5. Clique em **Confirmar importação**

{: .note }
> **Deduplicação automática**
>
> O sistema identifica transações já importadas e as ignora, evitando duplicatas.

## Lançamento em lote por unidade *(síndico)*

Para gerar cobranças mensais, taxas extras ou qualquer encargo que se aplique a múltiplas unidades de uma só vez, use o lançamento em lote.

Clique em **Lançamento em lote** e preencha o formulário:

![Formulário de lançamento em lote com tabela de unidades e valores pré-preenchidos](/assets/screenshots/financeiro-lancamento-lote.png)

**Campos comuns (aplicados a todas as unidades):**

1. **Categoria** — selecione entre as categorias de cobrança por unidade cadastradas em Configurações
2. **Descrição** — use `{unidade}` para personalizar automaticamente. Exemplo: `Taxa condominial — Apto {unidade}` gera "Taxa condominial — Apto 101", "Taxa condominial — Apto 102" etc.
3. **Vencimento** — data de vencimento das cobranças
4. **Competência** — mês/ano de referência (obrigatório)
5. **Conta bancária** — opcional
6. **Valor padrão** — usado para unidades sem taxa mensal configurada

**Tabela de unidades:**

Todas as unidades ativas aparecem com o valor pré-preenchido a partir da **taxa mensal configurada** em Configurações → Unidades. Unidades sem taxa configurada recebem o valor padrão informado acima. Todos os valores são ajustáveis individualmente antes de confirmar. Use o checkbox de cada linha para incluir ou excluir unidades; o rodapé exibe a contagem de selecionadas e o total.

Clique em **Criar lançamentos** para gerar um lançamento por unidade selecionada.

{: .tip }
> **Cancelar um lote**
>
> Na listagem do Financeiro, lançamentos criados em lote exibem o badge **Lote**. Clique no badge para ver todos os lançamentos do lote e, se necessário, cancelar o lote inteiro de uma vez.

{: .note }
> **Configure as taxas antes de usar**
>
> Para aproveitar o pré-preenchimento automático de valores, configure a taxa mensal de cada unidade em **Configurações → Unidades**.

## Importar lançamentos em lote *(síndico)*

Para cadastrar muitos lançamentos de uma vez — por exemplo, ao assumir um condomínio com histórico de inadimplência ou ao lançar despesas recorrentes de um período — use a importação em lote via planilha.

Clique em **Importar lançamentos** e siga as quatro etapas do wizard:

**1. Modelo**
Baixe o template `.xlsx`. Ele inclui as 16 colunas aceitas pelo sistema e uma planilha **Referências** com os nomes exatos das categorias e contas bancárias cadastradas no seu condomínio — use-os para preencher as colunas correspondentes.

Colunas obrigatórias: `tipo` (receita/despesa), `descricao`, `valor`, `vencimento` (DD/MM/AAAA) e `unidade` e `categoria`.

A coluna `comprovante` é opcional e aceita, em cada célula, uma **URL** (`https://…`) ou o **nome de um arquivo** que estará dentro do ZIP enviado na etapa seguinte. Para anexar **mais de um comprovante ao mesmo lançamento**, informe vários valores na mesma célula separados por vírgula (`,`), ponto e vírgula (`;`), pipe (`|`) ou nova linha — por exemplo, o PDF e o XML de uma mesma nota fiscal. **Espaço não separa** — pode fazer parte do nome do arquivo normalmente. Limite de 10 anexos por lançamento.

{: .note }
> Um arquivo `.zip` **não** pode ser usado como valor da coluna `comprovante` (não é expandido automaticamente). Se você tem vários documentos para o mesmo lançamento, referencie os arquivos individuais na mesma célula, separados por vírgula — não zipe-os juntos.

**2. Upload**
Selecione ou arraste o arquivo preenchido (`.xlsx` ou `.csv`, máx. 500 linhas). O sistema exibe quantas linhas foram detectadas e quantas têm erro de formato. Se quiser que todas as linhas usem a mesma conta bancária, selecione-a no seletor de conta padrão — linhas que já tiverem conta preenchida na planilha têm prioridade.

Se alguma linha referenciar comprovantes por **nome de arquivo** (não por URL), envie também o **ZIP de comprovantes** (opcional, até 25 MB) contendo esses arquivos. O sistema casa cada nome com o arquivo correspondente dentro do ZIP; comprovantes por URL são baixados em segundo plano, sem precisar do ZIP. Comprovantes não encontrados ou com formato não suportado geram um aviso na linha, mas não impedem a importação do lançamento.

**3. Pré-visualização**
Cada linha é validada pela Edge Function antes da importação. A tabela mostra o status de cada uma:

| Status | Significado |
|---|---|
| ✅ Válida | Pronta para importação |
| ⚠️ Aviso | Categoria não encontrada — será importada com categoria em branco |
| ⚠️ Possível duplicata | Combinação de unidade, categoria, valor e vencimento já existe |
| 🚫 Duplicata confirmada | `referencia_externa` já existe no condomínio — será ignorada |
| ❌ Erro | Descrição do problema na coluna Status |

Quando a coluna **Competência** estiver em branco, o sistema preenche automaticamente com o mês de vencimento e exibe o valor com a marcação **(auto)** na tabela — sem bloquear a importação.

Confirme apenas se houver pelo menos uma linha válida.

**4. Resultado**
Exibe quantos lançamentos foram importados, quais erros adicionais ocorreram e quantas duplicatas foram ignoradas. Se houver comprovantes na planilha, eles são processados em segundo plano — você recebe uma notificação in-app quando terminar. Clique em **Fechar** para voltar à lista atualizada.

{: .tip }
> **Deduplicação por referência externa**
>
> Preencha a coluna `referencia_externa` com um identificador único por lançamento (ex: número do boleto ou código interno). Se a mesma referência já existir no condomínio, a linha é ignorada silenciosamente — útil para reprocessar planilhas parcialmente importadas sem criar duplicatas.

{: .tip }
> **Match de categoria tolerante a acentos**
>
> O sistema normaliza nomes de categoria removendo acentos e espaços extras antes de comparar. "Administraçao" encontra "Administração", "taxa  extra" encontra "Taxa Extra". Se mesmo assim a categoria não for encontrada, o lançamento é importado com categoria em branco e um aviso é exibido no preview.

{: .note }
> **Competência**
>
> Use a coluna `competencia` (MM/AAAA) para indicar o mês de referência quando ele for diferente do mês de vencimento. Se não preenchida, o sistema usa o mês de vencimento. Para categorias de inadimplência, a competência é obrigatória.

## Importar retorno CNAB400 *(síndico — plano Pro)*

Após os boletos do mês serem processados pelo banco, importe o arquivo de retorno (.ret) para marcar automaticamente os lançamentos correspondentes como pagos.

Clique em **Importar retorno CNAB** e siga as quatro etapas:

![Wizard de importação de retorno CNAB400 mostrando pré-visualização com badges de correspondência por Nosso Número e CPF](/assets/screenshots/100-financeiro-cnab-retorno.png)

**1. Upload**
Selecione ou arraste o arquivo `.ret` gerado pelo Banco Inter (também aceito: `.txt`).

**2. Pré-visualização**
O sistema analisa os boletos liquidados (código de ocorrência 06) e busca os lançamentos correspondentes por dois critérios:

| Badge | Critério |
|---|---|
| ✅ Nosso Número | Lançamento encontrado pela referência do boleto. Disponível quando a remessa foi importada previamente via FIN-10a |
| ✅ CPF | Lançamento encontrado pelo CPF do pagador, unidade e competência — funciona sem a remessa |
| ❌ Sem correspondência | Boleto pago no banco mas sem lançamento correspondente no sistema |

Um resumo acima da tabela indica quantos registros foram encontrados por cada critério.

**3. Confirmação**
Revise a lista de lançamentos que serão marcados como pagos e confirme a importação.

**4. Resultado**
Exibe quantos lançamentos foram atualizados. Registros sem correspondência são listados para revisão manual.

{: .note }
> **Banco suportado**
>
> Nesta versão, o importador de retorno CNAB400 suporta exclusivamente o **Banco Inter (077)**. Suporte a outros bancos será adicionado em versões futuras.

{: .tip }
> **Conciliação sem remessa**
>
> Mesmo sem ter importado a remessa, é possível conciliar pagamentos: o sistema usa o CPF do pagador informado no arquivo de retorno para localizar a unidade e o lançamento na competência do mês. Se houver mais de um lançamento em aberto para a mesma unidade e mês, o registro ficará como "Sem correspondência" para revisão manual.

## Visão do condômino

Condôminos têm acesso de **leitura** ao módulo Financeiro — visualizam lançamentos, filtros e saldos, mas não podem criar, editar, excluir ou importar extratos. Transferências entre contas também são visíveis na listagem, identificadas pelo badge **Transferência**.
