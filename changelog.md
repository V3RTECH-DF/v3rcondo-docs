---
title: Changelog
nav_order: 5
---

Registro de versões e novidades do V3RCondo.

---

## v7.65.0 — Junho 2026

- **Desempenho — listas mais rápidas em condomínios grandes:** as telas de **Financeiro**, **Documentos**, **Notificações** e **Visitantes** passaram a carregar os registros em páginas (com botão **"Carregar mais"**) em vez de baixar todo o histórico de uma vez. Os filtros do Financeiro (tipo, situação, categoria e mês) e dos Documentos (categoria e mês) passaram a ser aplicados no servidor. Os totais dos cartões e do gráfico continuam exatamente os mesmos — a mudança é só de velocidade, especialmente perceptível em condomínios com muitos lançamentos.
- **Desempenho — Dashboard e Inadimplência:** os cartões e o gráfico de 6 meses do **Dashboard** e a visão de inadimplência por unidade passaram a ser calculados no servidor, deixando a abertura dessas telas mais leve.
- **Segurança — reforços internos (sem impacto na interface):** revisão ampla de permissões de acesso aos dados e às funções automáticas do sistema, restringindo cada operação ao mínimo necessário e reforçando a proteção das comunicações entre o aplicativo e o servidor. Nenhuma mudança visível no uso do dia a dia.

---

## v7.64.3 — Junho 2026

- **Correção — redefinição de senha por e-mail:** o e-mail de "Esqueci minha senha" havia parado de ser enviado por uma inconsistência interna no cadastro de usuários (contas criadas por inclusão direta, convite ou importação de planilha). A causa foi corrigida na origem — novos cadastros já nascem consistentes — e os cadastros existentes foram normalizados. A redefinição de senha por e-mail voltou a funcionar normalmente.
- **Melhorias internas de confiabilidade (sem impacto na interface):** concluída a migração da autenticação de todos os processos agendados (geração de cobranças, lembretes de reserva e assembleia, arquivamento de reservas e e-mails de acesso) para um segredo dedicado e estável, tornando-os imunes às rotações de chave da plataforma que haviam causado as falhas corrigidas na versão anterior.

---

## v7.64.2 — Junho 2026

- **Correção — geração automática de cobranças mensais:** as cobranças mensais dos condôminos voltaram a ser geradas automaticamente na data configurada. Por uma falha interna de autenticação dos processos agendados, a geração automática havia parado de funcionar; o problema foi corrigido. Além disso, a rotina passou a **tolerar atrasos**: se a execução de um dia falhar, a cobrança é gerada na próxima execução, dentro do mês, sem perder a competência. A regra de data (dia de vencimento e antecedência, em **Configurações → Cobranças & Acordos**) permanece inalterada.
- **Melhorias internas de confiabilidade (sem impacto na interface):** monitoramento automático da saúde dos processos agendados, com alerta aos administradores quando algo falha; otimização do envio dos e-mails de acesso (login, redefinição de senha e confirmação de cadastro), que passaram a ser processados de forma imediata em vez de aguardar um ciclo de processamento; e fortalecimento da autenticação dos processos automáticos, tornando-os resistentes a rotações de chave da plataforma.

---

## Revisão Documental — Maio 2026

- **Termos de Uso v1.1:** papéis de usuário expandidos (porteiro, Conselho Fiscal, subsíndico); Seção 8 adicionada — Do Uso de Inteligência Artificial (8.1–8.6); Seção 9 adicionada — Dos Acordos de Inadimplência (9.1–9.6); seções anteriores renumeradas (8–12 → 10–14); referência ao fluxo de convite removida (Art. 3.3); prazo CDC corrigido para "data da contratação" (Art. 5.3); prazo de exclusão de dados ajustado de 90 para 30 dias contados da suspensão (Art. 11.2); menção a boleto bancário removida por não estar implementado (Art. 4.5)
- **Política de Privacidade v1.1:** quatro categorias de dados adicionadas à Seção 2.1 (unidade residencial, pets/veículos/vagas, acordos de inadimplência, registros de assembleia, Telegram Chat ID); Seção 2.4 adicionada — Dados de visitantes (5 campos, base legal legítimo interesse); provedor de IA atualizado de DeepSeek para Google Gemini; Telegram (EAU) adicionado à lista de subprocessadores internacionais com admonition ANPD; remoção de "Convites expirados" e adição de "Dados de visitantes" e "Dados de conta suspensa por inadimplência" nas regras de retenção (Seção 4.2); parágrafo de resposta a incidentes adicionado (LGPD art. 48, Resolução CD/ANPD nº 2/2022, prazo de 3 dias úteis); portabilidade ajustada de JSON para XLSX com admonition da ANPD (Seção 6)

---

## v7.64.1 — Maio 2026

- **Correção — envio automático de e-mail de convite:** desde uma atualização anterior, o convite por e-mail havia parado de funcionar silenciosamente em quatro fluxos: convidar síndico pelo painel administrativo, convidar condômino via Configurações, reenviar convite e importar condôminos em planilha. O sistema ainda gerava o link de acesso corretamente, mas não enviava o e-mail — os síndicos estavam compartilhando o link manualmente. As três Edge Functions responsáveis foram corrigidas para enviar o e-mail com o link de acesso automaticamente, usando o mesmo canal de notificação já estabelecido no sistema. O comportamento visível da interface não muda: o sucesso ou falha no envio do e-mail ocorre em segundo plano e não altera a resposta exibida ao síndico

---

## v7.62.3 — Maio 2026

- **Financeiro — lançamentos parcelados:** ao registrar uma despesa (ou receita), o síndico pode ativar o toggle **Parcelado** para dividir o valor total em N parcelas mensais. O sistema exibe uma tabela de prévia com valor e vencimento calculados automaticamente; os valores são editáveis individualmente antes de salvar. Ao confirmar, são criados N lançamentos independentes, cada um identificado na lista com o badge **Parcela X/N**. Ao excluir uma parcela, o síndico escolhe se deseja remover apenas aquela, todas as pendentes ou o grupo completo. Os modos **Parcelado** e **Recorrente** são mutuamente exclusivos

---

## v7.61.0 — Maio 2026

- **Configurações — edição de dados de condôminos pelo síndico:** o síndico pode editar o perfil completo de qualquer condômino diretamente em **Configurações → Condôminos**, clicando no ícone de lápis ao lado do membro. O drawer **Editar Membro** reúne agora todos os campos de perfil: nome, unidade, título (papel), CPF (com validação e máscara), RG, telefone, profissão, Instagram, LinkedIn e dia e mês de aniversário

---

## v7.60.8 — Maio 2026

- **Correção — opt-out em preferências de notificação:** cinco Edge Functions (`get-recipients`, `handle-bulletin-notification`, `handle-file-notification`, `manage-reservation` e `send-platform-announcement`) tratavam a tabela de preferências de notificação como opt-in, ou seja, só enviavam para membros que tinham uma linha explícita com a preferência ativada. O comportamento correto é opt-out: todos recebem por padrão, exceto quem optou por não receber. Corrigido nas cinco funções. Aproveitou-se a correção para remover trechos de registro de diagnóstico adicionados temporariamente durante a investigação do bug anterior, sem afetar o tratamento de erros definitivo

---

## v7.60.7 — Maio 2026

- **Correção — notificação Telegram ao síndico após geração de ata:** o síndico não recebia mensagem no Telegram quando uma ata de assembleia era gerada pela IA. O problema era que o objeto enviado ao sistema de notificações não incluía o identificador do Telegram do síndico. Corrigido na Edge Function `manage-assembly`. Adicionalmente, o fluxo n8n de geração de ata (`v3rcondo-assembly-minutes`) foi atualizado para enviar o e-mail da ata a **todos os síndicos ativos** do condomínio (e não apenas ao primeiro cadastrado), e para disparar a notificação Telegram individualmente para cada síndico que tiver o bot conectado

---

## v7.60.6 — Maio 2026

- **Correção — e-mails dos condôminos ausentes no payload da ata de assembleia:** ao gerar a ata por IA, os e-mails de todos os membros chegavam em branco ao sistema de envio, o que impedia a entrega por e-mail. A causa era uma tentativa de cruzar dados entre duas tabelas sem vínculo direto no banco, que falhava silenciosamente. Corrigido na Edge Function `manage-assembly` com duas consultas separadas e combinação manual dos dados por identificador de usuário

---

## v7.60.5 — Maio 2026

- **Correção — notificações com erro 401 após atualização de segurança:** uma correção anterior nas Edge Functions introduziu uma forma de autenticação que depende de uma variável de ambiente não disponível na infraestrutura atual (`SUPABASE_JWT_SECRET`). Isso causava falha em 100% das notificações internas (e-mail e Telegram) disparadas pelo app. Revertido para o método de autenticação original, que usa a variável correta e já estava funcionando

---

## v7.60.1 — Maio 2026

- **Correção — e-mail dos managers ausente no relatório gerado por IA:** ao enviar o relatório periódico, o sistema não conseguia recuperar o endereço de e-mail dos síndicos para entrega. O campo aparecia vazio no payload enviado à IA, o que impedia o envio correto. Corrigido na Edge Function `get-report-data`, que passou a buscar o e-mail diretamente da tabela de perfis, alinhando-se ao mesmo padrão já usado no relatório de compras

---

## v7.60.0 — Maio 2026

- **Registro formal de aceite dos documentos legais:** o V3RCondo passa a registrar com precisão qual versão dos Termos de Uso e da Política de Privacidade cada usuário aceitou, e em que momento. Anteriormente, o sistema apenas anotava a data do primeiro aceite, sem informação de versão — o que impedia exigir nova confirmação quando os documentos fossem atualizados. A partir desta versão, sempre que os documentos forem revisados, todos os usuários verão automaticamente uma tela de confirmação na próxima vez que abrirem o app, com o título **"Atualizamos nossos documentos"**, antes de poder continuar usando a plataforma. O histórico completo de aceites anteriores é preservado permanentemente. Novos usuários continuam vendo a tela de boas-vindas com os documentos na primeira entrada

---

## v7.59.0 — Maio 2026

- **Nosso Condomínio — disponível no plano Básico:** o módulo Nosso Condomínio passou a ser acessível para todos os condomínios, independentemente do plano. As abas **Condôminos**, **Itens** e **Visitantes** estão disponíveis no plano Básico. A aba **Reservas** continua sendo exclusiva do plano Pro — no plano Básico, ela aparece com um cadeado e opção de upgrade
- **Compras e Serviços — visualização de Documentos e Anexos no plano Básico:** síndicos no plano Básico passam a visualizar a seção "Documentos e Anexos por fase" nas compras, mas o botão de upload é substituído por um indicador de plano Pro. Para fazer upload de arquivos por fase, é necessário o plano Pro
- **Minha Área — exportação CSV disponível para todos os planos:** o botão "Exportar CSV" do Extrato da Unidade estava disponível para todos e permanece assim. O botão "Exportar PDF" é exclusivo do plano Pro e agora exibe claramente o cadeado e uma mensagem explicativa ao passar o mouse
- **Dashboard — indicação de funcionalidade Pro para síndico no plano Básico:** o card "Últimas Notificações" no Dashboard passa a exibir um banner de apresentação da funcionalidade ("Envie notificações por e-mail para seus condôminos. Disponível no plano Pro.") em vez de aparecer vazio para síndicos no plano Básico
- **Mensagens de upgrade personalizadas por perfil:** as mensagens exibidas ao tentar usar funcionalidades Pro passam a levar em conta quem está vendo. Síndicos veem uma chamada para ação direta em Configurações; condôminos e porteiros veem uma orientação para solicitar ao síndico o upgrade do plano

---

## v7.58.0 — Maio 2026

- **Notificação extrajudicial para inadimplentes — disponível no plano Básico:** a funcionalidade de emitir notificações extrajudiciais para condôminos em atraso, anteriormente exclusiva do plano Pro, passou a estar disponível para todos os planos. Síndicos no plano Básico agora podem usar os botões "Notificar" e "Notificar em lote" na aba Inadimplência normalmente

---

## v7.56.0 — Maio 2026

- **Documentação atualizada:** todos os módulos da documentação pública receberam capturas de tela renovadas (1920×1080). Correções de texto em Configurações (7 abas), Relatórios (aba "Compras e Serviços"), Minha Área (seção "Meus acordos" com screenshots reais, hub atualizado), Financeiro (importação de retorno CNAB400 e lançamento em lote) e Navegação (tabela de módulos por perfil)
- **Importação de retorno CNAB400 *(síndico — plano Pro)*:** o síndico pode agora importar o arquivo de retorno CNAB400 (.ret) gerado pelo Banco Inter após o processamento dos boletos. O wizard de 4 etapas (Upload → Pré-visualização → Confirmação → Resultado) analisa o arquivo, identifica os boletos liquidados (código de ocorrência 06) e busca os lançamentos correspondentes no sistema por dois critérios: **nosso número** (quando a remessa foi previamente importada) ou **CPF do pagador** (fallback automático para conciliação sem remessa). Os lançamentos encontrados são marcados como pagos automaticamente; os não encontrados são listados para revisão manual

---

## v7.55.4 — Maio 2026

- **Correção — tela branca em Minha Área (Rules of Hooks):** ao abrir Minha Área em determinadas condições, o app exibia tela branca com o erro interno do React #310. A causa era a declaração de `useMemo` após returns condicionais no componente `NegociarDividaSection`, violando as Rules of Hooks. Corrigido reorganizando os hooks para que sejam sempre chamados na mesma ordem, independentemente das condições de renderização

---

## v7.55.3 — Maio 2026

- **Correção — visibilidade de acordos por condômino:** as políticas de segurança (RLS) das tabelas `agreements`, `agreement_entries` e `agreement_installments` foram corrigidas para que cada condômino visualize exclusivamente os acordos vinculados à sua própria unidade

---

## v7.55.2 — Maio 2026

- **Configurações → Cobranças & Acordos — layout em duas colunas:** em telas grandes, a aba foi reorganizada em duas colunas: configurações de cobrança automática à esquerda e parâmetros de acordo self-service à direita, facilitando a leitura e o acesso simultâneo às duas seções

---

## v7.55.1 — Maio 2026

- **Correção — RPC `create_agreement`:** geração do código de referência do acordo falhava por ausência da extensão `pgcrypto` no banco. Corrigido com implementação alternativa que não depende da extensão
- **Nova Edge Function `notify-agreement-created`:** ao confirmar um acordo self-service, todos os síndicos do condomínio recebem notificação por e-mail e Telegram com o nome do condômino, a unidade, o valor total acordado e o número de parcelas

---

## v7.55.0 — Maio 2026

- **Minha Área — Negociar dívida *(plano Pro)*:** condôminos com lançamentos de inadimplência vencidos podem iniciar um acordo de parcelamento diretamente pelo app, sem precisar contatar o síndico. A seção **Negociar dívida** aparece automaticamente em Minha Área quando há débitos elegíveis na unidade. O fluxo permite selecionar quais lançamentos incluir no acordo (tabela com checkboxes), visualizar o cálculo automático de multa e juros de mora com base nos parâmetros configurados pelo síndico, escolher o número de parcelas (opções abaixo do valor mínimo por parcela ficam desabilitadas), conferir o resumo financeiro completo (dívida selecionada, multa, juros estimados, total acordado e valor por parcela) e confirmar o acordo após aceitar o aviso legal de reconhecimento da dívida. Ao confirmar, o síndico recebe notificação por e-mail e Telegram
- **Minha Área — Meus acordos:** nova seção em Minha Área exibe os acordos existentes da unidade em cards de leitura, com opção de download do PDF de cada acordo. Os botões de cancelar e marcar pago não são exibidos para o condômino — essas ações são exclusivas do síndico no módulo Financeiro
- **Configurações → Cobranças & Acordos — Parâmetros de Acordo Self-Service *(plano Pro)*:** a aba Cobranças foi renomeada para **Cobranças & Acordos** e recebeu uma nova seção para configurar as condições dos acordos iniciados pelos condôminos: multa sobre o débito (%), juros de mora mensais (%), máximo de parcelas e valor mínimo por parcela

---

## v7.52.0 — Maio 2026

- **Configurações → Cobranças — seletor de mês ao gerar cobranças manualmente *(síndico)*:** o botão **Gerar agora** na aba Cobranças agora abre um diálogo de confirmação com três opções antes de disparar a geração: **Mês atual** (padrão), **Próximo mês** e **Escolher mês** (seletor de mês livre). O mês escolhido define tanto a competência quanto a data de vencimento dos lançamentos gerados, substituindo o cálculo automático. A idempotência é preservada: se já existirem cobranças daquela categoria para o mês selecionado, a ação é ignorada silenciosamente

---

## v7.51.0 — Maio 2026

- **Financeiro — coluna Competência ordenável:** a coluna **Competência** na tabela de lançamentos do Financeiro passou a ser ordenável por clique no cabeçalho, seguindo o mesmo padrão das demais colunas ordenáveis do módulo
- **Configurações — reordenação das abas:** as abas do módulo de Configurações foram reordenadas para: **Condomínio → Condôminos → Unidades → Cobranças → Categorias → Contas Bancárias → Notificações**
- **Configurações → Condôminos — cabeçalhos ordenáveis:** os cabeçalhos da tabela de condôminos (aba Condôminos em Configurações) agora permitem ordenar a lista por coluna ao clicar, seguindo o mesmo padrão dos demais módulos

---

## v7.50.0 — Maio 2026

- **Configurações → Unidades — configuração de taxas em lote *(síndico)*:** a aba Unidades ganhou recursos para editar a taxa mensal de várias unidades de uma só vez, sem precisar clicar em cada uma individualmente. Um filtro rápido acima da tabela — botões **Todas / Sem taxa / Com taxa** — permite focar nas unidades de interesse; trocar o filtro limpa automaticamente a seleção. Cada linha passou a ter um checkbox para seleção individual; o checkbox no cabeçalho da tabela seleciona ou deseleciona todas as linhas visíveis (com indicação visual de seleção parcial). Ao marcar ao menos uma unidade, surge a **barra de ação em lote** com dois modos: **Taxa fixa** — define o mesmo valor (R$) para todas as unidades selecionadas, com aviso em destaque quando o valor informado for zero (a taxa será removida dessas unidades); e **Reajuste %** — aplica um percentual de aumento ou desconto sobre a taxa atual de cada unidade selecionada (percentuais negativos representam desconto; unidades sem taxa configurada são automaticamente ignoradas). Antes de confirmar, um diálogo de confirmação exibe uma prévia das alterações, incluindo exemplos de cálculo no modo reajuste e a lista de unidades que serão ignoradas. A edição individual por janela flutuante segue disponível normalmente

---

## v7.49.0 — Maio 2026

- **Configurações — Geração automática de cobranças mensais *(síndico)*:** nova aba **Cobranças** em Configurações (ao lado de Unidades, exclusiva para síndicos). O síndico configura a categoria de cobrança mensal, o dia de vencimento preferencial (1 a 31), com quantos dias de antecedência deseja receber um aviso, e se o sistema deve gerar os lançamentos automaticamente ou apenas notificá-lo para gerar manualmente. Uma opção adicional controla se os condôminos recebem notificação quando as cobranças são geradas. Em meses com menos dias que o dia configurado (ex: dia 31 em fevereiro), o vencimento é ajustado automaticamente para o último dia do mês. O sistema verifica diariamente se as cobranças do mês já foram geradas antes de agir — nunca gera cobranças duplicadas para o mesmo mês. O síndico também pode acionar a geração manualmente a qualquer momento pelo botão disponível na aba

---

## v7.48.4 — Maio 2026

- **Correção — adição de condômino falhava em unidades com responsável cadastrado:** ao adicionar um condômino a qualquer unidade que já possuía um responsável, a operação retornava "Cada unidade deve ter exatamente um condômino responsável ativo" e o cadastro não era concluído. A causa era o trigger de inadimplência, que exige exatamente um responsável por unidade e verificava todas as unidades do condomínio após qualquer alteração. A correção adicionou uma verificação prévia nas funções de adição direta e importação em lote: o sistema consulta se a unidade já tem responsável antes de gravar, e define o papel do novo membro de acordo — responsável apenas se a unidade ainda não tiver um. A correção de dados foi aplicada ao condomínio Residencial TESTE, onde a unidade 103 havia acumulado dois responsáveis durante testes

---

## v7.48.3 — Maio 2026

- **Correção — erro ao adicionar condômino já cadastrado em outro condomínio:** ao tentar adicionar (via formulário direto ou importação de planilha) um e-mail que já existia em outro condomínio, o sistema retornava "Erro ao buscar usuário" e o cadastro não era concluído. A causa era uma limitação da API administrativa do Supabase no ambiente da plataforma. A solução migrou a busca de usuários para uma abordagem nativa: o e-mail passa a ser armazenado diretamente na tabela de perfis e a busca é feita por lá, eliminando a dependência da API problemática. Usuários com conta Google ou que trocar de e-mail têm o perfil sincronizado automaticamente

---

## v7.48.2 — Maio 2026

- **Autenticação — correção de logout ao recarregar a página:** ao pressionar F5 / Ctrl+R em qualquer módulo protegido, o app redirecionava para a tela de login em vez de restaurar a sessão. Causa: condição de corrida entre `onAuthStateChange` e `getSession()` no contexto de autenticação — em determinadas situações, o estado de loading era encerrado antes da sessão ser rehidratada. Corrigido eliminando a chamada redundante a `getSession()` e dependendo exclusivamente do evento `INITIAL_SESSION` disparado pelo `onAuthStateChange` do Supabase na montagem do app, que já carrega a sessão corretamente

---

## v7.48.1 — Maio 2026

- **Minha Área — correção de layout no Extrato da Unidade:** a página do extrato estava sem o padding interno padrão dos módulos do app, fazendo o conteúdo encostar nas bordas da área principal. Corrigido para seguir o mesmo padrão visual dos demais módulos

---

## v7.48.0 — Maio 2026

- **Financeiro — Melhorias na importação de lançamentos:** três refinamentos no wizard de importação em lote. (1) **Match de categoria tolerante a acentos:** o sistema agora normaliza nomes de categoria removendo acentos e espaços duplos antes de comparar, resolvendo erros como "Administraçao" vs "Administração". (2) **Categoria opcional:** se o nome da categoria não for encontrado no cadastro, a linha é importada com categoria em branco e o preview exibe um badge âmbar de aviso (⚠) em vez de rejeitar a linha com erro; se o campo vier vazio na planilha, é silenciosamente aceito. (3) **Auto-preenchimento de competência:** quando a coluna Competência estiver em branco, o sistema deriva automaticamente o mês/ano a partir da data de vencimento e exibe o valor com a marcação "(auto)" na tabela de preview, informando o usuário sem bloquear a importação

---

## v7.47.0 — Maio 2026

- **Financeiro — Lançamento em lote por unidade:** novo botão "Lançamento em lote" na página Financeiro (exclusivo para síndicos) abre um formulário lateral. O síndico seleciona a categoria (entre as categorias de cobrança por unidade), preenche descrição — com suporte ao placeholder `{unidade}` para personalizar automaticamente por unidade —, vencimento, competência e conta bancária. A tabela de unidades exibe todas as unidades ativas do condomínio com os valores pré-preenchidos a partir da configuração de taxa mensal (aba Unidades em Configurações); unidades sem taxa configurada usam o valor padrão informado no formulário; todos os valores são ajustáveis individualmente antes de confirmar. Ao criar, o sistema gera um lançamento por unidade selecionada via RPC `bulk_create_financial_entries`, agrupados sob um `entry_batch_id` único. Na listagem do Financeiro, lançamentos criados em lote exibem o badge **Lote** clicável, que abre um painel mostrando todos os lançamentos do lote com opção de **Cancelar lote inteiro** (remove todos com soft delete após confirmação)

---

## v7.46.0 — Maio 2026

- **Configurações — Aba Unidades:** nova aba exclusiva para síndicos em Configurações. Exibe a lista de todas as unidades ativas do condomínio (derivada dos condôminos cadastrados) com a taxa mensal configurada por unidade. O síndico pode definir ou editar o valor da taxa de cada unidade individualmente. O valor configurado aqui será usado como padrão no lançamento em lote por unidade (FIN-05)

---

## v7.45.0 — Maio 2026

- **Financeiro — Importação de lançamentos em lote:** novo botão "Importar lançamentos" na página Financeiro abre um wizard de 4 etapas. Na etapa Modelo, o síndico baixa um template XLSX com as 15 colunas suportadas e uma planilha de Referências com as categorias e contas bancárias disponíveis para consulta. Na etapa Upload, o arquivo (XLSX ou CSV, até 500 linhas) é carregado com drag-and-drop; o síndico pode indicar uma conta bancária padrão para as linhas sem conta preenchida. Na etapa Pré-visualização, o sistema valida cada linha via Edge Function e exibe o status de cada uma: válida, possível duplicata, duplicata confirmada (será ignorada) ou erro com a descrição do problema. A importação efetiva só ocorre após confirmação. O relatório final mostra quantos lançamentos foram importados, quais erros adicionais ocorreram e quais duplicatas foram ignoradas. A deduplicação é feita pelo campo `referencia_externa`: se preenchido e já existente no condomínio, a linha é ignorada silenciosamente. Colunas do template: tipo, descrição, valor, vencimento, competência, data de pagamento, unidade, categoria, conta bancária, referência externa, multa, juros, desconto, abatimento, observações

---

## v7.44.0 — Maio 2026

- **Financeiro — campo Competência:** os lançamentos financeiros passam a ter o campo **Competência** (mês/ano de referência), independente da data de vencimento. No formulário de novo/editar lançamento, o campo Competência é preenchido automaticamente com o mês de vencimento e marcado com asterisco quando a categoria é de inadimplência (campo obrigatório nesse caso). A coluna Competência foi adicionada à tabela de lançamentos na visualização desktop. A migração de banco inclui ainda as colunas `multa`, `juros`, `desconto` e `abatimento` (valores adicionais por lançamento) e `referencia_externa` (chave de deduplicação para importações)

---

## v7.43.0 — Maio 2026

- **Minha Área — identificação do responsável pela unidade:** a página do Extrato da Unidade passa a exibir, acima dos cartões de resumo, o nome completo e o CPF do condômino designado como responsável pela unidade. O mesmo bloco de identificação foi adicionado ao PDF exportado, posicionado entre o cabeçalho e a tabela de totais. Se o responsável não tiver CPF cadastrado, o campo é omitido sem afetar o restante do documento. Útil para uso em declarações de imposto de renda e como comprovante formal de pagamentos

- **Sidebar e menu mobile — ícone da Minha Área:** o ícone do item "Minha Área" foi atualizado para `UserCircle`, diferenciando visualmente o espaço pessoal do condômino do Dashboard gerencial, que mantém o ícone original

---

## v7.42.0 — Maio 2026

- **Extrato da Unidade — exportação em PDF:** além do CSV já disponível, o Extrato da Unidade passa a oferecer exportação em PDF. O documento inclui cabeçalho com o logo do V3RCondo, nome e CNPJ do condomínio e nome do síndico responsável pelas informações; uma tabela de resumo com os totais do período (total cobrado, total pago, em aberto e em atraso); e a listagem completa dos lançamentos com competência, descrição, valor, vencimento, data de pagamento e status. O PDF é gerado diretamente no app, sem armazenamento intermediário

---

## v7.41.2 — Maio 2026

- **Minha Área — correção de layout e navegação:** três ajustes no módulo lançado em v7.41: (1) o item "Dashboard" voltou para a primeira posição na sidebar quando o usuário tem acesso a "Minha Área"; (2) o conteúdo da página principal de Minha Área passa a ocupar a largura completa, alinhado ao padrão dos demais módulos; (3) correção de guard que impedia síndicos de acessar a página em determinadas condições

---

## v7.41.1 — Maio 2026

- **Minha Área — acesso para síndicos:** síndicos que também são condôminos (moradores do condomínio) passam a ter acesso à Minha Área e ao Extrato da Unidade. Anteriormente o módulo era exclusivo para residentes

---

## v7.41 — Maio 2026

- **Minha Área — Hub de autoatendimento para condôminos:** nova seção exclusiva para residentes, acessível pela sidebar e pelo menu mobile. A página principal reúne os serviços disponíveis em cards: "Extrato da Unidade" (ativo) e "Solicitar Documentos" (em breve). Síndicos e porteiros não visualizam este módulo
- **Extrato Individual da Unidade:** condôminos acessam o histórico completo de lançamentos da sua unidade (taxas, cobranças extras e similares) com filtro por ano, quatro cartões de resumo (total cobrado, total pago, em aberto, em atraso) e tabela com status por lançamento. Exportação em CSV disponível diretamente na página

---

## v7.40 — Maio 2026

- **Assembleias — edital com múltiplos síndicos:** o edital de convocação passa a listar todos os síndicos ativos do condomínio na seção de assinatura, lado a lado, cada um com seu título. Anteriormente apenas o primeiro síndico cadastrado era exibido

---

## v7.39 — Maio 2026

- **Perfil — CPF obrigatório:** o campo CPF no Perfil passa a ter máscara automática (`###.###.###-##`) e validação pelo algoritmo MOD-11. O preenchimento é obrigatório ao salvar o perfil. Usuários que ainda não cadastraram o CPF veem um aviso em destaque no topo da página solicitando o preenchimento

---

## v7.38 — Maio 2026

- **PDFs Gotenberg — padronização do cabeçalho:** todas as Edge Functions que geram PDFs via Gotenberg passam a usar cabeçalho unificado — layout em `<table>` 100% de largura (logo à esquerda, nome e CNPJ do condomínio à direita), logo `V3RCondo-Logo-Horizontal.png` via URL padrão `assets.v3rcondo.com.br`, fundo branco sem `background-color` explícito e diretiva `print-color-adjust: exact` no CSS. Margens padronizadas em 0,79 in em todos os lados. A Edge Function `manage-assembly` (edital de assembleia) foi atualizada; `manage-delinquency-notice` já estava no padrão desde v7.37

---

## v7.37 — Maio 2026

- **Inadimplência — Notificação Extrajudicial *(plano Pro)*:** síndicos podem emitir notificações extrajudiciais diretamente pelo app, de forma individual ou em lote para múltiplas unidades. A aba Inadimplência foi redesenhada em dois níveis: unidades no topo, com os lançamentos vencidos exibidos ao expandir cada linha. Para cada unidade, o síndico seleciona os débitos a incluir, define o prazo para regularização (padrão 15 dias), adiciona observações opcionais e escolha o canal de envio. Três canais disponíveis: **E-mail** (PDF em anexo), **E-mail + Telegram** (e-mail com PDF e aviso no Telegram) e **Apenas baixar PDF** (gera o documento sem enviar nada ao condômino). O PDF inclui logo e dados do condomínio, dados do notificado com CPF (se cadastrado), tabela de débitos com vencimento e dias em atraso, prazo formal, cláusula legal e assinatura do síndico. Um código de referência de 8 caracteres é gerado por notificação. Todas as notificações ficam registradas no histórico da aba com opção de download individual do PDF. Notificações em lote compartilham um identificador de grupo para rastreamento

- **Inadimplência — responsável por unidade:** cada unidade passa a ter um condômino designado como **responsável** — o destinatário das notificações extrajudiciais. O síndico define o responsável na aba Inadimplência ou em Configurações → Condôminos. O sistema garante exatamente um responsável por unidade: ao designar um novo, o anterior é substituído automaticamente; ao remover um condômino responsável, é obrigatório transferir a responsabilidade antes de confirmar a remoção

---

## v7.36 — Maio 2026

- **Financeiro — Unidade nos lançamentos:** ao registrar um lançamento financeiro em uma categoria configurada para compor o cálculo de inadimplência (como "Taxa de Contribuição" ou "Taxa Extra"), o síndico agora informa qual unidade do condomínio é responsável pelo pagamento. Esse vínculo torna o relatório de inadimplência mais preciso e abre caminho para recursos futuros como notificações e cobranças por unidade
- **Configurações — Categorias de receita:** categorias do tipo receita passam a ter um toggle "Considerar no cálculo de inadimplência". O síndico pode ativar essa opção em qualquer categoria de receita — não apenas nas categorias padrão — adaptando o sistema às particularidades do condomínio
- **Inadimplência — melhorias no relatório:** a aba Inadimplência em Relatórios passa a exibir a coluna **Unidade** em cada lançamento vencido. O filtro de período é pré-selecionado automaticamente com o histórico completo disponível ao abrir a aba, eliminando a necessidade de configurar o período manualmente

---

## v7.35 — Maio 2026

- **Compras e Serviços — Status de pagamento nas despesas:** cada despesa registrada em uma compra agora exibe um badge de status — **Pago** (quando o pagamento foi registrado), **Vencido** (quando o prazo expirou sem quitação) ou **Pendente** (aguardando pagamento dentro do prazo). O mesmo padrão visual já existente no módulo Financeiro

---

## v7.34 — Maio 2026

- **Relatórios — Projeção Financeira (Forecast) *(plano Pro)*:** nova aba "Projeção" disponível para síndicos no plano Pro. Projeta o fluxo de caixa futuro do condomínio combinando duas fontes: recorrências ativas cadastradas e média histórica de lançamentos pagos por categoria. O síndico escolhe o horizonte de projeção (1 mês, 3 meses, 6 meses, 12 meses, até o final do semestre ou até o final do ano). A aba exibe três cartões de resumo (saldo atual, saldo projetado, variação), um gráfico de barras com receitas e despesas projetadas por mês e um gráfico de linha com a evolução do saldo acumulado. Se o saldo projetar valor negativo em algum mês, um banner de alerta indica o mês de risco. Exportação em PDF e XLSX disponível. Condomínios no plano Básico visualizam a aba com cadeado e opção de upgrade

---

## v7.33 — Maio 2026

- **Correção — geração de relatório em Compras e Serviços:** ao clicar em "Gerar relatório", a Edge Function retornava erro 500 impedindo a geração. Causa: a função `buildPurchaseReportPayload` nas Edge Functions `manage-purchase-report` e `get-purchase-report-data` selecionava a coluna `category` de `purchase_expenses`, removida na v7.5 e substituída por `financial_category_id`. Corrigido para usar o schema atual com agrupamento dinâmico por nome de categoria

---

## v7.32 — Maio 2026

- **Landing page atualizada:** cards de Financeiro e Relatórios revisados para refletir as novidades recentes. Tabela de planos ganha transferências entre contas no módulo Financeiro (Básico e Pro), fuso horário configurável nas Configurações (Básico e Pro), e nova seção Relatórios no plano Básico com Fluxo de Caixa, Gastos por Categoria, Inadimplência e Compras

---

## v7.31 — Maio 2026

- **Relatórios — acesso para condôminos:** o módulo de Relatórios agora está disponível para condôminos. As abas Fluxo de Caixa, Gastos por Categoria e Compras exibem os mesmos dados do síndico. A aba Inadimplência exibe um painel resumido com indicadores agregados (total de unidades, percentual de adimplentes e inadimplentes, valor total em aberto), sem identificar individualmente os inadimplentes

---

## v7.30 — Maio 2026

- **Correção — Relatórios, Fluxo de Caixa:** transferências entre contas não afetam mais os totais de receita e despesa exibidos no gráfico e no Resumo Mensal. Apenas lançamentos reais de receita e despesa são considerados nos cálculos
- **Financeiro — filtro por Transferência:** o filtro de Tipo na listagem de lançamentos passa a incluir a opção "Transferência", exibindo apenas lançamentos de transferência entre contas. Os filtros "Receita" e "Despesa" passam a excluir transferências automaticamente

---

## v7.29 — Maio 2026

- **Financeiro — Enriquecimento de transferências:** ao registrar uma transferência entre contas, é possível informar uma **categoria** (ex: Fundo de Reserva, Reserva para equipamentos) e anexar um **comprovante**. As categorias de transferência são gerenciadas em Configurações → Financeiro → Categorias. O comprovante fica disponível na listagem de lançamentos com download por link seguro

---

## v7.28 — Maio 2026

- **Financeiro — Transferências entre contas:** síndicos podem registrar transferências entre duas contas bancárias do mesmo condomínio. A operação é atômica: gera automaticamente um débito na conta de origem e um crédito na conta de destino. As transferências aparecem na listagem de lançamentos com um badge identificador e podem ser excluídas de forma atômica. Os totais de receita, despesa e os relatórios financeiros não são afetados pelas transferências

---

## v7.27 — Maio 2026

- **Painel Admin — Comunicados da Plataforma:** super-admins podem agora enviar
  comunicados para todos os usuários ativos da plataforma diretamente pelo painel
  admin. O comunicado é entregue por e-mail (com o template visual V3RCondo) e
  por Telegram para quem tem o bot conectado. A nova aba **Comunicados** exibe
  um formulário com título e corpo da mensagem, confirmação antes do envio e
  histórico de todos os comunicados já enviados com data, título e número de
  destinatários

---

## v7.26.1 — Maio 2026

- **Correção — botão "Lembrete" em Condôminos:** ao clicar em "Lembrete" na lista
  de condôminos em Configurações, o app retornava "Erro ao enviar lembrete". Causa:
  variável interna da Edge Function `get-incomplete-profiles` referenciada antes de
  sua declaração na action `send_single_reminder` (erro de inicialização). Corrigido

---

## v7.26 — Maio 2026

- **Configurações — fuso horário por condomínio:** síndicos podem agora configurar o
  fuso horário do condomínio diretamente na aba **Condomínio** em Configurações. O
  padrão é Brasília (UTC−3). A configuração afeta como datas e horários são exibidos
  em todo o aplicativo — Dashboard, Financeiro, Tarefas, Assembleias, Compras e
  Serviços e Fale com o Síndico. Quatorze fusos brasileiros disponíveis, de Fernando
  de Noronha (UTC−2) a Rio Branco (UTC−5)

---

## v7.25 — Maio 2026

- **Documentação — screenshots em todos os módulos:** a documentação do usuário
  foi atualizada com capturas de tela reais do aplicativo em todos os módulos —
  Login, Sidebar, Dashboard, Financeiro, Fornecedores, Tarefas, Compras e
  Serviços, Notificações, Documentos, Mural, Fale com o Síndico, Nosso
  Condomínio, Assembleias, Relatórios, Configurações e Perfil. As imagens
  mostram o app em sua versão atual e estão inseridas nos pontos mais relevantes
  de cada página, ao lado do texto que descreve cada funcionalidade

- **Correção — login via e-mail/senha não carregava o condomínio:** ao fazer
  login digitando e-mail e senha, o dashboard abria sem nenhum condomínio
  selecionado, exibindo "Selecione um condomínio" e todos os dados zerados —
  como se fosse um usuário novo. O botão "Trocar" funcionava normalmente,
  mas a seleção automática não ocorria. A causa era uma condição na lógica
  de inicialização do contexto que só auto-selecionava o condomínio quando
  o usuário tinha exatamente um vínculo ativo; com dois ou mais condomínios
  e sem seleção salva no navegador, nada era escolhido. Corrigido: agora o
  primeiro condomínio ativo é selecionado automaticamente sempre que não
  houver uma seleção salva válida, independentemente do método de login
  (e-mail/senha ou Google)

---

## v7.24 — Maio 2026

- **Compras e Serviços — botões de relatório corrigidos:** os botões de relatório
  de execução agora refletem corretamente o estado da compra. Anteriormente, botões
  apareciam em situações incorretas (ex: "Ver relatório publicado" em compras ainda
  em andamento). A partir desta versão, os botões seguem cinco estados precisos:
  - Compra não concluída → nenhum botão de relatório exibido
  - Concluída, sem relatório → **Gerar relatório** (habilitado)
  - Gerando → **Gerando...** (desabilitado, com indicador de progresso)
  - PDF disponível → **Visualizar rascunho** + **Publicar**
  - Publicado → **Ver relatório publicado**
- O botão **Publicar** agora distribui o relatório diretamente pela plataforma
  para os destinatários selecionados na geração (síndicos sempre; condôminos
  e/ou Conselho Fiscal conforme marcação)

---

## v7.23 — Maio 2026

- **Assembleias — botão "Encerrar assembleia" no rodapé:** o botão de encerramento
  da assembleia, que existia apenas no topo da página de condução, agora aparece
  também no rodapé da página. Em assembleias com muitos itens de pauta, o síndico
  não precisa mais rolar até o topo para encerrar — o botão está disponível em
  ambas as extremidades da página, com o mesmo comportamento e confirmação

---

## v7.22 — Maio 2026

- **Fale com o Síndico — tooltip no badge de mensagens não lidas:** o badge
  vermelho sobre o avatar no cabeçalho agora exibe um tooltip ao passar o mouse,
  informando a origem e a quantidade de mensagens não lidas:
  "1 mensagem não lida — Fale com o Síndico" ou
  "N mensagens não lidas — Fale com o Síndico". O badge só exibe o tooltip
  quando há ao menos uma mensagem não lida

- **Fale com o Síndico — filtros e arquivamento para condôminos:** a visão do
  condômino agora tem os mesmos recursos de organização disponíveis para o síndico:
  abas de filtro por status (**Todas / Abertas / Em andamento / Resolvidas /
  Canceladas**), toggle **Exibir arquivadas** para mostrar ou ocultar solicitações
  arquivadas, e botão **Arquivar / Desarquivar** em cada solicitação. O condômino
  continua vendo apenas as próprias solicitações

---

## v7.21 — Maio 2026

- **Cabeçalho da sidebar redesenhado:** a área superior da sidebar, que antes
  tinha fundo escuro (#1e2d2b) com logo branca, agora exibe fundo branco com a
  logo colorida na versão compacta ("Simples"). A logo está alinhada à esquerda,
  no mesmo alinhamento visual dos ícones do menu. Quando a sidebar é recolhida,
  a logo horizontal é substituída automaticamente pelo favicon colorido. A
  altura do cabeçalho da sidebar foi igualada à do cabeçalho principal. A borda
  lateral direita que separava os dois cabeçalhos foi removida

---

## v7.20 — Maio 2026

- **Edital de assembleia — processado integralmente pela plataforma:** a geração
  e o envio do edital de assembleia, antes dependentes do n8n, agora são
  realizados diretamente pela Edge Function `manage-assembly`. O Gotenberg gera
  o PDF (cabeçalho com logo, convocação formal, pauta numerada e assinatura do
  síndico), o arquivo é salvo no Storage privado e enviado por e-mail a todos
  os condôminos com o PDF em anexo. Telegram enviado em paralelo para quem tem
  o bot conectado

- **Notificação de tarefas vencidas:** Edge Function `check-task-due` criada —
  busca tarefas com prazo para hoje que ainda não estão concluídas e notifica
  os síndicos por e-mail e Telegram. Executa automaticamente todo dia às 07h50

- **Correção — Relatório mensal por IA:** fluxo do n8n `relatorio-mensal-manual`
  estava quebrado após atualização interna da plataforma. O fluxo foi corrigido:
  a lista de managers (nome, e-mail, Telegram) agora é obtida diretamente da EF
  `get-report-data`, e o PDF gerado é entregue como anexo no e-mail de envio

- **Correção — Download de relatórios:** arquivos de relatório enviados pela
  plataforma não podiam ser baixados no módulo Documentos (toast de erro ao
  clicar). Corrigido — download funciona normalmente para todos os tipos de
  arquivo

- **Telegram no relatório mensal:** após o envio do e-mail com o relatório,
  os síndicos com Telegram conectado recebem também uma mensagem no Telegram
  com o nome do condomínio e o período do relatório. Aplica-se tanto ao
  relatório gerado manualmente quanto ao automático mensal

---

## v7.19 — Maio 2026

- **Lembrete individual de cadastro — sem intermediário:** o botão "Lembrete"
  na lista de condôminos (Nosso Condomínio e Configurações) agora envia
  diretamente pela plataforma, sem passar pelo n8n. O e-mail chega com a lista
  de campos pendentes e botão "Completar meu cadastro"

---

## v7.18 — Maio 2026

- **E-mails de assinatura — sem intermediário:** notificações de pagamento
  confirmado, falha no pagamento e cancelamento de assinatura agora são enviadas
  diretamente pela plataforma ao processar os eventos do Stripe

- **Suspensão e reativação de condomínio:** ao suspender ou reativar um
  condomínio pelo painel admin, todos os síndicos do condomínio recebem e-mail
  e Telegram com o aviso — enviados diretamente pela plataforma

---

## v7.17 — Maio 2026

- **Notificações de reservas — sem intermediário:** todos os cinco eventos de
  reserva (solicitação pendente, aprovada, recusada, cancelada pelo condômino
  e cancelada pelo síndico) agora são processados diretamente pela plataforma.
  Cada evento envia e-mail + Telegram para o destinatário correto (síndico ou
  condômino) sem depender do n8n

---

## v7.16 — Maio 2026

- **Automações recorrentes — sem intermediário:** quatro crons migrados do n8n
  para a infraestrutura nativa da plataforma:
  - **Arquivamento de reservas:** reservas com mais de 30 dias são arquivadas
    automaticamente todo dia às 03h
  - **Lembrete de reservas:** condôminos com reserva aprovada para o dia
    seguinte recebem lembrete por e-mail e Telegram todo dia às 08h
  - **Lembrete de assembleia:** membros ativos recebem lembrete 7 dias e 1 dia
    antes de assembleias com edital publicado
  - **Lembrete de cadastro incompleto:** lembrete enviado em lote no dia 1 de
    cada mês para condôminos com cadastro incompleto há mais de 28 dias

---

## v7.15 — Maio 2026

- **Migração n8n → Edge Functions — Sprint 2D:** quatro fluxos de notificação
  migrados do n8n para a plataforma nativa:
  - **Cancelamento de assembleia:** ao cancelar uma assembleia cujo edital
    já foi publicado, todos os membros ativos recebem notificação por e-mail
    e Telegram diretamente pela plataforma, sem dependência do n8n
  - **Publicação da ata:** ao publicar a ata de uma assembleia, todos os
    membros recebem e-mail com botão de download (link válido por 7 dias) e
    mensagem no Telegram. Síndicos recebem também as notas de governança
    geradas pela IA no mesmo e-mail
  - **Publicação de relatório de compra:** ao publicar um relatório de obra,
    os destinatários selecionados (síndicos sempre; condôminos e/ou Conselho
    Fiscal conforme escolha no momento da geração) recebem e-mail com botão
    de download e Telegram
  - **Conexão Telegram — sem intermediário:** o bot @V3RCondoBot agora se
    conecta diretamente à plataforma ao receber o comando `/start`. O fluxo
    de vinculação (gerar link no app → abrir no Telegram → confirmar) continua
    idêntico para o usuário; internamente, o n8n foi removido do caminho

---

## v7.14 — Maio 2026

- **Fale com o Síndico — notificação ao síndico na nova solicitação:** ao abrir
  uma nova solicitação, o síndico agora recebe uma notificação por e-mail e
  Telegram com o nome do condômino, o assunto da solicitação e um botão direto
  para responder. Antes, esse envio dependia de um intermediário externo (n8n)
  que não estava sendo migrado
- **Fale com o Síndico — correção de notificações de mensagens:** notificações
  de novas mensagens em threads (síndico ↔ condômino) estavam sendo perdidas em
  produção devido a um problema de execução assíncrona. Corrigido para garantir
  entrega confiável de e-mail e Telegram

---

## v7.13 — Maio 2026

- **Migração n8n → Edge Functions — Sprint 2C:** três fluxos de notificação
  adicionais migrados do n8n para a plataforma nativa:
  - **Fale com o Síndico — nova mensagem:** ao enviar uma mensagem em uma
    solicitação, o destinatário (síndico ou condômino) recebe notificação por
    e-mail com o conteúdo da mensagem e botão "Ver conversa", além de mensagem
    no Telegram se conectado. Antes, o envio passava pelo n8n como intermediário
  - **Envio de notificação manual:** ao usar o módulo Notificações para enviar
    um aviso a condôminos (todos, síndicos, unidades específicas ou indivíduos),
    os envios de e-mail e Telegram agora são processados diretamente pela
    plataforma, sem dependência do n8n
  - **Lembrete de cadastro incompleto:** o lembrete automático para condôminos
    com telefone ou CPF não preenchidos agora é processado em lote pela própria
    plataforma — e-mail com a lista de campos pendentes, botão "Completar meu
    cadastro" e mensagem no Telegram se conectado

---

## v7.12 — Maio 2026

- **Migração n8n → Edge Functions — Sprint 2B:** dois novos fluxos de
  notificação migrados do n8n para a plataforma nativa:
  - **Aviso no mural:** ao publicar um novo aviso, todos os membros ativos
    recebem notificação por e-mail com o template V3RCondo e, se conectados
    ao Telegram, também por Telegram. Antes, o envio dependia de um
    intermediário externo (n8n)
  - **Novo documento:** ao fazer upload de um documento, os síndicos ativos
    recebem notificação por e-mail e Telegram. Antes, mesmo fluxo via n8n

---

## v7.11 — Maio 2026

- **Template de e-mail V3RCondo (Sprint 0 da migração):** todos os e-mails
  transacionais da plataforma passam a usar o novo template com identidade visual
  V3RCondo — cabeçalho branco com logo colorida, separador verde escuro, área de
  conteúdo e rodapé verde claro com link para o app. Botões de ação em âmbar com
  texto em verde escuro. O template é aplicado automaticamente por todas as
  notificações enviadas a partir desta versão

- **Migração de notificações — Sprint 2A:** três fluxos de e-mail migrados do
  n8n para Edge Functions nativas, eliminando a dependência do intermediário para
  esses eventos:
  - **Exclusão de conta:** managers dos condomínios afetados recebem e-mail com
    os dados do condômino, aviso sobre obrigações financeiras pendentes e botão
    de acesso ao módulo Financeiro
  - **Redefinição de senha:** e-mail com botão "Redefinir senha" e link de
    fallback enviado diretamente pela plataforma, sem intermediário n8n
  - **Inclusão de condômino:** e-mail de boas-vindas com nome do condomínio,
    papel atribuído, número de unidade e botão de acesso enviado diretamente

- **Correção — exclusão de conta:** ao clicar em "Excluir conta" e confirmar
  via digitação de e-mail, a operação retornava "ação desconhecida". A causa era
  um parâmetro enviado pela URL em vez do corpo da requisição — corrigido

---

## v7.10.1 — Maio 2026

- **Correção — Síndico pode criar reservas:** o botão **+ Nova reserva** agora
  aparece para o síndico na aba Reservas, além dos condôminos. Reservas criadas
  pelo síndico são aprovadas automaticamente (sem necessidade de aprovação
  manual) e geram notificação de confirmação por e-mail e Telegram normalmente

- **Correção — Fluxos n8n de notificação Telegram:** expressões dos nós
  Telegram corrigidas em 9 fluxos após a entrega do TG-02, garantindo que
  `telegram_chat_id`, nomes e conteúdo das mensagens sejam referenciados
  corretamente em todos os cenários (reservas, assembleias, relatórios de
  compras, lembretes de cadastro e Fale com o Síndico)

---

## v7.10 — Maio 2026

- **Notificações via Telegram (TG-01 + TG-02) *(Básico e Pro)*:** integração
  completa com o Telegram. Cada usuário pode conectar sua conta ao bot
  **@V3RCondoBot** diretamente na página de Perfil — basta clicar em
  "Conectar Telegram", abrir o link que aparece e enviar `/start` no bot.
  A conexão é confirmada instantaneamente com uma mensagem de boas-vindas.
  Para desconectar, clique em "Desconectar" e confirme

- A partir da conexão, o usuário passa a receber **notificações no Telegram
  em paralelo ao e-mail** para os principais eventos do condomínio: reservas
  (solicitação, aprovação, recusa, cancelamento), respostas no Fale com o
  Síndico, avisos do mural, documentos publicados, notificações manuais,
  assembleias (edital, ata, cancelamento), relatórios de compras e lembretes
  de cadastro incompleto. As notificações chegam apenas se o usuário tiver
  o Telegram conectado — quem não conectou não recebe nem é afetado

---

## v7.9.1 — Maio 2026

- **Correção — modal de conclusão em Compras e Serviços:** o modal pós-conclusão
  que abre automaticamente ao marcar uma compra como "Concluída" agora funciona
  também na página de listagem (`/orcamentos`), tanto ao criar uma compra já
  com esse status quanto ao editar uma existente. Anteriormente o modal só
  abria na página de detalhe da compra

- **Landing page — atualização de conteúdo:** cards de funcionalidades e seção
  de planos atualizados para refletir o estado atual do produto. Os cards de
  planos foram reorganizados por módulo (Financeiro, Fornecedores, Compras e
  Serviços, Tarefas, etc.), tornando a comparação entre Básico e Pro mais clara
  e completa. A tabela comparativa redundante abaixo dos cards foi removida

---

## v7.9 — Maio 2026

- **Fale com o Síndico — Anexos (FS-02) *(plano Pro)*:** suporte a anexos em
  dois pontos do módulo. Na abertura de solicitações: campo de upload abaixo
  da descrição, com previews e remoção antes de enviar. Nas mensagens da
  thread: ícone de clipe ao lado do input, até 5 arquivos por envio (máximo
  5 MB cada). Imagens são exibidas como miniaturas clicáveis com lightbox;
  demais tipos aparecem como chips com ícone e nome, abrindo em nova aba via
  URL assinada. Extensões executáveis bloqueadas. Os arquivos da solicitação
  inicial ficam visíveis no card de detalhes no topo da thread

---

## v7.8 — Maio 2026

- **Fale com o Síndico — Thread de mensagens (FS-01) *(plano Pro)*:** cada
  solicitação agora tem uma conversa bidirecional estilo ticket de suporte.
  O botão **Ver conversa** na lista de solicitações abre uma página dedicada
  com o histórico completo de mensagens, identificação visual de cada lado
  (condômino à esquerda, síndico à direita) e campo de resposta. A cada nova
  mensagem, o outro lado recebe uma notificação por e-mail. Um badge vermelho
  sobre o avatar no cabeçalho indica mensagens não lidas em qualquer
  solicitação do condomínio, com atualização em tempo real. No plano Básico,
  o botão "Ver conversa" está visível mas bloqueado com indicação de upgrade

---

## v7.7 — Abril 2026

- **Configurações — Categorias em sub-abas (CFG-02):** a aba Categorias,
  que antes exibia todas as seções empilhadas em uma página longa, foi
  reorganizada em 7 sub-abas: **Financeiro**, **Tarefas**,
  **Compras e Serviços**, **Documentos**, **Mural**, **Fornecedores** e
  **Itens**. Cada sub-aba exibe apenas as categorias do seu módulo.
  O agrupamento interno de Financeiro (Receita / Despesa / Ambos) e a regra
  de não-exclusão das categorias padrão de Itens (Pet, Veículo, Vaga de
  garagem) foram preservados integralmente

---

## v7.6 — Abril 2026

- **Parceiros do Condomínio (CFG-01):** nova seção na aba Condomínio de
  Configurações para cadastro de contatos institucionais fixos do condomínio.
  Tipos disponíveis: Contador / Escritório Contábil, Advogado / Escritório
  Jurídico, Administradora, Segurança, Empresa de Elevadores, Bombeiros / AVCB,
  Limpeza e Conservação, Zeladoria e Outro (com rótulo personalizado). Cada
  parceiro pode ter empresa, nome do contato, CNPJ, telefone, e-mail e
  observações. Edição e exclusão via drawer lateral com confirmação

- **Card "Seu Plano" compactado:** a lista de funcionalidades com ícones de
  check foi removida do card, que agora exibe apenas o plano ativo, status do
  pagamento, data da próxima cobrança e o botão de gerenciar assinatura —
  liberando espaço para a nova seção de Parceiros

---

## v7.5 — Maio 2026

- **Fix — modal pós-conclusão em Compras e Serviços:** modal não abria
  automaticamente ao salvar compra como Concluída — causa era closure frágil
  sobre `request.status` no callback do mutate. Corrigido capturando
  `previousStatus` antes do mutate em `QuoteDetail.tsx`. Observações
  digitadas no drawer agora também pré-preenchem o modal sem depender
  de refetch

- **Fix — filtro de compras no Relatório Mensal por IA:** `fetchPurchases`
  em `get-report-data` incluía apenas compras criadas dentro do período do
  relatório, excluindo obras iniciadas antes. Filtro migrado do PostgREST
  para JavaScript — relatório agora inclui todas as compras ativas no
  período (criadas antes ou durante, não concluídas nem canceladas antes do
  início). Coluna `planned_start_date` adicionada à tabela `service_requests`

- **Fix — categoria de despesas em Compras e Serviços:** campo `category`
  com valores fixos (`material` / `mao_de_obra` / `outros`) substituído por
  `financial_category_id` (FK para `financial_categories`) com backfill dos
  registros existentes via `financial_entry_id`. Despesas agora usam as
  mesmas categorias financeiras do condomínio, eliminando inconsistência com
  os lançamentos em `financial_entries`. Edição de despesa existente
  implementada — anteriormente só era possível criar ou excluir

- **Relatório Mensal por IA — melhorias em Compras e Serviços:**
  - `get-report-data` expandida: cada item de `compras.lista` agora inclui
    array `despesas[]` com lançamentos individuais (descrição, categoria
    financeira, data, valor)
  - PDF reformulado: seção Compras e Serviços exibe um box por processo de
    compra, com metadados (estimado / valor final / despesas realizadas) e
    tabela de despesas individuais vinculadas
  - Prompt da IA atualizado: categorias exibidas dinamicamente a partir dos
    nomes reais das categorias financeiras; detalhamento por processo de
    compra incluído; bloco de instruções contextuais adicionado para evitar
    interpretação incorreta de despesas intencionais como irregulares

- **Configurações — sucessão de síndico:** síndico pode designar outro
  membro como Síndico (`role = 'manager'`) via edição na aba Condôminos em
  Configurações. Opção "Síndico" adicionada ao select de título. Ao promover
  outro membro, exibe confirmação informando que o condomínio terá mais de um
  síndico sem alterar o papel do síndico atual automaticamente. Ao rebaixar
  o próprio papel, exibe confirmação de perda de acesso de síndico

---

## v7.4 — Abril 2026

- **Módulo Visitantes (N4):**
  - Listas de visitantes por ocasião (data/horário), acessível via aba "Visitantes" em "Nosso Condomínio"
  - Adição de visitantes: um-a-um via botão "+ Adicionar visitante" ou importação em massa via planilha
  - Fluxo de criação: ao criar lista, modal de visitantes abre automaticamente
  - Importação de planilha: modelo XLSX para download, parser automático com validação de duplicatas
  - Tabelas: `visitor_lists`, `visitor_list_entries`; RLS por condomínio
  - Campos por visitante: Nome, Documento (CPF/CNPJ), Telefone, Horário de Chegada, Horário de Saída
  - Melhoria UX: botão "Importar planilha" removido da tela inicial e integrado ao modal de visitantes (junto com "+ Adicionar visitante")

- **Sprint Compras e Serviços — Entrega 3 (Relatório por IA):**
  - Relatório de execução gerado por DeepSeek V3 + Gotenberg,
    com estrutura: Resumo Executivo, Processo de Cotação,
    Execução Financeira e Considerações Finais
  - Modal de geração com campo "Observações e orientações para
    o relatório", checkbox "Enviar para condôminos" e checkbox
    "Enviar para Conselho Fiscal". Texto informativo: relatório
    enviado automaticamente para todos os síndicos
  - Campo "Observações para o relatório" disponível também no
    drawer de edição da compra (visível apenas quando status
    for Concluída) e pré-preenchido no modal de regeneração
  - Estados visuais: Gerando... (spinner) → Visualizar relatório
    + Regenerar → Ver relatório publicado
  - Visualização via URL assinada (válida 7 dias) em nova aba
  - Relatório publicado enviado por e-mail com link de download
    para condôminos e/ou Conselho Fiscal conforme seleção
  - Novas EFs: `get-purchase-report-data` (coleta dados da
    compra para a IA), `upload-purchase-report` (grava PDF no
    Storage e atualiza `report_file_id`), `manage-purchase-report`
    (actions: `request_report`, `publish_report`, `get_report_data`,
    `get_signed_url` — autenticação dupla JWT/N8N_API_KEY)
  - 2 novos fluxos n8n: `v3rcondo-purchase-report` (webhook →
    DeepSeek → Gotenberg → upload → e-mail aos managers com PDF)
    e `v3rcondo-purchase-report-publish` (webhook → URL assinada
    → e-mail com link para destinatários selecionados)
  - **Pendência:** modal pós-conclusão não abre automaticamente
    ao salvar compra como Concluída — em correção

- **Fix — botão "Gerar relatório da obra":** botão aparecia
  desabilitado mesmo com status 'done' e report_status nulo —
  condição de habilitação corrigida no frontend

- **Módulo renomeado:** "Compras" → "Compras e Serviços" em toda a interface (sidebar, cabeçalho, landing page). Nomes de arquivos, rotas e tabelas do banco não foram alterados

- **Sprint Compras e Serviços — Entrega 1:**
  - Bug restaurado: campo Status no formulário de criação e edição (valores: Planejada / Em Andamento / Concluída / Cancelada)
  - Novos campos no cabeçalho da compra: valor estimado (bloqueado após orçamento aprovado), valor final (sempre editável), data prevista de início, data de conclusão (preenchida automaticamente ao concluir se em branco)
  - Modal pós-conclusão com botão "Gerar relatório da obra" (desabilitado — disponível em breve)
  - Formulário de orçamento enriquecido: autocomplete de fornecedor existente, criação inline de novo fornecedor com upsert automático em `suppliers` (match por e-mail ou documento evita duplicatas; fornecedor soft-deleted é reativado)
  - Campos CPF/CNPJ e tipo (Pessoa Física/Jurídica) adicionados a fornecedores
  - Soft delete em `suppliers` — DELETE físico substituído por `deleted_at`
  - Seção "Documentos e Anexos" na página de detalhe da compra: upload múltiplo com filtro por fase (Planejamento / Execução / Conclusão / Geral), fase sugerida conforme status atual, URL assinada para download, soft delete
  - Nova tabela `purchase_attachments` com RLS para managers

- **Sprint Compras e Serviços — Entrega 2:**
  - Seção "Despesas" na página de detalhe da compra: lançamento de despesas por obra com categoria (Material / Mão de Obra / Outros), data da despesa, data de vencimento, toggle "Marcar como pago", comprovante e conta bancária (pré-selecionada a padrão)
  - Cada despesa cria automaticamente um lançamento em `financial_entries` (tipo expense, categoria lazy-created "Compras e Serviços")
  - Soft delete de despesa faz soft delete cascata no lançamento financeiro vinculado, com modal de confirmação
  - Total de despesas exibido no cabeçalho da compra com comparativo ao valor final quando disponível
  - Nova tabela `purchase_expenses` com RLS para managers
  - Hook `usePurchaseExpenses` + componente `PurchaseExpenseDrawer`

- **Fix — tipagem TypeScript:** `useBankAccounts`, `useFinancialEntries` e `useServiceRequests` corrigidos para usar `TablesUpdate<>` em vez de `Record<string, any>` — elimina erros de build introduzidos pela sprint

- **Fix — policies RLS de `purchase_attachments` e `suppliers`:** soft delete falhava por ausência de `condominium_id` no filtro de UPDATE. Corrigido em ambas as tabelas

---

## v7.3 — Abril 2026

- **Fix — relatório de inadimplência:** três correções acumuladas: filtro
  de período agora respeitado corretamente; categorias corrigidas para
  receita (`income`) — Taxa de Contribuição e Taxa Extra; colunas da
  tabela agora ordenáveis via `useSortableList` + `SortableTableHead`

- **Diretório de condôminos completo (N6):** evolução do N6-lite com
  novos campos de perfil (Instagram, LinkedIn, aniversário dia/mês,
  CPF obrigatório), consentimento granular campo a campo por condomínio
  (`directory_consent`), banner de cadastro incompleto e lembrete
  automático mensal para condôminos sem telefone ou CPF. Manager sempre
  vê e-mail, telefone e CPF; campos opcionais respeitam o consentimento
  do condômino para todos os papéis. Badge ✅/⚠️ de completude e botão
  "Lembrete" por linha em Nosso Condomínio e Configurações. RPC
  `get_condominium_directory` (SECURITY DEFINER) centraliza as regras
  de visibilidade

- **Sprint LGPD (L1–L4):**
  - **L1:** links "Termos de Uso · Política de Privacidade" no rodapé
    da sidebar e na página de login
  - **L2:** `TermsAcceptanceGate` — modal bloqueante para usuários sem
    aceite registrado; checkbox obrigatório no fluxo de primeiro acesso
    (`AcceptInvite.tsx`); campo `accepted_terms_at` em `profiles`
  - **L3:** botão "Exportar meus dados" em Perfil — XLSX com 3 abas
    (Perfil, Condomínios, Consentimentos) gerado client-side via SheetJS
  - **L4:** exclusão de conta com wizard de 3 etapas, bloqueio para
    manager único, aviso de obrigações financeiras persistentes,
    anonimização de perfil antes da exclusão no Auth, e-mail automático
    aos managers do condomínio

- **Novas Edge Functions:** `get-incomplete-profiles` (lista membros com
  cadastro incompleto + atualiza timestamp de lembrete; auth via Bearer
  N8N_API_KEY) e `delete-account` (check + execute; auth via JWT;
  anonimiza → inativa membros → hard delete consents → webhook →
  deleteUser, nessa ordem)

- **3 novos fluxos n8n:**
  - `v3rcondo-profile-reminder`: webhook manual disparado pelo síndico
    para lembrar um condômino específico de completar o cadastro
  - `v3rcondo-profile-reminder-cron`: cron mensal (dia 1, 09h) que
    busca todos os membros com cadastro incompleto há mais de 28 dias
    e envia lembrete automaticamente
  - `v3rcondo-account-deleted`: notifica managers dos condomínios
    quando um condômino exclui a própria conta

---

## v7.2 — Abril 2026

- **Módulo Assembleias — completo (A1+A2+A3):** ciclo completo de gestão de
  assembleias condominiais, do edital à ata publicada. Exclusivo plano Pro

- **Pré-assembleia (A1):** criação com título, tipo (Ordinária/Extraordinária),
  data/hora, local e configurações de lembrete. Montagem da pauta com itens
  de quatro tipos: Informativo, Votação, Discussão e Assunto Geral — com
  reordenação por setas. Upload de documentos adicionais com botão explícito
  e exclusão. Publicação do edital gera PDF via Gotenberg com template formal
  (cabeçalho, convocação, pauta numerada, assinatura do síndico), envia
  por e-mail para todos os condôminos com o PDF em anexo e dispara notificação
  interna no app. Cancelamento com notificação interna + e-mail para todos
  se edital já publicado. Botão de cancelamento disponível diretamente na
  listagem

- **Condução da assembleia (A2):** modal de abertura com presidente e
  secretário da mesa — toggle "Síndico presidiu" auto-preenche dados do
  perfil (nome, CPF, RG); campo livre para externos. Quórum com contagem
  de unidades, toggle atingido/não atingido, observações e aviso sobre
  verificação da convenção. Lista de presença gerada automaticamente com
  todos os membros ativos, marcados como presentes/presenciais por padrão —
  manager desmarca ausentes, altera modalidade (presencial/remoto) e edita
  CPF/RG inline (salvo via onBlur). Convidados externos com nome, papel,
  CPF e RG. Gestão da pauta em tempo real: status por item
  (pendente → em discussão → concluído), anotações do secretário por item
  (onBlur), formulário de deliberação inline para itens de votação concluídos
  (aclamação ou contagem com votos a favor/contra/abstenções, resultado e
  decisão tomada). Procurações com upload obrigatório do documento. Documentos
  da condução com seleção de tipo (transcrição, gravação, anotação, outro).
  Encerramento com confirmação

- **Ata por IA (A3):** popup pós-encerramento oferece geração da ata por IA.
  Campo de instruções adicionais pré-preenchido com prompt padrão editável.
  Geração assíncrona: n8n chama EF `get_assembly_data`, monta prompt completo
  com todos os dados da assembleia + instruções, envia ao DeepSeek V3,
  converte HTML para PDF via Gotenberg, faz upload via EF
  `upload-assembly-minutes` e atualiza `minutes_status='ready'`. PDF inclui
  ata formal com texto justificado, assinaturas do presidente/secretário/
  síndico sem repetição e anexo com lista de presença em nova página.
  Manager recebe e-mail com PDF em anexo e seção de itens de governança
  (tarefas sugeridas, prazos, comunicados recomendados). Três opções de
  revisão: Publicar / Regenerar com ajustes / Lançar ata própria.
  Publicação envia ata por e-mail a todos os condôminos com URL assinada
  para download, e e-mail especial ao síndico com governance_notes.
  Aviso sobre necessidade de registro em cartório exibido após publicação

- **5 fluxos n8n do módulo Assembleias:**
  - `v3rcondo-assembly-minutes`: recebe payload completo → monta prompt →
    DeepSeek V3 → HTML → Gotenberg → upload-assembly-minutes → e-mail ao
    manager com PDF em anexo e governance_notes. Merge de binário + JSON
    para viabilizar o anexo
  - `v3rcondo-assembly-edital`: HTML do edital → Gotenberg → manage-assembly-files
    (upload_edital) → e-mail com PDF em anexo para cada condômino (split)
  - `v3rcondo-assembly-publish`: get_signed_url da ata → e-mail com link de
    download para todos os condôminos; governance_notes exibido apenas para managers
  - `v3rcondo-assembly-cancelled`: e-mail de cancelamento para todos os condôminos
  - `v3rcondo-assembly-reminder`: cron diário às 8h → EF get_reminder_targets →
    e-mails de lembrete 7 dias e 1 dia antes da assembleia

- **Novas Edge Functions:**
  - `upload-assembly-minutes`: upload de PDF da ata via multipart/form-data →
    Storage + files + assembly_attachments + update assemblies
  - `manage-assembly-files`: dois modos — upload_edital (multipart) e
    get_signed_url (JSON) para geração de URLs assinadas de arquivos privados

- **Enriquecimento de perfil (Sprint-0):** campos `cpf`, `rg` e `profession`
  adicionados à tabela `profiles` (todos opcionais) e à tela de Perfil —
  pré-requisito para identificação formal nas atas de assembleia

- **Fix — sidebar mobile:** módulos "Nosso Condomínio" e "Assembleias" não
  apareciam em dispositivos móveis — componente de menu hambúrguer tinha lista
  separada que não havia sido atualizada com os novos módulos

- **Fix — tooltip na aba Reservas:** ícone "?" removido da aba Reservas em
  Nosso Condomínio, inconsistente com as demais abas do módulo

- **Fix — buildAssemblyPayload:** join via sintaxe `profiles:user_id(campos)`
  em `condominium_members` falhava silenciosamente por ausência de FK declarada.
  Corrigido com duas queries separadas em todas as funções afetadas
  (buildAssemblyPayload e openAssembly). Padrão documentado como regra #41

---

## v7.1 — Abril 2026

- **Módulo de Reservas (RC-01):** nova aba "Reservas" em Nosso Condomínio
  (ordem: Condôminos | Reservas | Itens). Permite reservar áreas comuns
  (churrasqueira, salão de festas, piscina) e itens emprestáveis (cortador de
  grama, enceradeira etc.). Recursos configuráveis com slots de horário por
  dia da semana (Manhã 08–12, Tarde 12–18, Noite 18–23, Dia inteiro para
  itens), capacidade máxima, regras de uso, taxa por uso, aprovação manual ou
  automática e limite de reservas simultâneas por condômino (padrão: 3).
  Anti-overbooking garantido por unique index no banco. Reservas com aprovação
  automática geram lançamento financeiro automaticamente (categoria "Reservas"
  lazy-created em `financial_categories`). Cancelamento faz soft delete do
  lançamento se não pago, ou avisa o síndico se já pago. Arquivamento manual
  e automático após 30 dias. Toggle lista/calendário com visão de
  disponibilidade mensal. Ordenação por coluna clicável na visão lista.
  Reservas pendentes exibidas no calendário do condômino em cinza com borda
  tracejada
- **Edge Function `manage-reservation`:** centraliza toda a lógica transacional
  de reservas (create, approve, reject, cancel, archive, bulk_archive,
  get_upcoming_reservations). JWT de usuário para ações mutantes;
  N8N_API_KEY para leitura e cron. Slots traduzidos para PT-BR via
  `SLOT_LABELS` antes de disparar webhooks. TODOs documentados para evolução
  futura: checkin, checkout, waitlist, recorrência, avaliação, pagamento
- **Fluxo n8n `v3rcondo-reservation`:** webhook único com 5 branches de
  e-mail — reserva pendente (síndico), aprovada, rejeitada, cancelada pelo
  condômino (síndico), cancelada pelo síndico (condômino)
- **Fluxo n8n `v3rcondo-reservation-reminder`:** cron diário às 08h envia
  lembrete 24h antes de cada reserva aprovada
- **Fluxo n8n `v3rcondo-reservation-archive`:** cron diário às 03h arquiva
  silenciosamente reservas com mais de 30 dias via EF bulk_archive
- **Categorias de Nosso Condomínio (CAT-01):** migradas da aba Categorias de
  Nosso Condomínio para Configurações → aba Categorias, seguindo o padrão dos
  demais módulos
- **Ordenação na aba Condôminos:** colunas ordenáveis com `useSortableList` +
  `SortableTableHead` na listagem de membros de Nosso Condomínio
- **N8-M01:** corpo da notificação (`message`) incluído no e-mail de
  notificações do fluxo `v3rcondo-notification-send`. `white-space: pre-line`
  preserva quebras de linha digitadas pelo manager

---

## v6.9 — Abril 2026

- **Fix — link de acesso inválido para novos condôminos:** corrigido bug no
  Path A da Edge Function `add-member-direct` onde `createUser` com
  `email_confirm: false` disparava e-mail de confirmação padrão do Supabase
  que invalidava o token do link de acesso enviado pelo n8n. Agora
  `email_confirm: true` suprime o e-mail automático e o link gerado usa
  `type=magiclink` consistente com o `verifyOtp` no frontend
- **Fix — segurança RLS em `condominium_members`:** policy "Invited users can
  join condominium" agora exige que o `role` inserido corresponda ao `role`
  definido no convite (`ci.role = condominium_members.role`), bloqueando
  escalação de privilégio por manipulação direta da API
- **Diretório de condôminos (N6-lite):** nova aba "Condôminos" no módulo
  Nosso Condomínio exibindo todos os membros ativos com nome, unidade e título
  visual. Visível para managers e residents. Toggle lista/grid com lista como
  padrão. Badges coloridos por título: Síndico/Subsíndico em roxo,
  Contador/Conselho Fiscal em azul, Condômino em verde. RPC
  `get_condominium_member_names` atualizada para retornar `role` e `title`

---

## v6.8 — Abril 2026

- **Módulo "Nosso Condomínio":** diretório compartilhado onde todos os
  moradores podem cadastrar e visualizar itens — pets, veículos, vagas de
  garagem e outros. Categorias configuráveis pelo síndico (padrão: Pet,
  Veículo, Vaga de garagem). Até 3 fotos por item com lightbox e navegação.
  Toggle lista/grid com lista como padrão. Filtros por categoria e unidade
  (exclusivo plano Pro)
- **Inventário de bens do condomínio:** síndico pode marcar itens como "bem do
  condomínio" (equipamentos, mobiliário etc.) — identificados com badge laranja
  e filtráveis pela opção "Condomínio" no filtro de unidade
- **Inclusão direta de condôminos:** síndico adiciona moradores sem fluxo de
  convite — preenche nome, e-mail, unidade e título; sistema cria o vínculo
  imediatamente e envia e-mail de boas-vindas com opção de definir senha ou
  entrar com Google
- **Importação de planilha de condôminos:** upload de XLSX/CSV com até 100
  condôminos por importação. Modelo disponível para download. Validação linha
  a linha com resumo de importados, ignorados e rejeitados
- **Bucket de arquivos privado:** arquivos do condomínio agora protegidos com
  URLs assinadas — acesso restrito a membros ativos. URLs legadas convertidas
  automaticamente
- **Tooltips na sidebar:** ícone `?` em todos os itens do menu com descrição
  do módulo ao passar o mouse
- **Fix — join request com duplicate key:** aprovação de solicitação de vínculo
  agora usa upsert, evitando erro ao aprovar usuário já membro
- **Fix — redirect pós-aceite:** aceite de link de acesso agora redireciona
  corretamente para o condomínio sem cair no onboarding
- **Landing page:** card "Nosso Condomínio" adicionado, Passo 2 atualizado
  ("Adicione os moradores"), tabela comparativa atualizada

---

## v6.7 — Abril 2026

- **Novos títulos/papéis:** Subsíndico (manager), Contador e Conselho Fiscal
  (resident) — campo `title` independente do `role`, apenas para identificação
  visual
- **Faixas de preço atualizadas:** Pro Pequeno até 10 unidades (R$ 49,90),
  Pro Médio 11-50 unidades (R$ 99,90), Pro Grande 51+ unidades (R$ 179,90).
  `plans.ts` como fonte única de verdade no frontend
- **Correções de segurança RLS:** upload de avatar restrito ao próprio usuário;
  restrição de escalada de privilégios em `user_roles`; restrição de papel em
  convites por residents; validação de role na aprovação de membros

---

## v6.6 — Abril 2026

- **Reenvio manual de link de acesso:** botão "Reenviar link" na lista de
  condôminos em Configurações, com loading individual e confirmação via toast
- **Reenvio automático de link de acesso:** fluxo n8n com cron diário às 9h
  reenvia automaticamente links não utilizados após 7 dias (uma única vez por
  membro)
- **Acesso para usuários já cadastrados:** síndico pode adicionar e-mails que
  já possuem conta no V3RCondo — o sistema gera um link de acesso direto via
  magiclink
- **Fluxo de aceite aprimorado:** usuários já cadastrados vinculados
  automaticamente ao condomínio ao clicar no link, sem precisar redefinir senha

---

## v6.5 — Abril 2026

- **Painel diário por e-mail (N8):** resumo diário com tarefas
  vencidas/hoje/próximos 3 dias, lançamentos com vencimento no dia,
  solicitações abertas e compras, enviado todo dia às 7h (exclusivo plano Pro)
- **Preferência de frequência:** seletor diário/semanal/desativado em
  Configurações
- **Segurança RLS:** upload de avatar restrito ao próprio usuário; privilege
  escalation em `user_roles` corrigido
- **Financeiro — card "Saldo Acumulado Projetado":** novo card exibindo saldo
  inicial das contas + lançamentos pagos anteriores ao mês atual + saldo
  projetado do mês
- **Financeiro — melhorias de UX:** recorrências ativas colapsadas por padrão;
  ordenação decrescente por vencimento; filtro com mês atual como padrão;
  coluna "Pago em" na listagem
- **Data de versão dinâmica:** lida do campo `versionDate` no `package.json`
- **Criar novo condomínio:** botão `＋` no cabeçalho + opção no modal de troca
  de condomínio

---

## v6.4 — Abril 2026

- **Tarefas recorrentes:** criação de séries de tarefas com recorrência diária,
  semanal, mensal ou anual — geração automática de todas as ocorrências ao
  salvar (exclusivo plano Pro)
- **Anexos em tarefas:** upload de até 5 arquivos por tarefa (máximo 10 MB
  cada), com visualização e remoção individual
- **Filtros no módulo de Tarefas:** filtros por período (mês atual como
  padrão), prioridade, status e categoria, com ordenação por prazo crescente
- **Badges e ícones nas tarefas:** ícone de recorrência e contador de anexos
  clicável nos cards e na listagem
- **Exclusão inteligente de recorrências:** modal com opções "Apenas esta" e
  "Esta e todas as futuras" ao excluir tarefa recorrente
- **Lembretes de tarefas por e-mail:** cron n8n diário às 8h com resumo de
  tarefas vencidas, com vencimento hoje e nos próximos 7 dias (exclusivo
  plano Pro)
- **Notificação interna de tarefas vencidas:** Edge Function `check-task-due`
  + pg_cron às 7h50 gera notificação no sino ao vencer uma tarefa
- **Toggle de lembretes:** preferência "Lembretes de tarefas por e-mail" em
  Configurações → Notificações
- **Bug fix — Relatório IA:** fluxo n8n agora filtra condomínios no plano free
  sem trial ativo, evitando geração e envio desnecessários
- **Edge Function `get-report-data`:** listagem de condomínios passa a retornar
  `plan_type`, `plan_status` e `trial_ends_at`

---

## v6.3 — Abril 2026

- **E-mails transacionais (M16):** fluxos automáticos de e-mail para
  boas-vindas, trial, pagamento confirmado, falha no pagamento e cancelamento
  de assinatura
- **Edge Function `get-billing-status`:** nova função para suporte aos crons
  de trial e inadimplência

---

## v6.2 — Abril 2026

- **Landing page comercial (M20):** nova página inicial com seções de
  funcionalidades, como funciona, planos comparativos, FAQ e footer
- Navbar com troca dinâmica de logo conforme scroll

---

## v6.1 — Abril 2026

- **Trial automático (M10):** novos condomínios recebem 30 dias de trial Pro
  ao criar o condomínio
- **Cron expiração trial (M11):** rebaixa planos com trial expirado
  automaticamente todo dia às 00h
- **Cron inadimplência (M12):** suspende condomínios com 30+ dias de
  inadimplência automaticamente todo dia às 01h

---

## v6.0 — Abril 2026

- **UI de Planos em Configurações (M8/M9):** card "Seu Plano" com badge,
  recursos, próxima cobrança e status do pagamento
- **Sheet de upgrade:** seletor de faixa de unidades com preço dinâmico e
  tabela comparativa Básico vs Pro
- **Botão "Gerenciar assinatura"** para condomínios Pro — abre o portal do
  cliente no Stripe

---

## v5.9 — Abril 2026

- **Feature flags por plano (M7):** recursos Pro bloqueados com cadeado no
  plano Básico
- Tarefas, recorrências, importação de extrato, notificações por e-mail,
  arquivos ilimitados, exportação PDF/XLSX, relatório IA e anexos em
  orçamentos agora requerem plano Pro
- Admin tem bypass total — nunca vê bloqueios

---

## v5.8 — Abril 2026

- **Portal do cliente Stripe (M6):** botão "Gerenciar assinatura" em
  Configurações

---

## v5.7 — Abril 2026

- **Stripe integrado em produção:** checkout, webhook, cupons habilitados
- Edge Functions `create-checkout-session` e `stripe-webhook`
- Primeiro pagamento processado com sucesso

---

## v5.6 — Abril 2026

- Admin pode criar condomínios pelo painel admin
- Unidades configuráveis por condomínio
- Links legais no rodapé da sidebar (Termos e Privacidade)
- Filtros de relatórios persistentes ao trocar de aba
- Reimportação de extrato bancário disponível na UI
- Combobox de busca no onboarding

---

## v5.5 — Abril 2026

- **Sprint 1 — Gestão de Papéis:** painel admin com métricas, lista de
  condomínios, suspensão/reativação e gestão de síndicos

---

## v5.4 — Abril 2026

- **Fale com o Síndico:** solicitações, status, arquivamento, notificação por
  e-mail, integração com Tarefas
- **Relatório Mensal com IA:** cron automático + geração manual, DeepSeek V3,
  Gotenberg

---

## v5.3 — Março 2026

- Exportação de relatórios em PDF e XLSX

---

## v5.2 — Março 2026

- Módulo de Relatórios: Fluxo de Caixa, Gastos por Categoria, Inadimplência
  e Compras

---

## v5.1 — Março 2026

- Logo do condomínio na sidebar
- Avatar do usuário na sidebar
- Formulário de sugestões na sidebar

---

## v5.0 — Março 2026

- Importação de extrato OFX/CSV com conciliação automática

---

## v4.9 — Março 2026

- Lançamentos recorrentes no módulo Financeiro
- Filtros avançados no Financeiro

---

## v4.8 — Março 2026

- Saldo inicial configurável por conta bancária

---

## v4.7 — Março 2026

- Múltiplas contas bancárias por condomínio

---

## v4.6 — Março 2026

- Cadastro e vínculo de condôminos por e-mail

---

## v4.5 — Março 2026

- Fluxo de onboarding completo: criar condomínio, solicitar vínculo, aceitar
  link de acesso

---

## v4.4 — Março 2026

- Mês/ano de referência nos documentos
- Edição de metadados de arquivos
- Suporte a arquivos ZIP

---

## v4.0 — Março 2026

- Landing page inicial

---

## v3.7 — Março 2026

- Login com Google (OAuth)

---

## v3.0 — Março 2026

- Notificações por e-mail via n8n

---

## v2.3 — Março 2026

- Identidade visual V3RCondo aplicada

---

## v1.5 — Março 2026

- Autenticação com Supabase integrada

---

## v1.0 — Março 2026

- Interface inicial completa (pré-banco de dados)
