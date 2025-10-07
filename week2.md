# Week 2 – Architecture Decisions and Context

## Summary
This week focused on defining the architecture for the Customer Management System (CMS), including the architectural style, technology stack, and database choice.  
I also began creating the C4 Level 1 diagram to show the system’s overall context and interactions.

---

## ADR 001 – Chosen Architectural Style

**Date:** 02-10-2025   
**Status:** Accepted  

**Context:**  
We needed to choose an architectural style for the Customer Management System (CMS). Options included Monolithic, Microservices, and Layered Architecture.  
The CMS will manage user roles, problem reports, and notifications, so structure and maintainability are important.

**Decision:**  
We chose the **Layered Architecture** approach because it clearly separates responsibilities into layers (UI, business logic, and data access).  
This supports future scalability and makes debugging easier.

**Consequences:**  
- Easier maintenance and unit testing  
- Supports future scalability and modular design  
- Can introduce slight overhead for smaller systems  
- Requires careful coordination between layers  

---

## ADR 002 – Database Choice

**Date:** 02-10-2025  
**Status:** Accepted  

**Context:**  
The CMS needs to store data such as user accounts, problems, and support tickets.  
I considered MongoDB (NoSQL) and MySQL (SQL). MongoDB provides flexible document-based storage suitable for varied data structures.

**Decision:**  
I selected MongoDB as the main database because it works well with Python (Flask), stores data in JSON-like format, and is scalable for future needs.

**Consequences:**  
- Easy integration with Flask and Python  
- Schema-less, flexible design for dynamic data  
- Less strict data consistency than SQL  
- Requires indexing for efficient querying  

---

## ADR 003 – Hosting & Framework Decision

**Date:** 02-10-2025  
**Status:** Accepted  

**Context:**  
The CMS will be a web-based application requiring fast setup, easy deployment, and a strong community.  
I considered Django, Flask, and Node.js frameworks.

**Decision:**  
I decided to use Flask because it is lightweight, simple to set up, and integrates well with MongoDB.  
It allows rapid prototyping and provides flexibility for future growth.

**Consequences:**  
- Easy to build prototypes quickly  
- Great documentation and community support  
- Requires manual configuration for larger projects  
- Limited built-in admin tools compared to Django  

---

### Reflection
These ADRs form the foundation for the system’s design and development.  
Choosing a layered architecture with Flask and MongoDB provides flexibility, clarity, and scalability for the prototype phase.  
This ensures that future development (wireframes and C4 Level 2 design) aligns with the selected technologies.

### This my C4 Level 1 Diagram:
<img width="1110" height="902" alt="image" src="https://github.com/user-attachments/assets/9d6cff14-e8cb-49f7-9dbf-c4b86094642f" />

