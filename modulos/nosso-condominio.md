---
title: Nosso Condomínio
parent: Módulos
nav_order: 11
---

# Nosso Condomínio

O módulo "Nosso Condomínio" centraliza o que é compartilhado entre os moradores:
o diretório de condôminos, as reservas de áreas e itens emprestáveis, e o
catálogo de pets, veículos, vagas e bens do condomínio.

O módulo é organizado em quatro abas: **Condôminos**, **Reservas**, **Itens** e **Visitantes**.

{: .note }
> **Planos**
>
> As abas **Condôminos**, **Itens** e **Visitantes** estão disponíveis para todos
> os planos (Básico e Pro). A aba **Reservas** é exclusiva do plano Pro — no
> plano Básico, ela aparece na interface com um cadeado e a opção de fazer upgrade.

---

## Aba Condôminos

![Aba Condôminos — visão lista com badges de papel e indicadores de completude](/assets/screenshots/49-nosso-cond-condominos-lista.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

Diretório completo dos membros ativos do condomínio. As informações exibidas
variam conforme o papel do usuário e as preferências de privacidade de cada
membro.

### Campos sempre visíveis para todos
Nome, unidade, papel e título. Os badges indicam o papel de cada membro:

- **Síndico / Subsíndico** → roxo/lilás
- **Contador / Conselho Fiscal** → azul
- **Condômino** → verde

### Campos visíveis apenas para o síndico
E-mail, telefone e CPF são sempre exibidos ao síndico, independentemente
das preferências de privacidade do condômino. Esses dados são necessários
para comunicação e emissão de cobranças.

### Campos controlados pelo próprio condômino
Foto de perfil, Instagram, LinkedIn, profissão e aniversário (dia e mês)
são exibidos apenas se o condômino tiver habilitado a visibilidade em
**Perfil → Minha visibilidade no diretório**. Cada campo é controlado
individualmente.

### Badge de completude de cadastro (visão síndico)
Cada linha exibe um badge indicando se o cadastro do condômino está completo:

- ✅ — telefone e CPF preenchidos
- ⚠️ — telefone ou CPF ausentes

O síndico pode enviar um lembrete individual clicando no botão **Lembrete**
na linha do condômino. O tooltip exibe a data do último lembrete enviado.
O botão global **"Lembrar todos incompletos"** em Configurações → Condôminos
dispara o lembrete para todos os membros com cadastro incompleto de uma vez.

{: .note }
> **Lembrete automático**
>
> No dia 1 de cada mês, o sistema envia automaticamente um e-mail para
> condôminos com telefone ou CPF ausentes — desde que não tenha sido
> enviado um lembrete nos últimos 28 dias. O envio cessa automaticamente
> quando o cadastro estiver completo.

### Alternância de visualização
Use o toggle **lista/grid** no canto superior direito. As colunas na visão
lista são ordenáveis — clique no cabeçalho para ordenar. No modo grid, cada
card exibe foto (ou avatar com inicial), nome, unidade, título e os campos
habilitados pelo condômino.

![Aba Condôminos — visão grid com foto, nome, unidade e título de cada morador](/assets/screenshots/50-nosso-cond-condominos-grid.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

### Configurar minha visibilidade no diretório
Cada condômino controla o que aparece para os demais em
**Perfil → Minha visibilidade no diretório**. Os toggles disponíveis são:

| Campo | Visível por padrão |
|---|---|
| Foto de perfil | ✅ Sim |
| Telefone / WhatsApp | ❌ Não |
| E-mail | ❌ Não |
| Instagram | ❌ Não |
| LinkedIn | ❌ Não |
| Profissão | ❌ Não |
| Aniversário | ❌ Não |

Se o condomínio participar de múltiplos condomínios, as preferências são
configuradas separadamente para cada um.

---

## Aba Reservas *(plano Pro)*

{: .warning }
> **Plano Pro**
>
> A aba Reservas é exclusiva do plano Pro. No plano Básico, a aba aparece
> com um cadeado — clique para conhecer o plano Pro e fazer upgrade em
> Configurações.

Permite reservar áreas comuns (churrasqueira, salão de festas, piscina) e itens
emprestáveis do condomínio (cortador de grama, enceradeira etc.).

![Aba Reservas — visão calendário com disponibilidade mensal do recurso](/assets/screenshots/51-nosso-cond-reservas-calendario.png)

![Aba Reservas — visão lista com histórico de reservas e badges de status](/assets/screenshots/52-nosso-cond-reservas-lista.png)

### Visão do condômino

Use o toggle **Calendário / Lista** no canto superior direito para alternar
entre as visões.

**Visão calendário:** exibe a disponibilidade mensal do recurso selecionado.
Clique em um dia disponível para iniciar uma nova reserva.

**Visão lista:** exibe o histórico das suas reservas com badge de status.
Reservas arquivadas ficam ocultas por padrão — use o toggle
"Exibir arquivadas" para consultá-las.

#### Fazer uma reserva

Clique em **+ Nova reserva** ou em um dia disponível no calendário e siga
os passos:

1. **Recurso** — selecione a área ou item desejado. Cada card exibe capacidade,
   taxa (se houver) e se a reserva requer aprovação do síndico
2. **Data** — selecione a data no mini-calendário (respeitando a antecedência
   mínima e máxima configurada pelo síndico)
3. **Horários** — selecione um ou mais blocos disponíveis:
   - Manhã: 08:00–12:00
   - Tarde: 12:00–18:00
   - Noite: 18:00–23:00
   - Dia inteiro (para itens emprestáveis)
4. **Convidados** — informe o número de convidados e, opcionalmente, os nomes.
   A soma de moradores + convidados não pode ultrapassar a capacidade do espaço
5. **Regras de uso** — leia as normas e marque o checkbox de concordância
   (obrigatório para confirmar)
6. **Resumo** — confirme os detalhes e clique em **Confirmar reserva**

![Formulário de nova reserva com seleção de recurso, data, blocos de horário e convidados](/assets/screenshots/53-nosso-cond-reservas-form.png)

Após a confirmação, a reserva pode ter dois caminhos:

- **Aprovação automática** — reserva confirmada imediatamente. Se houver taxa,
  um lançamento é gerado automaticamente no módulo Financeiro
- **Aguarda aprovação** — reserva aparece no calendário em cinza até o síndico
  aprovar ou rejeitar

#### Cancelar uma reserva

Clique em **Cancelar** na reserva desejada (respeitando a antecedência mínima
configurada). Reservas com lançamento financeiro já pago mantêm o lançamento —
o síndico precisa resolver manualmente no Financeiro.

### Visão do síndico

O síndico pode **criar reservas** da mesma forma que os condôminos, usando o
botão **+ Nova reserva**. Reservas criadas pelo síndico são aprovadas
automaticamente — sem necessidade de aprovação manual — e geram lançamento
financeiro normalmente caso o recurso tenha taxa configurada.

Além de fazer e cancelar reservas, o síndico tem acesso completo:

**Aprovar / rejeitar reservas pendentes:** clique na reserva no calendário ou
na lista e use os botões de ação. A rejeição exige um motivo.

**Gerenciar recursos:** clique em **Gerenciar recursos** para cadastrar e
configurar áreas e itens reserváveis.

![Tela de gerenciamento de recursos reserváveis com opções de configuração](/assets/screenshots/54-nosso-cond-reservas-gerenciar.png)

Para cada recurso é possível definir:

- Nome, tipo (área comum ou item), descrição e fotos
- Capacidade máxima de pessoas
- Regras de uso (exibidas ao condômino antes de confirmar)
- Blocos de horário disponíveis por dia da semana
- Antecedência mínima e máxima para reserva
- Limite de reservas simultâneas por condômino
- Se requer aprovação do síndico
- Se gera lançamento financeiro automaticamente ao aprovar
- Taxa por uso (opcional)
- Ativo / inativo

**Bloquear datas:** pelo gerenciamento de recursos, o síndico pode bloquear
períodos específicos (manutenção, feriados, eventos) com um motivo.

### Status das reservas

| Status | Significado |
|---|---|
| Pendente | Aguarda aprovação do síndico |
| Aprovada | Confirmada |
| Rejeitada | Não aprovada pelo síndico |
| Cancelada | Cancelada pelo condômino ou síndico |
| Arquivada | Reserva passada arquivada (manual ou automaticamente após 30 dias) |

{: .note }
> **Arquivamento automático**
>
> Reservas aprovadas ou canceladas com data anterior a 30 dias são arquivadas
> automaticamente. Use o toggle "Exibir arquivadas" para consultá-las.

{: .note }
> **Notificações**
>
> O síndico recebe e-mail quando há nova reserva pendente. O condômino recebe
> e-mail ao ter sua reserva aprovada, rejeitada ou cancelada, e um lembrete
> 24h antes da reserva confirmada.

---

## Aba Itens

Diretório compartilhado onde todos os moradores podem cadastrar seus itens —
pets, veículos, vagas de garagem e outros — e visualizar os itens dos demais
condôminos.

![Aba Itens com catálogo de pets, veículos, vagas e bens coletivos do condomínio](/assets/screenshots/55-nosso-cond-itens-lista.png)

Os itens são exibidos em **lista** (padrão) ou **grid** — use o toggle no
canto superior direito para alternar. Cada item exibe: foto (se houver),
categoria, nome, descrição resumida e o nome e unidade do dono.

Itens pertencentes ao condomínio (cadastrados pelo síndico como bem coletivo)
são identificados com um badge laranja **"Condomínio"** e borda accent.

**Filtros disponíveis:**
- **Categoria** — filtra por tipo de item (Pet, Veículo, Vaga de garagem ou
  categorias personalizadas)
- **Unidade** — filtra por morador ou exibe apenas itens do condomínio

### Cadastrar um item

Clique em **+ Adicionar item** e preencha:

1. **Categoria** — selecione o tipo do item (obrigatório)
2. **Nome** — identificação do item (obrigatório). Ex: "Mel", "Peugeot 208",
   "Vaga 12"
3. **Descrição** — detalhes adicionais (opcional). O campo exibe exemplos de
   boas práticas conforme a categoria selecionada
4. **Fotos** — até 3 fotos por item. Clique em qualquer foto para ampliar em
   lightbox com navegação entre imagens

![Formulário de cadastro de item com toggle "Item do condomínio"](/assets/screenshots/56-nosso-cond-itens-form.png)

{: .tip }
> **Item do condomínio**
>
> Síndicos podem ativar o toggle **"Item do condomínio"** para registrar um
> bem coletivo (ex: câmera de segurança, mobiliário de área comum). Esses
> itens aparecem identificados na listagem e podem ser filtrados pela opção
> "Condomínio" no filtro de unidade.

### Editar e excluir itens

Cada membro pode editar e excluir apenas seus próprios itens. Síndicos também
podem editar e excluir itens cadastrados como bens do condomínio.

### Visão do condômino

Condôminos visualizam todos os itens de todos os moradores e do condomínio,
cadastram e gerenciam seus próprios itens, mas não podem marcar itens como
bens do condomínio.

---

## Aba Visitantes

Gerencie as listas de visitantes para eventos, festas, churrascos e outras
ocasiões no condomínio. O síndico controla quem está autorizado a entrar,
facilitando a comunicação com a portaria.

![Aba Visitantes — tabela de listas de eventos com filtros Futuras/Passadas/Todas](/assets/screenshots/57-nosso-cond-visitantes-lista.png)

### Visão geral das listas

A tela inicial mostra todas as listas de visitantes cadastradas, filtradas por:
- **Futuras** — eventos agendados para datas futuras
- **Passadas** — eventos já realizados
- **Todas** — todas as listas

Cada linha exibe:
- **Ocasião** — nome do evento (ex: "Churrasco do Bruno")
- **Data** — data do evento
- **Visitantes** — número de visitantes já adicionados
- **Status** — Ativo (futura) ou Realizado (passada)

### Criar uma nova lista

Clique em **+ Nova lista** e preencha:

1. **Ocasião** — nome do evento (obrigatório)
2. **Data** — data do evento (obrigatório)
3. **Horário** — horário de início e término (opcional, mas recomendado)

Ao salvar, a tela abrirá automaticamente o modal de incluir visitantes para
começar a adicionar participantes.

![Formulário de nova lista de visitantes com campos de ocasião, data e horário](/assets/screenshots/58-nosso-cond-visitantes-nova-lista.png)

### Incluir visitantes

Dentro da lista de visitantes, você tem duas opções:

#### Opção 1: Adicionar um visitante por vez
Clique em **+ Adicionar visitante** e preencha:

![Modal de adição de visitante com nome, documento, telefone e horários](/assets/screenshots/59-nosso-cond-visitantes-adicionar.png)

- **Nome** — nome completo (obrigatório)
- **Documento** — CPF ou CNPJ (opcional mas recomendado para identificação)
- **Telefone** — número de contato (opcional)
- **Horário de Chegada** — quando chegará (opcional)
- **Horário de Saída** — quando sairá (opcional)

#### Opção 2: Importar planilha
Clique em **Importar planilha** para:

![Tela de importação de planilha de visitantes com download do modelo](/assets/screenshots/60-nosso-cond-visitantes-importar.png)

1. **Baixar modelo** — download de um arquivo XLSX com as colunas padrão
   (Nome, Documento, Telefone) já formatadas
2. **Preencher dados** — abra o arquivo em seu programa de planilhas e
   adicione os visitantes (até 100 por importação)
3. **Upload** — clique em "Importar planilha", selecione seu arquivo e
   o sistema fará upload automático

O sistema valida automaticamente:
- Duplicatas (se o mesmo documento já existe na lista, a entrada é atualizada)
- Campos obrigatórios (ao menos nome deve estar preenchido)

### Editar e remover listas

Dentro do modal de uma lista, você pode:

- **Editar lista** — alterar ocasião, data ou horário
- **Remover lista** — deletar a lista inteira (ação irreversível)

Para remover visitantes individuais, use o ícone de ações na linha de cada
visitante (menu com opção de deletar).

{: .note }
> **Compartilhamento com a portaria**
>
> A lista de visitantes criada fica visível apenas ao síndico. Recomenda-se
> imprimir ou encaminhar à portaria antes do evento para facilitar o acesso.
