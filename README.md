# 🎓 Student API with Gin

A RESTful API built with **Go** and the **Gin framework**.  
This project follows a **Layered Architecture** (Handler → Service → Repository → Model) and uses an **SQLite database** to manage student records.

---

## 🚀 How to Run the Project
### first u need to install golang on your pc  go to this link https://go.dev/dl/
### 1️⃣ Clone the Repository

```bash
git clone https://github.com/<your-username>/go-api-gin-lab.git
cd go-api-gin-lab
```

### 2️⃣ Install Dependencies

```bash
go mod tidy
```

### 3️⃣ Start the Server

```bash
go run main.go
```

The server will start at:

```
http://localhost:8080
```

---

## 📡 API Endpoints

| Method | Endpoint        | Description                              |
|--------|-----------------|------------------------------------------|
| GET    | `/students`     | Retrieve all students                    |
| GET    | `/students/:id` | Retrieve a student by ID                 |
| POST   | `/students`     | Create a new student                     |
| PUT    | `/students/:id` | Update an existing student's information |
| DELETE | `/students/:id` | Delete a student                         |

---

## ✅ Validation Rules

When creating (**POST**) or updating (**PUT**) a student:

- **id** → Required (must not be empty)
- **name** → Required (must not be empty)
- **gpa** → Must be a number between **0.00 and 4.00**

---

## 📥 Example JSON Request Body

```json
{
  "id": "66090001",
  "name": "John Doe",
  "major": "Computer Science",
  "gpa": 3.8
}
```

---

## 📁 Project Structure

This project follows a strict **Layered Architecture** to separate concerns and improve maintainability.

```
.
├── models/        # Data structures (e.g., Student)
├── config/        # Database connection and setup
├── repositories/  # Direct database (SQLite) queries
├── services/      # Business logic (between handlers and repositories)
├── handlers/      # HTTP requests, validation, JSON responses
└── main.go        # Application entry point
```

---

## 🛠 Tech Stack

- Go
- Gin
- SQLite
- RESTful API Design
