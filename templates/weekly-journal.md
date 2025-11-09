# 🗓️ Weekly Journal — Week {{YYYY-Wxx}}
**Date Range:** {{YYYY-MM-DD}} → {{YYYY-MM-DD}}  
**Focus Theme:** _Short theme for the week (e.g., “Understanding Go Project Structure”)_  
**Week #:** {{Number}}

---

## 🧭 Initial Plan (set at start of week)

**Planned Hours:** X  
**Intentions for the week:**
- [ ] Goal 1 — (e.g., Set up CourseBuilder locally and review architecture)
- [ ] Goal 2 — (e.g., Review Go modules and dependency management)
- [ ] Goal 3 — (e.g., Draft first ADR on repo organization)

**Success Indicators:**
- Clear deliverables by end of week (documents, diagrams, ADRs, or journal entries)
- Learning logs and reflection entries written

---

## 🧩 Activities Log (throughout the week)

| Date | Activity | Folder / File Updated | Notes |
|------|-----------|----------------------|--------|
| YYYY-MM-DD | e.g., Explored `/models/course.py` | `docs/module-maps/` | Identified entity relationships |
| YYYY-MM-DD | e.g., Experimented with Go templates | `journal/experiments/` | Compared with Jinja2 logic |
| YYYY-MM-DD | e.g., Created first ADR | `decisions/0001-initial-repo-setup.md` | Documented repo rationale |

---

## 🧠 TIL (Today I Learned) Notes

> Short, daily “aha!”s — even 1–2 lines each.

| Date | TIL |
|------|-----|
| YYYY-MM-DD | Go’s `defer` statement ensures cleanup even in early returns. |
| YYYY-MM-DD | CourseBuilder’s `models/lesson.py` ties lessons to units using datastore keys, not IDs. |
| YYYY-MM-DD | Markdown link check workflow catches stale external references early. |

🪶 *Tip:* Each TIL can be linked to external resources or code files for later indexing.

---

## 🔗 Link Blog & Reading Notes (inspired by Simon Willison)

> Curated short-form reflections on what you read, watched, or discovered this week.  
> Think of this as your **link-blog stream** — concise, contextual, and opinionated.

| Link / Reference | Context or Takeaway (1–3 sentences) |
|------------------|--------------------------------------|
| [Article Title](https://example.com) | Key insight that connects to this week’s focus. |
| [Go project layout guide](https://github.com/golang-standards/project-layout) | Helped me visualize folder naming conventions and modularization. |
| [Simon Willison on link blogs](https://simonwillison.net/2024/Dec/22/link-blog/) | Inspired me to treat references as micro-essays rather than bookmarks. |

---

## 🧑‍🏫 Teachable Moments (for readers / mentees)

> Summarize 1–2 concrete exercises or discussion prompts that readers can try, based on your week.

**Example Structure:**

### Teachable Moment #1 — “Trace a Legacy Architecture”
**Objective:** Practice mapping dependencies in a large Python repo.  
**Instructions:**
1. Pick any open-source Python webapp (e.g., CourseBuilder).
2. Trace the flow of a single user request (login → dashboard render).
3. Diagram it in your own words.

**Reflection Question:** What surprises you about how older webapps were structured?

---

### Teachable Moment #2 — “Go vs Python: Thinking in Types”
**Objective:** Compare dynamic vs static design thinking.  
**Instructions:**
1. Implement a simple “course entity” in both Python (dict) and Go (struct).
2. Write a short note on how you reason about types differently.

**Optional Discussion:** Share how explicit typing affected your understanding of dependencies.

---

## ⚙️ Challenges / Blockers

- ⛔ Describe technical or conceptual blockers.  
- 🔍 What hypotheses or debugging steps you tried.  
- 💬 Whether AI or external help contributed.

---

## 🤖 AI Interaction Notes (if applicable)

**Prompts Tried:**  
- _Summarize one or two successful prompts._  
**Outcome:**  
- What worked / what didn’t / what you learned from prompt refinement.

---

## 🔄 Weekly Reflection (end of week)

**Actual Hours Spent:** X  
**Key Accomplishments:**
- 1.
- 2.
- 3.

**Key Learnings:**
- Conceptual takeaway(s)
- Tooling or process improvements

**Next Week’s Focus:**
- Brief forward-looking plan.

---

## 🗂️ Related Artifacts

| Type | File / Link |
|------|--------------|
| ADRs | `decisions/0001-initial-repo-setup.md` |
| Experiments | `journal/experiments/2025-exp1.md` |
| Diagrams | `docs/architecture/coursebuilder-overview.svg` |

---

> “You don’t learn by consuming — you learn by reflecting, linking, and teaching.”  
> — _Adapted from Simon Willison & John Dewey_
