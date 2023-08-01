# Descrição do Projeto - Univali.Api

Este projeto é uma API desenvolvida utilizando o framework Microsoft.AspNetCore.Mvc e a biblioteca AutoMapper para mapeamento de entidades e DTOs (Data Transfer Objects). A API foi criada para gerenciar informações de clientes e endereços para uma empresa modelo do projeto  chamada Univali.

# Estrutura do Projeto:

O projeto é composto por dois controladores principais:

# 1. CustomersController: Responsável por gerenciar informações dos clientes da empresa.
   - GET /api/customers: Retorna a lista de todos os clientes cadastrados.
   - GET /api/customers/{id}: Retorna os detalhes de um cliente específico com base no ID fornecido.
   - GET /api/customers/cpf/{cpf}: Retorna os detalhes de um cliente específico com base no número de CPF fornecido.
   - POST /api/customers: Cria um novo cliente com base nos dados fornecidos no corpo da requisição.
   - PUT /api/customers/{id}: Atualiza os dados de um cliente existente com base no ID fornecido.
   - DELETE /api/customers/{id}: Exclui um cliente existente com base no ID fornecido.
   - PATCH /api/customers/{id}: Permite atualizar parcialmente os dados de um cliente com base no ID fornecido.

# 2. AddressesController: Responsável por gerenciar informações dos endereços dos clientes.
   - GET /api/customers/{customerId}/addresses: Retorna a lista de endereços associados a um cliente específico com base no ID do cliente fornecido.
   - GET /api/customers/{customerId}/addresses/{addressId}: Retorna os detalhes de um endereço específico associado a um cliente com base nos IDs fornecidos.
   - POST /api/customers/{customerId}/addresses: Cria um novo endereço associado a um cliente específico com base nos dados fornecidos no corpo da requisição.
   - PUT /api/customers/{customerId}/addresses/{addressId}: Atualiza os dados de um endereço associado a um cliente específico com base nos IDs fornecidos.
   - DELETE /api/customers/{customerId}/addresses/{addressId}: Exclui um endereço associado a um cliente específico com base nos IDs fornecidos.

A API utiliza a classe "Data" para simular um banco de dados contendo informações de clientes e endereços. O AutoMapper é utilizado para mapear entidades para DTOs e vice-versa, facilitando a transferência de dados entre a camada de controle e a camada de serviços.

# Além disso, a API fornece algumas funcionalidades adicionais:
- Busca de clientes com seus endereços associados através dos métodos GET /api/customers/with-addresses e GET /api/customers/with-addresses/{customerId}.
- Criação de clientes com seus endereços associados através do método POST /api/customers/with-addresses.
- Atualização de clientes com seus endereços associados através do método PUT /api/customers/with-addresses/{customerId}.

A API utiliza códigos de status HTTP adequados para fornecer respostas apropriadas em cada requisição, como 200 OK, 201 Created, 204 No Content, 400 Bad Request e 404 Not Found.

# Requisitos e Configuração do Projeto:

Para executar o projeto localmente, é necessário ter instalado o SDK do .NET Core e um ambiente de desenvolvimento integrado (IDE) como o Visual Studio ou o Visual Studio Code.

O projeto foi organizado seguindo os padrões do ASP.NET Core, com rotas, modelos e controladores devidamente configurados.

# Para compilar e executar o projeto, siga os passos abaixo:
1. Clone o repositório do projeto para o seu computador.
2. Abra o projeto utilizando o Visual Studio ou o Visual Studio Code.
3. Restaure as dependências do projeto.
4. Pressione F5 ou utilize o comando "dotnet run" para iniciar a aplicação.
5. A API estará disponível em http://localhost:porta/api/customers e http://localhost:porta/api/customers/{customerId}/addresses.

# Conclusão:

Este projeto demonstra a implementação de uma API para gerenciar informações de clientes e endereços para a empresa Univali. Utilizando o framework ASP.NET Core, a API fornece diversas funcionalidades para criação, leitura, atualização e exclusão de dados, bem como mapeamento de entidades para DTOs, garantindo a segurança e eficiência no gerenciamento dos recursos.

![alllog](https://github.com/leandro-guimaraes/AllogEnter_Exercicios_Modulo_01/assets/85081592/c62c8d57-f214-49d5-a99d-107885af3366)
