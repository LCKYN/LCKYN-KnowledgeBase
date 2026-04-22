---
id: 11
tags: [type/moc, status/evergreen, context/llm]
---

# 11 LLM Development MOC

## Concepts
- [[11.01 Attention Mechanism]] - Query-Key-Value scaled dot-product; the core of transformers
- [[11.02 LLM Agents]] - LLMs that plan, use tools, and act in loops
- [[11.03 LLM Tool Calls]] - Structured function-calling interface between models and external APIs
- [[11.04 LLM Workflows]] - Predefined orchestration patterns vs autonomous agents
- [[11.19 Era of LLM]] - Historical phases of LLM development and capability scaling
- [[11.06 AG-UI Protocol]] - Standard protocol for streaming agent state to frontends
- [[11.07 A2UI]] - Agent-to-UI communication patterns
- [[11.09 Placeholder-Based Generation]] - Template-driven structured output via slots
- [[11.10 LLM Guardrails]] - Input/output filters for safety, policy, and format enforcement
- [[11.11 Agentic LLM]] - Models trained or scaffolded for multi-step autonomous behavior
- [[11.12 RAG]] - Retrieval-Augmented Generation; ground responses in external knowledge
- [[11.13 Chain of Thought]] - Step-by-step reasoning prompting and training
- [[11.14 Prompt Engineering]] - Techniques for shaping LLM behavior via input design
- [[11.15 LLM Evaluation Metrics]] - Benchmarks, judges, and task-specific quality measures
- [[11.16 Context Window Management]] - Strategies for working within and across token limits
- [[11.28 Context Rot]] - Degradation of model performance as context grows
- [[11.18 LLM Throughput & Memory Bound]] - Why decode is memory-bound and prefill is compute-bound
- [[11.20 LLM Memory Architecture]] - Short-term, long-term, and episodic memory for agents
- [[11.21 Prompt Caching]] - Reuse KV cache across requests with shared prefixes
- [[11.22 Computing Units for AI]] - GPUs, TPUs, NPUs, LPUs and their trade-offs
- [[11.23 Workspace Indexing]] - Indexing codebases for AI assistant retrieval
- [[11.24 Clean Code for LLM Agents]] - Code conventions that improve LLM comprehension
- [[11.25 Writing Code That AI Assistants Understand]] - Authoring patterns for AI-friendly codebases
- [[11.29 One Function Per File for LLM Indexing]] - Granular file structure for precise retrieval

## Tools & Frameworks
- [[11.05 CopilotKit]]
- [[11.08 MCP Server]]
- [[11.26 XGrammar]] - Constrained generation via CFG token masking; near-zero overhead structured output

## Inference Engines
- [[11.27 LLM Generation Engines]] - vLLM, SGLang, TensorRT-LLM, TGI, llama.cpp, Ollama

## Inference Providers
- [[11.20 Groq]]
- [[11.21 Cerebras]]

## Architectures
- [[11.17 Mixture of Experts]]

## Training
- [[11.30 Scaling Laws]] - Chinchilla, compute-optimal training
- [[11.31 Supervised Fine-Tuning]] - Instruction tuning on labeled prompt-response pairs
- [[11.32 PEFT]] - LoRA, QLoRA, Adapters, Prefix Tuning
- [[11.33 Continued Pre-training]] - Domain adaptation via additional pre-training on raw corpora
- [[11.34 Full Fine-Tuning vs PEFT]] - Trade-offs between updating all weights vs adapter-based methods

## Optimization & Efficiency
- [[11.35 Mixed Precision Training]] - FP16, BF16, FP8 for faster, lower-memory training
- [[11.36 Gradient Checkpointing]] - Trade compute for activation memory
- [[11.37 Distributed Training]] - DDP, FSDP, DeepSpeed ZeRO, tensor/pipeline parallelism
- [[11.38 Flash Attention]] - IO-aware exact attention with linear memory

## Quantization & Compression
- [[11.39 Quantization]] - GPTQ, AWQ, GGUF, INT8/INT4 post-training quantization
- [[11.40 Pruning & Sparsity]] - Structured / unstructured weight removal
- [[11.41 Speculative Decoding]] - Draft-then-verify inference acceleration
- [[11.42 Chunked Prefill]] - Split long prefills into chunks; co-schedule with decode for higher throughput
