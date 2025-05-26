## 📋 API REST Cheat Sheet

### ✅ Princípios Fundamentais

* **Stateless:** Cada requisição é independente, não armazenando estado entre chamadas.
* **Resources:** Tudo é um recurso, identificado por uma URL.
* **Representações:** Recursos são representados por formatos como JSON ou XML.
* **HTTP Verbs:** Uso apropriado de métodos HTTP para definir ações.

### ✅ Verbos HTTP

* **GET:** Recuperar recursos.
* **POST:** Criar novos recursos.
* **PUT:** Atualizar recursos existentes ou criar se não existir.
* **PATCH:** Atualização parcial de recursos.
* **DELETE:** Remover recursos.

### ✅ Status Codes Comuns

* `200 OK`: Sucesso.
* `201 Created`: Recurso criado com sucesso.
* `204 No Content`: Sucesso sem retorno de corpo.
* `400 Bad Request`: Requisição malformada.
* `401 Unauthorized`: Falta de autenticação.
* `403 Forbidden`: Acesso negado.
* `404 Not Found`: Recurso não encontrado.
* `500 Internal Server Error`: Erro no servidor.

### ✅ Boas Práticas

* Use substantivos no plural para recursos: `/users`, `/products`.
* Filtragem, ordenação e paginação via query params: `/products?page=2&limit=10`.
* Utilize status codes corretos para indicar o resultado da operação.
* Versionamento via URI ou Header: `/v1/users` ou `Accept: application/vnd.api.v1+json`.
* HATEOAS: forneça links para ações relacionadas.

### ✅ Estrutura de URL

* `/users` → Lista ou cria usuários.
* `/users/{id}` → Detalhe, atualiza ou deleta usuário específico.

### ✅ Autenticação e Autorização

* **Token-Based (JWT):** Envio de token via `Authorization: Bearer <token>`.
* **OAuth2:** Padrão para autorização delegada.
* **API Keys:** Chaves de acesso simples.

### ✅ Documentação

* **OpenAPI/Swagger:** Padrão para especificação e documentação.
* **Postman Collections:** Para testes manuais.

### ✅ Segurança

* Use HTTPS.
* Valide e sanitize entradas.
* Rate limiting e proteção contra brute-force.
* CORS adequado.

### ✅ Testes

* Testes unitários: Validar regras de negócio.
* Testes de integração: Validar endpoints.
* Ferramentas: `Jest`, `Supertest`, `Postman/Newman`.

### ✅ Exemplos de Requisição

**GET**

```http
GET /users HTTP/1.1
Host: api.example.com
Authorization: Bearer <token>
```

**POST**

```http
POST /users HTTP/1.1
Host: api.example.com
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com"
}
```

**PATCH**

```http
PATCH /users/1 HTTP/1.1
Host: api.example.com
Content-Type: application/json

{
  "name": "Jane Doe"
}
```

**DELETE**

```http
DELETE /users/1 HTTP/1.1
Host: api.example.com
Authorization: Bearer <token>
```

---

### 📚 Recursos Úteis

* [RESTful API Design - Microsoft](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design)
* [OpenAPI Specification](https://swagger.io/specification/)
* [Postman](https://www.postman.com/)
