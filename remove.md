# Removendo um registro

## Via POSTMAN

httpdel https://localhost:3000/posts

informar no body, tipo json

{
    "id": "3", 
    "title": "a title", 
    "views": 300 }

## Via Curl

curl -d '{ "id": "3", "title": "a title", "views": 300 }' -X POST http://localhost:3000/posts -H "Content-Type: application/json"