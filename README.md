# Aplicação RESTful com Node.js

Os seguintes módulos e ferramentas foram utilizados para o desenvolvimento da aplicação:

Postman: https://www.getpostman.com/

Nodemon: https://github.com/remy/nodemon

Restify: https://github.com/restify/node-restify

Restify(errors): https://github.com/restify/errors

Knexjs: https://github.com/tgriesser/knex /  http://knexjs.org

## Instalação e execução:

E necessário ter previamente instalado Node ˆ8.x e o MySQL 

### Insira a estrutura utilizada no MySQL

```sql
CREATE DATABASE `db`;
USE `db`;

CREATE TABLE `rest` (
  `id` int(11) NOT NULL AUTO_INCREMENT PRIMARY KEY,
  `name` varchar(30) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

INSERT INTO `rest` VALUES(1, 'João Pessoa');
INSERT INTO `rest` VALUES(2, 'Pessoa joão');
```

### Configure a conexãono arquivo index.js.

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

## Instalação:

```
 1 cd Node-API-RESTful
 2 npm install
 3 npm run dev
 disponível: http://localhost:3000
```
