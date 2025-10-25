# Week 5 – Architecture Decision Records (ADRs)

## Summary
This week I started the implementation phase. The main focus was setting up the Flask project, defining the route structure, connecting to the database, and getting the application ready for coding. These choices build directly on the designs completed in the previous weeks.

---

## ADR 011 – Project Folder Structure

**Date:** 20-10-2025
**Status:** Accepted

**Context:**
To keep the codebase organised, a clear project structure was needed before starting development.

**Decision:**
The following folder structure was adopted:


<img width="584" height="976" alt="image" src="https://github.com/user-attachments/assets/9564e4ea-898b-4a3d-a46e-e68f89c97c87" />

**Pros:**
- Files remain organised and easy to navigate
- Makes collaboration and debugging simpler
- Separates frontend, backend, and documentation clearly

---

## ADR 012 – Database Integration Setup

**Date:** 20-10-2025
**Status:** Accepted

**Context:**
All modules of the system need to access the same database connection.

**Decision:**
A dedicated database.py file was created to manage a single MongoDB connection using PyMongo. Other modules import this connection as needed.

**Pros:**
- Avoids repeating database connection code
- Makes managing the database easier
- Simplifies future maintenance or migrations

---

## ADR 013 – RESTful Route Structure

**Date:** 20-10-2025
**Status:** Accepted

**Context:**
Routes are needed to handle different system actions, such as creating complaints, viewing updates, and generating reports.

**Decision:**
RESTful endpoints were created for each feature:

/api/users – Manage users
/api/complaints – Add, view, or update complaints
/api/updates – Log progress and notes
/api/reports – Generate reports

**Pros:**
- Provides a consistent RESTful structure
- Simplifies testing and integration with the frontend
- Easy to add more endpoints in the future

## ADR 014 – Role Based Access in Routes

**Date:** 20-10-2025
**Status:** Accepted

**Context:**
Different user roles require different access rights. Consumers can log complaints, while managers and agents have additional permissions.

**Decision:**
Flask-Login was used for session-based authentication, and role checks were added to specific routes. Roles are stored in the database and verified at login.

**Pros:**
- Protects sensitive data and routes
- Prevents unauthorised access
- Adds slight complexity to route handling

## ADR 015 – SON Response Format

**Date:** 20-10-2025
**Status:** Accepted

**Context:**
Backend responses need to be standardised so the frontend can handle them easily and reliably.

**Decision:**
All backend responses were returned in JSON format using Flask’s jsonify() function. Endpoints were tested with Postman to ensure they return valid, serialisable JSON objects and correct status codes.

**Pros:**
- Frontend JavaScript can handle responses easily
- Makes debugging via Postman straightforward
- Confirms that API endpoints work correctly before frontend integration
- Supports future expansion, like mobile or single-page apps

  

  
