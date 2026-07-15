---
name: writing-notes
description: How to create or edit notes in this Obsidian vault — frontmatter, tagging taxonomy, Obsidian formatting (callouts, math, mermaid), content style, note structure, Related Concepts links, and MOC linking rules. Use whenever writing, editing, or restructuring any .md note or MOC in this vault.
---

# Writing Notes in the LCKYN Knowledge Base

## YAML Frontmatter (required on every note)

```yaml
---
id: YY.NN
tags: [type/concept, status/evergreen, context/llm]
---
```

- `id` matches the filename prefix (`51.01 Johnny.Decimal System.md` → `id: 51.01`).
- Tags are an inline YAML array.

## Tagging Conventions

- **Lowercase only**, **kebab-case** for multi-word tags.
- Three nested namespaces, pick one from each:
  - `type/` → `concept`, `code`, `template`, `benchmark`, `tool`, `moc`
  - `status/` → `seed`, `growing`, `evergreen`
  - `context/` → `llm`, `mle`, `dl`, `finops`, `data-engineering`, `km`, `dev-tools`, `devops`, `python`, `mlops`, `safety`, `ai`
- The canonical, up-to-date tag list lives in `50-59 Knowledge_Management/52_Tagging_Taxonomy/52.01 Taxonomy & Tagging Strategy.md` — check it before inventing a new tag.

## Obsidian Formatting

- **Internal links**: wiki-links only — `[[Filename]]` or `[[Filename|Display Text]]`. Never standard markdown links between notes.
- **Callouts**:
  - `> [!INFO]` — definitions, background context
  - `> [!TIP]` — best practices, recommendations
  - `> [!WARNING]` — pitfalls, common mistakes
  - `> [!EXAMPLE]` — concrete scenarios
- **Math**: `$inline$` and `$$block$$` LaTeX.
- **Diagrams**: Mermaid for all diagrams (flowcharts, sequence, architecture).
- **Dataview**: never modify ` ```dataview ` blocks.

## Content Style

### Code examples
- Minimize code blocks — this is a knowledge base, not a code repository.
- Concise snippets only (3-10 lines); prefer pseudocode or bullets for logic.
- Include code only to demonstrate a specific concept or syntax pattern; no boilerplate, imports, or full implementations — link to docs instead.

### Length & tone
- Focused and scannable: bullets over paragraphs, tables for comparisons.
- Max ~200-400 lines per note; split large topics into linked notes.
- Concept-first (the "what" and "why" before the "how"); practical use cases over theoretical depth.
- **Bold** key terms on first mention.

### Standard structure for concept notes (adapt as needed)
1. **Overview** — 2-3 sentence definition
2. **Key Concepts** — core ideas as bullets
3. **Comparison Table** (if applicable)
4. **Practical Use Cases** — when/why to use
5. **Related Concepts** — wiki-links (see below)

### Don'ts
- ❌ Long paragraphs (use bullets)
- ❌ Full code implementations (link to docs)
- ❌ Orphan notes without wiki-links
- ❌ Duplicate content across notes
- ❌ Headers without content beneath them

## Related Concepts Section

End every note with:

```markdown
## Related Concepts
- [[Category_MOC]] - parent index
- [[Related Note 1]] - why it's related (e.g., "contrast", "example", "prerequisite")
- [[Related Note 2]] - brief context for the connection
```

- Parent `[[XX_Name_MOC]]` is always the **first** link.
- Annotate each link with a short phrase (<10 words) explaining the relationship: "contrast with X", "example of Y", "use when Z fails", "prerequisite for understanding".

## MOC Rules

- MOCs link **downward only**: `X0` (category MOC) → `XX` (subcategory MOCs); `XX` → its `XX.YY` notes.
- MOCs have **no** "Related Concepts" section and never link sideways to other MOCs; cross-category navigation happens through individual notes.
- Individual notes (`XX.YY`) may link to any note across categories.
- All MOC links use plain wiki-links (never `obsidian://` URIs):

```markdown
- [[22_MLOps_MOC]]
```

- When adding a new note, also add it to its parent `XX` MOC.
