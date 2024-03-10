# Intall

https://www.hostinger.com.br/tutoriais/instalar-node-js-ubuntu


sudo yum install nodejs

sudo yum install npm
    Last metadata expiration check: 0:06:23 ago on Sun Mar 10 17:49:31 2024.
    Package nodejs-npm-1:9.8.1-1.18.18.2.1.amzn2023.0.1.x86_64 is already installed.
    Dependencies resolved.
    Nothing to do.
    Complete!

node -v
    v18.18.2

npm -v
    9.8.1



npm i json-server

    added 54 packages in 6s

    14 packages are looking for funding
    run `npm fund` for details
    npm notice 
    npm notice New major version of npm available! 9.8.1 -> 10.5.0
    npm notice Changelog: https://github.com/npm/cli/releases/tag/v10.5.0
    npm notice Run npm install -g npm@10.5.0 to update!
    npm notice 


sudo npm install -g npm@10.5.0

    added 1 package in 4s

    24 packages are looking for funding
    run `npm fund` for details
    [ec2-user@ip-172-31-0-98 ~]$ npm i json-server

    up to date, audited 55 packages in 829ms

    14 packages are looking for funding
    run `npm fund` for details

    found 0 vulnerabilities

sudo vi db.json

    {
        "posts": [
            {
                "id": "1",
                "title": "a title",
                "views": 100
            },
            {
                "id": "2",
                "title": "another title",
                "views": 200
            }
        ],
        "comments": [
            {
                "id": "1",
                "text": "a comment about post 1",
                "postId": "1"
            },
            {
                "id": "2",
                "text": "another comment about post 1",
                "postId": "1"
            }
        ],
        "profile": {
            "name": "typicode"
        }
    }

npx json-server db.json
    JSON Server started on PORT :3000
    Press CTRL-C to stop
    Watching db.json...

    ♡( ◡‿◡ )

    Index:
    http://localhost:3000/

    Static files:
    Serving ./public directory if it exists

    Endpoints:
    http://localhost:3000/posts
    http://localhost:3000/comments
    http://localhost:3000/profile


Adicionar no Security Group o TCP personalizado com o meu IP e com a porta 3000

Acessar pelo IP

    http://44.222.173.205:3000/posts
