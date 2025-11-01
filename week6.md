# Week 6 – Architecture Decision Records (ADRs)

## Summary
This week I was focussed on completing the behavioural diagrams and continuing the implementation of the Complaint Management System.
Key progress included finalising the Use Case Diagram, refining actor relationships using <<include>> and <<extend>>, and advancing backend development.
On the coding side, Flask routes were expanded, user role functionality was tested, and JSON data handling was improved to ensure consistent communication between the frontend and backend.

---

## ADR 016 - Behavioural Modelling (Use Case Diagram)

**Date:** 29-10-2025
**Status:** Accepted

**Context:**
A detailed Use Case Diagram was created to illustrate the interactions between Consumers, Help Desk Agents, Managers, Support Person, and System Administrators. The <<include>> and <<extend>> relationships were applied to highlight dependencies and optional behaviours within use cases.

**Decision:**
A detailed Use Case Diagram was created to illustrate the interactions between Consumers, Help Desk Agents, Managers, Support Personnel, and System Administrators. The <<include>> and <<extend>> relationships were applied to highlight dependencies and optional behaviours within use cases.

**Pros:**
- Provides a clear visual overview of all user–system interactions
- Supports the implementation of role-based access control
- Strengthens the link between system design and functional implementation

---

## ADR 017 – Backend Route Development (Flask)

**Date:** 29-10-2025
**Status:** Accepted

**Context:**
As development progressed, backend routes were required to connect frontend user actions with the Flask logic and MongoDB database.

**Decision:**
Flask routes were implemented for the main complaint operations, including submitting, updating, and viewing complaints. Role-based access control was refined so that each user type can only access routes appropriate to their permissions.

**Pros:**
- Routes directly align with the use cases defined in the behavioural diagram
- Maintains secure and controlled access throughout the system
- Simplifies integration testing and backend debugging

---

## ADR 018 – JSON Response and Serialisation Fixes

**Date:** 29-10-2025
**Status:** Accepted

**Context:**
Some backend endpoints produced errors when serialising MongoDB ObjectIds into JSON responses.

**Decision:**
A custom serialisation fix was applied using Flask’s jsonify() function along with a converter to handle ObjectId fields. This ensures that all API responses are valid, properly formatted JSON compatible with the frontend.

**Pros:**
- Prevents “ObjectId not serialisable” errors
- Ensures consistent response formatting across all API routes
- Improves reliability when testing with Postman and during frontend integration

## ADR 019 – Dashboard and Role Navigation Enhancements

**Date:** 29-10-2025
**Status:** Accepted

**Context:**
Each user role required a tailored dashboard to access role-specific features and simplified navigation.

**Decision:**
Flask routing was updated so that, after login, users are automatically redirected to their relevant dashboards. For example, Help Desk Managers can assign tasks, Agents can view their assigned complaints, and Consumers can track their complaint status.

**Pros:**
- Enhances overall user experience and clarity
- Reinforces the role-based access model
- Prepares the system for further UI and frontend integration

## ADR 020 – Behavioural Diagram Integration in Report

**Date:** 29-10-2025
**Status:** Accepted

**Context:**
The completed behavioural diagram needed to be included in the project documentation alongside detailed design explanations.

**Decision:**
The Use Case Diagram was added to the design report under the behavioural modelling section. Each actor and interaction was described in detail to explain the relationships and flow of system operations.

**Pros:**
- Keeps documentation consistent with the system’s development progress
- Provides clear evidence of design planning before implementation
- Demonstrates strong traceability between design diagrams and working code

  

  

