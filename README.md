# Json_server


## Install
npm install json-server
npm install -g json-server


## Usage
Create a db.json or db.json5 file

{
  "posts": [
    { "id": "1", "title": "a title", "views": 100 },
    { "id": "2", "title": "another title", "views": 200 }
  ],
  "comments": [
    { "id": "1", "text": "a comment about post 1", "postId": "1" },
    { "id": "2", "text": "another comment about post 1", "postId": "1" }
  ],
  "profile": {
    "name": "typicode"
  }
}

## Run json-server

$ npx json-server db.json

Este comando fica escutando as alterações em tempo real e salvando o arquivo de dados.
$ json-server --watch db.json


A página vai responder na seguinte url:

https://localhost:3000/times





Para deletar um registro:

OBS. Para fazer delete e put precisa passar o id na url.

del https://localhost:3000/relatorios/5

Para fazer uma atualização

put https://localhost:3000/relatorios/5

{
    "id": 5,
    "time": "recomendação",
    "name": "cassandra recomendação"
}

------------------------------------------------------




Alterando o registro:

curl -d '{"id": 16, "name": "Outros Novos"}' -X PUT http://localhost:3000/relatorios/16 -H "Content-Type: application/json"


Apagando o registro:

curl -X DELETE http://localhost:3000/relatorios/16



Fontes:

https://devpleno.com/json-server-como-criar-uma-rest-api-para-testes-de-forma-simples/

https://medium.com/@MiltonFilho/testando-apis-com-postman-7ead94d38a0f

https://medium.com/@thi_carva/testando-servi%C3%A7os-web-api-com-postman-874ac81b20a3


