### TODO App Backend 

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

