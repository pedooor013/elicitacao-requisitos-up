# Levantamento de Requisitos

## 🧑‍💼 Vendedores

| # | Requisito | Fonte | Nível | Classe de Usuário |
|---|-----------|-------|-------|--------------------|
| 1 | O sistema deve registrar se o cliente vai pagar parcelado ou à vista e, se parcelado, em quantas parcelas | Humana | Operacional | Vendedor |
| 2 | O sistema deve calcular automaticamente a comissão em cima da venda que o vendedor realizou | Humana | Estratégico | — |
| 3 | O vendedor deve ter um retorno imediato do sistema sobre a disponibilidade dos produtos vendidos | Humana | Operacional | Vendedor |

## 🛠️ Administrador

| # | Requisito | Fonte | Nível | Classe de Usuário |
|---|-----------|-------|-------|--------------------|
| 1 | Deve ser possível editar o produto, como nome, preço e imagens | Humana | Operacional | Administrador |
| 2 | O sistema deve ter categorias de produtos para facilitar a busca e manutenção dos mesmos | Humana | Operacional | Administrador |
| 3 | O sistema deve ter bloqueadores para cadastro de produtos faltando informações, como nome, preço, etc. | Humana | Operacional | Administrador |

## 📦 Estoquistas

| # | Requisito | Fonte | Nível | Classe de Usuário |
|---|-----------|-------|-------|--------------------|
| 1 | O sistema deve avisar se há produtos com o estoque chegando ao fim | Humana | Estratégico | — |
| 2 | O sistema deve avisar em tempo real se o pedido tem estoque suficiente | Não Humana | Concorrentes | — |
| 3 | O sistema não deve aceitar pedidos com quantidade menor que 0 | Humana | Operacional | Estoquista |
