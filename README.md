# JP
Este código Python implementa um chatbot para o "JP o Jorge Produtos", um sistema de atendimento ao cliente para compras e vendas online. O código simula um fluxo de conversa interativo com o usuário, direcionando-o de acordo com suas necessidades.

# Fluxo de Interação - Compra e Venda

## Pergunta ao Usuário

Pergunta se o usuário é comprador ou vendedor:
- Se o usuário digitar "comprar", o fluxo segue para a busca de produtos.
- Se o usuário digitar "vender", o fluxo segue para opções específicas de vendedores.
- Se o usuário digitar algo inválido, ele é solicitado a tentar novamente.

## Busca de Produtos

Exibe uma lista de produtos (simulada por response.text).
Pergunta ao usuário qual produto ele procura.
Consulta a IA Gemini (simulada por produtos_similares) para verificar se o produto existe.
- Se o produto for encontrado:
  - Informa que um vendedor entrará em contato.
  - Agradece ao usuário e encerra a conversa.
- Se o produto não for encontrado:
  - Oferece a opção de cadastrar o produto.
    - Se o usuário escolher cadastrar:
      - Direciona para um formulário online (simulado por [este link](https://forms.gle/DwUfVCu4YhmuVJSF6)).
      - Informa que um vendedor entrará em contato.
      - Encerra a conversa.
    - Se o usuário escolher não cadastrar:
      - Agradece o interesse e convida a continuar navegando.
      - Encerra a conversa.

## Opções para Vendedores

Requer ID e nome válidos.
- Ver lista de produtos cadastrados:
  - Exibe um link para a lista de produtos cadastrados (simulado por [este link](https://docs.google.com/spreadsheets/d/1t6AWdJinpkbj5Bv4jnXrFJp02V4UvbE3QW1hKwWQV4I/edit?resourcekey#gid=1921930407)).
  - Agradece ao vendedor.
  - Encerra a conversa.
- Cadastrar novo produto:
  - Solicita informações sobre o produto (nome e tipo).
  - Informa que o produto será enviado para análise.
  - Informa que o status do cadastro será enviado por e-mail.

## Validação de ID e Nome do Vendedor

O código verifica se o ID e nome do vendedor são iguais a "1" e "teste", respectivamente.
- Se forem inválidos, o usuário é direcionado para entrar em contato com o time de cadastros.

## Repetição do Fluxo de Compra

Na opção de continuar navegando, o código utiliza `continue` para retornar ao início do fluxo de compra, permitindo que o usuário busque outro produto.

