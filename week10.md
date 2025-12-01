# Week 10 – Architecture Decision Records (ADRs)

## Summary
This week I focused on adding system features for Admins and Managers. I also started working on the notification system but could not finish it due to some problems with the backend (mainly the date/time errors and data format issues). Most of the work was successful except the notification part, which I will complete later once the errors are fixed.

---

## ADR 028 – Admin & Manager Features

**Date:** 27-11-2025
**Status:** Accepted

**Context:**
Admins and Managers needed different features from other users. For example, Admins manage users and companies, and Managers assign or monitor complaints.

**Decision:**
I added role checks so that only Admins and Managers can access their specific features. These include:
- Admins: user and company management
- Managers: assign complaints to agents and view complaint progress

**Pros:**
- Makes the system more organised
- Matches the original requirements
- Keeps control in the right hands
---

## ADR 029 – Notification System (Delayed)

**Date:** 27-11-2025
**Status:** Delayed

**Context:**
I tried to add notifications (e.g. when a complaint is updated or assigned), but some backend issues stopped it from working properly. Mainly, there were problems with how time and date were handled.

**Decision:**
I started developing the feature, but I’ve paused it until the backend issues are fixed. I will continue working on it next week.

**Pros (when completed):**
- Keeps users updated instantly
- Better communication between roles

**Why it's delayed:**
- Errors with date formats
- Notification logic depends on working database updates

---

## ADR 030 – Complaint Assignment & Escalation

**Date:** 28-11-2025
**Status:** Accepted

**Context:**
Previously, anyone could update a complaint. Now, Managers needed to assign complaints to agents properly and escalate if required.

**Decision:**
I added backend logic so that:
- Managers can assign complaints to specific agents
- Escalations are tracked properly

**Pros:**
- Improves complaint handling
- Provides better tracking and accountability

---

## ADR 031 – Backend Security & Role Checks

**Date:** 30-11-2025
**Status:** Accepted

**Context:**
Before, most restrictions were only done on the front-end, which could be bypassed. Backend checks were required to prevent unauthorised access.

**Decision:**
Before, most restrictions were only done on the front-end, which could be bypassed. Backend checks were required to prevent unauthorised access.

**Pros:**
- More secure
- Prevents users from accessing features they shouldn’t
- Future-proof for more features

---


  

  

