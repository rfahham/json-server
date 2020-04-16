Fontes:

https://devpleno.com/json-server-como-criar-uma-rest-api-para-testes-de-forma-simples/

https://medium.com/@MiltonFilho/testando-apis-com-postman-7ead94d38a0f

https://medium.com/@thi_carva/testando-servi%C3%A7os-web-api-com-postman-874ac81b20a3

Primeiro vamos instalar:
$ npm install -g json-server

Crie um arquivo com o nome db.json

{
	"times": [{
		"id": 1,
		"Flamengo Campeao": [
			"1980",
			"1982",
			"1983",
			"1987 - Há controversia, rsrs",
			"1992",
			"2009",
			"2019"
		]
	}]
}


Execute o comando:
$ json-server --watch db.json

Este comando fica escutando as alterações em tempo real e salvando o arquivo de dados.


A página vai responder na seguinte url:

https://localhost:3000/times



Maniputando o arquivo db.json
------------------------------------------------------

Para fazer o post utilziando o POSTMAN

post https://localhost:3000/relatorios

informar no body

{
    "id": 5,
    "time": "recomenda",
    "name": "cassandra recomendação"
}


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

Criando um registro com CURL:

curl -d '{"id": 16, "name": "Outros"}' -X POST http://localhost:3000/relatorios -H "Content-Type: application/json"


Alterando o registro:

curl -d '{"id": 16, "name": "Outros Novos"}' -X PUT http://localhost:3000/relatorios/16 -H "Content-Type: application/json"


Apagando o registro:

curl -X DELETE http://localhost:3000/relatorios/16


