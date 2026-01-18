# Backend_3task

## Company Task Manager  
**Backend & Frontend Application**

---

## Project Overview

The **Company Task Manager** is a web-based application designed for internal use in an organization.  
The system allows a **manager** to create tasks, assign them to employees, track priorities, and manage task data through a RESTful API.

The backend is built using **Node.js, Express, and MongoDB**, while the frontend is implemented using **pure HTML, CSS, and JavaScript**.  
The application demonstrates full **CRUD functionality**, data persistence, validation, and basic frontend interaction with the API.

This project was developed as part of **Assignment 3**, focusing on migrating from local JSON storage to a **MongoDB database**.

---

## Key Features

- Task creation and assignment to employees  
- Task priority management (low / medium / high)  
- Persistent data storage using MongoDB  
- RESTful API with full CRUD support  
- Simple dashboard-style frontend interface  
- Project structure prepared for future expansion  

---

## Technologies Used

### Backend
- **Node.js**
- **Express.js**
- **MongoDB (Local Instance)**
- **Mongoose**
- **dotenv**
- **CORS**

### Frontend
- **HTML**
- **CSS**
- **JavaScript (Fetch API)**

### Testing
- **Postman** (manual API testing)

---

## Project Structure

```text
assignment_3_task_manager/
├── models/
│   └── Task.js
├── routes/
│   └── tasks.js
├── public/
│   └── index.html
├── server.js
├── .env.example
├── package.json
└── README.md

