---
title: Tarefas
parent: Módulos
nav_order: 5
---

# Tarefas

{: .warning }
> **Plano Pro**
>
> Este módulo é exclusivo para síndicos com **plano Pro**. Condôminos não têm acesso — o item **não aparece no menu lateral** para esse perfil, independente do plano.

O módulo de Tarefas permite ao síndico registrar e acompanhar as pendências do condomínio — obras, contratações, revisões de contratos e qualquer atividade que precise ser monitorada.

![Lista de tarefas com filtros, badges de prioridade e status](/assets/screenshots/23-tarefas-lista.png)

## Visão geral

O módulo oferece duas visões: **Lista** e **Kanban**. Use os filtros no topo para refinar a exibição:

![Visão Kanban do módulo de Tarefas](/assets/screenshots/24-tarefas-kanban.png)

- **Período** — mês de vencimento das tarefas (padrão: mês atual)
- **Prioridade** — Todas, Alta, Média ou Baixa
- **Status** — Todos, A Fazer, Em Andamento ou Concluída
- **Categoria** — filtra por categoria cadastrada

As tarefas são ordenadas por prazo crescente (mais urgente primeiro). Tarefas sem prazo aparecem apenas quando o filtro de período estiver em "Todos".

Cada tarefa pode exibir:

- **Prioridade** — Baixa, Média ou Alta (vermelho para urgentes)
- **Status** — A Fazer, Em Andamento ou Concluída
- **Ícone de recorrência** — indica que a tarefa faz parte de uma série recorrente
- **Ícone de anexos** com contador — indica quantos arquivos estão anexados; clique para abrir a tarefa

O número em laranja ao lado de "Tarefas" no menu lateral indica quantas tarefas estão pendentes ou vencidas.

## Criar uma tarefa

Clique em **+ Nova Tarefa** e preencha:

![Formulário de nova tarefa](/assets/screenshots/25-tarefas-form.png)

1. **Título** — descrição resumida (obrigatório)
2. **Descrição** — detalhes adicionais (opcional)
3. **Tarefa recorrente** — ative o toggle para criar uma série de tarefas
4. **Prazo** — data limite para conclusão (obrigatório quando não-recorrente)
5. **Prioridade** — Baixa, Média ou Alta (padrão: Média)
6. **Status** — A Fazer, Em Andamento ou Concluída (padrão: A Fazer)
7. **Categoria** — classificação da tarefa (opcional)

{: .note }
> **Anexos**
>
> Você poderá adicionar anexos após salvar a tarefa. Edite a tarefa criada para acessar a seção de anexos.

## Tarefas recorrentes

{: .warning }
> **Plano Pro**
>
> Tarefas recorrentes são exclusivas do plano Pro.

Ao ativar o toggle **Tarefa recorrente**, o campo de prazo é substituído por:

- **Tipo de recorrência** — Diária, Semanal, Mensal ou Anual
- **Data de início** — primeira ocorrência (obrigatório)
- **Data de término** — última ocorrência (opcional; se não informada, o sistema gera ocorrências por até 12 meses)

Ao salvar, o sistema gera automaticamente todas as ocorrências da série com os dados informados.

![Formulário com toggle de recorrência ativado e campos de periodicidade](/assets/screenshots/26-tarefas-form-recorrente.png)

### Editar tarefa recorrente

A edição sempre afeta **apenas a ocorrência selecionada**. As demais tarefas da série permanecem inalteradas.

{: .tip }
> **Edição individual**
>
> Ao editar uma tarefa recorrente, uma mensagem indica que as alterações afetam somente aquela ocorrência.

### Excluir tarefa recorrente

Ao clicar na lixeira de uma tarefa recorrente, o sistema pergunta:

- **Apenas esta** — exclui somente a ocorrência selecionada
- **Esta e todas as futuras** — exclui a ocorrência atual e todas as seguintes da série

Tarefas já concluídas nunca são afetadas pela exclusão em lote.

## Anexos

Na edição de uma tarefa, a seção **Anexos** permite:

- Fazer upload de até **5 arquivos** por tarefa (máximo **10 MB** por arquivo)
- Visualizar e baixar arquivos anexados
- Remover anexos individualmente

## Lembretes por e-mail

{: .warning }
> **Plano Pro**
>
> Lembretes por e-mail são exclusivos do plano Pro.

O V3RCondo envia automaticamente um e-mail diário ao síndico com o resumo das tarefas pendentes:

- **Vencidas** — prazo já passou
- **Vencem hoje**
- **Vencem em breve** — próximos 7 dias

Para ativar ou desativar os lembretes, acesse **Configurações → Notificações → Lembretes de tarefas por e-mail**.

## Gerenciar tarefas

- **Editar** — clique no ícone de lápis
- **Excluir** — clique no ícone de lixeira e confirme
- **Alterar status** — edite a tarefa e atualize o campo Status

{: .tip }
> **Conclusão automática**
>
> Ao marcar uma tarefa como **Concluída**, a data de conclusão é registrada automaticamente.

{: .note }
> **Tarefas urgentes no Dashboard**
>
> Tarefas com prioridade **Alta** e prazo vencido aparecem em destaque na seção "Tarefas Urgentes" do Dashboard.

## Criar tarefa a partir de uma solicitação

No módulo **Fale com o Síndico**, o botão **Criar tarefa** abre o formulário de Tarefas com título e descrição pré-preenchidos a partir da solicitação do condômino, facilitando o encaminhamento interno.
