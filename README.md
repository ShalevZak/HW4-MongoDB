[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19869517&assignment_repo_type=AssignmentRepo)  
# 📝 To-Do App Assignment

## 👤 Student Info  
**Name:** Shalev Zaken, ID 318166303

---

## 🎯 Goal  
Build a full backend connection to a MongoDB database using Node.js, Express, and Mongoose.

---

## ✅ What You're Given  
- A working frontend with HTML/CSS/JS  
- A server that loads API routes (`server.js`)  
- A `.env` file for MongoDB connection (not submitted via GitHub)

---

## 🧠 What Was Implemented

### 1. `models/Task.js`  
- Defined a Mongoose schema with:  
  - `title: String` – required  
  - `done: Boolean` – defaults to `false`

### 2. `controllers/dbController.js`  
Implemented the following:
- `getTasks`: Returns all tasks from DB  
- `addTask`: Adds a new task based on `req.body.title`  
- `toggleTask`: Toggles the `done` status of a task  
- `deleteTask`: Deletes a task by ID  

### 3. `routes/api.js`  
Wired Express routes:  
- `GET /tasks` → `getTasks`  
- `POST /tasks` → `addTask`  
- `PATCH /tasks/:id` → `toggleTask`  
- `DELETE /tasks/:id` → `deleteTask`  

---

## 🌐 MongoDB Setup Instructions

1. Register at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register)
2. Create a free cluster.
3. Add your current IP address in **Network Access**.
4. Create a new database user and password.
5. Copy the connection string and paste it in `.env` file as:

```
MONGO_URL=mongodb+srv://<username>:<password>@<cluster-url>/?retryWrites=true&w=majority&appName=<cluster-name>
```

> ⚠️ **Never upload your `.env` file to GitHub.** It contains sensitive credentials.

---

## 🚀 Run the Project

```bash
npm install
npm start
```

The server will run on [http://localhost:3001](http://localhost:3001) (or port defined in `.env`).  
Open `index.html` in your browser to use the app.
