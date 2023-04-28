API EatSmart
________________________________________________________________________________________________________________

=>GET BUSAR TODOS USUÁRIOS (tanto os usuários consumidores, quanto as empresas)

*Apenas usuários logados podem visualizar todos os usuários;

Rota: https://json-server-projeto-front-end.onrender.com/users;

Tipo de rota: 'GET' para buscar todos os usuários;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };


Content-Type: application/json;

Body: O corpo de requisição NÃO é necessário.

*Apenas usuários logados podem visualizar todos os usuários. Não esquecer o token do usuário logado no authorization.
________________________________________________________________________________________________________________

=>GET BUSAR USUÁRIO PELO ID

Rota: https://json-server-projeto-front-end.onrender.com/users/{ID do usuário};

Tipo de rota: 'GET' para buscar um usuário;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };


Content-Type: application/json;

Body: O corpo de requisição NÃO é necessário;

*Apenas usuários logados podem visualizar os usuários. Não esquecer de passar o ID do usuário na rota e o token do usuário logado no authorization.
________________________________________________________________________________________________________________

=>POST LOGIN USUÁRIO

Rota: https://json-server-projeto-front-end.onrender.com/login;

Tipo de rota: 'POST' para realizar o login de um usuário;

Não é necessário envio de token de autenticação;

Content-Type: application/json;

Body: O corpo de requisição deve ser exatamente no seguinte formato:
{
	"email": "joao@mail.com",
	"password": "123456"
}.
________________________________________________________________________________________________________________

=>POST CRIAR USUÁRIO

Rota: https://json-server-projeto-front-end.onrender.com/register;

Tipo de rota: 'POST' para criar um novo usuário;

Não é necessário envio de token de autenticação;

Content-Type: application/json;

Body: O corpo de requisição deve ser exatamente no seguinte formato:
{
	"email": "joao@mail.com",
	"password": "123456",
	"confirmPassword": "123456",
	"userName": "João da Silva",
	"isCompany": false
};

*O campo “id” é preenchido automaticamente pela API.
________________________________________________________________________________________________________________

=>PATCH EDITAR USUÁRIO

Rota: https://json-server-projeto-front-end.onrender.com/register/{ID do usuário};

Tipo de rota: 'PATCH' para editar um usuário;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };

Content-Type: application/json;

Body: O corpo de requisição deve contar, ao menos, um dos campos no seguinte formato:
{
     	"email": "joao@mail.com",
    	"password": "123456",
	"confirmPassword": "123456",
     	"userName": "João da Silva"
};

*Apenas o usuário logado pode editar o seu próprio cadastro. Não esquecer de passar o ID na rota e o token do usuário logado no authorization.
________________________________________________________________________________________________________________

=>DELETE EXCLUIR USUÁRIO

Rota: https://json-server-projeto-front-end.onrender.com/register/{ID do usuário};

Tipo de rota: 'DELETE' para excluir um usuário;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };

Content-Type: application/json;

Body: O corpo de requisição NÃO é necessário;

*Apenas o usuário logado pode excluir o seu próprio cadastro. Não esquecer de passar o ID na rota e o token do usuário logado no authorization.

________________________________________________________________________________________________________________

=>POST LOGIN EMPRESA

Rota: https://json-server-projeto-front-end.onrender.com/signin;

Tipo de rota: 'POST' para realizar o login de uma empresa;

Não é necessário envio de token de autenticação;

Content-Type: application/json;

Body: O corpo de requisição deve ser exatamente no seguinte formato:
{
	"email": "deliciasdaterra@mail.com",
	"password": "123456"
}.
________________________________________________________________________________________________________________

=>POST CRIAR EMPRESA

Rota: https://json-server-projeto-front-end.onrender.com/signup;

Tipo de rota: 'POST' para criar uma nova empresa;

Não é necessário envio de token de autenticação;

Content-Type: application/json;

Body: O corpo de requisição deve ser exatamente no seguinte formato:
{
	"userName": "No Céu tem pão?",
 	"email": "pao@mail.com",
	"password": "123456",
 	"confirmPassword": "123456",
	"typeOfCompany": "panificação",
 	"isCompany" : true
};

*O campo “id” é preenchido automaticamente pela API.
________________________________________________________________________________________________________________

=>PATCH EDITAR EMPRESA

Rota: https://json-server-projeto-front-end.onrender.com/signup/{ID da empresa};

Tipo de rota: 'PATCH' para editar uma empresa;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };

Content-Type: application/json;

Body: O corpo de requisição deve contar, ao menos, um dos campos no seguinte formato:
{
	"userName": "No Céu tem pão?",
	"email": "pao@mail.com",
	"password": "123456",
	"confirmPassword": "123456",
	"typeOfCompany": "panificação"
};

*Apenas a empresa logada pode editar as suas próprias informções. Não esquecer de passar o ID da empresa na rota e o token da empresa logada no authorization.
________________________________________________________________________________________________________________

=>DELETE EXCLUIR EMPRESA

Rota: https://json-server-projeto-front-end.onrender.com/signup/{ID da empresa};

Tipo de rota: 'DELETE' para excluir uma empresa;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };

Content-Type: application/json;

Body: O corpo de requisição NÃO é necessário;

*Apenas a empresa logada pode excluir seu próprio perfil. Não esquecer de passar o ID da empresa na rota e o token da empresa logada no authorization.
________________________________________________________________________________________________________________

=>GET BUSAR TODOS OS PRODUTOS

Rota: https://json-server-projeto-front-end.onrender.com/products;

Tipo de rota: 'GET' para buscar todos os produtos;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };


Content-Type: application/json;

Body: O corpo de requisição NÃO é necessário;

*Apenas usuários logados podem visualizar todos os produtos. Não esquecer o token do usuário logado no authorization.
________________________________________________________________________________________________________________

=>GET BUSAR PRODUTO PELO ID

Rota: https://json-server-projeto-front-end.onrender.com/products/{ID do produto};

Tipo de rota: 'GET' para buscar os produtos;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };


Content-Type: application/json;

Body: O corpo de requisição NÃO é necessário;

*Apenas usuários logados podem visualizar os produtos. Não esquecer de passar o ID do produto na rota e o token da empresa logada no authorization.
________________________________________________________________________________________________________________

=>POST CRIAR PRODUTO

*Apenas empresas logados podem criar novos produtos;

Rota: https://json-server-projeto-front-end.onrender.com/products;

Tipo de rota: 'POST' para criar um novo produto;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };

Content-Type: application/json;

Body: O corpo de requisição deve ser exatamente no seguinte formato:
{
      "title": "Pão na chapa",
      "originalPrice": 10,
      "discount": 50,
      "quantity": 7,
      "userId": 2
    };
    
*Apenas a empresa logada pode criar um novo produto. Não esquecer de passar o token da empresa logada no authorization.

* No campo "userId" deve ser informado o id da empresa que está cadastrando o produto;

*O campo “id” é preenchido automaticamente pela API.
________________________________________________________________________________________________________________

=>PATCH EDITAR PRODUTO

Rota: https://json-server-projeto-front-end.onrender.com/products/{ID do produto};

Tipo de rota: 'PATCH' para editar um produto;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };

Content-Type: application/json;

Body: O corpo de requisição deve contar, ao menos, um dos campos no seguinte formato:
{
	"title": "Pão na chapa",
	"originalPrice": 10,
	"discount": 50,
	"quantity": 7
};

*Apenas a empresa logada pode editar o seu próprio produto. Não esquecer de passar o ID do produto na rota e o token da empresa logada no authorization.
________________________________________________________________________________________________________________

=>DELETE EXCLUIR PRODUTO

Rota: https://json-server-projeto-front-end.onrender.com/products/{ID do produto};

Tipo de rota: 'DELETE' para excluir um produto;

É necessário envio de token de autenticação no formato:
headers: {
            Authorization: `Bearer ${token}`,
          };

Content-Type: application/json;

Body: O corpo de requisição NÃO é necessário;

*Apenas a empresa logada pode excluir o seu próprio produto. Não esquecer de passar o ID do produto na rota e o token da empresa logada no authorization.

________________________________________________________________________________________________________________

Query Parameters

