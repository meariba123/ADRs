Date: 20-10-2025
Status: Accepted

Context:
The Complaint Management System (CMS) requires a lightweight but scalable technology stack that supports rapid development, RESTful communication, secure authentication, and database persistence. The options considered included:

Node.js + Express + MySQL (JavaScript-based stack)

Flask + MongoDB (Python-based stack)

Django + PostgreSQL (heavier, monolithic Python framework)

Decision:
I selected Flask (Python) for the backend framework, MongoDB as the NoSQL database, and HTML/CSS/JavaScript for the frontend. Flask was chosen because it is flexible, minimal, and integrates smoothly with REST APIs and MongoDB. This stack allows quick prototyping while maintaining modular separation of concerns (Frontend ↔ Backend ↔ Database).

Consequences:

Lightweight and easy to deploy with clear REST API endpoints

NoSQL MongoDB schema supports dynamic complaint and user data

Flask-Login integrates easily for session-based authentication

Simplifies the implementation of C4 Level-3 components (controllers, modules, and services)

Slightly less built-in tooling than Django, requiring custom setup for admin and validation
