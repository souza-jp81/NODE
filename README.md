# API REST de Cadastro de Usuários — Node.js

> API REST robusta e escalável para gerenciamento de usuários com persistência em banco NoSQL.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE) [![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-black?logo=github)](https://github.com/souza-jp81/NODE) 

## 📌 Visão Geral do Projeto

Este repositório contém a implementação profissional de **API REST de Cadastro de Usuários — Node.js**. O projeto foi estruturado seguindo as melhores práticas de desenvolvimento, promovendo alta manutenibilidade, arquitetura limpa e padrão de código.

### 🚀 Principais Funcionalidades

- ✨ Servidor Express configurado com roteamento HTTP modular
- ✨ Operações CRUD completas (GET, POST, PUT, DELETE)
- ✨ Modelagem de dados e migrations NoSQL via Prisma ORM
- ✨ Persistência de dados em cluster MongoDB Atlas
- ✨ Manipulação segura de variáveis de ambiente com dotenv
- ✨ Tratamento e suporte a requisições Cross-Origin (CORS)
- ✨ Programação assíncrona robusta utilizando suporte a Async/Await

## 🛠️ Tecnologias & Ferramentas

`Node.js` • `Express.js` • `JavaScript (ES6+)` • `Prisma ORM` • `MongoDB` • `CORS` • `dotenv`

## 📐 Arquitetura da Solução

```mermaid
graph TD
    classDef client fill:#1e293b,stroke:#0284c7,stroke-width:2px,color:#fff;
    classDef server fill:#0f172a,stroke:#16a34a,stroke-width:2px,color:#fff;
    classDef db fill:#1e1b4b,stroke:#9333ea,stroke-width:2px,color:#fff;

    subgraph ClientLayer ["Front-End (React SPA)"]
        UI["React 18 + Vite Components"]:::client
        Hooks["Hooks (useState, useEffect, useRef)"]:::client
        AxiosClient["Axios HTTP Client"]:::client
    end

    subgraph ServerLayer ["Back-End (Node.js REST API)"]
        ExpressApp["Express.js Server"]:::server
        Middleware["CORS & Body Parser"]:::server
        Routes["HTTP Routes (/usuarios)"]:::server
        Controllers["User Controllers (CRUD Logic)"]:::server
        PrismaORM["Prisma ORM Client"]:::server
    end

    subgraph DatabaseLayer ["Database"]
        MongoDB[("MongoDB Atlas NoSQL")]:::db
    end

    UI --> Hooks
    Hooks --> AxiosClient
    AxiosClient -- "REST HTTP (JSON)" --> ExpressApp
    ExpressApp --> Middleware
    Middleware --> Routes
    Routes --> Controllers
    Controllers --> PrismaORM
    PrismaORM -- "Async Queries" --> MongoDB
```

## ⚙️ Como Executar o Projeto Localmente

### Pré-requisitos

- [Node.js](https://nodejs.org/) (Versão 18 ou superior)
- Gerenciador de pacotes `npm` ou `yarn`
- Conta no [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) (ou banco local)

### Passo a Passo

1. **Clonar o repositório:**
```bash
git clone https://github.com/souza-jp81/NODE.git
cd api-rest-de-cadastro-de-usu-rios---node-js
```

2. **Instalar as dependências:**
```bash
npm install
```

3. **Configurar as Variáveis de Ambiente:**
Crie um arquivo `.env` na raiz do projeto baseado no arquivo `.env.example`:
```env
DATABASE_URL="mongodb+srv://usuario:senha@cluster.mongodb.net/meubanco?retryWrites=true&w=utf8"
PORT=3000
```

4. **Sincronizar o Prisma ORM:**
```bash
npx prisma db push
```

5. **Iniciar o Servidor de Desenvolvimento:**
```bash
npm run dev
```

## 📐 Arquitetura do Sistema

   
```mermaid
   graph TD
       A[Front-end React] -->|Requisição HTTP / JSON| B[API Express Node.js]
       B -->|Prisma ORM| C[(Banco MongoDB Atlas)]
   
```

## 👤 Autor

**João Paulo Campos de Souza**  
 Full Stack Developer | Node.js | React | Health Tech & Data  
- 💼 **LinkedIn:** [linkedin.com/in/devsouzajp](https://linkedin.com/in/devsouzajp/)
- 📬 **E-mail:** [jpcsonline@gmail.com](mailto:jpcsonline@gmail.com)
- 🐙 **GitHub:** [@souza-jp81](https://github.com/souza-jp81)

---
*Licenciado sob a [Licença MIT](LICENSE).*
