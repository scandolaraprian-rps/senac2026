ANALISE_REQRES_Rian

* **Verbo HTTP:** [Ex: GET, POST, PUT, DELETE]
* **URL Completa:** [Cole a URL testada aqui]
* **Body da Requisição:** [Teve que enviar algum JSON? Se não, escreva "Nenhum"]
* **Status Code Esperado:** [Ex: 200 OK, 201 Created, 404 Not Found]
* **Resposta da API (Exemplo do JSON):**

Cenário A: Buscar a lista de utilizadores da página 2
GET
https://reqres.in/api/users?page=2
Nenhum 
200 ok

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
        },
        {
            "id": 8,
            "email": "lindsay.ferguson@reqres.in",
            "first_name": "Lindsay",
            "last_name": "Ferguson",
            "avatar": "https://reqres.in/img/faces/8-image.jpg"
        },
        {
            "id": 9,
            "email": "tobias.funke@reqres.in",
            "first_name": "Tobias",
            "last_name": "Funke",
            "avatar": "https://reqres.in/img/faces/9-image.jpg"
        },
        {
            "id": 10,
            "email": "byron.fields@reqres.in",
            "first_name": "Byron",
            "last_name": "Fields",
            "avatar": "https://reqres.in/img/faces/10-image.jpg"
        },
        {
            "id": 11,
            "email": "george.edwards@reqres.in",
            "first_name": "George",
            "last_name": "Edwards",
            "avatar": "https://reqres.in/img/faces/11-image.jpg"
        },
        {
            "id": 12,
            "email": "rachel.howell@reqres.in",
            "first_name": "Rachel",
            "last_name": "Howell",
            "avatar": "https://reqres.in/img/faces/12-image.jpg"
        }
    ],
    "support": {
        "url": "https://benhowdle.im/first-cto-playbook?utm_source=reqres&utm_medium=json&utm_campaign=referral",
        "text": "Become a better CTO. A playbook of painful stories and practical advice from a two-time startup CTO."
    },
    "_meta": {
        "powered_by": "ReqRes",
        "docs_url": "https://app.reqres.in/documentation",
        "upgrade_url": "https://app.reqres.in/upgrade",
        "example_url": "https://app.reqres.in/examples/notes-app",
        "variant": "v1_a",
        "message": "Your data persists here. Add auth, logs, and custom schemas to build a real backend.",
        "cta": {
            "label": "See example app",
            "url": "https://app.reqres.in/examples/notes-app"
        },
        "context": "legacy_success"
    }
}

Cenário B Criar Novo Usuário

POST
https://reqres.in/api/users
JSON {
    "name": "Rian",
    "job": "Advogado"
}
201 Created

{
    "name": "Rian",
    "job": "Advogado",
    "id": "847",
    "createdAt": "2026-07-03T23:35:22.901Z",
    "_meta": {
        "powered_by": "ReqRes",
        "docs_url": "https://app.reqres.in/documentation",
        "upgrade_url": "https://app.reqres.in/upgrade",
        "example_url": "https://app.reqres.in/examples/notes-app",
        "variant": "v1_a",
        "message": "Your data persists here. Add auth, logs, and custom schemas to build a real backend.",
        "cta": {
            "label": "See example app",
            "url": "https://app.reqres.in/examples/notes-app"
        },
        "context": "legacy_success"
    }
}

Cenário C: Tentar procurar um utilizador que não existe (ex: utilizador com ID 23) e capturar o
erro devolvido pela API.

GET
https://reqres.in/api/users/123
Nenhum
404 Not Found

{}