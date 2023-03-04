
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
"bio": "escreva sobre você"<br/>
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
"img": "url de imagem aqui",<br/>
"content": "conteúdo da postagem aqui",<br/>
"likes": 0<br/>
}<br/>

***Obs: é necessário o envio do token para autorização***

### Todos os posts

GET /posts

***Obs: Não existe corpo de requisição, é necessário envio do token***

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

***Obs: Envio do token é obrigatório, "postId" se refere ao id do post a ser comentado***

### Obter comentário de um post

GET /posts/id_do_post/comments

***Obs: É necessário envio do token***


### Obter likes de um post

GET /posts/id_do_post/likes

***Obs: É necessário envio do token***

___
### Curtir publicação

***Desenvolvendo***

# Tech-Zone-API
