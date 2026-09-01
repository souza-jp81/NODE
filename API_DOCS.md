# 🔌 Documentação de API — API REST de Cadastro de Usuários

> **Base URL:** `http://localhost:3000 | https://api-usuarios.vercel.app`

## 📋 Resumo dos Endpoints

| Método | Rota | Descrição |
| :--- | :--- | :--- |
| **GET** | `/usuarios` | Retorna todos os usuários cadastrados |
| **POST** | `/usuarios` | Cria um novo usuário no banco de dados MongoDB |
| **PUT** | `/usuarios/:id` | Atualiza os dados de um usuário pelo ID |
| **DELETE** | `/usuarios/:id` | Remove um usuário do banco de dados pelo ID |

## 🔍 Detalhamento das Requisições

### GET `/usuarios`

**Descrição:** Retorna todos os usuários cadastrados

**Exemplo de Resposta (200 OK / 201 Created):**
```json
{
  "status": "success",
  "message": "Operação realizada com sucesso",
  "data": [{ "id": "64f1a2...", "name": "João Paulo" }]
}
```

---

### POST `/usuarios`

**Descrição:** Cria um novo usuário no banco de dados MongoDB

**Corpo da Requisição (Request Body):**
```json
{
  "name": "João",
  "email": "joao@email.com",
  "age": 28
}
```

**Exemplo de Resposta (200 OK / 201 Created):**
```json
{
  "status": "success",
  "message": "Operação realizada com sucesso",
  "data": {
  "name": "João",
  "email": "joao@email.com",
  "age": 28
}
}
```

---

### PUT `/usuarios/:id`

**Descrição:** Atualiza os dados de um usuário pelo ID

**Corpo da Requisição (Request Body):**
```json
{
  "name": "João Paulo",
  "email": "jp@email.com"
}
```

**Exemplo de Resposta (200 OK / 201 Created):**
```json
{
  "status": "success",
  "message": "Operação realizada com sucesso",
  "data": {
  "name": "João Paulo",
  "email": "jp@email.com"
}
}
```

---

### DELETE `/usuarios/:id`

**Descrição:** Remove um usuário do banco de dados pelo ID

**Exemplo de Resposta (200 OK / 201 Created):**
```json
{
  "status": "success",
  "message": "Operação realizada com sucesso",
  "data": [{ "id": "64f1a2...", "name": "João Paulo" }]
}
```

---

