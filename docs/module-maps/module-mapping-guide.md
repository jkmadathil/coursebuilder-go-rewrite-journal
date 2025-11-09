# 🧭 Module Mapping Guide  
*Companion reference for `module-mapping.csv`*

_Last updated: 2025-11-09_  
[_Linked ethics reference:_](../admin/personal-ethics.md)

---

## 🎯 Purpose

This guide explains the intent and structure of the `module-mapping.csv` file used to document the **CourseBuilder → Go learning and migration process**.  

The module map is not just an inventory of files — it is a **learning scaffold**.  
It connects **code artifacts → conceptual understanding → migration design choices.**

---

## 🗂️ File Location
```
docs/
└── module-maps/
├── module-mapping.csv
└── module-mapping-guide.md
```

---

## 🧩 Column Reference and Usage

| Column | Description | Example / Notes |
|--------|--------------|-----------------|
| **file_path** | The exact relative path of the file in the source repository. | `coursebuilder/modules/course.py` |
| **module** | The functional or architectural grouping within CourseBuilder. | `content`, `auth`, `analytics`, `appengine-config` |
| **component** | A finer sub-component or feature. Helps break large modules into logical parts. | `lesson-editor`, `email-sender` |
| **language** | The primary language or format of the file. Inferred automatically but review manually if needed. | `python`, `yaml`, `html`, `css`, `js` |
| **brief_description** | A one-line, plain-English explanation of what the file does. | “Defines datastore schema for courses and lessons.” |
| **dependencies** | Core dependencies or frameworks imported or referenced by the file. | `appengine`, `ndb`, `jinja2` |
| **notes** | Personal learning notes, quirks, or conceptual insights. | “Relies on App Engine APIs — evaluate migration to Firestore.” |
| **migration_status** | Current progress status. Choose from: `not-started`, `in-progress`, `reworked`, `validated`, `archived`. | `in-progress` |
| **go_target_module** | Target Go package or equivalent design area. | `pkg/course` |
| **complexity_rating** | Subjective estimate (1–5) of migration or conceptual complexity. | `4` |
| **learning_tags** | Keywords to categorize conceptual learnings. | `datastore`, `template`, `auth`, `cloud-deployment` |
| **reflection_link** | Link to relevant journal or experiment entries that capture your exploration. | `../journal/weekly/2025-W03.md#mapping` |

---

## 🧠 How to Use the Module Map

1. **Start Broad, Refine Weekly**  
   - Populate “brief_description” and “notes” columns while reading or debugging.  
   - Add “reflection_link” after writing your weekly journal or experiment report.  

2. **Think in Layers**  
   - **Technical layer:** dependencies, language, structure.  
   - **Conceptual layer:** learning tags, insights, decisions.  
   - **Pedagogical layer:** what this file *taught you* about design patterns or architecture.

3. **Tag and Cluster Learnings**  
   - Use `learning_tags` consistently — they’ll help you cluster insights later (e.g., filtering all `datastore`-related files).  

4. **Keep It Alive**  
   - This CSV is meant to evolve as your understanding deepens.  
   - Don’t wait to fill it “perfectly”; record raw impressions early and refine them over time.  

---

## 🧩 Suggested Workflow (Weekly)

| Step | Action | Tool / Location |
|------|---------|----------------|
| 1 | Pick 1–2 modules to study (e.g., `auth`, `content`) | `coursebuilder/modules/` |
| 2 | Open the corresponding CSV rows | `docs/module-maps/module-mapping.csv` |
| 3 | Explore files hands-on | local clone or IDE |
| 4 | Update `brief_description`, `learning_tags`, and `notes` | CSV editor / spreadsheet |
| 5 | Write a short summary in your weekly journal | `journal/weekly/YYYY-Wxx.md` |
| 6 | Link journal entry in the `reflection_link` column | CSV hyperlink |

---

## 🧭 Reflection Prompts (for self and readers)

Use these questions when updating rows or writing related journal entries:

1. What architectural or design pattern does this file reveal?  
2. What trade-offs do you notice between CourseBuilder’s design and modern Go idioms?  
3. Did AI assistance clarify or confuse your understanding here?  
4. What migration path would you propose — 1:1 port, redesign, or sunset?  
5. What did this file teach you about **how to learn from legacy systems**?

---

## ⚖️ Ethics and Transparency Reminder

Before finalizing updates:  
- Ensure that **no confidential code or data** from SWAYAM/SEEK or other internal systems is included.  
- Attribute all references following **IEEE citation format** (see [Personal Ethics Statement](../admin/personal-ethics.md)).  
- Treat AI-generated inferences as provisional — validate with your own understanding before accepting.  

---

> *“A module map is not a static index — it’s a mirror of your evolving understanding.”*  
> — _[ChatGPT-5], 09-Nov-2025_

