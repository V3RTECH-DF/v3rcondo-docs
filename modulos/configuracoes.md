---
title: Configurações
parent: Módulos
nav_order: 14
---

# Configurações

{: .warning }
> **Acesso restrito**
>
> O módulo de Configurações é exclusivo para **síndicos**. As preferências
> de notificação também estão disponíveis para condôminos.

O módulo reúne todas as opções de gestão do condomínio, organizadas em
sete abas.

![Aba Condomínio com dados cadastrais e card do plano atual](/assets/screenshots/73-config-condominio.png)

## Aba Condomínio

Exibe e permite editar os dados cadastrais:

- **Nome do Condomínio** — obrigatório
- **Endereço Completo** — logradouro e número
- **Cidade e Estado**
- **CNPJ** — cadastro nacional do condomínio
- **Quantidade de unidades** — número de unidades do condomínio
- **Logo do Condomínio** — PNG ou JPG até 2 MB. A logo aparece na sidebar
  ao lado do nome

- **Fuso horário** — selecione o fuso horário do condomínio entre os 14 fusos brasileiros disponíveis (padrão: Brasília, UTC−3). A configuração afeta como datas e horários são exibidos em todo o aplicativo — Dashboard, Financeiro, Tarefas, Assembleias, Compras e Fale com o Síndico

Clique em **Salvar alterações** para confirmar.

### Plano e assinatura

Na coluna direita da aba Condomínio, o card **Seu Plano** exibe o plano atual,
o status do pagamento e a data da próxima cobrança. A partir daqui você
pode assinar o plano Pro ou gerenciar a assinatura existente.

### Parceiros do Condomínio

Abaixo do card de plano, a seção **Parceiros do Condomínio** centraliza os
contatos institucionais fixos do condomínio — profissionais e empresas com
relacionamento contínuo, como contador, advogado e administradora.

Tipos de parceiro disponíveis:

- **Contador / Escritório Contábil**
- **Advogado / Escritório Jurídico**
- **Administradora**
- **Segurança**
- **Empresa de Elevadores**
- **Bombeiros / AVCB**
- **Limpeza e Conservação**
- **Zeladoria**
- **Outro** — com rótulo personalizado

Para cada parceiro é possível registrar: empresa, nome do contato, CNPJ,
telefone, e-mail e observações.

![Seção Parceiros do Condomínio com cards de contatos institucionais](/assets/screenshots/74-config-parceiros.png)

Clique em **+ Adicionar parceiro** para
cadastrar um novo contato, ou no ícone de lápis (✎) ao lado de um parceiro
existente para editar ou excluir.

![Modal de cadastro de parceiro do condomínio](/assets/screenshots/75-config-parceiro-modal.png)

{: .tip }
> **Diferença entre Parceiros e Fornecedores**
>
> **Parceiros** são contatos institucionais permanentes (contador, advogado,
> administradora). **Fornecedores** são empresas contratadas para serviços
> pontuais (elétrica, pintura, jardinagem). Use módulos separados para manter
> a organização.

## Aba Condôminos

Lista todos os membros ativos com: nome, e-mail, unidade, papel e título.
Use o filtro para visualizar apenas síndicos ou apenas condôminos. O condômino designado como **responsável** pela unidade aparece com um badge laranja "Responsável" — ele é o destinatário das notificações extrajudiciais.

![Aba Condôminos com lista de membros ativos, badges de responsável, ícone de editar perfil e botão Transferir](/assets/screenshots/config-condominos-editar.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

**Adicionar um condômino diretamente:** clique em **+ Adicionar condômino**,
preencha o nome completo, e-mail, unidade (opcional) e título (opcional:
Síndico, Subsíndico, Contador, Conselho Fiscal) e clique em **Adicionar**. O sistema
cadastra o membro imediatamente e envia um e-mail de boas-vindas com
instruções para definir a senha ou entrar com o Google.

![Modal de adição direta de condômino com campos de nome, e-mail, unidade e título](/assets/screenshots/77-config-condomino-modal.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

**Editar dados de um membro:** clique no ícone de lápis (✎) ao lado do membro para abrir o drawer **Editar Membro**. O síndico pode editar:

![Drawer Editar Membro com campos de Nome, Unidade, Título e dados pessoais incluindo CPF, RG, Telefone, Profissão, Instagram, LinkedIn e aniversário](/assets/screenshots/config-editar-membro-drawer.png)

- **Nome** — nome completo do membro
- **Unidade** — unidade à qual o membro pertence
- **Título** — Síndico, Subsíndico, Contador, Conselho Fiscal ou Condômino
- **CPF** — com formatação automática (000.000.000-00)
- **RG**
- **Telefone**
- **Profissão**
- **Instagram** e **LinkedIn** — links de perfil
- **Dia e Mês de aniversário**

Clique em **Salvar** para confirmar. Ao promover um membro para Síndico, o sistema exibe um aviso de que o condomínio passará a ter mais de um síndico — o papel do síndico atual não é alterado automaticamente. Ao alterar o próprio papel para um título sem permissão de síndico, o sistema exibe um aviso de confirmação, pois o acesso de síndico será removido imediatamente após salvar.

**Transferir responsabilidade:** quando um condômino responsável por uma unidade tem pelo menos outro membro na mesma unidade, o botão **Transferir** aparece ao lado do badge "Responsável". Clique nele para selecionar o novo responsável e confirmar a transferência — o sistema garante que sempre haverá exatamente um responsável por unidade.

![Modal de transferência de responsabilidade com seletor de novo responsável](/assets/screenshots/95-configuracoes-transferir-responsavel.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

**Importar planilha de condôminos:** clique em **Importar planilha** para
cadastrar vários condôminos de uma vez. Baixe o modelo, preencha com Nome,
E-mail, Unidade e Título e faça o upload. O sistema processa linha a linha,
ignora e-mails já cadastrados e exibe um resumo com importados, ignorados e
rejeitados (com o motivo). Limite de 100 condôminos por importação — se
houver mais, realize importações em lote.

![Tela de importação de planilha de condôminos](/assets/screenshots/78-config-importar-planilha.png)

**Solicitações pendentes:** solicitações de vínculo enviadas pelos próprios
moradores aparecem acima da lista. O síndico pode **Aprovar** ou **Rejeitar**
cada solicitação.

## Aba Unidades *(síndico)*

Lista todas as unidades ativas do condomínio (derivada dos condôminos cadastrados com unidade preenchida) e permite configurar a **taxa mensal** de cada uma, individualmente ou em lote.

![Aba Unidades com lista de unidades, filtro rápido e tabela de taxas mensais](/assets/screenshots/98-config-unidades.png)

| Coluna | Descrição |
|---|---|
| **Unidade** | Identificação da unidade (ex.: 101, Bloco A Apto 3) |
| **Taxa Mensal (R$)** | Valor configurado ou "—" se ainda não definido |
| **Ações** | Botão Editar para definir ou alterar o valor individualmente |

### Edição individual

Clique em **Editar** ao lado de uma unidade, informe o valor em reais e clique em **Salvar**. Para remover a taxa configurada, deixe o campo em branco e salve.

### Filtro rápido

Acima da tabela, os botões **Todas / Sem taxa / Com taxa** filtram as unidades exibidas. Trocar o filtro limpa a seleção atual.

### Aplicação em lote

Para configurar a taxa de várias unidades de uma vez:

1. **Selecione as unidades** marcando os checkboxes à esquerda de cada linha. O checkbox no cabeçalho da tabela seleciona ou deseleciona todas as unidades visíveis. Quando apenas algumas estão marcadas, o checkbox do cabeçalho exibe um estado intermediário (traço).
2. Ao selecionar ao menos uma unidade, a **barra de ação em lote** aparece acima da tabela, indicando quantas unidades estão selecionadas e oferecendo um botão **Desmarcar** para limpar a seleção.
3. Escolha o modo de aplicação:

    - **Taxa fixa (R$):** define o mesmo valor para todas as unidades selecionadas. Se o valor informado for zero, um aviso em destaque informa que a taxa será *removida* dessas unidades.

    ![Barra de ação em lote com modo Taxa fixa e 3 unidades selecionadas](/assets/screenshots/99-config-unidades-selecao-taxa-fixa.png)

    - **Reajuste (%):** aplica um percentual sobre a taxa atual de cada unidade selecionada. Use valores positivos para aumento e negativos para desconto (ex.: `-5` para 5% de desconto). Unidades sem taxa configurada são automaticamente ignoradas e listadas no diálogo de confirmação.

    ![Barra de ação em lote com modo Reajuste % e campo de percentual](/assets/screenshots/100-config-unidades-selecao-reajuste.png)

4. Clique em **Aplicar**. Um diálogo de confirmação exibe uma prévia das alterações — incluindo exemplos de cálculo no modo reajuste e a lista de unidades que serão ignoradas — antes de gravar.

{: .note }
> **Para que serve esse campo?**
>
> A taxa mensal por unidade é usada como valor padrão ao gerar cobranças em lote no módulo Financeiro. Configure antes de usar o lançamento em lote para não precisar preencher o valor manualmente para cada unidade.

{: .tip }
> **Unidades não aparecem na lista?**
>
> A lista é derivada dos condôminos cadastrados com unidade preenchida. Cadastre os condôminos em **Condôminos** antes de configurar as taxas.

## Aba Cobranças & Acordos *(síndico)*

Configura a geração automática de cobranças mensais do condomínio.

| Campo | Descrição |
|---|---|
| **Categoria de cobrança** | Categoria financeira que será usada nos lançamentos gerados (ex.: "Taxa de Contribuição") |
| **Dia de vencimento** | Dia do mês em que as cobranças vencem (1 a 31). Em meses com menos dias, o sistema ajusta automaticamente para o último dia do mês |
| **Antecedência do aviso** | Quantos dias antes do vencimento o síndico recebe um lembrete para revisar as cobranças |
| **Gerar automaticamente** | Quando ativado, o sistema gera os lançamentos por unidade no dia calculado, sem necessidade de ação manual |
| **Notificar condôminos** | Quando ativado (junto com "Gerar automaticamente"), os condôminos recebem uma notificação ao ter a cobrança lançada |

![Aba Cobranças com configurações de geração automática e botão Gerar agora](/assets/screenshots/101-config-cobranças.png)

Clique em **Salvar configurações** para confirmar.

{: .note }
> **Geração manual**
>
> Mesmo com a geração automática desativada, o botão **Gerar agora** permite disparar a criação das cobranças manualmente. Ao clicar, um diálogo apresenta três opções de mês antes de confirmar: **Mês atual** (padrão), **Próximo mês** e **Escolher mês** (seletor livre). O mês selecionado define a competência e o vencimento dos lançamentos gerados.

{: .tip }
> **Sem duplicatas**
>
> O sistema verifica se as cobranças do mês atual já foram geradas antes de agir. Se já existirem lançamentos daquela categoria para o mês, a ação é ignorada silenciosamente — sem duplicatas.

{: .warning }
> **Configure as unidades antes**
>
> Para que o valor de cada cobrança seja preenchido automaticamente, configure a taxa mensal por unidade em **Configurações → Unidades** antes de ativar a geração automática.

### Parâmetros de Acordo Self-Service *(plano Pro)*

Define as condições do acordo quando o próprio condômino inicia o parcelamento por Minha Área.

| Campo | Padrão | Descrição |
|---|---|---|
| **Multa sobre o débito (%)** | 2,00% | Percentual aplicado sobre o total dos débitos selecionados |
| **Juros de mora mensais (%)** | 1,00% | Percentual ao mês aplicado por mês de atraso em cada lançamento |
| **Máximo de parcelas permitidas** | 12 | Teto de parcelas que o condômino pode escolher |
| **Valor mínimo por parcela (R$)** | R$ 50,00 | Opções com valor de parcela abaixo deste limite não são oferecidas |

Clique em **Salvar parâmetros** para confirmar. Os valores entram em vigor imediatamente para novos acordos — acordos já criados não são afetados.

## Aba Notificações

Controla quais eventos geram notificações por e-mail para o usuário logado:

![Aba de preferências de notificações por e-mail com toggles por evento](/assets/screenshots/79-config-notificacoes.png)

- **Avisos no mural** — notificar ao publicar aviso
- **Novos documentos** — notificar ao adicionar arquivo
- **Comunicados gerais** — notificar ao receber comunicado

Ative ou desative cada toggle e clique em **Salvar preferências**.

{: .note }
> **Disponível para condôminos**
>
> Esta aba também está disponível para condôminos — cada morador controla
> individualmente suas preferências.

## Aba Categorias

Gerencia as categorias de cada módulo, organizadas em 7 sub-abas:

![Aba Categorias com sub-abas por módulo](/assets/screenshots/80-config-categorias.png)
**Financeiro**, **Tarefas**, **Compras e Serviços**, **Documentos**,
**Mural**, **Fornecedores** e **Itens**.

Selecione a sub-aba do módulo desejado. Para cada categoria é possível:

- **Adicionar** — clique em **+ Nova Categoria**
- **Editar** — clique no ícone de lápis
- **Excluir** — clique no ícone de lixeira (com confirmação)

{: .tip }
> **Categorias financeiras**
>
> A sub-aba Financeiro divide as categorias em quatro grupos: **Receita**,
> **Despesa**, **Ambos** e **Transferência**. O grupo Transferência reúne
> categorias usadas para classificar transferências entre contas (ex: Fundo
> de Reserva, Reserva para equipamentos). Informe o tipo ao criar uma nova
> categoria.

![Sub-aba Financeiro mostrando grupos Receita, Despesa, Ambos e Transferência](/assets/screenshots/81-config-categorias-financeiro.png)

{: .tip }
> **Categorias de Itens**
>
> As categorias padrão de Itens (**Pet**, **Veículo**, **Vaga de garagem**)
> não podem ser excluídas. Categorias personalizadas só podem ser excluídas
> se não houver itens vinculados a elas.

## Aba Contas Bancárias

Lista as contas bancárias com: nome, banco, agência, número e saldo inicial.
A conta marcada como **Padrão** é pré-selecionada automaticamente em novos
lançamentos.

![Aba Contas Bancárias com lista de contas e indicação de conta padrão](/assets/screenshots/82-config-contas.png)

Para adicionar uma nova conta, clique em **+ Nova Conta** e preencha:

1. **Nome da conta** — ex: "Conta Inter", "Fundo de Reserva" (obrigatório)
2. **Banco** — nome do banco
3. **Agência** — número da agência
4. **Número da conta**
5. **Saldo inicial** — saldo na data de implantação (padrão: 0,00)
6. **Data do saldo inicial** — data de referência do saldo
7. **Conta padrão** — ative para pré-selecionar em novos lançamentos

![Modal de cadastro de nova conta bancária com todos os campos](/assets/screenshots/83-config-conta-modal.png)
