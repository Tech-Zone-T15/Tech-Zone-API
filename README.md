___
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

___
### Login

POST /login

Corpo da requisição:<br/>
{<br/>
    "email": "email@mail.com",<br/>
    "password": "123456"<br/>
}<br/>

___
### Auto Login

GET /users/user_id

***Obs: é necessário o envio do token***

___
### Postar Publicação

POST /posts

Corpo da requisição:<br/>
{<br/>
    "userId": id do seu usuário aqui,<br/>
    "img": "url de imagem aqui",<br/>
    "content": "conteúdo da postagem aqui",<br/>
}<br/>

***Obs: é necessário o envio do token para autorização***

___
### Todos os posts

GET /posts

***Obs: É necessário envio do token***

___
### Comentar

POST /comments

Corpo da requisição:<br/>
{<br/>
    "postId": 2,<br/>
    "userId": 2,<br/>
    "comment": "conteúdo do comentário aqui"<br/>
}<br/>

***Obs: Envio do token é obrigatório, "postId" se refere ao id do post a ser comentado***

___
### Obter comentários de um post

GET /posts/id_do_post/comments

***Obs: É necessário envio do token***

___
### Obter likes de um post

GET /posts/id_do_post/likes

***Obs: É necessário envio do token***

___
### Curtir publicação

POST /likes

Corpo da requisição:<br/>
{<br/>
    "postId": id do post,<br/>
    "userId": id do user logado,<br/>
}<br/>

***Obs: É necessário envio do token, será necessário verificar se já existe o like do user para aquele post, caso haja o like a requisição não deverá ser feita***

___
### Obter IDS que o usuário segue

GET /users/user_id/follow

Resposta:<br/>
[<br/>
	{
		"userId": 1,
		"follows": 2,
		"id": 1
	}
]<br/>
Obs: Para renderizar o usuário seguido será necessário fazer um GET em /users/id, no exemplo acima seria um GET em /users/2

# Tech-Zone-API
