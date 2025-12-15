# Week 2 – Architecture Decisions and Context

## Summary
This week focused on defining the architecture for the Customer Management System (CMS), including the architectural style, technology stack, and database choice.  
I also began creating the C4 Level 1 diagram to show the system’s overall context and interactions.

---

## ADR 001 – Chosen Architectural Style

**Date:** 02-10-2025   
**Status:** Accepted  

**Context:**  
I needed to choose an architectural style for the Customer Management System (CMS). The system manages different user roles, problem reports, and notifications. It was important that the system was easy to maintain and could be expanded in the future.

The following options were considered:

- Monolithic architecture
- Microservices architecture
- Layered architecture

**Decision:**  
A layered architecture was chosen. This separates the system into three main parts: the user interface, the application logic, and the data access layer.

**Reason for the Decision:** 
The layered approach makes the system easier to understand, maintain, and test. Compared to microservices, it avoids extra complexity that is not needed for a system of this size. While a simple monolithic structure could work, using layers gives clearer separation of responsibilities within the application.


**Consequences:**  
Benefits:
- Easier maintenance and debugging
- Supports unit testing by keeping responsibilities separate
- Allows the system to grow without major restructuring

Drawbacks:
- Adds a small amount of overhead due to the use of layers
- Requires care to keep layers properly separated

---

## ADR 002 – Database Choice

**Date:** 02-10-2025  
**Status:** Accepted  

**Context:**  
The CMS needs to store data such as user accounts, problems, and support tickets.  
I considered MongoDB (NoSQL) and MySQL (SQL). MongoDB provides flexible document-based storage suitable for varied data structures.

**Decision:**  
I selected MongoDB as the main database because it works well with Python (Flask), stores data in JSON-like format, and is scalable for future needs.

**Pros:**  
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

**Pros:**  
- Easy to build prototypes quickly  
- Great documentation and community support  
- Requires manual configuration for larger projects  
- Limited built-in admin tools compared to Django  


