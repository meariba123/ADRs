# Week 9 – Architecture Decision Records (ADRs)

## Summary
This week involved implementing role-based access and coding several functional requirements such as complaint creation restrictions, dashboard control, and backend logic improvements. Progress focused on ensuring that users only access actions relevant to their role.

---

## ADR 025 – Role-Based Functional Requirement Implementation

**Date:** 20-11-2025
**Status:** Accepted

**Context:**
As core features were being coded, it was necessary to enforce functional requirements ensuring only authorised roles could perform certain actions.

**Decision:**
Role-based checks were implemented across key routes (e.g. only Consumers submit complaints, only Agents update assigned complaints, Managers assign tasks).

**Pros:**
- Increases system security and control
- Aligns code with original requirement specification
- Reduces risk of unauthorised access
  
---

## ADR 026 – Dashboard Access Logic Implementation

**Date:** 20-11-2025
**Status:** Accepted

**Context:**
User dashboards needed to adapt based on login role to streamline navigation.

**Decision:**
Route logic was updated so that each user is redirected to a role-specific dashboard after authentication.

**Pros:**
- Improves usability
- Supports modular system expansion
- Provides consistency between role UI and backend permissions

---

## ADR 027 – Enhancement of Complaint Model (Functional Update)

**Date:** 20-11-2025
**Status:** Accepted

**Context:**
As features expanded, additional attributes were required for better complaint tracking and workflow management.

**Decision:**
Fields for proposed solution and updates (activity log) were added into the complaint model.

**Pros:**
- Enables issue tracking
- Supports future resolution logging
- Improves transparency for Agents and Managers

---


  

  

