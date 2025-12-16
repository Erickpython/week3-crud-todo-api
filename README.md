# Week 3 — CRUD Todo API (BeTechified Dec 2025) ✅

**Aspiring JavaScript Backend Developer — Learning Node.js & Express** 💡

This repository contains a small CRUD (Create, Read, Update, Delete) Todo API built during Week 3 of the BeTechified Dec 2025 cohort. The API demonstrates routing for standard HTTP CRUD operations and basic request validation.

---

## 🚀 Features

- Create, read, update and delete todo items
- Endpoints for active and completed tasks
- Simple in-memory storage (array of todos) — great for learning and testing

## 🧰 Tech Stack

- **Node.js** — JavaScript runtime
- **Express** — Minimal web framework for routing and middleware
- **dotenv** — Environment variable management
- **nodemon** (dev) — Auto-restart during development

## ⚙️ Getting Started

Prerequisites:

- Node.js (v16+ recommended)

Clone and install:

```bash
git clone <this-repo-url>
cd week3-crud-todo-api
npm install
```

Create a `.env` file if you want to set a custom port:

```
PORT=3000
```

Run the server:

```bash
npm start       # production
npm run dev     # development (nodemon)
```

By default the server listens on the port defined by `PORT` in `.env` (or the environment).

---

## 🔌 API Endpoints

Base URL: http://localhost:PORT (replace PORT with your configured port)

- GET `/todos` — List all todos
	```bash
	curl http://localhost:3000/todos
	```

- GET `/todos/active` — List only active (not completed) todos
	```bash
	curl http://localhost:3000/todos/active
	```

- GET `/todos/:id` — Get a single todo by id
	```bash
	curl http://localhost:3000/todos/1
	```

- POST `/todos` — Create a new todo (JSON body; `task` required)
	```bash
	curl -X POST http://localhost:3000/todos -H "Content-Type: application/json" -d '{"task":"New task","completed":false}'
	```

- PATCH `/todos/:id` — Update a todo (partial update)
	```bash
	curl -X PATCH http://localhost:3000/todos/1 -H "Content-Type: application/json" -d '{"completed":true}'
	```

- DELETE `/todos/:id` — Delete a todo
	```bash
	curl -X DELETE http://localhost:3000/todos/1
	```

---

## 🧾 Notes

- This project uses an in-memory array for storage (see `app.js`). Restarting the server resets data.
- Input validation: creating a todo requires the `task` field; missing it returns a 400 error.

---

## 📫 Contact

If you want to reach out, contact me:

- **Email:** erick.wambugu23@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/erick-wambugu-425a15161/

## 🙏 Acknowledgements

Thank you, **BeTechified**, for this learning opportunity and mentorship during the Dec 2025 cohort — much appreciated! 🎉

---

**Happy hacking!** ✨

