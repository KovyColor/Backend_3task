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
```

---

Database Schema

The main entity of the system is Task.

Task Fields

- title (String, required)

- description (String, required)

- assignedTo (String, required)

- createdBy (String, required)

- priority (low / medium / high)

- status (pending / in_progress / completed)

- createdAt, updatedAt (auto-generated timestamps)

Schema validation is handled using Mongoose.

---

## API Endpoints

The backend exposes a RESTful API that provides full CRUD functionality for task management.

| Method | Endpoint | Description |
|------|---------|-------------|
| POST | `/tasks` | Create a new task |
| GET | `/tasks` | Retrieve all tasks |
| GET | `/tasks/:id` | Retrieve a task by its ID |
| PUT | `/tasks/:id` | Update an existing task |
| DELETE | `/tasks/:id` | Delete a task |

Each endpoint returns appropriate HTTP status codes such as **201 Created**, **200 OK**, and **404 Not Found**.

---

## API Testing (Postman)

All API endpoints were manually tested using **Postman** to ensure correct behavior and data persistence.

The following scenarios were tested:
- Creating a new task using POST request
- Retrieving all tasks using GET request
- Retrieving a single task by ID
- Updating task fields using PUT request
- Deleting a task using DELETE request
- Handling invalid or non-existing task IDs (404 error)

Screenshots of Postman requests and responses are included as part of the assignment submission.

---

## Frontend Interface

A simple frontend interface was implemented using **HTML, CSS, and JavaScript**.

The interface allows interaction with the backend API and demonstrates full-stack integration.

### Frontend Features
- Task creation form
- Display of all existing tasks
- Task deletion functionality
- Visual task priority indicators
- Dashboard-style layout with a collapsible sidebar
- Navigation buttons prepared for future modules (Employees, Reports, Settings)

The frontend communicates with the backend using the **Fetch API**.

---

## Environment Variables

Sensitive configuration data is stored in environment variables.

The `.env` file is excluded from the repository using `.gitignore` to prevent exposing sensitive information.

An example configuration file `.env.example` is provided:

```env
PORT=3000
MONGO_URI=mongodb://127.0.0.1:27017/taskmanager
```

---

## How to Run the Project

Follow the steps below to run the project locally.

1. Install dependencies
```
npm install
```

2. Ensure MongoDB is running locally

- MongoDB should be running as a local service on port 27017.

3. Start the backend server
```
node server.js
```

Expected output:
```
🚀 Server running on port 3000
✅ MongoDB connected
```

4. Open the frontend

- Open the following file in a web browser:

```
public/index.html
```

## Error Handling

The backend includes basic error handling to ensure stable behavior:

- Invalid request data returns 400 Bad Request

- Requests for non-existing resources return 404 Not Found

- Server-side issues return 500 Internal Server Error

This ensures predictable API behavior.

## Future Improvements

The project is designed to be easily extendable.
Possible future improvements include:

- User authentication and authorization

- Role-based access control (manager / employee)

- Task status updates from the frontend

- Filtering and sorting tasks

- Employee management module

- Reports and analytics dashboard

## Conclusion

- The Company Task Manager project demonstrates the use of:

- MongoDB for persistent data storage

- Mongoose for schema-based validation

- Express for RESTful API development

- Integration of backend and frontend components
