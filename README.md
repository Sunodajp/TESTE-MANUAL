# QA Manual - Demoblaze E-commerce

Projeto de portfólio de QA Manual no site https://www.demoblaze.com

## Objetivo
Validar o fluxo crítico de compra antes de uma release fictícia.

## Escopo testado
Cadastro (Sign up), Login, Home, Categorias Phones/Laptops/Monitors, Detalhe do produto, Carrinho, Checkout (Place Order), Contact, About Us

## Ambiente real usado
Google Chrome 156.0.8078.76 (Official Build) 64-bit
Windows 10 Version 22H2 Build 19045.6466
Resolução 1920x1080
Usuário criado via Sign up no dia da execução

## Técnicas aplicadas
- Partição de equivalência
- Valor limite (carrinho 0, 1, 2 itens)
- Testes positivos e negativos
- Exploratório no checkout e Contact


## Principais bugs encontrados
- BUG-003 Critical: Permite finalizar compra com carrinho vazio (CT-25)
- BUG-001 Major: Botão Previous ignora categoria (CT-03, CT-04)
- BUG-004 Major: Checkout aceita caracteres especiais no cartão (CT-21)
- BUG-002 Minor: Botão Next aparece em Monitors com só 2 produtos (CT-06)
- BUG-005 Minor: Contact envia mensagem vazia (CT-26)



## Ferramentas
Casos: Excel/Sheets
Bugs: GitHub Issues
Versionamento: Git/GitHub

Autor: Suellyne Tsunoda - QA Junior
