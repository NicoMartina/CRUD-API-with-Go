# 📝 Go Todo API (with Gin)

A simple REST API built in **Go** using the [Gin](https://github.com/gin-gonic/gin) framework.  
This project demonstrates basic **CRUD operations** with an in-memory store.

---

## ⚡ Features

- Fetch all todos (`GET /todos`)
- Fetch a single todo by ID (`GET /todos/:id`)
- Add a new todo (`POST /todos`)
- Toggle a todo’s completion status (`PATCH /todos/:id`)

---

## 📦 Tech Stack

- [Go](https://golang.org/) — Backend language
- [Gin](https://github.com/gin-gonic/gin) — Web framework for APIs
- `net/http` — Standard Go HTTP utilities
- `errors` — Error handling package

---

## ▶️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/go-todo-api.git
cd go-todo-api

```

2. Install dependencies

Make sure you have Go installed (go version should show >= 1.20).
Then run:

go mod init go-todo-api
go get github.com/gin-gonic/gin

---

3. Run the server

go run main.go

Server will start at:

http://localhost:9090

---

🔗 API Endpoints

✅ Get all todos
GET /todos

Response:
[
{"id":"1","item":"Make bed","completed":true},
{"id":"2","item":"Study Go","completed":false},
{"id":"3","item":"Make videos","completed":false}
]

---

📌 Get a todo by ID

GET /todos/:id

Example:
curl http://localhost:9090/todos/2

Response:
{"id":"2","item":"Study Go","completed":false}

---

➕ Add a new todo

POST /todos
Content-Type: application/json

Request body:
{"id":"4","item":"Walk the dog","completed":false}

Response:
{"id":"4","item":"Walk the dog","completed":false}

---

🔄 Toggle todo completion

PATCH /todos/:id

Example:
curl -X PATCH http://localhost:9090/todos/2

Response:
{"id":"2","item":"Study Go","completed":true}

---

🛠️ Next Steps

- Add persistent storage (SQLite/Postgres instead of in-memory slice).
- Add authentication.
- Deploy on Render or Railway.

---

📜 License
MIT — free to use, copy, and modify.

---

👉 If you drop that **exactly as above** into `README.md`, GitHub will render it with nice headings, code blocks, and syntax highlighting.

Do you want me to also give you a **`.gitignore` for Go** so you don’t accidentally commit binaries and cache files?
