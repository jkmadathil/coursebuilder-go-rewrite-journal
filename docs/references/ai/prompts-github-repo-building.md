# 🤖 Prompt Collection and Reflection: Repository Structure & Learning Framework

_Last updated: 2025-11-09_  
[_Linked Ethics Statement:_](../../admin/personal-ethics.md)

This document synthesizes all prompts used during the initial creation of the **CourseBuilder → Go Learning and Migration Journal** repository.  
Each section includes:
- the original **prompt or question**,  
- the **purpose** it served in the repo design process,  
- a **critical evaluation** of the AI’s response,  
- and **recommendations** for more effective future prompting.  

---

## 🧩 Prompt 2 — “Generate a full README.md for the repo”

**Actual Prompt:**
Refer the [prompt-001](./actual-prompts/repo-building-prompt-001.md)

**Purpose:**  
To create the narrative identity of the repository — its mission, workflow, and how learners should use it.  

**Output Summary:**  
Produced a well-structured README with clear purpose, folder descriptions, learning workflow, and reflection cadence.

**Critical Evaluation:**  
- ✅ **Strengths:** Clear structure, accessible language, reusable sections.  
- ⚠️ **Limitations:** The tone was somewhat impersonal and formal; lacked introspective context.  
- 💡 **Better Prompt Strategy:** Preface the request with _“Write this README in my personal reflective voice, balancing academic rigor with personal tone.”_  

---

## 🧩 Prompt 2 — “Generate ROADMAP.md for Weeks 1–9 with milestones, goals, and learning activities”

**Actual Prompt:**
Refer the [prompt-002](./actual-prompts/repo-building-prompt-002.md)

**Purpose:**  
To create a concrete temporal learning plan bridging technical tasks (CourseBuilder analysis) and pedagogical reflection.

**Output Summary:**  
AI generated a week-by-week roadmap integrating milestones, hands-on activities, reflective exercises, and AI-related meta-tasks.

**Critical Evaluation:**  
- ✅ **Strengths:** Beautifully aligned milestones → goals → learning activities; strong structure.  
- ⚠️ **Limitations:** Slightly linear; did not model iterative learning cycles or failure pathways.  
- 💡 **Better Prompt Strategy:** Add _“Include failure loops and reflection checkpoints per phase”_ to promote cyclical rather than linear learning design.  

---

## 🧩 Prompt 3 — “Create the Weekly Journal Template with TIL and teachable moments”

**Actual Prompt:**
Refer the [prompt-003](./actual-prompts/repo-building-prompt-003.md)

**Purpose:**  
To define a flexible, learning-oriented journaling scaffold integrating reflection, link-blogging (à la Simon Willison), and teachable moments.

**Output Summary:**  
Generated a multi-section markdown template including plans, activities, TILs, link blog, teachable moments, and reflection.

**Critical Evaluation:**  
- ✅ **Strengths:** Excellent coverage of reflective dimensions (plan, learning, externalization, teaching).  
- ⚠️ **Limitations:** Could be simplified for weekly reuse; slightly verbose.  
- 💡 **Better Prompt Strategy:** Next time, include _“Make it concise and easy to reuse weekly; optimize for iterative entries”_ to keep cognitive load lower.  

---

## 🧩 Prompt 4 — “Create Experiment Report Template (for both technical and pedagogical experiments)”

**Actual Prompt:**
Refer the [prompt-004](./actual-prompts/repo-building-prompt-004.md)

**Purpose:**  
To scaffold reflective documentation for all forms of experiments — technical, process, and pedagogical.

**Output Summary:**  
A deeply reflective structure with ethical anchoring, failure documentation, and teachable moment sections.

**Critical Evaluation:**  
- ✅ **Strengths:** Outstanding coverage of non-technical experiments, failure visibility, and ethical linkage.  
- ⚠️ **Limitations:** Slightly abstract — may overwhelm early-stage experimenters.  
- 💡 **Better Prompt Strategy:** Add _“Include a minimal quick version at the end for short experiments”_ to make it more flexible.

---

## 🧩 Prompt 5 — “What key points should I include in a personal ethics statement?”

**Actual Prompt:**
Refer to the first prompt in [prompt-005](./actual-prompts/repo-building-prompt-005.md)

**Purpose:**  
To define the philosophical and behavioral foundation for the learning repo.

**Output Summary:**  
AI proposed a multi-section ethical framework covering integrity, attribution, AI use, learning in public, and reflection revision.

**Critical Evaluation:**  
- ✅ **Strengths:** Comprehensive, aligned with reflective pedagogy.  
- ⚠️ **Limitations:** Initially generic; needed contextual personalization.  
- 💡 **Better Prompt Strategy:** Provide more self-context at the outset (e.g., “I work on CourseBuilder-related projects and teach faculty development”) to ground AI’s tone and focus.  

---

## 🧩 Prompt 6 — “Draft my first personal ethics statement” (+ your inputs)

**Actual Prompt:**
Refer to the second prompt in [prompt-005](./actual-prompts/repo-building-prompt-005.md)

**Purpose:**  
To produce a deeply contextual ethics statement incorporating your real professional setting, conflicts of interest, and AI practices.

**Output Summary:**  
Resulted in a rich, nuanced personal ethics statement with nine sections and an actionable reflection checklist.

**Critical Evaluation:**  
- ✅ **Strengths:** Authentically personalized; transparent; pedagogically grounded.  
- ⚠️ **Limitations:** Quite detailed; may need a shorter public summary for readers.  
- 💡 **Better Prompt Strategy:** Use _“Also draft a one-page summary for public sharing”_ to make it more portable.  

---

## 🧩 Prompt 8 — “Populate the ADR template” and “Create ADR 0001-initial-repo-structure.md”

**Actual Prompt:**
Refer to the Prompts 1-3 in [prompt-007](./actual-prompts/repo-building-prompt-007.md)

**Purpose:**  
To formalize architectural decision-making for reflective and meta-learning contexts.

**Output Summary:**  
A hybrid ADR template combining engineering reasoning, reflection, and ethics.  
Then, an ADR documenting the meta-decision to use a reflective repo structure.

**Critical Evaluation:**  
- ✅ **Strengths:** Bridged engineering documentation with meta-cognitive reflection.  
- ⚠️ **Limitations:** Overly verbose for everyday decisions; might discourage consistent use.  
- 💡 **Better Prompt Strategy:** Add _“Make ADRs modular — a short version for small decisions, full version for major ones”_.

---

## 🧩 Prompt 9 — “What should the module-mapping.csv look like?”

**Actual Prompt:**
Refer to the Prompt 4-5 in [prompt-007](./actual-prompts/repo-building-prompt-007.md)


**Purpose:**  
To define how to transform a technical inventory into a learning-centric data artifact.

**Output Summary:**  
Outlined a hybrid schema balancing structural metadata and reflection-driven fields.

**Critical Evaluation:**  
- ✅ **Strengths:** Elegant synthesis of technical and pedagogical data design.  
- ⚠️ **Limitations:** Could include examples of linking reflection links dynamically.  
- 💡 **Better Prompt Strategy:** Add _“Include examples of how to automate or visualize reflection links later”_.  

---

## 🧩 Prompt 10 — “Create module-mapping-guide.md and advise where to store it”

**Actual Prompt:**
Refer to the Prompt 6 in [prompt-007](./actual-prompts/repo-building-prompt-007.md)


**Purpose:**  
To produce a companion manual that helps future contributors interpret the CSV structure and workflow.

**Output Summary:**  
A comprehensive guide covering each column, reflection process, and weekly workflow.

**Critical Evaluation:**  
- ✅ **Strengths:** Readable, self-contained, pedagogically sound.  
- ⚠️ **Limitations:** Slightly dense — could be chunked into shorter pages if used for teaching.  
- 💡 **Better Prompt Strategy:** Add _“Design it for multi-page GitHub Pages navigation”_ if later you plan to publish it as a guidebook.  

---

## 🧩 Prompt 11 — “Synthesize all prompts into prompts-repo-structure.md”

**Actual Prompt:**
Refer to the [prompt-013](./actual-prompts/repo-building-prompt-013.md)

**Purpose:**  
To compile a reflective log of AI–human collaboration in shaping this repository.

**Output Summary:**  
(You are reading it!) A meta-summary of all prompt interactions, their purposes, and improvement strategies.

**Critical Evaluation:**  
- ✅ **Strengths:** Embeds meta-cognition into the documentation; traces evolution of AI usage.  
- ⚠️ **Limitations:** Time-bound — should be versioned or snapshot periodically.  
- 💡 **Better Prompt Strategy:** Add _“Create a periodic prompts summary (quarterly) to capture evolving prompt design patterns.”_

---

## 🔍 Meta-Insights Across All Prompts

| Dimension | Observation | Future Prompting Strategy |
|------------|--------------|----------------------------|
| **Framing** | Most prompts were task-driven (“Generate X”) rather than intention-driven (“Help me reason about…”). | Use verbs like *reason*, *reflect*, *compare*, *simulate* to draw deeper outputs. |
| **Context Setting** | The most effective prompts gave self-context (your professional background, teaching goals). | Always include 1–2 sentences of personal context for tone alignment. |
| **AI Role Framing** | Explicitly naming the AI’s role (collaborator, evaluator, co-learner) improved outcomes. | Begin prompts with: *“Act as a reflective learning partner helping me reason about…”*. |
| **Output Guidance** | Specifying structure (tables, Markdown, sections) produced reproducible, high-quality outputs. | Continue using format hints, but balance them with creative space. |
| **Iteration** | Most drafts were refined by dialogue — the quality came from conversation, not the first hit. | Encourage iterative prompting: *“Generate a base draft, then refine tone and pedagogy.”* |

---

> “Prompting is not command-giving — it’s co-design.  
> The clearer the intent, the deeper the understanding that emerges.”  
> — *ChatGPT-5, 2025*
