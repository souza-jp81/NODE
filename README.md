<div align="center">

🚀 API de Cadastro de Usuários — Node.js

API REST com Express, Prisma e MongoDB

<p>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express">
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
</p>



</div>

📌 Sobre o projeto

Este repositório contém uma API REST para gerenciamento de usuários, desenvolvida com Node.js e Express e conectada a um banco de dados MongoDB por meio do Prisma ORM.

A aplicação implementa as operações essenciais de um CRUD: cadastrar, listar, atualizar e excluir usuários. O modelo de dados possui os campos name, email e age, com identificação automática e restrição de unicidade para o e-mail.

O projeto funciona como back-end do repositório devclub-cadastro-usuarios.

✨ Funcionalidades

✅ Cadastro de usuários.

✅ Listagem de todos os usuários.

✅ Atualização de dados por ID.

✅ Exclusão de usuários por ID.

✅ Persistência de dados em MongoDB.

✅ Comunicação com o banco por meio do Prisma ORM.

✅ Suporte a requisições JSON.

✅ CORS habilitado para integração com aplicações front-end.

✅ Execução em modo de desenvolvimento com node --watch.

🧱 Arquitetura atual

NODE/
├── prisma/
│   └── schema.prisma
├── .gitignore
├── package.json
├── package-lock.json
├── server.js
└── yarn.lock

Principais arquivos

Arquivo

Responsabilidade

server.js

Inicialização do Express e definição das rotas da API

prisma/schema.prisma

Configuração do banco e modelo User

package.json

Dependências e scripts do projeto

.gitignore

Arquivos que não devem ser versionados

🗃️ Modelo de dados

User
├── id: String / ObjectId
├── name: String
├── email: String único
└── age: Int

🔌 Endpoints

A API é executada, por padrão, em:

http://localhost:3000

Método

Endpoint

Função

GET

/usuarios

Lista todos os usuários

POST

/usuarios

Cadastra um novo usuário

PUT

/usuarios/:id

Atualiza um usuário existente

DELETE

/usuarios/:id

Exclui um usuário

Exemplo de corpo da requisição

{
  "name": "João Paulo",
  "email": "usuario@email.com",
  "age": 45
}

🛠️ Tecnologias utilizadas

Node.js — ambiente de execução JavaScript.

Express 5 — criação do servidor e rotas HTTP.

Prisma ORM — acesso e modelagem dos dados.

MongoDB — banco de dados NoSQL.

CORS — integração com aplicações executadas em outra origem.

dotenv — suporte a variáveis de ambiente.

JavaScript ES Modules — sistema de módulos utilizado no projeto.

▶️ Como executar

Pré-requisitos

Node.js;

npm ou Yarn;

acesso a uma instância MongoDB.

1. Clone o repositório

git clone https://github.com/souza-jp81/NODE.git
cd NODE

2. Instale as dependências

npm install

3. Configure as variáveis de ambiente

Crie um arquivo .env na raiz do projeto:

DATABASE_URL="sua_string_de_conexao_mongodb"

Nunca publique senhas, tokens ou strings de conexão reais no GitHub.

4. Gere o Prisma Client

npx prisma generate

5. Inicie a API

npm run dev

🔗 Integração com o front-end

Este back-end pode ser utilizado em conjunto com:

👉 devclub-cadastro-usuarios

O front-end utiliza Axios e está configurado para consumir a API local na porta 3000.

🔐 Segurança

Credenciais e segredos de infraestrutura não devem ser armazenados no código-fonte.

Boas práticas recomendadas:

usar .env para DATABASE_URL;

manter .env no .gitignore;

rotacionar imediatamente qualquer credencial que tenha sido publicada;

não armazenar tokens, senhas ou chaves em comentários;

utilizar variáveis de ambiente também em produção.

🎯 Conceitos praticados

API REST e métodos HTTP.

CRUD.

Rotas e parâmetros dinâmicos.

Programação assíncrona com async/await.

Integração entre Node.js e banco de dados.

Prisma ORM e MongoDB.

CORS.

Integração front-end/back-end.

🚀 Próximas melhorias

Adicionar validação de dados com Zod, Joi ou biblioteca equivalente.

Implementar tratamento centralizado de erros.

Retornar 404 para usuários inexistentes.

Separar rotas, controllers e services.

Criar variável PORT.

Adicionar testes automatizados.

Documentar a API com Swagger/OpenAPI.

Implementar paginação e filtros.

Adicionar autenticação e autorização.

Criar deploy da API.

👨‍💻 Autor

Desenvolvido por João Paulo Campos de Souza como parte da evolução em desenvolvimento Full Stack.





<div align="center">

Back-end, dados e APIs como próximos passos na construção de soluções Full Stack.

⭐ Se este projeto foi útil para você, considere deixar uma estrela.

</div>
