<p align="center">
  <a href="https://devfel.com/" rel="noopener">
 <img  src="https://devfel.com/imgs/devfel-logo-01.JPG" alt="DevFel"></a>
</p>

<h1 align="center">RocketSeat Challenge 06</h1>
<h3 align="center">GoFinance - Backend - pt-BR</h3>


<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center"> 
Este é um aplicativo de gerenciamento de transações para praticar Node.js juntamente com TypeScript, incluindo o uso de um banco de dados Postgres com TypeORM e envio de arquivos com Multer. Este aplicativo permite o armazenamento de transações financeiras com entradas e saídas. Além disso o app permite o registro e listagem dessas transações, a criação de novos registros na base de dados, a remoção desses registros, e o envio de um arquivo csv para inserir várias transações simultaneamente.  </p>

---

## 📝 Table of Contents

- [Rotas da Aplicação](#about)
- [Primeiros Passos](#getting_started)
- [Ferramentas Utilizadas](#built_using)
- [Dependências](#dependencies)
- [Autor](#authors)
- [Agradecimentos](#acknowledgement)

---

## 🧐 Rotas da Aplicação <a name = "about"></a>

- **_POST /transactions:_** Essa rota é responsável pela criação de transações financeiras. A rota recebe título, valor, tipo e categoria dentro do corpo da solicitação. O tipo deve ser income ou outcome apenas. Ao registrar uma nova transação, ela será armazenada no banco de dados contendo os campos id, título, valor, tipo, category_id, created_at, updated_at. Além disso, a categoria é uma tabela separada. Antes de criar uma nova categoria, o sistema verifica se já existe uma categoria com o mesmo título. Se existir, usa a id da categoria que já existe no banco de dados.
- **_GET /transactions:_** Esta rota retorna uma listagem de todas as transações registradas até o momento, junto com a soma das entradas, saques e o crédito total.
- **_DELETE /transactions/:id:_** Esta rota exclui uma transação com o id presente nos parâmetros da rota;
- **_POST /transactions/import:_** O backend permite ainda a importação de um arquivo .csv contendo as mesmas informações necessárias para criar uma transação: id, título, valor, tipo e categoria, onde cada linha de o arquivo CSV deve ser um novo registro para o banco de dados e, finalmente, retorna todas as transações que foram importadas para o seu banco de dados.

---

## 🏁 Primeiros Passos <a name = "getting_started"></a>

Para obter uma cópia deste projeto e executar em sua máquina local para fins de desenvolvimento e teste, você precisará clonar o projeto, execute o comando "yarn" em seu terminal para instalar todas as dependências e executar o comando "yarn dev:server" para iniciar o servidor.
É importante notar que este projeto requer um banco de dados em execução, sugiro que você use Docker juntamente com Insomnia e DBeaver.

---

## ⛏️ Ferramentas Utilizadas <a name = "built_using"></a>

- [PostgreSQL](https://www.postgresql.org/) - Database
- [Express](https://expressjs.com/) - Server Framework
- [NodeJs](https://nodejs.org/en/) - Server Environment
- [Insomnia](https://insomnia.rest/) - Rest Client
- [DBeaver](https://dbeaver.io/) - DB administration tool
- [Docker](https://www.docker.com/) - Docker Container
- [Typescript](https://www.typescriptlang.org/) - Programming Language

---

## 🔁 Dependências <a name = "dependencies"></a>

Algumas dependências e bibliotecas do projeto incluem, mas não estão limitadas a:

- "cors": "^2.8.5",
- "csv-parse": "^4.8.8",
- "dotenv": "^8.2.0",
- "express": "^4.17.1",
- "express-async-errors": "^3.1.1",
- "multer": "^1.4.2",
- "pg": "^8.3.0",
- "reflect-metadata": "^0.1.13",
- "typeorm": "^0.2.24"
- "typescript": "~3.7.2"

---

## ✍️ Author <a name = "authors"></a>

- [@devfel](https://github.com/devfel) - Luiz Flávio Felizardo

---

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- Agradecimento a equipe da RocketSeat pela proposta desse desafio e os ensinamentos até aqui. (Turma - Bootcamp GoStack 14)
