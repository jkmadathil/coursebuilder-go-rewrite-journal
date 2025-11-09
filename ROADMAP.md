# 🛣️ CourseBuilder → Go Learning Roadmap (Weeks 1 – 9)

> _A structured 9-week roadmap for exploring Google CourseBuilder and translating its concepts into a modern Go-based webapp architecture._

This roadmap defines **weekly milestones**, **learning goals**, and **activities** that combine:
- Hands-on exploration of CourseBuilder’s code and deployment model.
- Complementary conceptual learning in Go, cloud architecture, and design patterns.
- Reflection and journaling to consolidate learning.

---

## 🌍 Phase Overview

| Phase | Weeks | Focus |
|--------|--------|--------|
| **Phase 1 – Orientation & Setup** | 1–2 | Environment setup, repo initialization, base understanding of CourseBuilder |
| **Phase 2 – Deep Exploration** | 3–5 | Module mapping, experimentation, Go ecosystem learning |
| **Phase 3 – Migration Thinking** | 6–8 | Architecture translation, ADRs, component refactoring plans |
| **Phase 4 – Reflection & Synthesis** | 9 | Summarization, retrospectives, roadmap revision |

---

## 🗓️ Week-by-Week Plan

### **Week 1 – Project Setup & Baseline**
**Milestone:** Repository created and structured for journaling.

**Goals**
- Initialize GitHub repo with all base folders and templates.
- Run CourseBuilder locally (Docker or App Engine SDK).
- Document initial understanding of project purpose and structure.

**Learning Activities**
- Hands-on:  
  - Clone CourseBuilder repo and explore directory structure.  
  - Set up local environment (Docker or Python virtualenv).  
- Reflection:  
  - Write first weekly journal (`journal/weekly/2025-W01.md`).  
  - Record ADR 0001 (“Initial Repository Setup”).  
- Beyond CourseBuilder:  
  - Read “How Google App Engine Works” and “GAE → Cloud Run migration” articles.  
  - Watch one intro talk on Go’s philosophy and standard library organization.

---

### **Week 2 – Go Foundations & Web Architecture Primer**
**Milestone:** Comfortably run Go locally and understand Go project structure.

**Goals**
- Learn Go basics: syntax, modules, packages, testing.
- Compare Python’s CourseBuilder architecture to Go’s conventions.
- Capture early insights into module boundaries.

**Learning Activities**
- Hands-on:  
  - Build a small Go web server (simple HTTP handler).  
  - Explore Go’s `net/http`, `html/template`, and basic REST design.  
- Reflection:  
  - Document “Python vs Go Architecture” in `docs/learning-notes/`.  
- Beyond CourseBuilder:  
  - Complete Tour of Go (https://go.dev/tour/).  
  - Read “Twelve-Factor App” principles and map to CourseBuilder’s design.

---

### **Week 3 – Module Mapping & Static Analysis**
**Milestone:** Draft `docs/module-maps/coursebuilder_files.csv` completed.

**Goals**
- Understand how CourseBuilder modules interconnect.
- Classify core domains (content, auth, analytics, UI).

**Learning Activities**
- Hands-on:  
  - Analyze 50–100 files and populate `module-mapping.csv`.  
  - Identify external dependencies (App Engine APIs, Jinja2, NDB).  
- Reflection:  
  - Record findings in `journal/weekly/W03.md`.  
- Beyond CourseBuilder:  
  - Study Go dependency management (`go.mod`, vendoring).  
  - Read about hexagonal / clean architecture in Go.

---

### **Week 4 – Experimentation & Prototype Setup**
**Milestone:** First small experiment completed and documented.

**Goals**
- Run one component of CourseBuilder in isolation.
- Create first Go prototype replicating a minimal feature.

**Learning Activities**
- Hands-on:  
  - Experiment #1 — Run CourseBuilder in Docker or GAE local dev.  
  - Prototype a Go handler serving a Course/Module list from mock data.  
- Reflection:  
  - Write `experiment-report-001.md` and journal observations.  
- Beyond CourseBuilder:  
  - Learn Go templates, middleware pattern, and routing libraries (`chi` / `gin`).  
  - Watch a short video on Go concurrency basics.

---

### **Week 5 – Data Layer & Persistence Decisions**
**Milestone:** First ADRs for persistence & configuration recorded.

**Goals**
- Understand CourseBuilder’s datastore model.
- Evaluate potential Go replacements (PostgreSQL + GORM, or Firestore).

**Learning Activities**
- Hands-on:  
  - Inspect `models/` in CourseBuilder; note schema and relationships.  
  - Write ADR 0002 – “Data Persistence Approach in Go”.  
- Reflection:  
  - Journal how state management differs in Go.  
- Beyond CourseBuilder:  
  - Learn SQL basics for Go (database/sql).  
  - Explore Go ORMs and their trade-offs (GORM, sqlx, ent).  

---

### **Week 6 – Architecture Diagrams & API Mapping**
**Milestone:** Draft architecture diagram for Go-based design.

**Goals**
- Visualize CourseBuilder architecture (current) and planned Go version.
- Identify service boundaries and request flow.

**Learning Activities**
- Hands-on:  
  - Create `docs/architecture/coursebuilder-overview.svg`.  
  - Create corresponding Go version diagram.  
- Reflection:  
  - Record ADR 0003 – “Monolith vs Modular Go Structure”.  
- Beyond CourseBuilder:  
  - Study “Go project layout” (golang-standards/project-layout).  
  - Watch one talk on microservices vs modular monoliths in Go.

---

### **Week 7 – Cloud Deployment & Config Strategy**
**Milestone:** Deployment plan outline for Go version.

**Goals**
- Understand CourseBuilder’s deployment in App Engine.
- Design equivalent Go deployment (Cloud Run / GKE / Docker).

**Learning Activities**
- Hands-on:  
  - Write a Dockerfile for your prototype.  
  - Run it on local container runtime.  
- Reflection:  
  - ADR 0004 – “Deployment Strategy”.  
- Beyond CourseBuilder:  
  - Learn about CI/CD with GitHub Actions + Cloud Run.  
  - Read about environment variable config and secrets management in Go.

---

### **Week 8 – Observability & Error Handling**
**Milestone:** Logging and error strategy defined for migration.

**Goals**
- Review CourseBuilder’s logging/error approach.
- Define Go-based observability stack.

**Learning Activities**
- Hands-on:  
  - Experiment #2 — Integrate structured logging in your Go prototype.  
  - Capture metrics or tracing (log output suffices).  
- Reflection:  
  - ADR 0005 – “Error & Logging Policy”.  
- Beyond CourseBuilder:  
  - Learn Go error wrapping (`errors`, `%w`) and logging packages (`zerolog`, `slog`).  
  - Read “Structured Logging in Go at Scale”.

---

### **Week 9 – Synthesis & Retrospective**
**Milestone:** Phase 1 learning complete; reflection and roadmap v2 drafted.

**Goals**
- Consolidate insights, finalize documentation, and identify next focus areas.
- Evaluate progress and gaps.

**Learning Activities**
- Hands-on:  
  - Write `journal/retrospectives/2025-phase1-retrospective.md`.  
  - Update ROADMAP.md with next-phase goals.  
- Reflection:  
  - Review all ADRs and journals; highlight three key decisions to revisit.  
- Beyond CourseBuilder:  
  - Write a blog-style summary or LinkedIn post sharing your learning journey.  
  - Explore “Go web frameworks comparison” (standard lib vs Gin vs Fiber).

---

## 🧭 How to Use This Roadmap

- Treat each **week** as a **focused sprint** with tangible deliverables.
- Use **weekly journals** to document not just what you did, but what you _learned_.
- Link all artifacts (ADRs, diagrams, experiments) to the related week.
- Adjust milestones as insights evolve — this roadmap is living documentation.

---

## 🧠 Stretch Activities (Optional Enrichment)

- Keep an **AI prompt log** (`docs/references/ai-prompts.md`) for prompts that yield strong architectural insights.
- Start a **personal glossary** of terms learned (`docs/references/glossary.md`).
- Maintain a **resource index** — favorite papers, articles, and repos.
- At the end of Week 9, conduct a **self-review** of how effectively AI assisted your exploration.

---

> “Learning to architect systems means learning to _see_ — to trace dependencies, identify patterns, and make reasoning explicit.”  
> — *Adapted from Martin Fowler*
