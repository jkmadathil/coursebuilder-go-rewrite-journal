# ADR NNN: [Short, Descriptive Title]

**Date:** YYYY-MM-DD  
**Status:** Proposed / Accepted / Superseded / Deprecated  
**Version:** 1.0  
**Author:** [Your Name or Handle]  
**Linked Ethics Statement:** [../admin/personal-ethics.md]  

---

## 1. Context  

Describe the situation that led to this decision.  
Include technical, pedagogical, or organizational factors that shaped the choice.  

Questions to guide you:
- What problem or limitation were you addressing?  
- What background knowledge or constraints influenced the situation?  
- Were there known issues or dependencies (e.g., CourseBuilder legacy design, cloud provider limits)?  

*(Example: “CourseBuilder’s data model relies on App Engine’s NDB; in migrating to Go, we need an equivalent persistence abstraction without locking into a single cloud.”)*  

---

## 2. Decision  

State the **specific choice** made — clearly and concisely.  

Example phrasing:
- “We will adopt a modular service architecture with a shared domain library.”  
- “We will maintain Python module parity before optimizing for Go idioms.”  
- “We will treat CourseBuilder’s ‘course.yaml’ as the canonical configuration format during migration.”  

---

## 3. Alternatives Considered  

List the main alternative approaches you evaluated — and **why each was not chosen**.  
Include both technical and reasoning aspects (e.g., cognitive load, maintainability, team familiarity).

| Alternative | Summary | Reason Rejected |
|--------------|----------|----------------|
| A | ... | ... |
| B | ... | ... |
| C | ... | ... |

If the decision was AI-assisted, add a note such as:
> “Explored alternatives with ChatGPT (prompt: ‘design migration strategy from App Engine to Go microservices’) — discarded option X due to high complexity.”  

---

## 4. Consequences  

Describe the **expected outcomes** — both positive and negative.  
This section is critical for transparency and for future revisitation.  

Include:
- Benefits gained (e.g., clarity, maintainability, scalability)  
- Risks introduced or deferred (e.g., performance trade-offs, technical debt)  
- Migration or adaptation steps required  

---

## 5. Reflection and Learning Value  

*(This section is unique to your repo and supports your learning-oriented ADR style.)*  

Reflect briefly on:
- What did you *learn* while making this decision?  
- Did AI, peer input, or prior work influence the choice?  
- What would you do differently if you had more time or data?  
- Were there any **teachable moments** worth sharing (e.g., misunderstandings corrected, conceptual shifts)?  

If this decision later proves suboptimal, record it here with a note like:
> “2025-12-02: Subsequent experiments revealed that this approach limits Go’s concurrency benefits; reconsidering for ADR-002.”  

---

## 6. Ethical Reflection  

Use this section to connect back to your [Personal Ethics Statement](../admin/personal-ethics.md).  
Revisit your **Reflection Checklist** questions before finalizing.  

- Did I disclose relevant conflicts of interest?  
- Have I represented external ideas and AI contributions transparently?  
- Could this decision, if replicated, cause harm or confusion for others?  

Add any contextual clarifications (e.g., “This decision aligns with fairness in attribution but may introduce implicit bias via model assumptions.”).  

---

## 7. References  

List all key materials consulted. Use **IEEE-style referencing**.  

Example:  
> [1] G. Orosz, “Lessons from building large engineering teams,” *blog.pragmaticengineer.com*, 2023.  
> [2] OpenAI, “ChatGPT System Card,” 2024.  
> [3] Google Developers, “App Engine NDB API Overview,” *cloud.google.com*, 2020.  

---

## 8. Revision History  

| Date | Version | Author | Notes |
|-------|----------|---------|-------|
| YYYY-MM-DD | 1.0 | [You] | Initial draft |
| YYYY-MM-DD | 1.1 | [You/Reviewer] | Updated after implementation review |

---

> *“Every architectural choice is also a pedagogical one — it teaches future readers how I thought, not just what I built.”*
