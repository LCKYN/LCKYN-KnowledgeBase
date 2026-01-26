# Copilot Instructions for LCKYN Knowledge Base

This is an **Obsidian vault** organized using the **Johnny.Decimal system** for a Senior Data/ML/LLM Engineer's personal knowledge management.

## Architecture Overview

### Johnny.Decimal Structure
Folders follow the `XX-XX Category/YY_Subcategory/` pattern with two-level hierarchy:
- **10-19**: Intelligence & Modeling (LLM, ML, Deep Learning, XAI)
- **20-29**: Engineering & MLOps (Infrastructure, MLOps/LLMOps, Databases)
- **30-39**: Strategy & Architecture (System Design, Cost, Project Management)
- **40-49**: Data Management (Engineering, Quality, Feature Engineering)
- **50-59**: Knowledge Management (System Guides, Tagging, Tools)
- **60-69**: Game Development (Side projects)
- **70-79**: Development Toolbox (Python, SQL, Shell snippets)
- **90-99**: Archive & Personal (Post-mortems, Logs, Reading List)

Files use the `YY.NN Title.md` naming convention (e.g., `51.01 Johnny.Decimal System.md`).

## Obsidian Formatting Requirements

### YAML Frontmatter (Required)
Every note MUST include frontmatter with these fields:
```yaml
---
id: YY.NN
tags: [type/concept, status/evergreen, context/llm]
---
```

### Tagging Conventions
- **Lowercase only**, use **kebab-case** for multi-word tags
- Nested tag structure:
  - `#type/` → `concept`, `code`, `template`, `benchmark`, `tool`, `moc`
  - `#status/` → `seed`, `growing`, `evergreen`
  - `#context/` → `llm`, `mle`, `dl`, `finops`, `data-engineering`, `km`, `dev-tools`, `devops`, `python`, `mlops`, `safety`, `ai`

### Internal Links
Use Obsidian wiki-links: `[[Filename]]` or `[[Filename|Display Text]]`
Never convert to standard markdown links `[Text](URL)`.

### Callouts
Use Obsidian callout syntax:
```markdown
> [!INFO] Title
> Content here
```

### Math
Use `$inline$` and `$$block$$` LaTeX syntax.

### Diagrams
Use Mermaid for all diagrams (flowcharts, sequence diagrams, architecture diagrams, etc.):
```mermaid
graph TD
    A[Start] --> B[Process]
    B --> C[End]
```

### Dataview
Never modify ` ```dataview ` code blocks.

## Content Style Guidelines

### Code Examples
- **Minimize code blocks** - This is a knowledge base, not a code repository
- Prefer **concise snippets** (3-10 lines max) over full implementations
- Use **pseudocode or bullet points** to explain logic when possible
- Only include code when it demonstrates a **specific concept** or **syntax pattern**
- Avoid boilerplate, imports, and repetitive patterns
- Reference external documentation for full implementations

### Note Length
- Keep notes **focused and scannable**
- Use **tables** for comparisons instead of verbose explanations
- Prefer **bullet points** over paragraphs
- Target **200-400 lines** per note maximum
- Split large topics into multiple linked notes

### Writing Style
- **Concise over comprehensive** - link to docs for details
- **Concept-first** - explain the "what" and "why" before "how"
- Use **bold** for key terms on first mention
- Include **practical use cases** over theoretical depth

### Note Structure Template
Standard sections for concept notes (adapt as needed):
1. **Overview** - 2-3 sentence definition
2. **Key Concepts** - Core ideas with bullet points
3. **Comparison Table** (if applicable)
4. **Practical Use Cases** - When/why to use
5. **Related Concepts** - Wiki-links to connected notes

### Callout Usage
- `> [!INFO]` - Definitions, background context
- `> [!TIP]` - Best practices, recommendations
- `> [!WARNING]` - Pitfalls, common mistakes
- `> [!EXAMPLE]` - Concrete scenarios

### Related Links Section
End notes with a "Related Concepts" section using wiki-links with brief annotations explaining the relationship:
```markdown
## Related Concepts
- [[Related Note 1]] - Why it's related (e.g., "contrast", "example", "prerequisite")
- [[Related Note 2]] - Brief context for the connection
```

**Link annotation guidelines:**
- Add a brief phrase after the dash explaining the relationship
- Use patterns like: "contrast with X", "example of Y", "use when Z fails", "prerequisite for understanding"
- Keep annotations under 10 words
- Always include `[[Category_MOC]]` as the first link

### Avoid (Don'ts)
- ❌ Long paragraphs (use bullets instead)
- ❌ Full code implementations (link to docs)
- ❌ Orphan notes without wiki-links
- ❌ Duplicate content across notes
- ❌ Headers without content beneath them

## File Conventions

### MOC Files (Maps of Content)
Each category has a `_MOC.md` file (e.g., `50_Knowledge_Management_MOC.md`) serving as an index.

**MOC linking rules:**
- MOCs only link **downward** to their subcategories (e.g., `20_MOC` → `21`, `22`, `23`, `24`)
- MOCs do **NOT** have a "Related Concepts" section linking to other MOCs
- Cross-category navigation happens through subcategory notes, not MOCs
- Individual notes link to their parent MOC as the first Related Concept

**Hierarchical linking rules:**
- `X0` (category MOC) only links to `XX` (subcategory MOCs)
- `XX` (subcategory MOC) only links to `XX.YY` (individual notes)
- `XX.YY` (individual notes) can link to any `XX.YY` across categories

### Attachments
Store images/PDFs in `99_Attachments/` folder.

### Archive
Legacy/deprecated content lives in `.old/` (gitignored patterns may apply).

## Key Reference Files
- System guide: [51.01 Johnny.Decimal System.md](50-59%20Knowledge_Management/51_System_Guides/51.01%20Johnny.Decimal%20System.md)
- Tagging strategy: [52.01 Taxonomy & Tagging Strategy.md](50-59%20Knowledge_Management/52_Tagging_Taxonomy/52.01%20Taxonomy%20%26%20Tagging%20Strategy.md)

