# Backend_3task

Company Task Manager — Backend & Frontend Application
Project Overview

This project is a Company Task Manager designed for internal use in an organization.
The system allows a manager to create tasks, assign them to employees, track priorities, and manage task data through a RESTful API.

The backend is built using Node.js, Express, and MongoDB, while the frontend is implemented using pure HTML, CSS, and JavaScript.
The application demonstrates full CRUD functionality, data persistence, validation, and basic frontend interaction with the API.

This project was developed as part of Assignment 3, focusing on migrating from local JSON storage to a MongoDB database.

Technologies Used
Backend

Node.js

Express.js

MongoDB (Local Instance)

Mongoose

dotenv

CORS

Frontend

HTML

CSS

JavaScript (Fetch API)

Testing

Postman (manual API testing)

Project Structure
assignment_3_task_manager/
├── models/
│   └── Task.js
├── routes/
│   └── tasks.js
├── public/
│   └── index.html
├── server.js
├── .env
├── package.json
└── README.md

Database Schema
Task Schema

The main entity in the project is Task.
Each task represents a unit of work assigned by a manager to an employee.

Fields:

title (String, required)

description (String, required)

assignedTo (String, required)

createdBy (String, required)

priority (String: low | medium | high)

status (String: pending | in_progress | completed)

deadline (Date, optional)

createdAt (Timestamp, auto-generated)

updatedAt (Timestamp, auto-generated)

Mongoose is used to define the schema and validate incoming data.

API Endpoints
Method	Endpoint	Description
POST	/tasks	Create a new task
GET	/tasks	Retrieve all tasks
GET	/tasks/:id	Retrieve a task by ID
PUT	/tasks/:id	Update an existing task
DELETE	/tasks/:id	Delete a task

All endpoints return appropriate HTTP status codes such as 201 Created, 200 OK, and 404 Not Found.

API Testing (Postman)

All CRUD operations were manually tested using Postman.

Tested scenarios include:

Creating a task (POST)

Retrieving all tasks (GET)

Retrieving a task by ID (GET)

Updating task data (PUT)

Deleting a task (DELETE)

Handling non-existing task IDs (404)

Screenshots of all tests are included in the assignment submission.

Frontend Interface

A simple frontend interface was implemented using HTML, CSS, and JavaScript.

Features:

Create new tasks using a form

Display a list of existing tasks

Delete tasks

Visual task priority indicators

Dashboard layout with a collapsible sidebar

Prepared navigation buttons for future expansion (Employees, Reports, Settings)

The frontend communicates with the backend using the Fetch API.

Environment Configuration

Create a .env file in the project root:

PORT=3000
MONGO_URI=mongodb://127.0.0.1:27017/taskmanager


The project uses a local MongoDB instance, which is allowed by the assignment requirements.

How to Run the Project
1. Install dependencies
npm install

2. Start MongoDB

Make sure MongoDB is running locally as a Windows service.

3. Run the server
node server.js


Expected output:

🚀 Server running on port 3000
✅ MongoDB connected

4. Open frontend

Open public/index.html in a browser.

Error Handling

Invalid IDs return 404 Not Found

Validation errors return 400 Bad Request

Server errors return 500 Internal Server Error

This ensures robust and predictable API behavior.

Future Improvements

The project architecture allows easy expansion, including:

User authentication (manager / employee roles)

Task status updates from the frontend

Filtering and sorting tasks

Employee management module

Reports and analytics dashboard

Conclusion

This project successfully demonstrates:

Migration from JSON storage to MongoDB

Full CRUD API implementation

Proper schema design and validation

Manual API testing

Frontend and backend integration

The application meets all functional and technical requirements of Assignment 3 and is ready for further development.
