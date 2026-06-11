# Frontend–Backend Integration Resources

## Purpose

This document provides carefully selected resources to help students strengthen their understanding of frontend-backend communication, API development principles, HTTP protocols, JSON data exchange, and modern web application architecture.

Students are encouraged to use these resources whenever they encounter difficulties during implementation or wish to explore concepts beyond classroom discussions.

---

# Official Documentation

## React Documentation

Website:
https://react.dev

Recommended Sections:

- State: A Component's Memory
- Synchronizing with Effects
- Rendering Lists
- Conditional Rendering
- Fetching Data with Effects

Why Read?

React documentation is considered the most reliable and up-to-date source for understanding modern React development practices.

---

## MDN Web Docs – Fetch API

Website:
https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API

Recommended Topics:

- fetch()
- Promises
- Request Objects
- Response Objects
- Error Handling

Why Read?

MDN is the industry-standard reference for JavaScript and browser APIs.

---

## JSON Official Documentation

Website:
https://www.json.org

Recommended Topics:

- JSON Objects
- JSON Arrays
- Data Serialization

Why Read?

JSON is the primary data exchange format used between frontend and backend applications.

---

## REST API Tutorial

Website:
https://restfulapi.net

Recommended Topics:

- REST Architecture
- HTTP Methods
- Status Codes
- API Design Best Practices

Why Read?

Understanding REST principles helps students build scalable backend services later in the course.

---

# Recommended Engineering Blogs

## Robin Wieruch

Website:
https://www.robinwieruch.de

Recommended Articles:

- React Fetch API Tutorial
- Data Fetching in React
- React useEffect Guide

Why Read?

Robin Wieruch explains React concepts with practical examples that are easy for beginners to follow.

---

## Josh W. Comeau

Website:
https://www.joshwcomeau.com

Recommended Topics:

- React State Management
- Modern React Development
- Interactive UI Design

Why Read?

Josh provides industry-grade explanations with a strong focus on understanding how React works internally.

---

## Kent C. Dodds

Website:
https://kentcdodds.com/blog

Recommended Topics:

- React Patterns
- Managing Effects
- Component Architecture

Why Read?

Kent focuses on writing maintainable and production-ready React applications.

---

# HTTP Fundamentals

Students should understand the purpose of common HTTP methods.

GET

Used to retrieve data.

Example:

GET /students

---

POST

Used to create data.

Example:

POST /students

---

PUT

Used to update existing data.

Example:

PUT /students/1

---

DELETE

Used to remove data.

Example:

DELETE /students/1

---

# Common HTTP Status Codes

200 OK

Request processed successfully.

---

201 Created

Resource created successfully.

---

400 Bad Request

Invalid request from client.

---

401 Unauthorized

Authentication required.

---

404 Not Found

Requested resource does not exist.

---

500 Internal Server Error

Unexpected server-side failure.

---

# Useful Developer Tools

## Browser Developer Tools

Available in:

- Google Chrome
- Microsoft Edge
- Firefox

Useful Tabs:

- Console
- Network
- Application

Students should learn how to inspect API requests and responses using the Network tab.

---

## Postman

Website:
https://www.postman.com

Purpose:

- Test APIs
- Send Requests
- Analyze Responses
- Debug Backend Services

Industry Relevance:

Widely used by backend and full-stack developers.

---

## Hoppscotch

Website:
https://hoppscotch.io

Purpose:

Lightweight browser-based API testing platform.

Useful for quick experimentation.

---

# Common Errors and Troubleshooting

## Failed to Fetch

Possible Causes:

- Backend server not running
- Wrong API URL
- Network restrictions

Check:

```javascript
fetch("http://localhost:5000/students")
