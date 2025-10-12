# Week 3 – Architecture Decision Records (ADRs)
## Summary
Week 3 ADRs focus on communication design (API), secure access control (Authentication), and user interaction (Wireframes/UI). These decisions show architectural refinement and progression from Week 2’s foundational choices, demonstrating continuous, well-documented evolution of the CMS system.
ADR 004 – API Design and Communication Approach

---
## ADR 004 – API Design and Communication Approach

**Date:** 12-10-2025
**Status:** Accepted

**Context:**  
The CMS requires smooth communication between the frontend (web browser) and backend (Flask server) for operations like logging problems, updating statuses, and confirming resolutions. The options were RESTful APIs, GraphQL, or direct template rendering.

**Decision:**
I selected a RESTful API design to handle client-server communication. This allows the frontend and backend to remain loosely coupled, making future integration with mobile apps easier.

**Consequences:**  
  - Clear separation between frontend and backend
  - Easier to scale and extend for new interfaces (e.g., mobile)
  - Requires defining and testing API routes for CRUD operations
  - Slightly more setup effort than traditional page rendering

---

## ADR 005 – Authentication and Role Management

**Date:** 12-10-2025
**Status:** Accepted

**Context:**  
Different users (Consumer, Agent, Support Person, Manager, Admin) require access to different features. I compared using Flask’s built-in session-based authentication, JWT (JSON Web Tokens), and OAuth.

**Decision:**  
I selected Flask-Login for session-based authentication and implemented role-based access control (RBAC) using user roles stored in MongoDB.

**Consequences:** 
  - Simple integration with existing Flask routes
  - Secure session management with login and logout
  - Easier to manage multiple user roles
  - Requires extra logic to restrict access for each role

---

## ADR 006 – User Interface and Wireframe Layout Choice

**Date:** 05-10-2025
**Status:** Accepted

**Context:**
The CMS must support multiple user dashboards (Consumer, Agent, Manager, Admin) with easy navigation. Options included a single-page dynamic UI (React) or multi-page HTML templates.

**Decision:**
I selected a multi-page layout using HTML/CSS/JavaScript templates rendered through Flask routes. Each role has a separate dashboard wireframe showing their key functions (e.g., Report Problem for Consumers, Assign Support Person for Agents).

**Consequences:**
  - Easier to design and present wireframes per role
  - Works well with Flask template engine (Jinja2)
  - Less dynamic than React-based SPA
  - Faster to implement and test for coursework scope
