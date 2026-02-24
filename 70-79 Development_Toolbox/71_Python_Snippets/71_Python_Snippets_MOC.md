---
id: 71
tags: [type/moc, status/growing, context/python]
---

# 71 Python Snippets MOC

**Overview**: Curated code snippets, language features, and practical references. Primary language: **Python** (main). Learning: **Rust** (for performance-critical work).

---

## 🐍 Python

### Language Features
- [[71.01 Python 3.14 New Features]]
  - **REPL**: Syntax highlighting, import autocompletion, custom themes
  - **Syntax**: T-strings (safe interpolation), parentheses-optional exceptions, `finally` warnings
  - **Type System**: Deferred annotations (PEP 649), forward references without quotes
  - **Performance**: Free-threading (no GIL), subinterpreters, JIT compiler, incremental GC
  - **Tools**: Live process debugging (PEP 768), better error messages

### Style & Best Practices
- [[71.04 Google Python Style Guide]] - Google's canonical conventions for language rules, formatting, naming, and type annotations

### Libraries & Packages
- [[71.02 Disnake Package]] - Discord API wrapper with slash commands, buttons, modals
- [[71.03 FastAPI]] - Modern web framework for building APIs

### Code Patterns
- Design patterns
- Decorators and context managers
- Async/await patterns
- Functional programming
- Data structures

### Performance Tips
- Profiling and optimization (`cProfile`, `line_profiler`)
- Memory management
- Concurrency strategies (`asyncio`, `threading`, `multiprocessing`)
- Caching techniques

### Testing & Debugging
- pytest patterns
- Mock strategies
- Debugging workflows
- Logging best practices

---

## 🦀 Rust
> Learning path: systems programming & performance-critical modules (e.g., via PyO3 for Python extensions)

- Ownership & borrowing basics
- Error handling (`Result`, `Option`)
- Iterators & closures
- Concurrency (`Arc`, `Mutex`, `async/await`)
- PyO3 — calling Rust from Python

---

## 🌐 Language-Agnostic
- [[71.05 Programmer Performance Micro-Techniques]] - Short-circuit, memoization, loop invariant hoisting, branch reduction — with compiled vs interpreted applicability
