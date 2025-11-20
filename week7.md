# Week 7 – Architecture Decision Records (ADRs)

## Summary
This week focused on transitioning from initial backend setup to refining role handling logic and preparing the system for multi-user interaction. Early implementation of user authentication and basic route structure was completed. Planning also started for future role-based dashboards.

---

## ADR 021 – Initial Role Handling Strategy

**Date:** 12-11-2025
**Status:** Accepted

**Context:**
The project needed a clear strategy for handling different user types (Consumer, Agent, Manager, Admin) before implementing any system logic.

**Decision:**
A role attribute was added to the user model during account creation. This allows future role-specific features and dashboard redirection logic.

**Pros:**
- Establishes foundation for role-based functionality
- Keeps user structure future-proof
- Ensures logical alignment with functional requirements

---

## ADR 022 – Basic Backend Route Planning

**Date:** 12-11-2025
**Status:** Accepted

**Context:**
To ensure consistent structure, high-level Flask routes were planned before integrating them with the frontend.

**Decision:**
Core routes such as /login, /register, and /dashboard were documented and structured to allow expansion.

**Pros:**
- Provides clean backend architecture
- Simplifies future frontend integration
- Reduces rework later

---

