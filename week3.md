# Week 3 – Architecture Decision Records (ADRs)
## Summary
Week 3 focused on refining the system’s communication design (API), strengthening secure access control (authentication), and improving user interaction through wireframes and UI planning. These decisions build upon Week 2’s foundational work, showing clear architectural progress and a structured evolution of the CMS system.

---
## ADR 004 – API Design and Communication Approach

**Date:** 12-10-2025
**Status:** Accepted

**Context:**  
The CMS needs smooth and reliable communication between the frontend (web browser) and backend (Flask server) for actions like logging issues, updating statuses, and confirming resolutions. The main options considered were RESTful APIs, GraphQL, and direct template rendering.

**Decision:**
A RESTful API structure was chosen for client-server communication. This design keeps the frontend and backend loosely connected, allowing for easier future integration with mobile or other platforms.

**Pros:**  
- Maintains a clear separation between frontend and backend
- Easier to scale and extend to other interfaces, such as mobile apps
- Requires defining and testing dedicated API routes for CRUD operations
- Involves slightly more setup than basic page rendering

---

## ADR 005 – Authentication and Role Management

**Date:** 12-10-2025
**Status:** Accepted

**Context:**  
Different types of users; Consumers, Agents, Support Personnel, Managers, and Admins—need different access levels within the CMS. The options reviewed were Flask’s session-based authentication, JWT (JSON Web Tokens), and OAuth.

**Decision:**  
Flask-Login was chosen for session-based authentication, combined with role-based access control (RBAC). User roles are stored in MongoDB and used to determine access rights.

**Pros:** 
- Integrates easily with existing Flask routes
- Provides secure session handling with login and logout functions
- Simplifies managing multiple user roles
- Requires additional logic to apply permissions per role

---

## ADR 006 – User Interface and Wireframe Layout Choice

**Date:** 05-10-2025
**Status:** Accepted

**Context:**
The CMS must include several dashboards (for Consumers, Agents, Managers, and Admins) that are easy to navigate. The options considered were building a single-page app with React or using Flask-rendered HTML templates.

**Decision:**
A multi-page layout using HTML, CSS, and JavaScript templates rendered through Flask was selected. Each user role has its own dashboard wireframe showing key actions, for example, “Report Problem” for Consumers and “Assign Support Person” for Agents.

**Pros:**
- Easier to design and test wireframes specific to each role
- Integrates smoothly with Flask’s Jinja2 template engine
- Less dynamic than a React single-page application
- Quicker to implement and suitable for the project’s timeframe
