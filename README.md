### TODO App Backend 

---

# TODO App Backend

This is a simple TODO app backend built with Node.js, Express.js, and MongoDB. The app allows users to create, read, update, and delete todo items.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
- [Folder Structure](#folder-structure)
- [API Endpoints](#api-endpoints)
- [License](#license)

## Features

- Create a new todo item
- Get all todo items
- Get a todo item by ID
- Update a todo item
- Delete a todo item

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- dotenv

## Getting Started

### Prerequisites

- Node.js and npm installed on your local machine.
- MongoDB installed and running on your local machine or a cloud-based MongoDB service.

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/todoapp-backend.git
   cd todoapp-backend
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Create a `.env` file in the root directory and add the following environment variables:
   ```
   PORT=3000
   DATABASE_URL=mongodb://127.0.0.1:27017/babbarDataBase
   ```

### Running the App

1. Start the server:
   ```sh
   npm start
   ```

2. For development, you can use nodemon to automatically restart the server on code changes:
   ```sh
   npm run dev
   ```

The server will start on `http://localhost:3000`.

## Folder Structure

```
todoapp-backend
├── config
│   └── database.js
├── controllers
│   ├── createTodo.js
│   ├── getTodo.js
│   ├── updateTodo.js
│   └── deleteTodo.js
├── models
│   └── Todo.js
├── routes
│   └── todo.js
├── .env
├── index.js
├── package-lock.json
├── package.json
```

- **config:** Configuration files, including database connection setup.
- **controllers:** Contains the logic for handling requests and responses for different routes.
- **models:** Mongoose schemas and models for MongoDB collections.
- **routes:** Route definitions for the API endpoints.
- **index.js:** Entry point of the application.
- **.env:** Environment variables configuration.
- **package.json:** Metadata and dependencies of the project.

## API Endpoints

- **Create Todo**
  - **POST** `/api/v1/createTodo`
  - Request Body: `{ "title": "Sample Todo", "description": "Sample Description" }`

- **Get All Todos**
  - **GET** `/api/v1/getTodos`

- **Get Todo by ID**
  - **GET** `/api/v1/getTodos/:id`
  - Params: `id`

- **Update Todo**
  - **PUT** `/api/v1/updateTodo/:id`
  - Params: `id`
  - Request Body: `{ "title": "Updated Title", "description": "Updated Description" }`

- **Delete Todo**
  - **DELETE** `/api/v1/deleteTodo/:id`
  - Params: `id`



















---

- **Express.js:** A web framework for Node.js used to build web applications and APIs.
- **Mongoose:** An ODM (Object Data Modeling) library for MongoDB and Node.js, which provides a straight-forward, schema-based solution to model your application data.
- **CRUD Operations:** The core actions to Create, Read, Update, and Delete resources, which are the backbone of this TODO application.

#### **Folder Structure:**

1. **config:**
   - `database.js`: Configuration for connecting to the MongoDB database.

2. **controllers:**
   - `createTodo.js`: Handles creating a new todo.
   - `getTodo.js`: Handles fetching todos.
   - `updateTodo.js`: Handles updating an existing todo.
   - `deleteTodo.js`: Handles deleting a todo.

3. **models:**
   - `Todo.js`: Defines the Todo model schema for MongoDB.

4. **routes:**
   - `todo.js`: Defines the routes/endpoints for todo operations.

5. **Root Files:**
   - `.env`: Environment variables (e.g., PORT, DATABASE_URL).
   - `index.js`: Main entry point for the app.
   - `package-lock.json` & `package.json`: Node.js package management files.

---

**index.js**:
- Entry point of the application.


---

#### **.env:**

- Store environment variables.
  ```
  PORT = 3000
  DATABASE_URL = mongodb://127.0.0.1:27017/babbarDataBase
  ```

---

#### **database.js:**

- Handle MongoDB connection.
- **Key Parts:**
  - Connect to the database using `mongoose`.
  - Log success or error message.

---


#### **package.json**

- **Scripts**:
  - `start`: Runs the app with Node.
  - `dev`: Runs the app with Nodemon for development.
- **Dependencies**:
  - `dotenv`: For loading environment variables.
  - `express`: For server setup.
  - `mongoose`: For interacting with MongoDB.
  - `nodemon`: For auto-restarting the server during development.

```json
{
  "name": "todoapp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "dotenv": "^16.4.5",
    "express": "^4.18.2",
    "mongoose": "^7.7.0",
    "nodemon": "^2.0.22"
  }
}
```

---

