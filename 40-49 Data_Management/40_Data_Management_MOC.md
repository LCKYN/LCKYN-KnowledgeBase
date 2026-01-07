---
id: 40
tags: [type/moc, status/evergreen, context/data-engineering]
---

# 40 Data Management MOC

**Overview**: Best practices, tools, and techniques for managing data throughout its lifecycle—from ingestion and storage to quality assurance and feature engineering for ML/LLM applications.

## 41 Data Engineering
- [[41_Data_Engineering_MOC]]
  - **41.01 Parquet**: Binary columnar format for analytics (compression, partitioning, predicate pushdown)
  - **41.02 CSV**: Character-based row-oriented format (human-readable, universal compatibility)
  - **41.03 JSON**: Nested text format for APIs and hierarchical data
  - **41.04 Apache Arrow**: In-memory columnar format for zero-copy IPC and fast analytics

## 42 Data Quality & Governance
- Data profiling and validation
- Data contracts and schemas
- Quality metrics and monitoring
- Lineage tracking

## 43 Feature Engineering
- Feature extraction techniques
- Transformation pipelines
- Feature stores
- Time-series features
- Text embeddings
