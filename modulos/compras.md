---
title: Compras e Serviços
parent: Módulos
nav_order: 6
---

# Compras e Serviços

O módulo de Compras e Serviços organiza o ciclo completo de aquisição de produtos e contratação de serviços — desde o registro da necessidade até o controle financeiro da execução.

![Lista de compras e serviços em tabela com filtros de categoria e status](/assets/screenshots/27-compras-lista.png)

## Visão geral

A tela principal exibe as compras em modo **lista** (tabela) ou **grid** (cards), alternável pelo toggle no canto superior direito. Em ambos os modos são exibidos: título, categoria, status, data, fornecedor aprovado (quando houver) e número de orçamentos. Use os filtros de **categoria** e **status** para refinar a visualização.

**Status disponíveis:**

| Status | Descrição |
|---|---|
| Planejada | Registrada, ainda sem orçamentos ou em cotação |
| Em Andamento | Processo de compra em execução |
| Concluída | Compra finalizada |
| Cancelada | Compra cancelada |

## Registrar uma nova compra *(síndico)*

Clique em **+ Nova Compra** e preencha:

1. **Título** — descrição resumida (obrigatório)
2. **Descrição** — detalhes do que precisa ser adquirido ou executado
3. **Categoria** — classificação (obrigatório)
4. **Status** — padrão: Planejada
5. **Valor estimado** — referência antes de receber orçamentos (opcional)
6. **Valor final** — custo total realizado (opcional, sempre editável)
7. **Data prevista de início** — planejamento de quando o serviço começa
8. **Data de conclusão** — preenchida automaticamente ao concluir, mas editável

![Formulário de registro de nova compra ou serviço](/assets/screenshots/28-compras-form.png)

{: .tip }
> **Valor estimado**
>
> O valor estimado fica bloqueado após um orçamento ser aprovado — é preenchido automaticamente com o valor do orçamento aprovado. O valor final permanece sempre editável para registrar variações (imprevistos, material extra etc.).

## Gerenciar orçamentos *(síndico)*

Clique em **Ver detalhes** para abrir a página da compra.

![Página de detalhe de uma compra com cabeçalho, orçamentos e layout de duas colunas na parte inferior](/assets/screenshots/29-compras-detalhe.png)

Para adicionar um orçamento, clique em **+ Adicionar Orçamento** e preencha:

![Formulário de adição de orçamento com fornecedor, valor e prazo](/assets/screenshots/31-compras-orcamento-form.png)

1. **Fornecedor** — busque um fornecedor já cadastrado pelo nome. Se não encontrar, clique em **+ Cadastrar novo fornecedor** para preencher os dados e criar o registro automaticamente no módulo Fornecedores
2. **Valor (R$)** — obrigatório
3. **Prazo de Execução** — número de dias
4. **Data do Orçamento**
5. **Observações**
6. **Anexo** — PDF, JPG ou PNG até 10 MB *(plano Pro)*

{: .note }
> **Integração com Fornecedores**
>
> Ao salvar um orçamento com dados de fornecedor, o sistema faz upsert automático em Fornecedores — evitando duplicatas por e-mail ou CPF/CNPJ. Fornecedores inativos são reativados automaticamente.

**Aprovar um orçamento:** clique em **Aprovar** no card desejado. Os demais são automaticamente rejeitados. Para desfazer, clique em **Desaprovar**. O fornecedor e valor aprovados ficam em destaque no cabeçalho da compra.

## Layout da página de detalhe

Na página de detalhe de uma compra, a seção inferior é exibida em **duas colunas** em telas maiores (desktop):

- **Coluna esquerda** — Documentos e Anexos
- **Coluna direita** — Despesas e Anotações (síndico)

Em dispositivos móveis, as seções são exibidas empilhadas na ordem: Documentos e Anexos → Despesas → Anotações.

![Seção inferior da página de detalhe com layout em duas colunas: Documentos e Anexos à esquerda, Despesas e Anotações à direita](/assets/screenshots/30-compras-despesas.png)

## Documentos e Anexos *(síndico)*

Na página de detalhe da compra, a seção **Documentos e Anexos** permite visualizar e registrar arquivos organizados por fase da compra.

{: .note }
> **Upload de arquivos — plano Pro**
>
> A **visualização** da seção está disponível para todos os planos. O **upload de novos arquivos** é exclusivo do plano Pro. Síndicos no plano Básico visualizam a seção, mas o botão de upload exibe um indicador de plano Pro com opção de upgrade em Configurações.

| Fase | Exemplos de uso |
|---|---|
| Planejamento | Fotos do ambiente, memorial descritivo, plantas |
| Execução | Fotos da obra em andamento, notas de material |
| Conclusão | Fotos da obra finalizada, relatório de entrega |
| Geral | Contratos, garantias, documentos sem fase específica |

- Upload de múltiplos arquivos de uma vez *(plano Pro)*
- Aceita PDF, JPG, PNG e DOCX (máx. 20 MB por arquivo)
- A fase sugerida é determinada automaticamente pelo status atual da compra
- Download via URL segura; exclusão preserva histórico via soft delete

## Controle financeiro da obra *(síndico)*

A seção **Despesas** na página de detalhe registra cada pagamento realizado e cria automaticamente o lançamento correspondente no módulo Financeiro.

Para registrar uma despesa, clique em **+ Adicionar despesa** e preencha:

1. **Descrição** — obrigatório
2. **Categoria** — Material / Mão de Obra / Outros
3. **Valor** — obrigatório
4. **Data da despesa** — padrão: hoje
5. **Data de vencimento** — pré-preenchida com a data da despesa, editável
6. **Conta bancária** — pré-selecionada a conta padrão do condomínio, editável
7. **Marcar como pago** — toggle; se ativado, registra o pagamento na data da despesa
8. **Observações** — opcional
9. **Comprovante** — PDF, JPG, PNG ou ZIP até 10 MB

Cada despesa exibe um **badge de status de pagamento**:

| Badge | Significado |
|---|---|
| **Pago** | Pagamento registrado (toggle "Marcar como pago" foi ativado) |
| **Pendente** | Aguardando pagamento dentro do prazo |
| **Vencido** | Prazo de vencimento expirado sem quitação |

O **total acumulado de despesas** é exibido no cabeçalho da compra. Quando o valor final estiver preenchido, o sistema exibe o comparativo **Total gasto vs. Orçado**.

{: .warning }
> **Excluir despesa**
>
> Ao excluir uma despesa, o lançamento correspondente no módulo Financeiro também é removido. Uma confirmação é exibida antes da exclusão.

## Anotações do síndico *(síndico)*

A seção **Anotações**, visível somente para síndicos e subsíndicos, permite registrar ocorrências, decisões e observações ao longo da execução de uma compra ou obra.

- Digite livremente no campo de texto e clique em **Salvar anotações** para persistir o conteúdo
- As anotações ficam disponíveis a qualquer momento enquanto a compra estiver ativa
- O conteúdo é automaticamente incluído no prompt de geração do relatório de execução, enriquecendo a análise feita pela inteligência artificial

{: .tip }
> **Boas práticas**
>
> Registre anotações sempre que houver uma decisão relevante: troca de fornecedor, imprevisto na obra, alteração de escopo, prazo renegociado. Quanto mais contexto o síndico registrar, mais completo e preciso será o relatório gerado pela IA.

## Relatório de execução *(síndico)*

Ao concluir uma compra (status Concluída), o sistema oferece a geração
de um relatório de execução por inteligência artificial com dados
financeiros, prazos, orçamentos e anotações da obra.

### Gerar o relatório

Clique em **Gerar relatório da obra** no cabeçalho da compra e preencha:

- **Observações e orientações para o relatório** — descreva imprevistos,
  alterações de escopo, comentários sobre a execução (opcional, mas
  recomendado para enriquecer o relatório)
- **Enviar para condôminos** — marque para que o relatório seja
  distribuído a todos os moradores após geração
- **Enviar para Conselho Fiscal** — marque para incluir os membros
  do Conselho Fiscal na distribuição

{: .note }
> **Destinatários automáticos**
>
> O relatório é enviado automaticamente por e-mail para todos os
> síndicos do condomínio assim que a geração for concluída.
> A distribuição para condôminos e Conselho Fiscal é opcional.

### Estados do relatório

| Estado | Botão exibido |
|---|---|
| Compra não concluída | Nenhum botão de relatório |
| Concluída, sem relatório | **Gerar relatório** |
| Gerando... | **Gerando...** (desabilitado, com indicador de progresso) |
| PDF disponível para revisão | **Visualizar rascunho** + **Publicar** |
| Relatório publicado | **Ver relatório publicado** |

### Revisar e publicar

- **Visualizar rascunho** — abre o PDF em nova aba via link seguro
  (válido por 7 dias). Disponível para síndicos e condôminos
- **Publicar** — distribui o relatório para os destinatários selecionados
  na geração (síndicos sempre; condôminos e/ou Conselho Fiscal conforme
  as marcações feitas ao solicitar o relatório). Após publicar, o botão
  muda para **Ver relatório publicado**

### Conteúdo do relatório

O relatório gerado pela IA inclui:

- **Resumo executivo** — síntese dos principais pontos da obra
- **Processo de cotação** — todos os orçamentos recebidos com
  comparativo entre aprovado e rejeitados
- **Execução financeira** — total gasto por categoria (material,
  mão de obra, outros) com comparativo ao valor previsto
- **Considerações finais** — análise da execução com base nas
  observações informadas pelo síndico e nas **anotações registradas
  durante a execução** (ver seção Anotações do síndico)

### Campo de observações

O campo de observações pode ser preenchido ou atualizado a qualquer
momento no drawer de edição da compra (visível quando status for
Concluída) e é pré-carregado no modal de geração/regeneração.

## Visão do condômino

Condôminos têm **acesso de leitura** — visualizam a lista de compras, detalhes, orçamentos, anexos e despesas, mas não podem criar, editar ou excluir nenhum registro.
