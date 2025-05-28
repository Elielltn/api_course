# 📚 Course & Modules API

Uma API RESTful desenvolvida com **Node.js**, **Express** e **Knex.js** para gerenciar cursos e seus respectivos módulos. Ideal para fins educativos e como base para projetos maiores.

---

## 🚀 Tecnologias Utilizadas

- [Node.js](https://nodejs.org/)
- [Express](https://expressjs.com/)
- [Knex.js](https://knexjs.org/)
- [SQLite3](https://www.sqlite.org/index.html) (padrão, mas adaptável para outros bancos)
- [Typescript](https://www.typescriptlang.org/)

---

## ⚙️ Instalação e Execução

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repo.git
   cd nome-do-repo
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

3. **Configure o banco de dados:**

   * Execute as migrations:
     ```bash
     npx knex migrate:latest --knexfile knexfile.ts
     ```

   * (Opcional) Popule com dados iniciais:
     ```bash
     npx knex seed:run --knexfile knexfile.ts
     ```

4. **Inicie o servidor:**
   ```bash
   npm run dev
   ```

   O servidor estará disponível em: `http://localhost:3333`

---

## 📌 Endpoints da API

### 📘 Cursos

* **Criar curso**
  * `POST /courses`
  * Body:
    ```json
    {
      "name": "Nome do curso"
    }
    ```

* **Listar cursos**
  * `GET /courses`

* **Atualizar curso**
  * `PUT /courses/:id`
  * Body:
    ```json
    {
      "name": "Novo nome"
    }
    ```

* **Deletar curso**
  * `DELETE /courses/:id`

---

### 🧩 Módulos

* **Criar módulo**
  * `POST /modules`
  * Body:
    ```json
    {
      "name": "Nome do módulo",
      "course_id": 1
    }
    ```

* **Listar todos os módulos**
  * `GET /modules`

* **Listar módulos de um curso**
  * `GET /courses/:id/modules`

---

## 🛠 Scripts úteis

* `npm run dev`: inicia a API em modo de desenvolvimento (usando nodemon)
* `npx knex migrate:latest`: aplica todas as migrations
* `npx knex migrate:rollback`: desfaz a última migration
* `npx knex seed:run`: executa os seeds

---

## 📝 Licença

Esse projeto está sob a licença MIT.
