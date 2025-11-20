# Week 8 – Architecture Decision Records (ADRs)

## Summary
This week focused on documenting the software architecture via structural diagrams (including the high-level system architecture and component interaction). Although it may change to future updates if route changes occur, this provided a strong visual foundation for report and implementation.

---

## ADR 023 – Structural Architecture Diagram

**Date:** 29-10-2025
**Status:** Accepted

**Context:**
The project required clear architectural modelling to visualise how the frontend, backend, and MongoDB database interact.

**Decision:**
A Structural Diagram was created showing front end layer, application layer, service layer, data access layer, Flask (Controller Layer / Entry Point), database layer, and role access routes. It will be updated if changes occur.

**Pros:**
- Helps link implementation to design documentation
- Visual clarity for frontend–backend data flow
- Supports maintainability and scalability planning

---

## ADR 024 – Route-to-Component Mapping

**Date:** 29-10-2025
**Status:** Accepted

**Context:**
Back-end routes needed alignment with user interactions and database functions.

**Decision:**
Mapping was created showing which role uses each route and what database collections they interact with.

**Pros:**
- Supports traceability between roles and features
- Enhances testing and debugging
- Helps implement security restrictions

---


  

  
