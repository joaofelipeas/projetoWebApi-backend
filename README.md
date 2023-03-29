
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

Este endpoint adiciona uma nova categoria ao banco de dados. O corpo da solicitação deve ser um objeto JSON com os seguintes campos:

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

Este endpoint retorna a lista de todas as categorias no banco de dados.

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

  O código apresenta algumas vulnerabilidades que podem ser exploradas por um invasor mal-intencionado:

<ul>
  <li>Falta de autenticação e autorização: qualquer pessoa pode acessar os endpoints da API sem autenticação ou autorização, o que pode permitir ações não autorizadas no banco de dados.</li>
  <li>Injeção de SQL: os parâmetros do SQL não são sanitizados corretamente, permitindo que um invasor mal-intencionado injete código SQL para executar ações não autorizadas no banco de dados.</li>
  <li>Validação</li>
</ul>

# Documentação do código DataContext

  Este documento fornece as informações necessárias para entender e utilizar o código DataContext da API da Loja. DataContext é uma classe que herda de DbContext e fornece uma conexão com o banco de dados para a API. O código foi escrito em C# usando o Entity Framework Core.
  
## Pré-requisitos

<ul>
  <li>Microsoft.EntityFrameworkCore (3.1 ou superior)</li>
  <li>Microsoft.EntityFrameworkCore.SqlServer (3.1 ou superior)</li>
</ul>

## Uso

  A classe DataContext é uma classe genérica que permite o acesso a um banco de dados específico. No caso da API da Loja, a classe permite o acesso à tabela Categoria do banco de dados.

  Para utilizar a classe DataContext, basta instanciá-la e passar as opções de configuração do DbContext no construtor. Por exemplo:

<p>
<div align="center">
  <img src="https://user-images.githubusercontent.com/104281444/228645311-d79a2f56-029d-4e64-9d5b-749fbe773cf6.jpg" width="700"/>
</div>
</p>

## Propriedades

  Categorias (DbSet<Categoria>) - A tabela Categoria do banco de dados.

## Vulnerabilidades

  Não existem vulnerabilidades conhecidas no código DataContext. No entanto, a segurança da conexão com o banco de dados depende das configurações adequadas da conexão e das permissões de usuário no banco de dados.
  
# Documentação do código Categoria

  Este documento fornece as informações necessárias para entender e utilizar o código Categoria da API da Loja. Categoria é uma classe que representa uma categoria de produtos da loja. O código foi escrito em C# usando a biblioteca padrão do .NET.
  
## Propriedades

<ul>
  <li>`Id` (int) - O identificador único da categoria. É gerado automaticamente pelo banco de dados.</li>
  <li>`Nome` (string) - O nome da categoria. É obrigatório e deve ter pelo menos 5 caracteres.</li>
  <li>`Departamento` (string) - O departamento da categoria (opcional).</li>
  <li>`DataCadastro` (DateTime) - A data de cadastro da categoria. É definido automaticamente como a data e hora do sistema quando a categoria é criada.</li>
</ul>

## Vulnerabilidades

Não existem vulnerabilidades conhecidas no código Categoria. No entanto, é importante lembrar que a validação de entrada é essencial para evitar ataques de injeção de código malicioso. Além disso, é importante manter o código atualizado e aplicar patches de segurança para proteger a aplicação contra vulnerabilidades conhecidas.

---

<p>
<div align="center">
  <img src="https://user-images.githubusercontent.com/104281444/228647522-2236e343-2e2c-4c40-8298-f3632d8845ea.jpg" width="700"/>
</div>
</p>
