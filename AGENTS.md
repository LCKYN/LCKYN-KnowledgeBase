# LCKYN Knowledge Base — Agent Instructions

This is an **Obsidian vault** organized with the **Johnny.Decimal system** for a Senior Data/ML/LLM Engineer's personal knowledge management. It is a knowledge base, not a code repository.

> **When creating or editing notes**, follow the note-authoring skill at `.claude/skills/writing-notes/SKILL.md` — it covers frontmatter, tagging, formatting, content style, and linking rules.

## Vault Structure (Johnny.Decimal)

Folders follow `XX-XX Category/YY_Subcategory/` with a two-level hierarchy:

| Range | Category |
|-------|----------|
| 10-19 | Intelligence & Modeling (LLM, ML, Deep Learning, XAI) |
| 20-29 | Engineering & MLOps (Infrastructure, MLOps/LLMOps, Databases) |
| 30-39 | Strategy & Architecture (System Design, Cost, Project Management) |
| 40-49 | Data Management (Engineering, Quality, Feature Engineering) |
| 50-59 | Knowledge Management (System Guides, Tagging, Tools) |
| 60-69 | Game Development (Side projects) |
| 70-79 | Development Toolbox (Python, SQL, Shell snippets) |
| 90-99 | Archive & Personal (Post-mortems, Logs, Reading List) |

- Notes use the `YY.NN Title.md` naming convention (e.g., `51.01 Johnny.Decimal System.md`).
- Each category and subcategory has a `_MOC.md` index file (e.g., `50_Knowledge_Management_MOC.md`).
- Images/PDFs go in `99_Attachments/`. Legacy content lives in `.old/`.

## Hard Rules

- **Never modify** ` ```dataview ` code blocks.
- **Always use Obsidian wiki-links** (`[[Filename]]` or `[[Filename|Display Text]]`) between notes — never convert them to standard markdown links `[Text](URL)`.
- Every note **must** have YAML frontmatter with `id` and `tags` (see the skill).
- Respect the MOC hierarchy: `X0` MOCs link only to `XX` MOCs; `XX` MOCs link only to `XX.YY` notes; individual notes may link across categories.

## Key Reference Files

- System guide: `50-59 Knowledge_Management/51_System_Guides/51.01 Johnny.Decimal System.md`
- Tagging strategy (canonical tag list): `50-59 Knowledge_Management/52_Tagging_Taxonomy/52.01 Taxonomy & Tagging Strategy.md`
