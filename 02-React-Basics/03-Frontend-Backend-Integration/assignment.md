# Engineering Assignment: Student Placement Dashboard

## Assignment Overview

In modern organizations, frontend applications rarely work with hardcoded data. Instead, information is fetched dynamically from backend services through APIs.

In this assignment, students will build a Placement Dashboard that retrieves student placement records from an API and displays them in a React application.

The goal is to understand how frontend applications consume backend data and present it to users in a meaningful way.

---

# Learning Objectives

By completing this assignment, students should be able to:

- Use React State Management
- Work with useEffect()
- Consume REST APIs using Fetch API
- Handle JSON Responses
- Render Dynamic Lists
- Implement Search Functionality
- Build Interactive User Interfaces

---

# Problem Statement

A placement department wants a dashboard that displays student placement records.

The frontend should:

- Fetch student data from an API
- Display student details
- Show placement status
- Allow searching students by name

---

# Sample API Response

```json
[
  {
    "id": 1,
    "name": "Rahul Sharma",
    "department": "CSE",
    "status": "Placed"
  },
  {
    "id": 2,
    "name": "Aisha Khan",
    "department": "ECE",
    "status": "Not Placed"
  }
]
```

Expected Outcome:

Data should be retrieved successfully.
State should store API data.
Task 2: Display Student Information

Render all students dynamically.

Example:
{
 students.map(student => (
   <div key={student.id}>
      <h3>{student.name}</h3>
      <p>{student.department}</p>
      <p>{student.status}</p>
   </div>
 ))
}

Expected Outcome:

Every student record should appear on the screen.
No hardcoded entries.
Task 3: Add Search Functionality

Users should be able to search students by name.

Example:

    const filteredStudents = students.filter(student =>
  student.name
    .toLowerCase()
    .includes(search.toLowerCase())
);

  Expected Outcome:

Search updates results instantly.
Filtering works without page refresh.
Task 4: Placement Statistics

Display:

Total Students
Total Placed
Total Not Placed

Example:

  const placedStudents =
students.filter(student =>
student.status === "Placed"
).length;

  Expected Outcome:

Dashboard statistics update automatically.

Task 5: Loading State

Display a loading message while data is being fetched.

Example:

  const [loading, setLoading] = useState(true);
  if (loading) {
  return <h2>Loading...</h2>;
}
Expected Outcome:

Users receive visual feedback while data loads.

Task 6: Error Handling

Handle API failures gracefully.

Example:

  fetch(url)
 .then(response => response.json())
 .catch(error =>
   console.error(error)
 );

 Expected Outcome:

Application should not crash if API is unavailable.


Extension Challenge 1

Add a department filter.

Example:

CSE
ECE
EEE
MECH

Extension Challenge 2

Add sorting functionality.

Examples:

Sort by Name
Sort by Department
Sort by Placement Status
Extension Challenge 3

Create Student Cards using a reusable React component.

Example:

  <StudentCard
 name={student.name}
 department={student.department}
 status={student.status}
/>

This introduces component reusability and clean architecture.

Industry Perspective

This assignment simulates the same workflow used in:

Placement Management Systems
Learning Management Platforms
Employee Dashboards
Banking Portals
E-Commerce Applications

The frontend retrieves information from APIs and dynamically updates the user interface.

Submission Requirements

Students must submit:

Source Code
React Application
Well-structured Components
GitHub Repository

Repository should contain

  README.md
src/
components/

Documentation

Include:

Project Overview
Features Implemented
Challenges Faced
Learning Outcomes
Proof of Work (PoW)

A successful submission must demonstrate:

✓ API Data Retrieval

✓ State Management

✓ Dynamic Rendering

✓ Search Functionality

✓ Error Handling

✓ GitHub Repository Documentation

Reflection Questions
Why do modern applications use APIs?
What role does useEffect() play?
Why is JSON important?
Why should React avoid hardcoded data?
How does State help build dynamic applications?
What challenges did you face during implementation?
Expected Learning Outcome

After completing this assignment, students should clearly understand how React applications communicate with backend systems and how dynamic data-driven interfaces are built in real-world software products
