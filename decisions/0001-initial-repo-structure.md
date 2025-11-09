# ADR 0001: Establish Initial Repository Structure as a Reflective Learning Space

**Date:** 2025-11-08  
**Status:** Accepted  
**Version:** 1.0  
**Author:** Jayarishnan M  
[**Linked Ethics Statement:**](../admin/personal-ethics.md)  

---

## 1. Context  

While exploring the re-architecture of CourseBuilder to Go, I recognized that this journey would be as much pedagogical as technical.  
Instead of creating a monolithic code repository, I wanted to build a **meta-repository** — a place to journal the process, reflect on design trade-offs, document learnings, and showcase the use of AI as both collaborator and evaluator.  

The repo will not contain executable code initially; instead, it will host structured artifacts:  
- Weekly journals  
- Experiment reports  
- Architectural decision records (ADRs)  
- Ethics and reflection documents  
- Roadmaps and planning artifacts  

This structure supports personal growth, transparency, and shareable learning outcomes that can inform others attempting similar migrations or reflective engineering practices.

---

## 2. Decision  

We will establish a **documentation-first repository structure** with a focus on reflection and meta-learning rather than code.

### Folder Outline (Initial Draft)
```
/admin/
personal-ethics.md
roadmap.md
/decisions/
adr-template.md
0001-initial-repo-structure.md
/experiments/
experiment-template.md
/journals/
weekly-journal-template.md
```

Each folder represents a reflective layer:
- `/admin` → strategic intent and ethics  
- `/decisions` → technical and pedagogical choices  
- `/experiments` → empirical inquiry and testing (including failed ones)  
- `/journals` → ongoing narrative of learning and discovery  

---

## 3. Alternatives Considered  

| Alternative | Summary | Reason Rejected |
|--------------|----------|----------------|
| **A. Code-first migration repo** | Begin direct migration of CourseBuilder Python code to Go with inline documentation. | Would obscure reflection and learning process; reduces pedagogical value. |
| **B. Hybrid repo (code + notes)** | Maintain code and documentation together in a single repo. | Harder to maintain clarity between reflection and implementation; conflates learning artifacts with code maintenance. |
| **C. Blog or wiki format** | Host reflections as blog posts (e.g., Hugo, Notion, GitHub Pages). | Lacks version control history and architectural rigor of ADRs; unsuitable for traceable experimentation. |

---

## 4. Consequences  

**Positive:**
- Encourages transparency and deep reflection in the learning process.  
- Makes failures, iterations, and reasoning visible to others.  
- Provides a structured framework for adding code artifacts later.  
- Enables reuse of templates for other reflective tech projects.  

**Negative / Trade-offs:**
- Requires discipline in documentation upkeep.  
- May appear “non-technical” to casual observers.  
- Progress may be harder to quantify initially (no code metrics).  

---

## 5. Reflection and Learning Value  

This decision reframes “architecture” as a **learning journey**.  
It aligns with my intent to explore reflection as a form of engineering design documentation.  
By separating the reflective space from code, I preserve **cognitive space** for experimentation, exploration, and introspection.  

AI (ChatGPT-5 and Claude Sonnet4.5) was used as a co-creator and evaluator, helping structure the ADR template and suggest scaffolding for the reflective repo.  

*Teachable Moment:*  
Documentation is not post-hoc; it *is* the architecture when the goal is learning.

---

## 6. Ethical Reflection  

- **Conflict of Interest:** I am involved in other CourseBuilder-derived projects (SWAYAM, SEEK).  
  Transparency in referencing and comparative discussions will be essential.  
- **AI Use:** ChatGPT-5 and Claude Sonnet 4.5 was used to design this ADR structure and the underlying template.  
  Evaluation and reflection remain human-led.  
- **Pedagogical Ethics:** The reflective materials will be shared publicly but will avoid proprietary or confidential architectural details of existing systems.  

This decision aligns with my [Personal Ethics Statement](../admin/personal-ethics.md), specifically the commitments to transparency, attribution, and contextual honesty.  

---

## 7. References  

> [1] S. Willison, “Link Blog and Thinking in Public,” simonwillison.net, Dec. 2024. [Online]. Available: https://simonwillison.net/2024/Dec/22/link-blog/<br/>
> [2] G. Orosz, The Software Engineering Guidebook, The Pragmatic Engineer, 2023. [Online]. Available: https://blog.pragmaticengineer.com/software-engineering-guidebook/<br/>
> [3] S. Iyer and S. Murthy, “The role of reflection in learner-centered education,” IEEE Transactions on Education, vol. 59, no. 4, pp. 246–252, 2016.<br/>
> [4] OpenAI, “ChatGPT System Card,” 2024. [Online]. Available: https://openai.com/research/system-card-chatgpt<br/>

---

## 8. Revision History  

| Date | Version | Author | Notes |
|-------|----------|---------|-------|
| 2025-11-08 | 1.0 | [Your Name] | Initial ADR for repository structure |
| — | — | — | — |

---

> *“This repo is not just about what I build, but how I learn to build it better.”*
