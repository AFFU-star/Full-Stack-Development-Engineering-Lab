🧩 Assignment: Student Management Backend API
🎯 Problem Statement

Develop a backend system using Node.js, Express.js, and MySQL that manages student records and provides RESTful API endpoints for CRUD operations.

🎯 Learning Objectives

Students will practice:

Creating REST APIs
Connecting backend with database
Writing SQL queries
Handling HTTP requests
Structuring backend applications
🗄️ Database Setup
📌 Create Database
    CREATE DATABASE college;
USE college;

    📌 Create Table
      CREATE TABLE students (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100),
  department VARCHAR(50),
  status VARCHAR(20)
);

  🔌 Task 1: Setup Express Server
Create a Node.js project
Install dependencies:
npm install express mysql2 cors body-parser
Create basic server

    📥 Task 2: GET API (Read Data)

Create API to fetch all students:

app.get("/students", (req, res) => {
  db.query("SELECT * FROM students", (err, result) => {
    if (err) return res.send(err);
    res.json(result);
  });
});
➕ Task 3: POST API (Create Data)
app.post("/students", (req, res) => {
  const { name, department, status } = req.body;

  db.query(
    "INSERT INTO students (name, department, status) VALUES (?, ?, ?)",
    [name, department, status],
    (err, result) => {
      if (err) return res.send(err);
      res.json({ message: "Student added successfully" });
    }
  );
});
✏️ Task 4: PUT API (Update Data)
app.put("/students/:id", (req, res) => {
  const { name, status } = req.body;

  db.query(
    "UPDATE students SET name=?, status=? WHERE id=?",
    [name, status, req.params.id],
    (err, result) => {
      if (err) return res.send(err);
      res.json({ message: "Student updated successfully" });
    }
  );
});
❌ Task 5: DELETE API
app.delete("/students/:id", (req, res) => {
  db.query(
    "DELETE FROM students WHERE id=?",
    [req.params.id],
    (err, result) => {
      if (err) return res.send(err);
      res.json({ message: "Student deleted successfully" });
    }
  );
});
🧪 Task 6: API Testing

Use:

Postman
Thunder Client
Browser (GET only)
🧠 Skills Practiced
REST API development
Database integration
SQL queries
CRUD operations
Backend architecture
Request-response handling
📄 resources.md
📚 Backend Learning Resources

This module is based on backend development using:

Node.js
Express.js
MySQL
📘 Official Documentation
⚙️ Node.js

https://nodejs.org

Topics:

Event loop
Modules system
Async programming
🚀 Express.js

https://expressjs.com

Topics:

Routing
Middleware
API creation
Error handling
🗄️ MySQL

https://dev.mysql.com

Topics:

Database design
CRUD queries
Joins
Indexing
🧠 Important Concepts to Study
🔹 Backend Fundamentals
REST API structure
Client-server communication
HTTP methods
🔹 Database Concepts
Tables & schema design
Primary keys
Query optimization
🔹 Express Concepts
Routing system
Middleware flow
Request lifecycle
🧪 Practice Platforms
https://www.postman.com/
https://www.w3schools.com/nodejs/
https://www.geeksforgeeks.org/nodejs/
🏭 Real-World Applications

This backend architecture is used in:

E-commerce systems (orders, products)
Social media platforms (posts, users)
Banking systems (transactions)
College management systems
Booking applications
📌 Summary

This module helps students understand how real-world backend systems are built using APIs, databases, and server-side logic. It forms the foundation for full-stack development careers.

    
