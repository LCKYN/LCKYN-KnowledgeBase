# LCKYN Knowledge Base — Agent Instructions

This is an **Obsidian vault** organized with the **Johnny.Decimal system** for a Senior Data/ML/LLM Engineer's personal knowledge management. It is a knowledge base, not a code repository.

> **When creating or editing notes**, follow the note-authoring skill at `.claude/skills/writing-notes/SKILL.md` — it covers frontmatter, tagging, formatting, content style, and linking rules.

## Vault Structure (Johnny.Decimal)

Folders follow `XX-XX Category/YY_Subcategory/` with a two-level hierarchy:

| Range | Category |
|-------|----------|
| 10-19 | Intelligence & Modeling (LLM Dev, Machine Learning, Deep Learning / CV) |
| 20-29 | Engineering & MLOps (Infrastructure, MLOps/LLMOps, Database & Retrieval, Monitoring) |
| 30-39 | Strategy & Architecture (System Design, Cost Management, Project Management) |
| 40-49 | Data Management (Data Engineering, Data Quality, Feature Engineering) |
| 50-59 | Knowledge Management (System Guides, Tagging Taxonomy) |
| 60-69 | Game Development (Godot side projects) |
| 70-79 | Development Toolbox (Python Snippets, Algorithms, Shell, Git Workflows, Dev Tools) |
| 90-99 | Archive & Personal (Learning Platforms, Books, Career Tools) |

- Notes use the `YY.NN Title.md` naming convention (e.g., `51.01 Johnny.Decimal System.md`). IDs must be unique — check the folder for the next free number before creating a note.
- Each category and subcategory has a `_MOC.md` index file (e.g., `50_Knowledge_Management_MOC.md`) with `id` set to its bare number (e.g., `id: 50`).
- Only add a subcategory to its `X0` MOC once the folder and its `_MOC.md` exist — no links to planned-but-missing MOCs.
- Images/PDFs go in `99_Attachments/` (Obsidian's configured attachment folder; created on first use).

## Hard Rules

- **Never modify** ` ```dataview ` code blocks.
- **Always use Obsidian wiki-links** (`[[Filename]]` or `[[Filename|Display Text]]`) between notes — never convert them to standard markdown links `[Text](URL)`.
- Every note **must** have YAML frontmatter with `id` and `tags` (see the skill).
- Respect the MOC hierarchy: `X0` MOCs link only to `XX` MOCs; `XX` MOCs link only to `XX.YY` notes; individual notes may link across categories.

## Key Reference Files

- System guide: `50-59 Knowledge_Management/51_System_Guides/51.01 Johnny.Decimal System.md`
- Tagging strategy (canonical tag list): `50-59 Knowledge_Management/52_Tagging_Taxonomy/52.01 Taxonomy & Tagging Strategy.md`
