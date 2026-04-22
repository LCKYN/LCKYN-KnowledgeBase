---
id: 11
tags: [type/moc, status/evergreen, context/llm]
---

# 11 LLM Development MOC

## Concepts
- [[11.01 Attention Mechanism]]
- [[11.02 LLM Agents]]
- [[11.03 LLM Tool Calls]]
- [[11.04 LLM Workflows]]
- [[11.19 Era of LLM]]
- [[11.06 AG-UI Protocol]]
- [[11.07 A2UI]]
- [[11.09 Placeholder-Based Generation]]
- [[11.10 LLM Guardrails]]
- [[11.11 Agentic LLM]]
- [[11.12 RAG]]
- [[11.13 Chain of Thought]]
- [[11.14 Prompt Engineering]]
- [[11.15 LLM Evaluation Metrics]]
- [[11.16 Context Window Management]]
- [[11.28 Context Rot]]
- [[11.18 LLM Throughput & Memory Bound]]
- [[11.20 LLM Memory Architecture]]
- [[11.21 Prompt Caching]]
- [[11.22 Computing Units for AI]]
- [[11.23 Workspace Indexing]]
- [[11.24 Clean Code for LLM Agents]]
- [[11.25 Writing Code That AI Assistants Understand]]
- [[11.29 One Function Per File for LLM Indexing]]

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
