# CourseBuilder → Go: Learning & Migration Journal 🧭

> _A structured documentation and reflection repository for learning modern webapp development using Go, by migrating Google CourseBuilder’s architecture._

---

## 🎯 Purpose

This repository serves as a **learning journal, technical notebook, and architectural reflection space**.  
It documents the process of understanding, decomposing, and planning a re-implementation of **Google CourseBuilder** in **Go**, focusing on:

1. Building webapp architecture fluency (design, data, and deployment).
2. Documenting decisions, trade-offs, and reasoning transparently.
3. Tracking learning progress through structured journaling.
4. Capturing key resources, references, and experiment results.

No production code lives here — this repo is for **plans, insights, and artifacts**, not implementation.

---

## 🗂️ Repository Structure

```

/
├── README.md                   # This file
├── ROADMAP.md                  # High-level plan, milestones & phases
├── docs/                       # Architecture, references, module maps
│   ├── architecture/            # Diagrams, architecture outlines, cloud notes
│   ├── module-maps/             # File→module mapping (CSV, XLSX)
│   ├── references/              # Articles, papers, and official docs
│   └── howto/                   # Short guides (e.g. “Run CourseBuilder in Docker”)
├── journal/                    # Weekly logs, experiments, retrospectives
│   ├── weekly/                  # Weekly learning journals (YYYY-Wxx.md)
│   ├── learning-notes/          # Bite-sized topic notes
│   ├── experiments/             # Small hands-on experiments
│   └── retrospectives/          # Monthly/quarterly reflections
├── decisions/                   # ADRs — architectural decision records
├── templates/                   # Markdown templates for consistency
├── artifacts/                   # Generated diagrams, CSVs, exports
├── admin/                       # Repo policies (LICENSE, CONTRIBUTING, etc.)
└── .github/                     # GitHub issue templates & workflows

```

Each directory plays a defined role to keep your documentation organized, searchable, and easy to extend.

---

## 🧩 Core Components

| Area | Purpose |
|------|----------|
| **docs/** | Canonical references — architecture diagrams, design variants, technical mappings. |
| **journal/** | Your running log of learning, exploration, and weekly progress. |
| **decisions/** | Architectural Decision Records (ADRs) documenting why certain paths were chosen. |
| **templates/** | Ready-to-use Markdown templates for journals, ADRs, and experiments. |
| **artifacts/** | Any generated or exported materials (images, spreadsheets). |
| **admin/** | Governance files — LICENSE, CODE_OF_CONDUCT.md, etc. |
| **.github/** | GitHub automation (issues, workflows, markdown lint). |

---

## 🧠 Learning Workflow

This repo works best as a **weekly reflection and structured learning loop**:

| Step | Action | Folder |
|------|---------|--------|
| 1️⃣ | Capture **weekly progress**, including what you tried, learned, and failed at | `journal/weekly/` |
| 2️⃣ | Record **hands-on experiments** (logs, results, conclusions) | `journal/experiments/` |
| 3️⃣ | Maintain a **file → module mapping** of CourseBuilder | `docs/module-maps/` |
| 4️⃣ | Write **ADRs** for each architectural decision you reach | `decisions/` |
| 5️⃣ | Reflect monthly via **retrospectives** | `journal/retrospectives/` |

Optional but powerful:
- Keep a prompt bank (`docs/references/ai-prompts.md`) of AI prompts that helped.
- Maintain a glossary (`docs/references/glossary.md`) of new technical terms.

---

## 🗺️ Roadmap Overview

See [`ROADMAP.md`](./ROADMAP.md) for detailed milestones.  
High-level phases:

| Phase | Focus |
|--------|-------|
| **Setup** | Repo initialization, templates, and structure. |
| **Analysis** | Explore CourseBuilder’s architecture, create module maps. |
| **Experimentation** | Run and test small isolated components locally. |
| **Design Decisions** | Write ADRs to define migration choices (data layer, framework, etc.). |
| **Reflection** | Retrospectives and knowledge consolidation. |

---

## 🔀 Branching & Commit Strategy

| Branch | Use |
|---------|-----|
| `main` | Stable, curated documentation and finalized artifacts. |
| `dev/` | Working branch for drafts and in-progress notes. |
| `feat/...` | For specific journal/experiment additions. |

**Commit message examples:**
- `docs: add weekly journal W45`
- `chore: add ADR template`
- `experiment: run coursebuilder docker image`
- `refactor: reorganize module maps`

---

## 🧩 Issues, Labels & Milestones

| Label | Meaning |
|--------|---------|
| `journal` | Entry to document. |
| `experiment` | Hands-on test or exploration. |
| `decision` | ADR pending or accepted. |
| `resource` | New article, doc, or reference to add. |
| `blocked` | Waiting on clarification or tool setup. |
| `refactor` | Reorganizing existing notes. |

Example milestones:
- **Setup complete** — base folders, templates added.
- **Module map draft** — file-level analysis done.
- **Architecture diagrams** — baseline visual created.
- **First experiment** — Docker-based CourseBuilder run.

---

## ⚙️ CI & Automation (Optional)

Located under `.github/workflows/`

- `link-check.yml` → checks markdown links automatically.  
- `markdown-lint.yml` → enforces formatting rules.  
- `export-artifacts.yml` → optional workflow to push diagrams or CSVs to releases.

---

## 🧰 Templates

See [`/templates`](./templates/) for ready-to-use Markdown files:
- `weekly-journal.md` — consistent structure for weekly entries.
- `experiment-report.md` — step-by-step experiment documentation.
- `adr-template.md` — decision record structure.
- `module-mapping.csv` — schema for mapping CourseBuilder files.

---

## 🧩 Example Weekly Workflow

1. **Start week** → copy `templates/weekly-journal.md` → `journal/weekly/2025-W45.md`
2. **Explore** → inspect CourseBuilder module, read source, or test in Docker.
3. **Log findings** → write notes, decisions, challenges.
4. **Add ADRs** → if new design choice made.
5. **Push branch** → open PR with descriptive title (`journal: week 45 entry`).
6. **Reflect** → end of month, summarize learnings.

---

## 🪶 Author Notes

Created as part of a personal migration and learning project inspired by **Google CourseBuilder**.  
The intent is to **make learning visible**, document how AI-assisted development fits into architectural exploration, and establish a reproducible approach for deep-technical self-learning.

---

## 📜 License

This repository is licensed under the [MIT License](./admin/LICENSE).  
Feel free to fork, adapt, and use the structure for your own learning projects.

---

> “We do not learn from experience… we learn from reflecting on experience.”  
> — *John Dewey*
```