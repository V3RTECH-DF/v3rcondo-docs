---
title: Assembleias
parent: Módulos
nav_order: 12
---

# Assembleias

{: .warning }
> **Plano Pro**
>
> Este módulo é exclusivo para condomínios com **plano Pro**. No plano Básico,
> o módulo aparece na sidebar com cadeado — clique para conhecer o plano Pro.

O módulo Assembleias digitaliza todo o ciclo de vida de uma assembleia
condominial: da convocação formal até a publicação da ata gerada por
inteligência artificial. O módulo é organizado em três fases —
**Pré-assembleia**, **Condução** e **Pós-assembleia**.

![Lista de assembleias com colunas de título, tipo, data e status](/assets/screenshots/61-assembleias-lista.png)

---

## Listagem de assembleias

A tela inicial exibe todas as assembleias do condomínio em uma tabela com
colunas ordenáveis: título, tipo, data e status. Use o cabeçalho de cada
coluna para ordenar.

{: .note }
> **Visão do condômino**
>
> Condôminos visualizam apenas assembleias a partir do status **Edital
> publicado**. Rascunhos são visíveis somente para o síndico.

### Status das assembleias

| Status | Significado |
|---|---|
| Rascunho | Em elaboração — não visível para condôminos |
| Edital publicado | Convocação enviada — condôminos notificados |
| Em andamento | Assembleia aberta e sendo conduzida |
| Encerrada | Assembleia finalizada — aguardando ata |
| Ata publicada | Ata disponível para todos os condôminos |

---

## Pré-assembleia *(síndico)*

### Criar uma assembleia

Clique em **+ Nova assembleia** e preencha:

1. **Título** — ex: "AGO 2026", "Assembleia Extraordinária — Obras" (obrigatório)
2. **Tipo** — Ordinária ou Extraordinária
3. **Data e hora** — data e horário de realização (obrigatório)
4. **Local** — endereço físico ou link da plataforma de videoconferência
5. **É virtual?** — ative para assembleias online ou híbridas
6. **Enviar lembretes automáticos** — quando ativo, o sistema envia lembretes
   por e-mail aos condôminos 7 dias e 1 dia antes da assembleia

Clique em **Salvar** para criar a assembleia com status **Rascunho**. Você
pode editar todos os campos enquanto a assembleia estiver em rascunho.

![Formulário de criação de nova assembleia com toggle de lembretes automáticos](/assets/screenshots/62-assembleias-form.png)

### Montar a pauta

Na seção **Pauta**, clique em **+ Adicionar item** e preencha:

- **Título** — descrição do item (obrigatório)
- **Descrição** — detalhamento adicional (opcional)
- **Tipo** — selecione o tipo do item:
  - **Informativo** — apresentação de informações, sem votação
  - **Votação** — requer registro de deliberação e resultado
  - **Discussão** — debate livre com anotações
  - **Assunto geral** — itens surgidos durante a assembleia

Use as setas para reordenar os itens. Clique no ícone de lápis para editar
ou no ícone de lixeira para excluir (com confirmação).

![Detalhe da assembleia com seções de pauta, documentos adicionais e procurações](/assets/screenshots/63-assembleias-detalhe-pauta.png)

{: .tip }
> **Assuntos gerais**
>
> Itens não previstos na pauta original podem ser adicionados durante a
> condução da assembleia, diretamente na tela de condução.

### Anexar documentos

Na seção **Documentos adicionais**, anexe arquivos de apoio que devem
acompanhar o edital — orçamentos, laudos, propostas etc. Clique em
**Escolher arquivo**, informe uma descrição opcional e clique em
**Enviar arquivo**.

Os documentos aparecem também no módulo **Documentos** com a categoria
"Assembleias".

### Publicar o edital

Quando a pauta estiver completa, clique em **Publicar edital** no cabeçalho
da página. Uma confirmação será exibida antes de prosseguir.

Ao publicar:

- O V3RCondo gera automaticamente o PDF do edital de convocação
- Um e-mail com o edital em anexo é enviado para todos os condôminos
- Uma notificação interna é disparada no aplicativo
- O status muda para **Edital publicado**
- O edital fica disponível em **Documentos → Assembleias**

{: .warning }
> **Ação irreversível**
>
> Após publicar o edital, os dados da assembleia não podem mais ser editados.
> Certifique-se de que a pauta está completa antes de publicar.

### Cancelar uma assembleia

Para cancelar uma assembleia em **Rascunho** ou com **Edital publicado**,
clique em **Cancelar assembleia** no cabeçalho. Uma confirmação será exibida.

Se o edital já foi publicado, os condôminos são notificados automaticamente
por e-mail e pelo aplicativo sobre o cancelamento.

{: .note }
> **Restrição de cancelamento**
>
> Não é possível cancelar uma assembleia que já foi iniciada (status
> **Em andamento** ou posterior).

### Registrar procurações

Na seção **Procurações**, registre os condôminos que outorgaram poderes a
outro membro para votar em seu nome. Clique em **+ Registrar procuração** e:

1. Selecione o **outorgante** — quem concedeu a procuração
2. Selecione o **procurador** — quem vai representar o outorgante
3. Adicione observações (opcional)
4. Anexe o documento da procuração (obrigatório)

---

## Condução da assembleia *(síndico)*

### Iniciar a assembleia

No dia da assembleia, abra a assembleia no app e clique em **Iniciar
assembleia**. Um painel de abertura será exibido com três blocos:

**Presidente da mesa:**

- Ative **"Síndico presidiu a mesa"** para preencher automaticamente com
  os seus dados
- Desative para informar outro nome — pode ser um membro do condomínio
  (selecione da lista) ou uma pessoa externa (digite o nome livremente)
- Informe CPF e RG quando disponíveis — necessários para registro cartorial

**Secretário:**

- Mesma lógica do presidente — toggle de síndico ou preenchimento manual

**Quórum:**

- Informe o número de **unidades presentes**
- Marque se o **quórum foi atingido**
- Adicione observações (ex: "Chamada única — qualquer número de presentes")

{: .warning }
> **Atenção ao quórum**
>
> O quórum mínimo varia conforme o tipo de deliberação e o regulamento do
> seu condomínio. Verifique a convenção condominial e o Código Civil antes
> de declarar quórum atingido.

Clique em **Abrir assembleia** para confirmar. O status muda para
**Em andamento**.

### Lista de presença

A lista é gerada automaticamente com todos os membros ativos do condomínio,
marcados como **presentes** e **presenciais** por padrão.

Para cada membro, você pode:

- Desmarcar a presença (toggle presente/ausente)
- Alterar a modalidade (Presencial / Remoto)
- Preencher ou corrigir CPF e RG diretamente na linha — os campos são
  salvos automaticamente ao sair do campo

**Convidados externos:** clique em **+ Adicionar convidado** para registrar
pessoas que não são condôminos (ex: representante da administradora). Informe
nome, papel, CPF e RG.

### Condução da pauta

A seção **Pauta — condução** exibe os itens em ordem. Para cada item:

- Altere o **status** conforme a assembleia avança:
  - **Pendente** → **Em discussão** → **Concluído**
- Digite as **anotações do secretário** no campo de texto — salvo
  automaticamente ao sair do campo

**Para itens de votação** com status **Concluído**, um formulário aparece
para registrar a deliberação:

1. **Tipo de deliberação:**
   - Por aclamação — sem contagem de votos
   - Por contagem de votos — informe votos a favor, contra e abstenções
   - Sem votação
2. **Resultado** — Aprovado, Reprovado ou Adiado
3. **Decisão tomada** — texto livre com o teor da deliberação

### Documentos da condução

Durante a assembleia, anexe documentos adicionais como transcrições,
gravações ou anotações. Selecione o **tipo** antes de enviar:
Transcrição, Gravação, Anotação ou Outro.

### Encerrar a assembleia

Clique em **Encerrar assembleia** — o botão está disponível tanto no cabeçalho
quanto no rodapé da página de condução. Em assembleias com muitos itens de pauta,
use o botão do rodapé para encerrar sem precisar rolar de volta ao topo. Uma
confirmação será exibida antes de prosseguir.

{: .warning }
> **Ação irreversível**
>
> Após encerrar, a assembleia não pode ser reaberta. Certifique-se de que
> todas as anotações e deliberações foram registradas.

---

## Pós-assembleia — Geração da ata *(síndico)*

Após encerrar a assembleia, o V3RCondo oferece três opções para a ata:

### Gerar ata com inteligência artificial

Ao encerrar, um painel pergunta se deseja gerar a ata com IA. Você também
pode acessar essa opção a qualquer momento pela seção **Ata da assembleia**
na tela da assembleia encerrada.

Antes de solicitar a geração, você pode revisar e complementar as
**Instruções para a IA** — um campo de texto com orientações sobre tom,
estrutura e destaques que a ata deve conter. Um texto padrão já é
pré-preenchido e pode ser editado livremente.

{: .tip }
> **Qualidade da ata**
>
> Quanto mais detalhadas forem as anotações do secretário em cada item da
> pauta, melhor será a qualidade da ata gerada. Preencha os campos de
> anotações durante a condução.

Após clicar em **Solicitar geração**, o sistema processa a ata em segundo
plano. Você receberá uma cópia por e-mail assim que estiver pronta —
o processo pode levar alguns minutos.

Quando a ata estiver disponível, três opções são exibidas:

- **Publicar ata** — aceita a ata gerada e publica para todos os condôminos
- **Regenerar com ajustes** — descreva o que precisa ser ajustado e uma nova
  versão será gerada
- **Lançar ata própria** — faça upload de um PDF elaborado externamente

{: .warning }
> **Aviso sobre IA**
>
> A ata é gerada com auxílio de inteligência artificial com base nos dados
> registrados na plataforma. Revise o documento antes de publicar
> oficialmente.

### Regenerar com ajustes

Clique em **Regenerar com ajustes** e descreva no campo de texto o que
precisa ser corrigido ou modificado. Uma nova versão será gerada e enviada
por e-mail.

### Lançar ata própria

Clique em **Lançar ata própria** para fazer upload de um PDF elaborado
externamente. Selecione o arquivo e clique em **Enviar**.

---

## Publicação da ata

Clique em **Publicar ata** para confirmar a publicação. Uma confirmação
será exibida antes de prosseguir.

Ao publicar:

- Todos os condôminos recebem um e-mail com link para download da ata
- Uma notificação interna é disparada no aplicativo
- A ata fica disponível em **Documentos → Assembleias**
- O síndico recebe um e-mail com a ata e uma seção de **itens de governança**
  gerada pela IA — tarefas sugeridas, prazos, comunicados recomendados e
  próximos passos com base nas deliberações

Após a publicação, um aviso é exibido:

{: .note }
> **Registro em cartório**
>
> Verifique a necessidade de registrar esta ata em cartório. Se necessário,
> reúna o edital de convocação, as evidências de publicação, a lista de
> presença, a ata e o requerimento de registro, e submeta ao Cartório de
> Registro de Títulos e Documentos da sua região.

---

## Documentos gerados

Todos os documentos da assembleia — edital, ata e anexos — ficam disponíveis
no módulo **Documentos** com a categoria **Assembleias**, e também acessíveis
diretamente na tela da assembleia com links individuais para cada arquivo.

---

## Visão do condômino

Condôminos acessam o módulo Assembleias para consultar o histórico de
assembleias do condomínio. Para cada assembleia com edital publicado é
possível:

- Visualizar os dados gerais (data, local, tipo)
- Acessar os documentos vinculados (edital, ata, anexos)
- Baixar os arquivos disponíveis

Os controles de criação, condução e publicação são exclusivos do síndico.
