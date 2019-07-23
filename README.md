CRUD with database Postgres and SpringBoot and Docker

Este é um exemplo de CRUD utilizando serviços REST com database Postgres, Docker, Maven, Springboot e Testes Unitários JUnit.

Para executar a aplicação é necessário seguir alguns passos (todos os comandos dentro da pasta raiz do projeto):

-> gerar a build do projeto: mvn clean package dockerfile:build -Dmaven.test.skip=true (rodar sem testes nesse passo por 2 motivos, velocidade e não consegui separar as urls de localhost e database interno da imagem docker);

-> docker-compose rm (só para garantir que não tenha nenhuma imagem rodando)

-> docker-compose up

-> http://localhost:15432/browser/ (este será o caminho do pgAdmin4) - user: teste@teste.com.br - password: 123456

-> o arquivo "CRUD cliente.postman_collection.json" que está na raiz do projeto, é uma collection para executar os comandos via Postman.

Obs.: caso queira rodar a aplicação de forma local (IDE), alterar as linhas no arquivo "application.properties" apontando para "localhost", inclusive para rodar os testes.
