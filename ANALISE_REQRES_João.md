Documentação de Análise da API - ReqRes
Feito por: João

Cenário A: Ver a lista de utilizadores da página 2

Verbo HTTP usado: GET
Link (URL) que testei: https://reqres.in/api/users?page=2
Corpo (Body) enviado: Nenhum. Como era só para ler a lista, não precisei enviar nenhuma informação em JSON para o servidor.
Status Code esperado: 200 OK (deu tudo certo!)
Resposta que recebi da API:

(Nota: Colei aqui só o primeiro utilizador para o texto não ficar gigante, mas quando cliquei no botão, a API me devolveu os 6 utilizadores dessa página certinho).

{
"page": 2,
"per_page": 6,
"total": 12,
"total_pages": 2,
"data": [
{
"id": 7,
"email": "michael.lawson@reqres.in",
"first_name": "Michael",
"last_name": "Lawson",
"avatar": "https://reqres.in/img/faces/7-image.jpg"
}
]
}

Cenário B: Criar um utilizador novo com o meu nome

Verbo HTTP usado: POST (mudei o verbo porque agora a ideia era eu enviar os meus dados para lá).
Link (URL) que testei: https://reqres.in/api/users
Corpo (Body) enviado: Sim. Dessa vez escrevi os meus dados num JSON e enviei assim:
{
"name": "João",
"job": "Desenvolvedor Front-end"
}
Status Code esperado: 201 Created (que significa que o perfil foi criado com sucesso).
Resposta que recebi da API:

(Nota: A API não só confirmou os dados que enviei, mas também já gerou um ID e a data de criação).

{
"name": "João",
"job": "Desenvolvedor Front-end",
"id": "789",
"createdAt": "2026-07-03T10:15:30.000Z"
}

Cenário C: Procurar um utilizador que não existe

Verbo HTTP usado: GET (voltei para o GET porque era só uma tentativa de busca).
Link (URL) que testei: https://reqres.in/api/users/23
Corpo (Body) enviado: Nenhum.
Status Code esperado: 404 Not Found (Deu erro de propósito! Como o utilizador 23 não existe no banco deles, esse é o erro certo).
Resposta que recebi da API:

(Nota: O sistema me respondeu com isso vazio, o que faz sentido já que não encontrou nada).

{}
