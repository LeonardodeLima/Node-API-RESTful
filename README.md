# Aplicação RESTful com Node.js

Os seguintes módulos e ferramentas foram utilizados para o desenvolvimento da aplicação:

Cliente de acesso ao servidor: https://www.getpostman.com/

Módulo para manter o servidor funcionando: https://github.com/remy/nodemon

Framework para rotas REST: https://github.com/restify/node-restify

Plugin para definir mensagens de erro: https://github.com/restify/errors

Módulo ORM para Mysql: https://github.com/tgriesser/knex, http://knexjs.org

## Instalação e execução

Para testar a aplicação, você deve ter o MySQL instalado, com a estrutura de banco de dados e tabela já criados. Você pode executar o script a seguir para gerar esta estrutura!

```sql
CREATE DATABASE `db`;
USE `db`;

CREATE TABLE `rest` (
  `id` int(11) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  `name` varchar(30) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

INSERT INTO `rest` VALUES(1, 'João Pessoa');
INSERT INTO `rest` VALUES(2, 'Maria Joaquina');
```

No arquivo index.js,  se encontra as configuração do MySQL.

```javascript
var knex = require('knex')({
  client: 'mysql',
  connection: {
    host : 'localhost',
    user : 'root',
    password : '',
    database : ''
    }
});
```
Instalção:

Acesse o terminal e execute o comando `npm i -g nodemon` para instalar o nodemon como global.

Em seguida, dentro da pasta do projeto, execute

```
npm install
```
Após concluída a instalação, execute o comando `nodemon index.js`

Acesso a API http://localhost:8080
