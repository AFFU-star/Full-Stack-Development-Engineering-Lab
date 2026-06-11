🎯 Module Overview

This module focuses on building the backend layer of full-stack web applications using modern JavaScript technologies. Students will learn how to create RESTful APIs, connect to databases, and handle client-server communication efficiently.

The backend is developed using:

Node.js → Executes JavaScript outside the browser
Express.js → Handles routing and API creation
MySQL → Stores and manages application data
🧠 Core Concept: Backend Architecture

Modern applications follow a structured flow:

  Frontend (React)
        ↓
API Request (HTTP)
        ↓
Backend Server (Express.js)
        ↓
Database (MySQL)

  💡 Explanation
Frontend sends requests (data request / submission)
Backend processes logic and rules
Database stores and retrieves data
Backend sends response back to frontend in JSON format
⚙️ Node.js Fundamentals

Node.js allows JavaScript to run on the server side.

Example:

console.log("Server is running...");

Key Features:
Non-blocking I/O
Event-driven architecture
Fast execution using V8 engine
Ideal for scalable backend systems
🌐 Express.js Fundamentals

Express.js simplifies backend development by providing routing and middleware support.

Basic Server Example:

  const express = require("express");
const app = express();

app.get("/", (req, res) => {
  res.send("Welcome to Backend API");
});

app.listen(5000, () => {
  console.log("Server running on port 5000");
});

  🔌 REST API Concepts

A REST API allows communication between frontend and backend using HTTP methods.

  | Method | Purpose       | Example     |
| ------ | ------------- | ----------- |
| GET    | Retrieve data | /students   |
| POST   | Create data   | /students   |
| PUT    | Update data   | /students/1 |
| DELETE | Remove data   | /students/1 |


  📦 JSON Data Exchange

Backend and frontend communicate using JSON format.

Example:

  {
  "id": 1,
  "name": "Rahul",
  "status": "Placed"
}

Why JSON?
Lightweight
Easy to read/write
Language independent
Standard format for APIs
🗄️ MySQL Database Integration

MySQL is used to store structured data in tables.

Database Connection Example:

  const mysql = require("mysql2");

const db = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "",
  database: "college"
});

db.connect((err) => {
  if (err) {
    console.log("Connection failed");
  } else {
    console.log("MySQL Connected Successfully");
  }
});

  🧾 CRUD Operations Overview

Backend systems are built around CRUD operations:

C → Create (INSERT)
R → Read (SELECT)
U → Update (UPDATE)
D → Delete (DELETE)
🔁 Example API Flow
GET Request Example:

  app.get("/students", (req, res) => {
  db.query("SELECT * FROM students", (err, result) => {
    res.json(result);
  });
});


POST REQUEST  EXAMPLE  :  

app.post("/students", (req, res) => {
  const { name, status } = req.body;

  db.query(
    "INSERT INTO students (name, status) VALUES (?, ?)",
    [name, status],
    (err, result) => {
      res.json({ message: "Student added successfully" });
    }
  );
});

🧠 Learning Outcomes

By completing this module, students will be able to:

Build backend servers using Node.js
Create RESTful APIs using Express.js
Connect applications to MySQL databases
Perform CRUD operations
Understand request–response flow
Build full-stack integration systems
🏭 Real-World Applications

This backend architecture is used in:

E-commerce platforms (Amazon-like systems)
Social media apps (Instagram, LinkedIn)
Streaming services (Netflix)
Banking systems (transaction APIs)
College management systems
🛠️ Tools & Technologies
Node.js runtime
Express.js framework
MySQL database
Postman / Thunder Client for API testing
VS Code for development
📌 Summary

This module bridges the gap between frontend and backend development by teaching how data flows through APIs, how servers handle requests, and how databases store persistent information
