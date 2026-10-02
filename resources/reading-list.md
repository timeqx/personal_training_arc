# Reading List

Prefer primary documentation and foundational books/papers. Check that online docs match the current stable version before relying on details.

## Rust — primary resources

1. **The Rust Programming Language**
   https://doc.rust-lang.org/book/

2. **Rust By Example**
   https://doc.rust-lang.org/rust-by-example/

3. **The Rust Reference**
   https://doc.rust-lang.org/reference/

4. **The Rustonomicon**
   https://doc.rust-lang.org/nomicon/

5. **The Cargo Book**
   https://doc.rust-lang.org/cargo/

6. **Rust API Guidelines**
   https://rust-lang.github.io/api-guidelines/

7. **Tokio Tutorial**
   https://tokio.rs/tokio/tutorial

Read source code after fundamentals:
- Tokio
- Axum
- Serde
- tracing
- reqwest/hyper ecosystem

Do not attempt to read entire large repositories sequentially. Follow one feature or control flow.

---

## Computer science / systems

Books worth sustained study:
- *Computer Systems: A Programmer's Perspective*
- *Operating Systems: Three Easy Pieces* — freely available from the authors
- *Designing Data-Intensive Applications*
- *Computer Networking: A Top-Down Approach*
- *Database Internals* after database fundamentals

Practice:
- Linux man pages
- PostgreSQL official docs
- Docker docs
- OpenTelemetry docs

---

## Math / ML

Suggested:
- *Mathematics for Machine Learning*
- *An Introduction to Statistical Learning*
- Stanford/other reputable linear algebra materials
- probability/statistics text at undergraduate level

Do exercises. Watching lectures without solving problems is insufficient.

---

## Deep learning

1. **PyTorch Tutorials**
   https://pytorch.org/tutorials/

2. *Dive into Deep Learning*
   https://d2l.ai/

3. *Deep Learning* — Goodfellow, Bengio, Courville for reference/depth

4. Read influential papers alongside implementation:
- Attention Is All You Need
- BERT
- GPT-family papers/technical reports where available
- LoRA
- retrieval/RAG papers
- relevant evaluation papers

Use current papers for modern practice; use foundational papers to understand why techniques exist.

---

## Transformers / LLMs

1. **Hugging Face LLM Course**
   https://huggingface.co/learn/llm-course/

2. **Hugging Face Agents Course**
   https://huggingface.co/learn/agents-course/

3. Provider documentation for:
- structured outputs,
- function/tool calling,
- streaming,
- rate limits,
- safety.

Avoid learning core concepts solely through rapidly outdated framework tutorials.

---

## Agent orchestration

Study the primitives first:
- state,
- graph/workflow,
- tools,
- checkpoints,
- retries,
- deterministic boundaries,
- evaluation.

Then learn:
- LangGraph current documentation
  https://docs.langchain.com/oss/python/langgraph/overview

Also study one provider-native agent SDK to understand a different design.

---

## MCP

Use the **current official Model Context Protocol documentation/specification**:
https://modelcontextprotocol.io/

Study:
- architecture,
- lifecycle,
- transports,
- tools,
- resources,
- prompts,
- authorization/security guidance.

Because MCP evolves, prefer current specification pages over old tutorials.

---

## RAG / search

Study:
- information retrieval metrics,
- BM25,
- embeddings,
- ANN indexes,
- rerankers,
- hybrid retrieval.

Primary docs:
- PostgreSQL + pgvector
- Qdrant docs
- search-engine docs if using BM25/hybrid search

Papers/topics:
- original RAG work,
- dense passage retrieval,
- reranking/cross-encoder methods,
- modern retrieval evaluation.

---

## MLOps

Study:
- experiment tracking,
- reproducibility,
- model serving,
- monitoring,
- data/model versioning,
- canary releases,
- rollback.

Use current official docs for tools you actually deploy. Do not learn five MLOps products just for keywords.

---

# Reading method

For technical chapters/papers:

1. First pass: understand the problem.
2. Second pass: annotate mechanisms.
3. Close the source.
4. Explain from memory.
5. Implement something.
6. Write questions you still cannot answer.
7. Re-read only those areas.
8. Add one exam question from the material.

## Paper template

- Problem:
- Prior baseline:
- Dataset:
- Metric:
- Method:
- Main result:
- Assumptions:
- Weaknesses:
- Reproduction idea:
- What would falsify the claim?:
