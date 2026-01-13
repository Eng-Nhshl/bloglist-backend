# Bloglist Backend

A professional, production-ready RESTful API built with **Node.js** and **Express**, featuring a robust **MongoDB** integration and a comprehensive **automated testing** suite.

---

## 🛠 Features

- **RESTful API**: Full CRUD operations for blogs and user management
- **Data Relationships**: One-to-many relationship between Users and Blogs
- **Validation**: Strict schema-level validation using Mongoose
- **Security**: Password hashing (Bcrypt) and sensitive data filtering
- **Testing**: 100% logic coverage using the native Node.js test runner and Supertest
- **Code Quality**: ESLint configuration with stylistic plugins

---

## Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Runtime** | Node.js (v22.x) |
| **Framework** | Express.js |
| **Database** | MongoDB Atlas (NoSQL) |
| **ODM** | Mongoose |
| **Testing** | Node `--test` & Supertest |
| **Environment** | cross-env / dotenv |

---

## Project Structure

```text
bloglist-backend/
├── controllers/         # Route handlers (blogs.js, users.js)
├── models/              # Mongoose schemas (blog.js, user.js)
├── tests/               # API & Integration tests
├── utils/               # Middleware (logger.js, errorHandler.js)
├── app.js               # Express application configuration
└── index.js             # Server entry point
````

---

## Getting Started

### Prerequisites

* **Node.js** installed
* A **MongoDB Atlas** account

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Eng-Nhshl/bloglist-backend.git
   cd bloglist-backend
   ```

---

## Install Dependencies

```bash
npm install
```

---

## Environment Setup

Create a `.env` file in the root directory:

```env
MONGODB_URI=your_production_mongodb_uri
TEST_MONGODB_URI=your_test_mongodb_uri
PORT=3001
```

---

## Run the Application

```bash
npm run dev
```

---

## Running Tests

The project uses a dedicated test database to ensure the safety of development data.

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch
```

---

## API Endpoints

### Blogs

* **GET** `/api/blogs` – Retrieve all blogs (includes user info)
* **POST** `/api/blogs` – Create a new blog (requires `userId`)
* **PUT** `/api/blogs/:id` – Update blog likes
* **DELETE** `/api/blogs/:id` – Remove a blog

### Users

* **GET** `/api/users` – List all users and their associated blogs
* **POST** `/api/users` – Register a new user with a hashed password

---

## License

This project is part of the **Full Stack Open** coursework.

**Questions?**

🔗 **Project Repository:**
[https://github.com/Eng-Nhshl/bloglist-backend](https://github.com/Eng-Nhshl/bloglist-backend)

**Author:** Eng-Nhshl

```