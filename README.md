# projetoWebApi-backend

### Projeto Web: .NET 6 Web API + HTML + CSS + JS

  Projeto de Desenvolvimento de uma Web API com DOTNET 6 utilizando o VSCode. Criado em 2 pastas diferentes projetoWebAPI-backend / projetoWebApi-frontend. Utilizando Microsoft Entity Framework Core(Design/InMemory) para salvar os dados no Banco de Dados em um banco em memória. Foram utilizadas os métodos Post, Get e Delete.

----

<h2>Documentação do código LojaApi</h2>

  <div>Este documento fornece as informações necessárias para executar o código da API da Loja, que gerencia as categorias dos produtos. A API foi escrita em C# usando   o framework Microsoft ASP.NET Core e o Entity Framework Core para acesso aos dados. O código fornece as seguintes funcionalidades:
  </div>
  <ul>
    <li>POST - Adiciona uma nova categoria</li>
    <li>GET - Retorna a lista de todas as categorias</li>
    <li>DELETE - Exclui uma categoria</li>
  </ul>
<h3>Pré-requisitos</h3>
  <ul>
    <li>Visual Studio (2019 ou superior)</li>
    <li>.NET Core SDK (3.1 ou superior)</li>
    <li>Banco de dados SQL Server</li>
  </ul>  
<h2>Configuração</h2>
  <ol>
    <li>Clone o repositório do código</li>
    <li>Abra a solução LojaApi.sln no Visual Studio</li>
    <li>Crie um novo banco de dados no SQL Server</li>
    <li>Configure a conexão com o banco de dados no arquivo appsettings.json</li>
    <li>No Package Manager Console, execute o comando Update-Database para criar as tabelas no banco de dados</li>
    <li>Pressione F5 para executar o projeto</li>
  <ol>  
<h2>Endpoints</h2>
  <h3>POST /categorias</h3>

    <div>Este endpoint adiciona uma nova categoria ao banco de dados. O corpo da solicitação deve ser um objeto JSON com os seguintes campos:</div>

  <ul>
    <li>`Nome` (string) - O nome da categoria</li>
    <li>`DataCadastro` (datetime) - A data de cadastro da categoria</li>
    <li>`Departamento` (string) - O departamento da categoria</li>
  </ul>
