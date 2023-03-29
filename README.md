# projetoWebApi-backend

### Projeto Web: .NET 6 Web API + HTML + CSS + JS

  Projeto de Desenvolvimento de uma Web API com DOTNET 6 utilizando o VSCode. Criado em 2 pastas diferentes projetoWebAPI-backend / projetoWebApi-frontend. Utilizando Microsoft Entity Framework Core(Design/InMemory) para salvar os dados no Banco de Dados em um banco em memória. Foram utilizadas os métodos Post, Get e Delete.

----

<h2>Documentação do código LojaApi</h2>
Este documento fornece as informações necessárias para executar o código da API da Loja, que gerencia as categorias dos produtos. A API foi escrita em C# usando o framework Microsoft ASP.NET Core e o Entity Framework Core para acesso aos dados. O código fornece as seguintes funcionalidades:

*POST - Adiciona uma nova categoria
*GET - Retorna a lista de todas as categorias
*DELETE - Exclui uma categoria
Pré-requisitos
Visual Studio (2019 ou superior)
.NET Core SDK (3.1 ou superior)
Banco de dados SQL Server
Configuração
Clone o repositório do código
Abra a solução LojaApi.sln no Visual Studio
Crie um novo banco de dados no SQL Server
Configure a conexão com o banco de dados no arquivo appsettings.json
No Package Manager Console, execute o comando Update-Database para criar as tabelas no banco de dados
Pressione F5 para executar o projeto
Endpoints
POST /categorias
Este endpoint adiciona uma nova categoria ao banco de dados. O corpo da solicitação deve ser um objeto JSON com os seguintes campos:

Nome (string) - O nome da categoria
DataCadastro (datetime) - A data de cadastro da categoria
Departamento (string) - O departamento da categoria

