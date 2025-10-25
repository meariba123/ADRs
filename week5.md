# Week 5 – Architecture Decision Records (ADRs)
## Summary

Week 5 marks the start of the implementation phase. The focus was on setting up the Flask project, defining the route structure, connecting to the database, and preparing the application for coding. These decisions link directly to the designs completed in previous weeks.

## ADR 011 – Project Folder Structure

**Date:** 26-10-2025
**Status:** Accepted

**Context:**
To keep the codebase well-organised, I needed a clear project structure before beginning implementation.

**Decision:**
The following layout was chosen:

cms_app/
- app.py
- database.py
models/
- user_model.py
- complaint_model.py
- report_model.py
templates/
- login.html
- dashboard_consumer.html
- dashboard_agent.html
- dashboard_manager.html
- admin.html
static/
- css/
- js/
- images/
docs/
- adr/


**Consequences:**
- Keeps files tidy and easy to navigate.
- Makes collaboration and debugging simpler.
- Separates the frontend, backend, and documentation layers.

## ADR 012 – Database Integration Setup

**Date:** 26-10-2025
**Status:** Accepted

**Context:**
Each module of the system needs access to the same database connection.

**Decision:**
I created a dedicated database.py file to manage a single MongoDB connection using PyMongo. This connection is imported into other modules as needed.

**Consequences:**
- Prevents repeated database code.
- Makes connection management easier.
- Simplifies future maintenance or migrations.

## ADR 013 – RESTful Route Structure

Date: 26-10-2025
Status: Accepted

Context:
Routes were needed to handle different system actions such as creating complaints, viewing updates, and generating reports.

Decision:
I created RESTful endpoints for each feature:

/api/users – Manage users

/api/complaints – Add, view, or update complaints

/api/updates – Log progress and notes

/api/reports – Generate reports

Consequences:

Follows a consistent REST structure.

Simplifies testing and integration with the frontend.

Easy to extend with more endpoints later.

ADR 014 – Role-Based Access in Routes

Date: 26-10-2025
Status: Accepted

Context:
Different roles require different access rights. Consumers can log complaints, while managers and agents have extra permissions.

Decision:
I used Flask-Login for session-based authentication and added role checks before certain actions. Roles are stored in the database and verified during login.

Consequences:

Protects sensitive data and routes.

Prevents unauthorised access.

Adds a small amount of complexity to route handling.

ADR 015 – JSON Response Format

Date: 26-10-2025
Status: Accepted

Context:
The system must communicate smoothly between the backend and frontend.

Decision:
I standardised all backend responses using Flask’s jsonify() function so data is returned in JSON format.

Consequences:

Easy for frontend JavaScript to handle.

Improves consistency and debugging.

Enables future expansion into a mobile or single-page interface.

Reflection

By the end of Week 5, the project moved from planning to development. The database, route design, and authentication setup were all clearly defined. These decisions create a solid foundation for coding the backend and testing the first working version of the CMS.
