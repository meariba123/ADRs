## Week 4 – Architecture Decision Records (ADRs)
## Summary

During Week 4, I focused on refining the system architecture and finalising the C4 diagrams (Levels 1 to 3). I also developed the data model to define clear relationships between users, complaints, updates, and reports. These decisions mark the shift from conceptual design to a detailed implementation plan.

--- 

## ADR 007 – System Architecture and C4 Model Selection

**Date:** 19-10-2025
**Status:** Accepted

**Context:**
A consistent approach was needed to represent the system at different levels of detail. I compared simple flow diagrams, UML diagrams, and the C4 Model.

**Decision:**
The C4 Model was chosen to document the architecture.
- Level 1 shows the overall system and its external users
- Level 2 breaks the system into containers such as the frontend, backend, and database
- Level 3 focuses on detailed backend components like the API gateway and data modules

**Pros:**
- Provides a clear and professional representation of the system’s structure
- Makes it easier to understand both high-level and technical details
- Requires more time to complete, but improves documentation quality overall

---

## ADR 008 – Data Model and Entity Relationships

**Date:** 19-10-2025
**Status:** Accepted

**Context:**
To manage users, complaints, updates, and reports effectively, a well-structured data model was needed. I considered using a flat JSON layout versus a structured entity-relationship model.

**Decision:**
An entity diagram was created with four main entities: User, Complaint, Resolution Update, and Report. Each entity includes relevant fields and clearly defined relationships.

**Pros:**
- Simplifies data handling and improves accuracy
- Provides a solid foundation for database implementation
- Ensures data consistency across different system modules

---

## ADR 009 – Backend Framework Decision

**Date:** 19-10-2025
**Status:** Accepted

**Context:**
The backend needed to support authentication, routing, and database operations efficiently. I evaluated Flask, Django, and Node.js.

**Decision:**
Flask was selected because it is lightweight, easy to set up, and integrates smoothly with MongoDB. It also fits well with the project’s scale and time constraints.

**Pros & Cons:**
- Enables quick and flexible development
- Allows greater control over routing and configuration
- Requires more manual setup compared to larger frameworks like Django

--- 

## ADR 010 – Database and Collection Structure

**Date:** 20-10-2025
**Status:** Accepted

**Context:**
The system needed a database to store user information, complaints, and related data. I compared relational databases such as MySQL with document-based databases like MongoDB.

**Decision:**
MongoDB was chosen for its flexible, schema-free design and strong compatibility with Flask through the PyMongo library.

**Pros:**
- Stores data in a natural, JSON-like format
- Makes CRUD operations straightforward
- Scales easily to support future features and enhancements
