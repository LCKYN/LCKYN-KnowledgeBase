**Core Concept:**  
While Johnny.Decimal provides a **fixed physical location** for files, Tags provide **dynamic context**. This dual-system allows for multi-dimensional discovery, enabling you to find related concepts across different numerical areas (e.g., linking LLM costs to Business strategy).

**Tagging Framework (Nested Tags):**  
To keep the tag pane organized, use **Nested Tags** (Parent/Child structure):

1. **`#type/` (The "What"):** Defines the nature of the content.
    - `#type/concept`: Theoretical frameworks and definitions.
    - `#type/code`: Implementation scripts and battle-tested snippets.
    - `#type/template`: Boilerplates for projects or configurations (Docker, K8s).
    - `#type/benchmark`: Performance metrics and model comparisons.
2. **`#status/` (The "State"):** Manages the lifecycle of the note.
    - `#status/seed`: Raw thoughts or quick captures.
    - `#status/growing`: Actively researched and structured content.
    - `#status/evergreen`: High-quality, verified knowledge ready for production use.
3. **`#context/` (The "Where"):** Connects technology to its application domain.
    - `#context/llm`: Specific to Large Language Models.
    - `#context/mle`: Specific to Machine Learning Engineering.
    - `#context/finops`: Specific to cost and resource management.

**Implementation Rules:**

- **Case Sensitivity:** Always use **lowercase** for tags to avoid duplication (e.g., `#ML` vs `#ml`).
- **Kebab-case:** Use hyphens for multi-word tags (e.g., `#topic/system-design`).
- **Frontmatter:** Place tags in the YAML frontmatter for better metadata management and plugin compatibility.

**Example YAML Metadata:**

markdown

```
---
id: 32.01
title: LLM Inference Cost Optimization
tags: [type/concept, status/evergreen, context/llm, context/finops]
created: 2025-12-30
---
```

Use code with caution.

**Benefits for Senior Workflow:**

- **Graph Filtering:** Color-code your Obsidian Graph based on tags to see how "Cost" (#context/finops) impacts different "Engineering" areas.
- **Dataview Integration:** Use the Obsidian Dataview plugin to automatically generate tables of all `#type/code` snippets for quick access.