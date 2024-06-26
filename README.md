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


#### **.env:**

- *Store environment variables.
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

