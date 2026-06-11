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

Verify that the backend service is active.

Unexpected Token in JSON

Possible Cause:

Response is not valid JSON.

Check:
response.json()

Ensure the backend returns properly formatted JSON.

CORS Error

Possible Cause:

Frontend and backend are running on different origins.

Example:

Frontend:

http://localhost:3000

Backend:

http://localhost:5000

Solution:

Enable CORS middleware in Express.js.

Students will learn this in the upcoming backend module.

Industry Connection

Every modern application relies on frontend-backend communication.

Examples:

Amazon Product Catalog
Netflix Movie Listings
LinkedIn User Profiles
Swiggy Order Tracking
Banking Dashboards
University Management Systems

The concepts in this module serve as the foundation for:

Node.js
Express.js
Database Connectivity
Authentication Systems
Full Stack Development
Self-Study Challenge

Explore a public API and display its data inside a React application.

Suggested APIs:

JSONPlaceholder
https://jsonplaceholder.typicode.com
DummyJSON
https://dummyjson.com
OpenWeather
https://openweathermap.org/api

Goal:

Practice fetching, storing, and displaying real-world data using React.

