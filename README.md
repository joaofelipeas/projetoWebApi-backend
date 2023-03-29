# projetoWebApi-backend

# Projeto Web: .NET 6 Web API + HTML + CSS + JS

  <strong>Projeto de Desenvolvimento de uma Web API com DOTNET 6 utilizando o VSCode. Criado em 2 pastas diferentes projetoWebAPI-backend / projetoWebApi-frontend. Utilizando Microsoft Entity Framework Core(Design/InMemory) para salvar os dados no Banco de Dados em um banco em memória. Foram utilizadas os métodos Post, Get e Delete.</strong>

----

# Documentação do código LojaApi

  Este documento fornece as informações necessárias para executar o código da API da Loja, que gerencia as categorias dos produtos. A API foi escrita em C# usando   o framework Microsoft ASP.NET Core e o Entity Framework Core para acesso aos dados. O código fornece as seguintes funcionalidades:
  
  <ul>
    <li>POST - Adiciona uma nova categoria</li>
    <li>GET - Retorna a lista de todas as categorias</li>
    <li>DELETE - Exclui uma categoria</li>
  </ul>
  
## Pré-requisitos
  
  <ul>
    <li>Visual Studio (2019 ou superior)</li>
    <li>.NET Core SDK (3.1 ou superior)</li>
    <li>Banco de dados SQL Server</li>
  </ul> 
  
## Configuração
  
  <ol>  
      <li>Clone o repositório do código</li>      
      <li>Abra a solução LojaApi.sln no Visual Studio</li>      
      <li>Crie um novo banco de dados no SQL Server</li>      
      <li>Configure a conexão com o banco de dados no arquivo appsettings.json</li>      
      <li>No Package Manager Console, execute o comando Update-Database para criar as tabelas no banco de dados</li>      
      <li>Pressione F5 para executar o projeto</li>
  </ol>   
  
## Endpoints

POST /categorias

<p>Este endpoint adiciona uma nova categoria ao banco de dados. O corpo da solicitação deve ser um objeto JSON com os seguintes campos:</p>

  <ul>
    <li>`Nome` (string) - O nome da categoria</li>
    <li>`DataCadastro` (datetime) - A data de cadastro da categoria</li>
    <li>`Departamento` (string) - O departamento da categoria</li>
  </ul>
</br>

Exemplo de solicitação:

<p> 
<div align="center">
  <img src="https://user-images.githubusercontent.com/104281444/228407235-0ccd1ca0-24fc-40e3-b292-d00298e6ea0d.jpg" width="700"/>
</div>
</p>

Exemplo de resposta:

<p> 
<div align="center">
  <img src="https://user-images.githubusercontent.com/104281444/228407235-0ccd1ca0-24fc-40e3-b292-d00298e6ea0d.jpg" width="700"/>
</div>
</p>

GET /categorias

<p>Este endpoint retorna a lista de todas as categorias no banco de dados.</p>

Exemplo de resposta:

<p>
<div align="center">
  <img src="https://user-images.githubusercontent.com/104281444/228410506-a890e3b3-e579-4fc2-bb0f-7ab65513bf02.jpg" width="700"/>
</div>
</p>

DELETE /categorias/{id}

<p>Este endpoint exclui a categoria com o ID especificado do banco de dados.</p>

Exemplo de solicitação:

<p>
<div align="center">
  <img src="https://user-images.githubusercontent.com/104281444/228411634-67c809ad-9402-46b2-b2d6-603ac1484081.jpg" width="700"/>
</div>
</p>

Exemplo de resposta:

<p>
<div align="center">
  <img src="https://user-images.githubusercontent.com/104281444/228411858-bed67ad6-40a5-4997-be0f-acca590c6455.jpg" width="700"/>
</div>
</p>

## Vulnerabilidades

<p>O código apresenta algumas vulnerabilidades que podem ser exploradas por um invasor mal-intencionado:</p>

<ul>
  <li>Falta de autenticação e autorização: qualquer pessoa pode acessar os endpoints da API sem autenticação ou autorização, o que pode permitir ações não autorizadas no banco de dados.</li>
  <li>Injeção de SQL: os parâmetros do SQL não são sanitizados corretamente, permitindo que um invasor mal-intencionado injete código SQL para executar ações não autorizadas no banco de dados.</li>
  <li>Validação</li>
</ul>
