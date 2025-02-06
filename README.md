
# Desafio de Projeto - DIO

## Refinando um Projeto Conceitual de Banco de Dados – E-COMMERCE

O diagrama EER (Enhanced Entity-Relationship) apresenta a estrutura básica de um sistema de e-commerce, com foco em entidades como Cliente, Produto, Pedido, Pagamento e Entrega.

### Relacionamento

- Produtos_Vendedor_Terceiro: Relaciona Terceiro_Vendedor com Produto, indicando quais produtos estão disponíveis por vendedor.

- Disponibiliza_Produto: Relaciona Fornecedor com Produto, indicando quais produtos são fornecidos por quais fornecedores.

- Relacao_Produto_Estoque: Relaciona Produto com Estoque, indicando a quantidade de cada produto em cada local de estoque.

- Pedido: Relaciona Cliente com Produto através de Pedido_id_Pedido.

- Cliente: Pode ser Pessoa Jurídica (PJ) ou Pessoa Física (PF), mas não ambos.

- Pagamento: Relaciona com pedido e está associado a várias Forma_Pagamento.

- Forma_Pagamento: Entidade foi bem expandida para suportar múltiplos métodos de pagamento, incluindo Pix e Boleto.

- Entrega: Relaciona com Pedido, os campos Status_Entrega e Codigo_Rastreio são fundamentais para acompanhamento do pedido.

### Vantagens da Estrutura de Pagamento

 - **Flexibilidade:** Permite inserir novas formas de pagameto sem alterar a lógica do BD
 - **Organização:** Evita a mistura de informações, pois cada tipo de pagamento tem seus campos específicos.
 - **Escalabilidade:** Se no futuro surgirem novos métodos de pagamento, basta adicionar na entidade Forma_Pagamento.


### Melhorias e Implementações

- Validar de dados e segurança
- Criar nova entidade para histórico de alterações de status dos pedidos
- Expandir categoria Produto.

### Considerações:

A estrutura está bem organizada e atende aos requisitos de um sistema de e-commerce moderno, com suporte a múltiplos métodos de pagamento e um controle detalhado de estoque e entregas.
