# 🧠 LCKYN Knowledge Base

A personal knowledge vault for a **Data / ML / LLM Engineer**, organized using the [Johnny.Decimal](https://johnnydecimal.com/) system. Built for [Obsidian](https://obsidian.md/).

> [!IMPORTANT]
> This repository is an **Obsidian vault**. While the Markdown files are readable on GitHub, the full experience — wiki-links, graph view, dataview queries, and callouts — requires opening in Obsidian.

## 📂 Structure

| Area | Category | Topics |
|------|----------|--------|
| **10-19** | Intelligence & Modeling | LLM Dev, Machine Learning, Deep Learning / CV |
| **20-29** | Engineering & MLOps | Infrastructure, MLOps/LLMOps, Databases, Monitoring |
| **30-39** | Strategy & Architecture | System Design, Cost Management |
| **40-49** | Data Management | Data Engineering, Data Quality, Feature Engineering |
| **50-59** | Knowledge Management | System Guides, Tagging & Taxonomy |
| **60-69** | Game Development | Side projects (Godot) |
| **70-79** | Development Toolbox | Python Snippets, Algorithms, Shell, Git, Dev Tools |
| **90-99** | Archive & Personal | Learning Platforms, Books, Career Tools |

Each area follows the `XX-XX Category/YY_Subcategory/YY.NN Title.md` naming convention.

## 🔮 Opening in Obsidian

1. Clone the repository:
   ```bash
   git clone https://github.com/LCKYN/LCKYN-KnowledgeBase.git
   ```
2. Open Obsidian → **Open folder as vault** → select the cloned folder.
3. Trust the vault when prompted (to enable community plugins if configured).

The `.obsidian/` directory contains workspace settings, themes, and plugin configs.

## 🏷️ Tagging Conventions

Notes use a nested tag taxonomy:

- `#type/` → `concept`, `code`, `template`, `benchmark`, `tool`, `moc`
- `#status/` → `seed`, `growing`, `evergreen`
- `#context/` → `llm`, `mle`, `dl`, `finops`, `data-engineering`, `km`, `dev-tools`, `devops`, `python`, `mlops`

## 📝 Note Anatomy

Every note includes:
- **YAML frontmatter** with `id` and `tags`
- **Wiki-links** (`[[Note Name]]`) for internal navigation
- **Obsidian callouts** for tips, warnings, and info blocks
- **Related Concepts** section at the bottom with annotated links

## 📄 License

[MIT](LICENSE)
