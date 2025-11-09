## Prefix prompt
Below is the output of ChatGPT for my intention to prepare a Github repo to document my learning process of WebApp Development using GO.

## Earlier output provided by ChatGPT
```
Nice — turning the learning/migration journey into a **structured, strategic GitHub repo** is a brilliant idea. Below is a complete, ready-to-use plan for the repo’s **folder architecture**, plus file templates, commit/branch guidance, issue/label strategy, and step-by-step next actions so you can start filling it immediately.

# Repo purpose (short)

A journal + project notebook for the CourseBuilder → Go migration.
No production code required — store plans, decisions, learnings, module maps, resources, retrospectives, and checkpoints. Use it as your single source of truth while you learn.

---

# Top-level folder architecture (recommended)

```md
/
├── README.md
├── ROADMAP.md
├── ROADMAP-boards/            # optional: exports from GitHub Projects (json/md)
├── docs/
│   ├── architecture/          # high-level diagrams, deployment variants, Container/Cloud run notes
│   ├── module-maps/           # file→module spreadsheets, CSVs, JSON
│   ├── references/            # papers, blog posts, official docs you referenced
│   └── howto/                 # short howtos (e.g., run original in Docker)
├── journal/
│   ├── weekly/                # weekly journals (YYYY-Wxx.md)
│   ├── learning-notes/        # bite-sized concepts & explanations
│   ├── experiments/           # small experiment writeups (what I tried, result)
│   └── retrospectives/        # monthly/quarterly retros
├── decisions/                 # ADRs (Architectural Decision Records)
│   ├── 0001-choice-template.md
│   └── ...                    
├── templates/                 # markdown templates for entries
│   ├── weekly-journal.md
│   ├── experiment-report.md
│   ├── module-mapping.csv
│   └── adr-template.md
├── artifacts/                 # generated artifacts: diagrams (svg/png), spreadsheets (xlsx/csv)
├── admin/                     # repo-level policies: CONTRIBUTING.md, CODE_OF_CONDUCT.md, LICENSE
└── .github/
    ├── ISSUE_TEMPLATE/
    │   ├── journal-issue.md
    │   ├── task.md
    └── workflows/
        ├── link-check.yml    # check dead links in docs
        └── ci-docs-lint.yml  # optionally lint markdown
```

---
```
# What each folder is for (concise)

* **docs/** — Canonical reference material and diagrams. Keep architectural diagrams and your CloudRun / GKE deployment model here.
* **journal/** — Your weekly, hands-on log. This is where you reflect: steps taken, code you explored, surprises, AI misses.
* **decisions/** — ADRs: capture each important architecture decision, alternatives, and reasons for choosing.
* **templates/** — Reusable markdown templates so entries are consistent and searchable.
* **artifacts/** — Generated files (images, spreadsheets exported from your analysis).
* **.github/** — Templates for GitHub issues and simple CI that ensures docs health (link checks, markdown linting).
* **admin/** — Repo governance (README, contributing guide, license).

---

# Essential files to create first (templates + examples)

## README.md (starter content)

```md
# CourseBuilder → Go: Learning & Migration Journal

This repository documents my learning journey and migration plan for rewriting Google CourseBuilder in Go.

Contents:
- `docs/` — architecture docs, module maps, references
- `journal/` — weekly journals, experiments, retrospectives
- `decisions/` — ADRs (architectural decisions)
- `templates/` — Markdown templates

Goals:
1. Learn modern webapp architecture via a real migration.
2. Produce a minimal, testable Go implementation of core modules.
3. Keep a clear record of what worked, what failed, and why.

See ROADMAP.md for milestones.
```
```
## templates/weekly-journal.md
```
```
# Weekly Journal - YYYY-MM-DD to YYYY-MM-DD

## Time spent (hrs)
- Planned: 5
- Actual: X

## Goals for the week
- 1.
- 2.

## Activities (hands-on first)
- Actions I took (commands, files inspected, experiments).

## Findings & Learnings
- Key takeaways, small diagrams.

## Challenges / blockers
- What failed / why (include exact errors and relevant logs).

## Where AI helped / failed
- Prompts used and how helpful they were.

## Next week plan
- 3 clear tasks for next week.
```
```
## templates/experiment-report.md
```
```
# Experiment: [short name]
Date: YYYY-MM-DD
Duration: X hrs

## Purpose
## Steps performed
## Results (screenshots, outputs, logs)
## Conclusion & Next Steps
```
```
## templates/adr-template.md
```
```
# ADR NNN: Short title
Date: YYYY-MM-DD

## Status
proposed / accepted / deprecated

## Context
Describe the problem or requirement.

## Decision
What decision was made.

## Consequences
Implications, migration steps, rollback plan.

## Alternatives considered
- Option A (rejected): reason
- Option B (rejected): reason
```
```
## templates/module-mapping.csv (columns)
```
```
file_path,module,component,language,brief_description,dependencies,notes
```

---
```
# File → module spreadsheet schema (precise)

Use CSV or Excel with these columns (keeps it machine-readable and easy to filter):

* **file_path** — path relative to repo root (e.g., `coursebuilder/models/course.py`)
* **module** — high level module (e.g., `content`, `auth`, `analytics`, `ui`, `notifications`)
* **component** — finer-grain (e.g., `lesson editor`, `email sender`)
* **language** — `python`, `js`, `html`, etc.
* **brief_description** — one-line summary of purpose
* **dependencies** — key imports/3rd-party libs or services (e.g., `appengine`, `ndb`, `jinja2`)
* **entrypoints** — main functions/classes or handlers defined
* **notes** — any migration notes (e.g., "stateful; convert to Postgres", "uses App Engine memcache API")

Put `module-maps/` CSV files and `artifacts/` exported xlsx here.

---

# Branching & commit strategy

* **main** — stable documentation & final artifacts.
* **draft/** or **dev/** — working branch for drafting notes and maps.
* **feat/journal-setup** — create initial folder + templates.
* **task/module-map** — add CSV module mapping.
  Commits: small, frequent. Use clear messages: `docs: add weekly journal template` or `chore: add ADR template`.

---

# Issues, labels & milestones (lean)

* **Issue templates**: `journal-entry`, `task`, `research-item`, `experiment`.
* **Labels**:

  * `journal` — entries to write
  * `experiment` — small hands-on trial
  * `blocked` — needs external help
  * `refactor` — reorganize docs
  * `decision` — ADR to write/accept
  * `resource` — add to refs
* **Milestones**:

  * `setup` — repo initialised, templates in place
  * `map-complete` — file→module spreadsheet done
  * `arch-diagram` — diagram for containerized deployment
  * `first-experiment` — run CourseBuilder in Docker locally

---

# CI / GitHub Actions (suggested)

Minimal workflows:

* **link-check.yml** — run a link checker on markdown to catch broken external refs.
* **markdown-lint.yml** — optional linting (markdownlint) to keep docs consistent.
* **export-artifacts.yml** — on push to main, export `artifacts/` to release (optional).

These protect your docs and keep the repo tidy.

---

# Start-up checklist (step by step to get repo live)

1. Create a new GitHub repo with the name you want (e.g., `coursebuilder-migration-journal`).
2. Add a `README.md` with the starter content above.
3. Create `templates/` and add the 3 template files.
4. Create `journal/weekly/` and add a sample entry `YYYY-W01.md` using the weekly template.
5. Add `decisions/0001-choice-template.md` (ADR template).
6. Add `.github/ISSUE_TEMPLATE/` with `journal-issue.md` and `task.md`.
7. Add a `.github/workflows/link-check.yml` (simple link check).
8. Create initial milestone `setup` and label `journal`.
9. Make a first commit and push to `main`. Create `dev` branch for drafts.
10. Open an Issue: “Populate file→module mapping” and assign to yourself.

I can generate the exact markdown files if you want — tell me which files to create and I’ll produce their contents here for copy/paste.

---

# How to use the repo as you learn (workflow)

* **Weekly**: create a `journal/weekly/YYYY-Wxx.md` within your 5 hours. Be specific: commands, file paths you opened, errors, and links to resources.
* **When you make a decision**: write an ADR (`decisions/0002-...md`) immediately with alternatives.
* **When you inspect code**: update `docs/module-maps/coursebuilder_files.csv` with any files you analyzed that week.
* **When experiments fail**: write an `experiments/` entry with steps and logs (this is gold for later reflection).
* **At the end of month**: write a `retrospective` summarizing what you learned, what to change in plan.

---

# Extra ideas (optional but high value)

* Keep an **AI prompt bank** (templates of prompts that worked well with ChatGPT/Claude) under `docs/references/ai-prompts.md`.
* Maintain a **glossary** (`docs/references/glossary.md`) of terms you learn (e.g., GKE, Cloud Run, App Engine, blobstore).
* Use GitHub Projects (board) for Kanban of experiments, mapping to milestones.

---

# Quick sample: first 3 commits to land

1. `chore: add README, LICENSE, basic folder skeleton`
2. `chore: add templates (weekly, experiment, adr, module-csv)`
3. `docs: add initial sample weekly journal and module-mapping stub`

---

If you want, I’ll do one of these next (choose one and I’ll produce the file contents ready to paste):

* A full `README.md` file (complete version).
* The `templates/` files as full markdown content (I can paste each file).
* The `module-mapping.csv` starter with the schema and example rows (small sample).
* A sample ADR (`0001`) populated with a hypothetical decision.

Which one shall I generate first?
```
## Suffix prompt
Can you generate a full README.md file for the repo?

