# Levantamento de Requisitos

## 🧑‍💼 Vendedores

| # | Requisito | Fonte |
|---|-----------|-------|
| 1 | O sistema deve registrar se o cliente vai pagar parcelado ou à vista e, se parcelado, em quantas parcelas | Fonte Humana, nível operacional, classe usuário vendedor |
| 2 | O sistema deve calcular automaticamente a comissão em cima da venda que o vendedor realizou | Fonte Humana, nível estratégico |
| 3 | O vendedor deve ter um retorno imediato do sistema sobre a disponibilidade dos produtos vendidos | Fonte Humana, nível operacional |

## 🛠️ Administrador

| # | Requisito | Fonte |
|---|-----------|-------|
| 1 | Deve ser possível editar o produto, como nome, preço e imagens | Fonte Humana, nível operacional |
| 2 | O sistema deve ter categorias de produtos para facilitar a busca e manutenção dos mesmos | Fonte Humana, nível operacional |
| 3 | O sistema deve ter bloqueadores para cadastro de produtos faltando informações, como nome, preço, etc. | Fonte Humana, nível operacional |

## 📦 Estoquistas

| # | Requisito | Fonte |
|---|-----------|-------|
| 1 | O sistema deve avisar se há produtos com o estoque chegando ao fim | Fonte Humana, nível estratégico |
| 2 | O sistema deve avisar em tempo real se o pedido tem estoque suficiente | Fonte Não Humana, nível concorrentes |
| 3 | O sistema não deve aceitar pedidos com quantidade menor que 0 | Fonte Humana, nível operacional |