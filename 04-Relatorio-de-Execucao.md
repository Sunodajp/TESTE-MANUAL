# Relatório de Execução de Testes - Demoblaze

- **Site:** https://www.demoblaze.com
- **Responsável:** Suellyne Tsunoda
- **Ambiente:** Chrome 156.0.8078.76 · Windows 10 22H2 (Build 19045.6466) · 1920x1080

Dos 26 casos executados, 21 passaram e 5 falharam. Foram registrados 5 bugs, um deles crítico (compra concluída com carrinho vazio), e 2 melhorias.

## Resumo da execução

| Status | Quantidade |
|---|---|
| Passou | 21 |
| Falhou | 5 |
| Bloqueado | 0 |
| Não executado | 0 |
| **Total** | **26** |

## Casos de teste executados

Os passos e resultados esperados de cada caso estão em [02-Casos-de-Teste-Demoblaze.md](02-Casos-de-Teste-Demoblaze.md).

| ID | Título | Resultado obtido | Status | Prioridade | Bug / Obs. |
|---|---|---|---|---|---|
| CT-001 | Carregar a página inicial | Home carregou conforme esperado. | Passou | Alta | - |
| CT-002 | Filtrar produtos por Phones | Somente celulares exibidos. | Passou | Média | - |
| CT-003 | Filtrar produtos por Laptops | Ao avançar a página e clicar em Previous, a lista volta com produtos de várias categorias, não só laptops. | Falhou | Média | BUG-001 |
| CT-004 | Filtrar produtos por Monitors | Monitors exibe só 2 produtos e o botão Next. Next abre outra página e, ao voltar com Previous, a lista deixa de ser Monitors (produtos variados). | Falhou | Média | BUG-001, BUG-002 |
| CT-005 | Abrir detalhe de um produto | Detalhe exibido conforme esperado. | Passou | Alta | - |
| CT-006 | Cadastrar usuário novo | Usuário criado com sucesso. | Passou | Alta | - |
| CT-007 | Cadastrar usuário já existente | Cadastro tratado como esperado para usuário já existente. | Passou | Média | - |
| CT-008 | Cadastrar com campos vazios | O site exibiu o alerta "Please fill out Username and Password". | Passou | Média | - |
| CT-009 | Login com credenciais válidas | Conforme esperado. | Passou | Alta | - |
| CT-010 | Login com senha incorreta | Conforme esperado. | Passou | Alta | - |
| CT-011 | Login com usuário inexistente | Conforme esperado. | Passou | Média | - |
| CT-012 | Logout | Conforme esperado. | Passou | Média | - |
| CT-013 | Adicionar um produto ao carrinho | Produto vai ao carrinho. Não há contador de itens visível fora da página do carrinho. | Passou | Alta | MEL-001 |
| CT-014 | Adicionar dois produtos e validar o total | Conforme esperado. | Passou | Alta | - |
| CT-015 | Adicionar o mesmo produto duas vezes | O produto aparece em 2 linhas separadas, não em uma linha com quantidade 2. Total correto. | Passou | Média | MEL-002 |
| CT-016 | Excluir um item do carrinho | Conforme esperado. | Passou | Alta | - |
| CT-017 | Abrir carrinho vazio | Conforme esperado. | Passou | Média | - |
| CT-018 | Finalizar compra com dados válidos | Compra concluída. | Passou | Alta | - |
| CT-019 | Finalizar compra com formulário vazio | Compra bloqueada com o formulário vazio. Veja também BUG-003: com carrinho vazio e nome e cartão preenchidos, a compra é concluída. | Passou | Alta | - |
| CT-020 | Finalizar compra sem número de cartão | Compra bloqueada sem o número do cartão. Veja também BUG-004: os campos aceitam caracteres especiais. | Passou | Alta | - |
| CT-021 | Cartão com letras e caracteres especiais | Com letras e caracteres especiais (como @) em nome e cartão, a compra foi concluída. Os campos não são validados. | Falhou | Média | BUG-004 |
| CT-022 | Carrinho esvazia após a compra | Conforme esperado. | Passou | Alta | - |
| CT-023 | Enviar mensagem pelo modal Contact | Mensagem enviada com dados válidos. | Passou | Baixa | - |
| CT-024 | Abrir e fechar o modal About us | Conforme esperado. | Passou | Baixa | - |
| CT-025 | Finalizar compra com carrinho vazio | A compra foi concluída com o carrinho vazio. | Falhou | Alta | BUG-003 |
| CT-026 | Enviar mensagem com todos os campos vazios | A mensagem foi enviada com todos os campos vazios. | Falhou | Baixa | BUG-005 |

## Bugs e melhorias registrados

O detalhe de cada um, com passos e evidências, está em [03-Bugs-Demoblaze.md](03-Bugs-Demoblaze.md).

| ID | Título | Severidade | Prioridade | Caso |
|---|---|---|---|---|
| BUG-003 | CHECKOUT – Compra é concluída com o carrinho vazio | Critical | Alta | CT-025 |
| BUG-001 | PAGINAÇÃO – Botão Previous ignora a categoria e lista produtos de todas as categorias | Major | Média | CT-003, CT-004 |
| BUG-004 | CHECKOUT – Campos nome e cartão aceitam letras e caracteres especiais sem validação | Major | Média | CT-021 |
| BUG-002 | MONITORS – Botão Next aparece em categoria com apenas 2 produtos | Minor | Baixa | CT-004 |
| BUG-005 | CONTACT – Mensagem é enviada com todos os campos vazios | Minor | Baixa | CT-026 |
| MEL-001 | CARRINHO - Falta contador de itens no ícone do carrinho (melhoria) | Trivial | Baixa | CT-013 |
| MEL-002 | CARRINHO - Mesmo produto adicionado 2 vezes gera 2 linhas, não quantidade 2 (melhoria) | Minor | Baixa | CT-015 |
