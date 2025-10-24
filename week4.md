## Week 4 – Architecture Decision Records (ADRs)
## Summary

During Week 4, I focused on refining the system architecture and finalising the C4 diagrams (Levels 1 to 3). I also developed the data model, ensuring clear relationships between users, complaints, updates, and reports. The following decisions reflect how the design moved from a conceptual overview to a more detailed implementation plan.

--- 

## ADR 007 – System Architecture and C4 Model Selection

**Date:** 19-10-2025
**Status:** Accepted

**Context:**
A consistent method was needed to represent the system at different levels of detail. I considered using simple flow diagrams, UML, or the C4 Model.

**Decision:**
I decided to use the C4 Model to document the architecture. Level 1 shows the overall system and external users, Level 2 breaks the system into containers (Frontend, Backend, Database), and Level 3 focuses on individual backend components such as the API Gateway and data modules.

**Consequences:**
- Clear and professional presentation of the system’s structure.
- Helps readers understand both high-level and technical perspectives.
- Takes more time to complete but makes the documentation more effective.

## ADR 008 – Data Model and Entity Relationships

**Date:** 19-10-2025
**Status:** Accepted

**Context:**
To manage users, complaints, and reports effectively, the database structure needed to be carefully planned. I compared using a flat JSON structure or a more formal entity model.

**Decision:**
I designed an entity diagram with four key entities: User, Complaint, Resolution Update, and Report. Each entity includes its relevant attributes and relationships.

**Consequences:**
- Simplifies data management and improves accuracy.
- Forms a clear foundation for database design.
- Ensures data consistency across different modules.

## ADR 009 – Backend Framework Decision

**Date:** 19-10-2025
**Status:** Accepted

**Context:**
The backend needed to handle authentication, routing, and database operations efficiently. I compared Flask, Django, and Node.js.

**Decision:**
I selected Flask, as it is lightweight, simple to set up, and integrates easily with MongoDB. It also suits the project scale and timeline.

**Consequences:**
- Ideal for rapid development.
- Offers flexibility for future improvements.
- Requires manual setup for routing and access control.

## ADR 010 – Database and Collection Structure

**Date:** 20-10-2025
**Status:** Accepted

**Context:**
The system requires a database to store all user and complaint data. I considered relational databases (MySQL) and document-based databases (MongoDB).

**Decision:**
I chose MongoDB due to its flexible schema design and compatibility with Flask via the PyMongo library.

**Consequences:**
- Data can be stored in a natural JSON-like format.
- CRUD operations are easy to perform.
- Offers strong scalability for additional features in the future.
