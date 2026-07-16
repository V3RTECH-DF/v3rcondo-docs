---
title: Caça-diferenças
parent: Módulos
nav_order: 3.2
---

# Caça-diferenças

Quando o saldo que o V3RCondo mostra para uma conta **não bate** com o saldo do extrato do banco, o caça-diferenças ajuda a descobrir **onde está o furo** — mesmo que você tenha o extrato só em papel ou PDF. Você informa o saldo que o banco apresenta e o app calcula a diferença e sugere as causas mais prováveis, com correção em um clique nos casos seguros.

{: .note }
> **Quem usa**
>
> Ferramenta do **síndico**. O botão não aparece para condôminos.

## Abrir o caça-diferenças

No módulo **Financeiro**, na seção **Saldos por Conta**, cada conta tem um botão de lupa 🔍 ("Conferir saldo"). Clique nele na conta que quer conferir.

![Seção Saldos por Conta com o botão de lupa em cada conta](/assets/screenshots/caca-diferencas-botao.png)

## Passo a passo

1. No painel que abre, informe o **Saldo do banco** — o valor que aparece no seu extrato — e a **Data do saldo** (por padrão, hoje).

   ![Painel do caça-diferenças com os campos Saldo do banco e Data do saldo](/assets/screenshots/caca-diferencas-entrada.png)

2. O app calcula o **saldo dele até aquela data** e mostra a **diferença** entre o banco e o app.
3. Se estiver tudo certo, aparece **"Tudo batendo ✅"**. Se houver diferença, o app lista as **hipóteses** mais prováveis de onde ela está — as que mais provavelmente explicam a diferença vêm primeiro.

   ![Painel mostrando a diferença e a lista de hipóteses, com a mais provável no topo](/assets/screenshots/caca-diferencas-hipoteses.png)

## O que cada hipótese significa

- **Duplicata** — o mesmo lançamento foi registrado duas vezes. Excluir uma das cópias zera a diferença.
- **Lançamento que explica a diferença** — um lançamento do mesmo valor da diferença, que pode ter sido lançado por engano.
- **Conta errada** — um lançamento que provavelmente deveria estar nesta conta (por exemplo, caiu na conta do cartão em vez da conta corrente). Movê-lo para cá acerta o saldo.
- **Valor quase igual** — um lançamento com valor um pouco diferente do real (típico de tarifa bancária, IOF ou conversão de moeda). Corrigir o valor resolve.
- **Combinação** — dois lançamentos que, somados, explicam a diferença.
- **Procure no extrato** — quando nada no app explica a diferença, provavelmente falta lançar algo (uma tarifa, um débito ainda não registrado). O app indica o valor exato a procurar.

## Corrigir

Cada hipótese traz uma ação:

- **Excluir duplicata** e **Mover para esta conta** são feitos **em um clique**, com uma confirmação antes — e são ações **reversíveis**.
- As demais abrem a tela correspondente para você conferir o lançamento, corrigir o valor ou criar o que falta (já pré-preenchido com o valor da diferença).

A cada correção, o app **recalcula a diferença** na hora e mostra se o saldo fechou ou quanto ainda falta — assim você vai ajustando até zerar.

{: .tip }
> **Não precisa importar o extrato**
>
> O caça-diferenças trabalha só com o **número** do saldo do banco. É ideal para quando você tem o extrato apenas impresso ou em PDF e não consegue importar o arquivo. Se você **tem** o arquivo OFX/CSV, use o **[Importar extrato](financeiro.md)** para conciliar transação a transação.

{: .note }
> **Cobranças iguais não são confundidas com duplicata**
>
> Cobranças legitimamente repetidas (a mesma taxa em várias unidades, por exemplo) **não** são listadas como duplicata — o caça-diferenças mostra só o que realmente explica a diferença daquela conta.
