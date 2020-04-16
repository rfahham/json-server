https://devpleno.com/json-server-como-criar-uma-rest-api-para-testes-de-forma-simples/

Primeiro vamos instalar:

$ npm install -g json-server


$ json-server --watch db.json

o arquivo db.json tem um esquema json


a página responde na seguinte url

https://localhost:3000/relatorios


https://medium.com/@MiltonFilho/testando-apis-com-postman-7ead94d38a0f

https://medium.com/@thi_carva/testando-servi%C3%A7os-web-api-com-postman-874ac81b20a3


Para fazer o post

post https://localhost:3000/relatorios

informar no body

{
    "id": 5,
    "time": "recomenda",
    "name": "cassandra recomendação"
}

Para fazer delete e put precisa passar o id na url.

para deletar um registro:

del https://localhost:3000/relatorios/5

para fazer uma atualização

put https://localhost:3000/relatorios/5

{
    "id": 5,
    "time": "recomendação",
    "name": "cassandra recomendação"
}



Criando um registro com CURL

curl -d '{"id": 16, "name": "Outros"}' -X POST http://localhost:3000/relatorios -H "Content-Type: application/json"


Alterando o registro

curl -d '{"id": 16, "name": "Outros Novos"}' -X PUT http://localhost:3000/relatorios/16 -H "Content-Type: application/json"


Apagando o registro

curl -X DELETE http://localhost:3000/relatorios/16


