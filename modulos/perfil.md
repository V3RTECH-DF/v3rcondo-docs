---
title: Perfil
parent: Módulos
nav_order: 15
---

# Perfil

A página de Perfil permite gerenciar suas informações pessoais e senha de acesso. Está disponível para síndicos e condôminos.

Para acessar, clique no seu nome ou avatar no canto inferior esquerdo da sidebar.

![Página de Perfil com avatar, dados pessoais e botão Salvar](/assets/screenshots/84-perfil-dados.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

## Dados Pessoais

Exibe seu avatar, nome e e-mail no topo. Para atualizar o avatar, clique no ícone de câmera sobre a foto.

Campos editáveis:

- **Nome completo** — nome exibido no sistema e nas publicações do mural
- **E-mail** — somente leitura, não pode ser alterado
- **Telefone** — número de contato (opcional)
- **CPF** — cadastro de pessoa física no formato ###.###.###-## (obrigatório). Enquanto não preenchido, um banner de aviso é exibido no perfil

{: .warning }
> **CPF obrigatório**
>
> O CPF é necessário para emissão de notificações extrajudiciais e identificação em documentos gerados pelo sistema. Preencha-o para remover o aviso.

Clique em **Salvar dados** para confirmar as alterações.

## Alterar Senha

Preencha os campos **Nova senha** e **Confirmar nova senha** e clique em **Alterar senha**.

![Seção de alteração de senha no Perfil](/assets/screenshots/85-perfil-senha.png)

{: .note }
> **Login com Google**
>
> Usuários que fizeram login com o Google não precisam definir senha — o acesso é gerenciado pela conta Google.

## Notificações via Telegram *(Básico e Pro)*

O card **Notificações via Telegram** permite conectar sua conta ao bot **@V3RCondoBot** para receber alertas do condomínio diretamente no Telegram.

### Conectar

1. Clique em **Conectar Telegram**
2. O link abre o Telegram no bot **@V3RCondoBot**
3. Envie o comando `/start` no bot
4. Uma mensagem de confirmação aparece no Telegram e o card atualiza para o estado conectado

### Desconectar

Clique em **Desconectar** e confirme. As notificações via Telegram são interrompidas imediatamente.

![Card de conexão com o Telegram — bot @V3RCondoBot](/assets/screenshots/86-perfil-telegram.png)

{: .tip }
> **Quais eventos geram notificação?**
>
> Veja a lista completa na página de [Notificações](/modulos/notificacoes/).

## Privacidade e visibilidade no diretório

O card **Minha visibilidade no diretório** permite controlar quais dados pessoais são visíveis para outros condôminos no diretório do condomínio. Os campos configuráveis variam por condomínio.

![Toggles de visibilidade de campos no diretório do condomínio](/assets/screenshots/87-perfil-visibilidade.png)

*Os dados pessoais apresentados nesta imagem são fictícios e foram utilizados apenas para fins ilustrativos.*

## Exportar meus dados

O botão **Exportar meus dados** gera um arquivo XLSX com todas as informações do seu perfil armazenadas no V3RCondo: dados pessoais, condomínios vinculados e consentimentos de visibilidade.

## Excluir minha conta

O botão **Excluir minha conta** inicia um assistente de 3 etapas com confirmação por digitação de e-mail. A ação é irreversível: o perfil é anonimizado e o acesso é removido de todos os condomínios.

{: .warning }
> **Síndico único**
>
> Se você for o único síndico de um condomínio, a exclusão fica bloqueada até que outro membro assuma o papel de síndico.

![Botões de exportação de dados e exclusão de conta](/assets/screenshots/88-perfil-exportar-excluir.png)
