# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Projetos Front-end.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /users

Corpo da requisição:<br/>
{<br/>
"name": "seu nome aqui",<br/>
"email": "email@mail.com",<br/>
"password": "123456",<br/>
"profile_img": "link de uma imagem",<br/>
"age": "sua idade",<br/>
"city": "São Paulo"<br/>
}<br/>

### Login

POST /login

Corpo da requisição:<br/>
{<br/>
"email": "email@mail.com",<br/>
"password": "123456"<br/>
}<br/>

### Postar Publicação

POST /posts

Corpo da requisição:<br/>
{<br/>
"userId": id do seu usuário aqui,<br/>
"title": "título do post aqui",<br/>
"img": "url de imagem aqui",<br/>
"content": "conteúdo da postagem aqui",<br/>
"likes": 0<br/>
}<br/>

Obs: é necessário o envio do token para autorização

### Todos os posts

GET /posts

**_Não existe corpo de requisição e não é necessário envio do token_**

### Comentar

POST /comments

Corpo da requisição:<br/>
{<br/>
"postId": 2,<br/>
"userId": 2,<br/>
"name": "nome do usuário que está comentando",<br/>
"profile_img": "link da imagem do usuário",<br/>
"comment": "conteúdo do comentário aqui"<br/>
}<br/>

Obs: Envio do token é obrigatório, "postId" se refere ao id do post a ser comentado.

### Curtir publicação

***Desenvolvendo***

# Tech-Zone-API
