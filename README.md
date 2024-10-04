Entidades:
- **Produto.**
  - ProdutoID.
  - Nome do produto.
  - Preço do produto.
  - QTD mínimo.
  - Descrição do produto.
    - Cor do produto.
    - Tamanho do produto.
- **Estoque.**
  - QTD em estoque.
  - ProdutoID.
- **Venda.**
  - ProdutoID.
  - QTD Produto.
  - QTD vendida.
  - Total de Lucro.
  - Data da venda.
  - Preço unitário.
- **Histórico.**
  - ProdutoID.
  - Data movimentação.
  - Entrada ou saída.
  - QTD movimentada.
- **Alerta.**
  - ProdutoID.
  - Tipo de alerta.
  - Data do alerta.
- **Compra.**
  - ProdutoID.
  - FornecedorID.
  - QTD comprada.
  - Preço unitário.
  - Data da compra.
  - Prazo de entrega.
- **Operador.**
  - OperadorID
  - Nome do operador.
  - CPF do operador.
  - Cargo do operador.
- **Fornecedor.**
  - Nome fornecedor.
  - Contato.
  - Prazo de entrega.

Caso de uso:
- ## **Cadastrar *Produto*.**
  ### Requisitos Funcionais.
  - O sistema deve permitir a inclusão de *produtos* com id, nome, preço, descrição(cor e tamanho), qtd inicial em estoque, qtd minima em estoque.

  ### Requisitos não Funcionais.
  - cor e tamanho são opcionais.


- ## **Atualizar *Produto*.**
  ### Requisitos Funcionais.
  - O sistema deve permitir a alteração de *produtos* com id, nome, preço, descrição e etc.

  ### Requisitos não Funcionais.
  - O sistema deve permitir a alteração de *produtos* apenas para os operadores com cargo de gerente.


- ## **Rastrear *Produto*.**
  ### Requisitos Funcionais.
  - O sistema deve consultar informações detalhadas sobre um *produto* específico, incluindo seu *histórico* de movimentações no *estoque*, tamanho, cor, quantidade atual, e vendas.

  ### Requisitos não Funcionais.
  - O sistema deve permitir a consulta de *produtos* apenas para os *operadores* com cargo de gerente
  - Individualmente.
  - Movimentações dentro do *estoque*.
  - Movimentações de entrada e saída.
  - Deve utilizar cor e tamanho para tornar o rastreamento ainda mais preciso.


- ## **Definir quantidade minima de Estoque.**
  ### Requisitos Funcionais.
  - O sistema deve permitir a definição de quantidade minima de *estoque* para cada *produto*

  ### Requisitos não Funcionais.


- ## **Alerta quantidade mínima do *produto* no *estoque*.**
  ### Requisitos Funcionais.
  - O sistema deve enviar um alerta para o *operador* responsável quando a quantidade mínima for atingida.

  ### Requisitos não Funcionais.
  - O sistema deve enviar o alerta apenas para os *operadores* com cargo de gerente

  - Receber alertas quando estivermos ficando sem determinado *produto*, baseado na quantidade minima do *produto*.
  - Receber notificação via email e dentro da aplicação.
- Visualização de histórico.
  - Visualização de quantos *produtos* foram vendidos em determinado tempo
  - Visualização de qual foi o lucro gerado por *produto*.


- ## **Visualizar Histórico de um produto.**
  ### Requisitos Funcionais.
  - O sistema deve permitir a visualização do histórico de um *produto* específico
  - O sistema deve mostrar entradas e saídas.

  ### Requisitos não Funcionais.
  - O sistema deve permitir a visualização do histórico apenas para os *operadores* com o cargo de gerente.
  

- ## **Visualizar histórico de vendas.**
  ### Requisitos Funcionais.
  - O sistema deve permitir a visualização do histórico de vendas de cada *produto*
  - O sistema deve mostrar o valor total de vendas de cada *produto*

  ### Requisitos não Funcionais.
  - O sistema deve permitir a visualização do histórico apenas para os *operadores* com o cargo de gerente


- ## **Emitir relatórios de desempenho.**
  ### Requisitos Funcionais.
  - O sistema deve gerar relatórios com base no histórico de vendas e estoque, permitindo ao usuário visualizar quais produtos têm melhor desempenho em termos de vendas e tendências de estoque ao longo do tempo.

  ### Requisitos não Funcionais.
  - O sistema deve permitir a geração de relatórios apenas para os *operadores* com cargo de gerente.
  - O sistema deve permitir a exportação dos relatórios em formato CSV ou PDF.


- ## **Criar ordem de compra.**
  ### Requisitos Funcionais.
  - O sistema deve gerar automaticamente uma ordem de compra.
  - O sistema deve permitir a visualização da ordem de compra.
  - O sistema deve permitir a atualização da ordem de compra.
  - O sistema deve permitir a confirmação da ordem de compra.
  - O sistema deve permitir a cancelamento da ordem de compra.

  ### Requisitos não Funcionais.
  - O sistema deve permitir a criação de ordem de compra apenas para os *operadores* com cargo de gerente.
  - O sistema deve permitir a visualização da ordem de compra apenas para os *operadores* com cargo de gerente
  - O sistema deve permitir a atualização da ordem de compra apenas para os *operadores* com cargo de gerente
  - O sistema deve permitir a confirmação da ordem de compra apenas para os *operadores* com cargo de gerente
  - O sistema deve permitir a cancelamento da ordem de compra apenas para os *operadores* com cargo de gerente
  - O sistema deve gerar automaticamente uma ordem de compra quando um produto atinge o limite mínimo de estoque, baseada nas necessidades de reposição e nas tendências de vendas.


- ## **Gerenciar fornecedores.**
  ### Requisitos Funcionais.
  - O sistema deve permitir a criação de fornecedores.
  - O sistema deve permitir a visualização de fornecedores.
  - O sistema deve permitir a atualização de fornecedores.
  - O sistema deve permitir a exclusão de fornecedores.
  - O sistema deve permitir a atribuição de fornecedores a produtos.

  ### Requisitos não Funcionais.
  - O sistema deve permitir a criação de fornecedores apenas por *operadores* com cargo de gerente.
  - O sistema deve permitir a visualização de fornecedores apenas para todos os *operadores*
  - O sistema deve permitir a atualização de fornecedores apenas para os *operadores* com cargo de gerente.
  - O sistema deve permitir a exclusão de fornecedores apenas para os *operadores* com cargo de gerente.
  - O sistema deve permitir a atribuição de fornecedores a produtos apenas para todos so *operadores*.


- ## **Receber atualização de prazo de entrega.**
  ### Requisitos Funcionais.
  - O sistema deve integrar com o sistema do fornecedor via webhook para receber atualizações do prazo de entrega em tempo real.
  - O sistema deve atualizar automaticamente o prazo de entrega no sistema.
  - O sistema deve enviar notificação para os *operadores* com cargo de gerente quando

  ### Requisitos não Funcionais.




- Quantos produtos foram vendidos em determinado tempo.
- Calculo de lucro gerado por produto.
- Avaliação de quais produtos estão vendendo melhor em cada período
- Criar e gerenciar ordens de compra automaticamente.





