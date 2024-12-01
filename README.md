# library api

# Como utilizar a api

Para usar este arquivo no Insomnia ou Postman:

Abra o Insomnia ou Postman
Clique em "Import"
Selecione a aba "File"
Arraste o arquivo HAR ou clique para selecioná-lo
Clique em "Import"

Você terá acesso a todas estas requisições:
Livros:

POST /books - Criar novo livro
GET /books - Listar todos os livros
GET /books/1 - Buscar livro específico
PUT /books/1 - Atualizar livro
DELETE /books/1 - Deletar livro

Usuários:

POST /users - Criar novo usuário
GET /users - Listar todos os usuários
GET /users/1 - Buscar usuário específico
PUT /users/1 - Atualizar usuário
DELETE /users/1 - Deletar usuário

Empréstimos:

POST /loans - Criar novo empréstimo
GET /loans - Listar todos os empréstimos
PUT /loans/1/return - Devolver livro
GET /loans/overdue - Listar empréstimos atrasados

Lembre-se de:

Iniciar o servidor Node.js antes de testar
Ajustar os IDs nas URLs conforme necessário
Modificar os dados nos bodies das requisições POST/PUT conforme sua necessidade

# Passo a passo

Vou te exemplificar o passo a passo como usar o Insomnia ou Postman para testar a API e adicionar dados ao banco:

1 - Primeiro, crie uma Collection no Insomnia:

Clique em "Create"
Escolha "Request Collection"
Nome: "Library API"


2 - Para adicionar um livro (POST /books):

Clique em "New Request"
Nome: "Create Book"
Método: POST
URL: http://localhost:3000/api/books
Body: JSON

{
  "title": "O Pequeno Principe",
  "author": "Antoine de Saint-Exupéry",
  "genre": "Fábula infantil",
  "publicationYear": 1943
}

3 - Para adicionar um usuário (POST /users):

Nova Request
Nome: "Create User"
Método: POST
URL: http://localhost:3000/api/users
Body: JSON

{
  "name": "João Silva",
  "email": "joao@email.com",
  "address": "Rua A, 123",
  "phone": "11999999999"
}

4 - Para criar um empréstimo (POST /loans):

Nova Request
Nome: "Create Loan"
Método: POST
URL: http://localhost:3000/api/loans
Body: JSON

{
  "userId": 1,
  "bookId": 1,
  "returnDate": "2024-12-30"
}

Importante:

Certifique-se que o servidor está rodando (npm run dev)
Verifique se o banco de dados está conectado
Os IDs (userId e bookId) precisam existir no banco


