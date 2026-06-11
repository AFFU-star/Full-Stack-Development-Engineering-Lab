# Frontend–Backend Integration using React and APIs

## Overview

Modern web applications are built using multiple layers that work together to deliver information to users. A React application is responsible for presenting data to users, while backend services handle business logic, data processing, authentication, and communication with databases.

This module introduces students to the communication bridge between React applications and backend services using APIs.

By the end of this module, students will understand how data travels from a database to a user interface and how modern applications dynamically fetch and display information.

---

# Learning Objectives

After completing this module, students will be able to:

* Understand Client–Server Architecture
* Explain the role of APIs in modern applications
* Use the Fetch API to retrieve data
* Handle JSON responses
* Display dynamic data using React
* Understand REST API fundamentals
* Prepare for Node.js and Express.js backend development

---

# Why Frontend–Backend Integration Matters

Consider a Student Management System.

A user opens the application and requests student records.

The frontend interface alone does not contain this information.

Instead:

1. React sends a request.
2. The backend receives the request.
3. The backend retrieves data from a database.
4. The data is returned to React.
5. React displays the results.

This architecture is used by:

* Amazon
* Netflix
* LinkedIn
* Instagram
* Banking Applications
* University Management Systems

---

# Understanding Client and Server

## Client

The Client is the application that users interact with.

Examples:

* React Application
* Web Browser
* Mobile Application

Responsibilities:

* Display information
* Accept user input
* Send requests to backend services

---

## Server

The Server processes requests and returns responses.

Examples:

* Express.js Application
* Spring Boot Application
* Django Application

Responsibilities:

* Business Logic
* Authentication
* Data Processing
* Database Communication

---

# What is an API?

API stands for Application Programming Interface.

An API acts as a communication bridge between applications.

Example:

```http
GET /students
```

Meaning:

```text
Request all student records.
```

Backend Response:

```json
[
  {
    "id": 1,
    "name": "Rahul",
    "department": "CSE"
  }
]
```

React receives this data and displays it to users.

---

# Understanding REST APIs

REST is the most common architecture style for web APIs.

Common Operations:

| Method | Purpose       |
| ------ | ------------- |
| GET    | Retrieve Data |
| POST   | Create Data   |
| PUT    | Update Data   |
| DELETE | Remove Data   |

Examples:

```http
GET /students
```

Retrieve all students.

```http
POST /students
```

Create a new student.

```http
PUT /students/1
```

Update student information.

```http
DELETE /students/1
```

Delete a student record.

---

# Introduction to Fetch API

React applications use the Fetch API to communicate with backend services.

Basic Example:

```javascript
fetch("http://localhost:5000/students")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

Explanation:

```javascript
fetch(...)
```

Sends a request to the server.

```javascript
response.json()
```

Converts the response into JavaScript objects.

```javascript
.then(...)
```

Processes successful responses.

```javascript
.catch(...)
```

Handles errors.

---

# Fetching Data in React

The most common approach uses:

* useState()
* useEffect()

Example:

```jsx
import { useState, useEffect } from "react";

function Students() {

  const [students, setStudents] = useState([]);

  useEffect(() => {

    fetch("http://localhost:5000/students")
      .then(response => response.json())
      .then(data => setStudents(data));

  }, []);

  return (
    <div>
      {students.map(student => (
        <p key={student.id}>
          {student.name}
        </p>
      ))}
    </div>
  );
}

export default Students;
```

---

# Understanding the Code

## State Initialization

```jsx
const [students, setStudents] = useState([]);
```

Creates a state variable to store student records.

Initially:

```javascript
[]
```

Empty Array.

---

## useEffect()

```jsx
useEffect(() => {

}, []);
```

Runs once when the component loads.

This is the ideal place to fetch data from APIs.

---

## Updating State

```jsx
.then(data => setStudents(data))
```

Stores API data inside React State.

Once state updates, React automatically re-renders the interface.

---

## Displaying Data

```jsx
students.map(student => (
  <p key={student.id}>
    {student.name}
  </p>
))
```

Converts an array into visual UI elements.

---

# Understanding JSON

Most APIs exchange data using JSON.

Example:

```json
{
  "id": 101,
  "name": "Affaan Safi",
  "department": "CSE"
}
```

Advantages:

* Lightweight
* Human Readable
* Language Independent
* Industry Standard

---

# Real-World Example

Imagine a Placement Dashboard.

Backend Response:

```json
[
  {
    "id": 1,
    "name": "Rahul",
    "status": "Placed"
  },
  {
    "id": 2,
    "name": "Aisha",
    "status": "Not Placed"
  }
]
```

React receives this information and dynamically generates student cards.

Without APIs:

Every student would need to be manually added.

With APIs:

The interface automatically updates whenever the database changes.

---

# Common Beginner Mistakes

## Forgetting JSON Conversion

Wrong:

```javascript
fetch(url)
  .then(response => response);
```

Correct:

```javascript
fetch(url)
  .then(response => response.json());
```

---

## Missing Error Handling

Wrong:

```javascript
fetch(url)
  .then(response => response.json());
```

Better:

```javascript
fetch(url)
  .then(response => response.json())
  .catch(error => console.error(error));
```

---

## Missing Key Property

Wrong:

```jsx
students.map(student => (
  <p>{student.name}</p>
))
```

Correct:

```jsx
students.map(student => (
  <p key={student.id}>
    {student.name}
  </p>
))
```

---

# Industry Relevance

Every modern application uses API-driven communication.

Examples:

### E-Commerce

* Product Catalog
* Shopping Cart
* Order History

### Banking

* Account Information
* Transactions
* Notifications

### Social Media

* Posts
* Comments
* Likes

### Education Platforms

* Student Records
* Attendance
* Results

The concepts learned here form the foundation for:

* Express.js
* Node.js
* Database Connectivity
* Full Stack Development

---

# Key Takeaways

* React applications rarely contain static data.
* APIs provide a communication layer between frontend and backend systems.
* Fetch API is used to retrieve server data.
* JSON is the standard format for exchanging information.
* useEffect() is commonly used for API requests.
* React State stores and displays API responses.
* Understanding API integration is essential before learning Express.js and MySQL.
