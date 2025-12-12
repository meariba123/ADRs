# Week 12 – Architecture Decision Records (ADRs)

## Summary
This week I focused mostly on improving and updating the report rather than adding new system features. I spent time fixing the structural diagram, adding more detail to the architecture comparisons, improving the security section, and finishing my reflective write up.

---

## ADR 035 – Update of Structural Architecture Diagram

**Date:** 09-12-2025
**Status:** Accepted

**Context:**
After reviewing my report, I noticed the old structural diagram didn’t fully match the current version of the system. Some roles and routes were missing, and a few parts were no longer correct after recent changes.

**Decision:**
I updated the diagram to:
- clearly show each route for Admin, Manager, Support Person, Agent and Consumer.
- show the correct MongoDB collections (users, complaints, reports).
- remove anything that wasn’t actually used in the final system.
- tidy up the layout so it’s easier to understand.

**Pros:**
- the diagram now reflects the real system.
- it’s cleaner and easier for markers to follow.
- it supports the final write-up and justification sections.
  
---

## ADR 036 – Expanding Security Considerations

**Date:** 09-12-2025
**Status:** Accepted

**Context:**
I already had basic security in place, but the write-up didn’t fully explain why some advanced features weren’t added. The report needed clearer reasoning and more depth.

**Decision:**
I rewrote and expanded the security section to explain:
- what security features I included,
- what I didn’t include,
- and why (mainly time limits and the scope of the assignment).
- I also added a short “future improvements” list to show what could be added later.

**Pros:**
- the report reads more clearly and honestly.
- shows awareness of real-world security needs.
- helps meet the mark scheme for justification and evaluation.
  
---

## ADR 037 – Editing and Improving Architecture Comparisons
**Date:** 11-12-2025
**Status:** Accepted

**Context:**
The original comparison between different architecture styles (monolithic, layered, microservices, etc.) was too brief and didn’t fully explain why the final choice made sense.

**Decision:**
I added more explanation to each architecture type and made the comparison clearer. I also linked the comparison to my actual system choices, so it didn’t feel generic.
  
**Pros:**
- Stronger justification for the chosen architecture.
- Fits better with the reflective account.
- Shows I understand the differences, not just listing them.

---

## ADR 038 – Reflective Account Work
**Date:** 12-12-2025
**Status:** Accepted

**Context:**
The final report needs a reflective section, so I started writing it based on the challenges, changes, and design decisions made throughout the project.

**Decision:**
I wrote about:
what went well, what caused problems, how the architecture supported the project, and things I would improve if I had more time. 

**Pros:**
- Adds depth to the final report.
- Shows critical thinking, not just writing what happened.
- Helps meet the marking criteria for evaluation and reflection.
- 
---

  



