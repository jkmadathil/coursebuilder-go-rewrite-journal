# 🧠 AI Prompts Log — Planning CourseBuilder Migration to Go 

_Last updated: 2025-11-09_  
[_Linked Ethics Statement:_](../../admin/personal-ethics.md)



---

## Prompt 1 - Identify existing architecture documentation for CourseBuilder
## Actual Prompt
I'm planning to rewrite Google Course Builder in Go. The repository can be found at: https://github.com/google/coursebuilder-core

Is there a way I can get the architecture document to understand the modules in this codebase

## Purpose
Find any official or community architecture/design documentation (diagrams, papers, READMEs) to understand the system modules before attempting a rewrite.

## Output summary
The assistant searched public resources and returned: link to the GitHub repo (archived), references to archive pages, and related academic/technical papers describing CourseBuilder architecture. It concluded there is no single authoritative architecture document in the repo and suggested a process for reconstructing one from code and available resources.

## Critical Evaluation

### Strengths
- The prompt gives immediate context (intent to rewrite) and a direct pointer to the repo URL — allowing the assistant to prioritize repository-specific resources.
- It asks a precise, actionable question (“Is there a way I can get the architecture document…”) which leads to concrete search and reconstruction suggestions.

### Limitations
- It asks for an "architecture document" but doesn't specify what format/output you want if none exists (e.g., diagram, module list, PlantUML, or a procedural plan to reconstruct).
- It assumes such a document exists; the assistant needed to clarify next steps when it does not.

### Better Prompt Strategy
- If you want a final artifact produced by the assistant when no doc exists, specify format and scope. Example improved prompt:
  > “I’m planning to rewrite Google Course Builder in Go. The repo is at https://github.com/google/coursebuilder-core. Search for any architecture or design documentation and, if none exists, reconstruct a high-level architecture diagram (PlantUML + Markdown) and a module mapping by analyzing the repo’s top-level folders. Export the module map as CSV.”

---

## Prompt 2 - Can the assistant analyze the repository?
## Actual Prompt
Will it be possible for you to go through the code repo of course builder?

## Purpose
Confirm assistant capability and scope for codebase analysis (what it can and cannot do), and the kinds of deliverables to expect.

## Output summary
Assistant confirmed it can go through the repo and described possible deliverables: module/folder mapping, dependencies, high-level architecture, and redesign suggestions for Go. It also noted the repo is archived and may use older App Engine patterns.

## Critical Evaluation

### Strengths
- Short, direct question; good for scope confirmation.
- Allowed the assistant to set expectations and outline deliverables.

### Limitations
- Does not specify *how deep* the analysis should be (file-level, function-level, or only folder-level).
- No output format requested (table, CSV, visual diagram).

### Better Prompt Strategy
- Ask for specific depth and format. Example:
  > “Yes/no: can you analyze the repository at this depth — 1) folder-level responsibilities, 2) file-to-module mapping (CSV), 3) dependency graph (graphviz)? If yes, produce items 1 and 2 first.”

---

## Prompt 3 - Prioritize initial steps
## Actual Prompt
Do steps 1 and 2 first

## Purpose
Directive to the assistant to execute the previously discussed first tasks (likely: produce a high-level folder map and begin code walkthrough).

## Output summary
Assistant acknowledged and proposed an approach: listing top-level folders, annotating responsibilities, creating architecture artifacts, and mapping to Go packages.

## Critical Evaluation

### Strengths
- Conveys clear sequencing: do foundational tasks first.
- Keeps the interaction action-oriented.

### Limitations
- Relies on the assistant's interpretation of “steps 1 and 2” — could be ambiguous depending on prior messages.
- Would be stronger if you restated the exact steps (to avoid misinterpretation).

### Better Prompt Strategy
- Repeat the two steps explicitly in the prompt to remove ambiguity. Example:
  > “Do these first: (1) List top-level folders and describe each folder’s responsibility; (2) Produce a CSV mapping of files to tentative modules.”

---

## Prompt 4 - Create a high-level architecture diagram and containerization suggestions
## Actual Prompt
Create a high-level architecture diagram first and suggest modifications to reflect the containerized application deployment (like CloudRun or GKE) that is available at the moment

## Purpose
Produce a diagram and migration recommendations for modern containerized deployment (Cloud Run/GKE)—a modernization view.

## Output summary
Assistant produced a textual high-level architecture and suggested containerization-friendly adjustments (service boundaries, statelessness, externalized config) and recommended deployment targets but did not produce an image. Also recommended steps to make diagram after module mapping.

## Critical Evaluation

### Strengths
- Clear aim: modernize architecture for containers.
- Triggers useful containerization concerns (statelessness, storage, sessions).

### Limitations
- The prompt requests a “diagram” but does not specify the desired diagram format (textual, PlantUML, PNG) or whether the assistant should auto-generate PlantUML/ASCII diagrams.
- Without the repo-level module mapping, the diagram would be speculative.

### Better Prompt Strategy
- Specify the desired output format and acceptability of a textual diagram. Example:
  > “Produce a PlantUML component diagram and accompanying notes showing how CourseBuilder’s major modules map to containerized services for Cloud Run or GKE. If repository analysis isn’t done yet, annotate areas requiring confirmation.”

---

## Prompt 5 - Produce a detailed file→module map
## Actual Prompt
Produce a detailed file→module map

## Purpose
Obtain a machine-readable mapping of source files to higher-level functional modules to guide migration.

## Output summary
Assistant produced a heuristic-based mapping (handlers, models, templates, static, utils, etc.) and offered to export to Excel/CSV. It noted heuristics may need refinement (e.g., analyzing imports for higher accuracy).

## Critical Evaluation

### Strengths
- Very actionable and directly helpful for migration planning.
- Clear deliverable: file→module map, exportable for spreadsheets.

### Limitations
- Short prompt — no format/columns specified (e.g., file path, inferred module, evidence, major classes, TODO).
- Heuristic-only mapping can misclassify files; import dependency analysis or docstring parsing would improve accuracy.

### Better Prompt Strategy
- Specify required columns and analysis depth. Example:
  > “Produce a CSV with columns: file_path, inferred_module, key_classes/functions, supporting_evidence (import lines or docstring excerpt), confidence_score. Use import analysis where possible.”

---

## Prompt 6 - Microservices migration plan context
## Actual Prompt
I am looking at a microservices migration plan

## Purpose
Communicate high-level intent to migrate the system towards microservices — sets context for follow-up work.

## Output summary
Assistant incorporated this intent later in suggested architecture and migration planning, recommending service boundaries and migration strategies (strangler, incremental extraction).

## Critical Evaluation

### Strengths
- Important context that informs design, deployment, and testing recommendations.

### Limitations
- Very terse. Doesn’t provide constraints (must-run-on-CloudRun, latency targets, budget, or team size), which affect migration choices.

### Better Prompt Strategy
- Augment with constraints and goals: Example:
  > “I aim to migrate CourseBuilder toward microservices with these constraints: single developer initially, target Cloud Run, goal to containerize one service every 4 weeks, and minimal cloud costs. Propose a migration plan.”

---

## Prompt 7 - Provide a precise file-module spreadsheet from uploaded zip
## Actual Prompt
Attached is a zip of the coursebuilder-core. Can you create a precise file-module spreadsheet?

## Purpose
Have the assistant operate on the uploaded code archive to produce a concrete spreadsheet mapping files to modules.

## Output summary
Assistant extracted the zip (attempted), ran a heuristic classifier and saved a spreadsheet (XLSX) with `path` and `module` columns. The assistant noted that classification was heuristic and could be improved by analyzing imports and semantics.

## Critical Evaluation

### Strengths
- Directly actionable: uses the actual code archive the user provided.
- Produced a tangible artifact (spreadsheet) to iterate on.

### Limitations
- The mapping approach was heuristic; the result may be noisy or miss cross-file semantics.
- The prompt could have requested additional columns (e.g., file size, lines of code, last modified, primary classes/functions) to prioritize work.

### Better Prompt Strategy
- Request explicit spreadsheet columns and ask for a confidence metric. Example:
  > “Using the attached `coursebuilder-core.zip`, create a CSV with these columns: file_path, inferred_module, top_level_classes/functions, import_signatures (first 10 imports), LOC, confidence(0-1). Also include a filtered sheet with files that likely belong to 'content' or 'auth' modules.”

---

## Prompt 8 - Beginner-friendly 3-month plan
## Actual Prompt
If I told you that i do not have any background on Application Development, can you provide me a 3 month plan (Assuming I will be able to devote 5 hours every week) to understand the architecture of coursebuilder and how a web application works

## Purpose
Obtain a paced, beginner-friendly learning plan aligned with the CourseBuilder context and limited weekly time.

## Output summary
Assistant produced a 12-week plan focusing on running CourseBuilder locally, learning web fundamentals, and incremental exploration of modules, with deliverables and suggested reading.

## Critical Evaluation

### Strengths
- Practical, achievable pacing that matches the 5 hours/week constraint.
- Emphasized hands-on work, which suits newcomers.

### Limitations
- Could include exact resource links and commands for hands-on setup.
- No embedded checkpoints for journaling or measuring progress.

### Better Prompt Strategy
- Ask for a week-by-week checklist with direct resource links and journaling prompts. Example:
  > “Produce a 12-week plan with weekly hands-on tasks, terminal commands to run CourseBuilder locally, and a short journaling prompt per week to reflect learnings.”

---

## Prompt 9 - Local install feasibility and cloud subscription requirement
## Actual Prompt
Can I install coursebuilder in my local machine (Ubuntu Linux) and get my hands dirty? Does it need a cloud subscription?

## Purpose
Clarify whether local experimentation is possible and whether cloud services are mandatory.

## Output summary
Assistant answered: yes, you can run locally (Docker recommended), and a cloud subscription is not required for local dev. Optionally mentioned App Engine specifics and suggested Dockerizing the app.

## Critical Evaluation

### Strengths
- Directly reduces friction to getting started.
- Emphasized Docker approach which is practical and cloud-independent.

### Limitations
- The prompt could have asked for a ready-to-run Dockerfile and step-by-step commands to be included in the response.

### Better Prompt Strategy
- Be actionable: Example:
  > “Confirm local install is possible and provide a Dockerfile plus step-by-step commands to run CourseBuilder on Ubuntu without Google Cloud subscription.”

---

## Prompt 10 - Dockerfile then step-by-step instructions
## Actual Prompt
Provide a Dockerfile first, then provide step-by-step instructions on using it

## Purpose
Request concrete tooling to run CourseBuilder locally (Dockerfile + instructions).

## Output summary
Assistant acknowledged and attempted to provide a Dockerfile and steps (later in the conversation the assistant produced guidance and attempted to run code to produce artifacts).

## Critical Evaluation

### Strengths
- Very actionable; when fulfilled, removes setup blockers.

### Limitations
- The prompt does not specify environment preferences (Python version, ports, whether to use Cloud Datastore emulator or a local DB) or how to persist data across restarts.

### Better Prompt Strategy
- Include execution environment details. Example:
  > “Provide a Dockerfile that runs the CourseBuilder code on Ubuntu with Python 3.9, exposes port 8080, uses SQLite for local storage (or an emulated Datastore), and add step-by-step commands to build and run.”

---

## Prompt 11 - 6-month, hands-on Go learning plan
## Actual Prompt
What if I plan to learn WebApp development by using the CourseBuilder migration project in GO? Can you provide me a 6 month plan to proceed? The plan should consider the fact that 
- I have only 5 hours to spend in a week for learning and development, 
- I like doing hands-on first and then learning theory, 
- I have some basic understanding of CourseBuilder functionalities
- I do have some basic Python scripting experience
- I do have subscriptions to Claude (Pro) and ChatGPT

## Purpose
Request an extended, project-based learning plan that uses CourseBuilder migration as the learning vehicle — with hands-on-first emphasis and limited weekly time.

## Output summary
Assistant provided a detailed 6-month plan broken into phases (run & explore original, Go fundamentals, re-architecting, implement core services, containerization & cloud, and documentation), with recommended resources and deliverables.

## Critical Evaluation

### Strengths
- Comprehensive and well-structured; balances hands-on coding and theory.
- Tailored to constraints and existing skills.

### Limitations
- Could include more explicit milestones (sample PRs, specific microservices to extract first), assessment rubrics, or sample weekly exercises.

### Better Prompt Strategy
- Ask for taskable micro-sprints and milestone checkpoints. Example:
  > “Produce a 6-month plan with 2-week sprints, list of sprint goals, sample issues/PR titles for each sprint, and acceptance criteria for each milestone.”

---

## Prompt 12 - Convert plan into a GitHub journaling repo
## Actual Prompt
I would want to make a harder commitment by converting the current plan as part of a Github repo. This repo will be both my journaling space and space to reflect back on the learning process. This repo will not have any code, rather will have steps, resources referred, key challenges, learnings from the challenges, things where AI didn't work etc 

I need to create a strategic plan for the folder architecture first and then move step by step

## Purpose
Design a repository structure and strategy for journaling and documenting the learning & migration process (non-code repo).

## Output summary
Assistant suggested a repo folder structure (`/docs/`, `/journal/weeks/`, `/ai/`, `/resources/`, `/milestones/`) and content guidance for what to put in each folder.

## Critical Evaluation

### Strengths
- Suitable structure for reflection, tracking, and resource curation.
- Keeps code and learning artifacts separate (per your requirement).

### Limitations
- Could have provided concrete README templates and sample file templates for weekly journaling and AI-interaction logs.

### Better Prompt Strategy
- Request ready-made templates. Example:
  > “Provide a GitHub repo folder structure plus README templates for `/journal/week-##/`, `/ai/`, and `/milestones/`, and a sample weekly journal entry file.”

---

## Prompt 13 - Synthesize prompts into ai-prompts.md
## Actual Prompt
I need to synthesize all the prompts that I have used in this chat so that I can add it to a file ai-prompts.md.

While creating the markdown file, it will be useful to comment on what the prompt helps in and also provide a critical evaluation of it to recommend better prompting strategies to obtain a much better output

## Purpose
Request a meta-document that catalogs prompts, their purpose, output, and critical evaluation for future prompt-engineering improvements.

## Output summary
Assistant produced an `ai-prompts.md` draft with summarized prompts, purposes, output summaries, and critique. (This current document is the revised version.)

## Critical Evaluation

### Strengths
- Useful for meta-learning and improving prompt craft.
- Encourages reflective practice.

### Limitations
- The initial draft paraphrased prompts rather than including the exact raw prompts; you later asked for verbatim prompts to be stored separately.

### Better Prompt Strategy
- Combine both needs: ask explicitly for a verbatim `actual-prompts/*.md` file and a separate analyzed `ai-prompts.md` referencing that raw file. Example:
  > “Create `./actual-prompts/planning-prompt-001.md` containing exact prompts, then produce `ai-prompts.md` with analysis referencing that file.”

---

## Prompt 14 - Request for verbatim prompts concatenation
## Actual Prompt
Many of the prompts given in the ai-prompts.md seems to be summary of the actual prompts that I gave. Is there a way to concatenate the actual prompts as is in an md file?

## Purpose
Clarify the desire to have unmodified, verbatim prompts stored in an MD file for reproducibility.

## Output summary
Assistant confirmed this was possible and offered an approach (manual copy or script to extract prompts from chat export). The assistant subsequently produced the verbatim raw prompts in `./actual-prompts/planning-prompt-001.md`.

## Critical Evaluation

### Strengths
- Explicitly asks for reproducible record keeping — an excellent research practice.
- Enables later analysis and fine-grained prompt improvement.

### Limitations
- None — this was a precise and actionable request.

### Better Prompt Strategy
- If you want automation, specify the chat-export format you will use (ChatGPT JSON or another) and ask the assistant to produce a script to extract prompts automatically.

---

# Meta-insights (observations across all prompts)
1. **Be explicit about output format.** Many prompts asked for artifacts (diagram, spreadsheet, Dockerfile) but didn’t specify exact output format (PlantUML, PDF, CSV columns). Adding precise output constraints produces more usable results.
2. **Context + constraints matter.** When asking for architecture/migration, include operational constraints (target cloud, budget, team size, latency, storage patterns). These materially change recommendations.
3. **Ask for evidence.** When the assistant maps a file to a module, request the supporting evidence (import lines, docstring excerpt) so you can trust classifications.
4. **Iterative, layered prompting works best.** Big requests should be split: (A) discover, (B) map, (C) diagram, (D) migrate. Use short, clear steps and affirm outputs at each stage.
5. **Preserve raw prompts.** Keeping verbatim prompts in `/actual-prompts/` is essential for reproducibility and for later automated analysis (e.g., prompt-performance tracking).
6. **Add acceptance criteria.** For actionable deliverables (e.g., “produce spreadsheet”), include expected columns and an acceptance test (e.g., “contains at least these 5 modules: content, auth, tracking, UI, integrations”).
7. **Templates accelerate journaling.** When creating the learning repo, request templates for weekly journals, AI-interaction logs, and ADRs — this reduces cognitive load and increases consistency.

---

### ✨ Final Note

This file itself is *both* a learning artifact and a template for others doing AI-assisted software redesign.  
Keep adding to it weekly — log new prompts, annotate why they were used, and refine your prompting craft as part of your developer growth.

---
