# Week 11 – Architecture Decision Records (ADRs)

## Summary
This week focused on documentation and validation rather than new features. I reviewed the existing architecture, updated the structural diagram to match the current implementation, and wrote up non-functional requirements. I also began the reflective account to explain the reasoning behind the chosen architecture and design.

---

## ADR 032 – Update of Structural Architecture Diagram

**Date:** 03-12-2025
**Status:** Accepted

**Context:**
After implementing role-based access, reporting features and modals in the UI, parts of the original architecture diagram were no longer accurate. For example, the new roles (Admin/Manager/Support/Consumer) and the addition of reporting logic needed to be shown in the structure. The old diagram also did not show service separation clearly.

**Decision:**
The structural diagram was updated to:
- show individual route controllers for each role (Admin, Manager, Support, Consumer).
- include the Report Model.
- separate the MongoDB collections clearly (users, complaints, reports).
- indicate planned but not implemented services (e.g., notification service as a future extension).

**Pros:**
- Easier to maintain and extend in future work.
- Supports proof-of-concept presentation more clearly.
---

## ADR 033 – Documentation of Non-Functional Requirements (NFRs)

**Date:** 03-12-2025
**Status:** Accepted

**Context:**
The project requires non-functional requirements such as performance, usability, scalability and security to prepare for a real rollout in large banking/telecom scenarios. These were not fully documented earlier in the project.

**Decision:**
A non-functional requirements template was completed and added to the documentation. It includes:
- **Performance**: Respond within 2 seconds.
- **Scalability**: Support growth and cloud deployment.
- **Security**: Use RBAC, HTTPS, and secure authentication.
- **Reliability**: Handle errors and stay functional.
- **Usability**: Simple, consistent UI with labelled forms.
- **Maintainability**: Modular structure for easy updates.
- **Portability**: Work on modern browsers and mobile.
- **Auditability**: Log key actions for review

**Pros:**
- Helps justify architectural choices in the reflective account.
- Supports investor-focused system design intentions.
---

## ADR 034 – Reflective Account Drafting for Architecture & Design
**Date:** 05-12-2025
**Status:** Accepted

**Context:**
The final report requires a reflection explaining what worked, what failed, and how the architecture supports the system. This reflection must be based on real implementation experience and testing outcomes.

**Decision:**
The reflective section was started, focusing on:
- how Flask Blueprints helped maintain separation of roles.
- issues encountered with session handling and redirects.
- challenges around MongoDB validation and flexible schema.
- how UI design depends on backend response accuracy.
  
**Pros:**
- Creates a meaningful link between theory and implementation.
- Shows awareness of real-world challenges, not just diagrams.
- Strengthens justification for architectural decisions.

---


  

  


