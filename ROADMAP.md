# 24-Week Intensive Roadmap

This is a **job-readiness accelerator**, not a claim that six months creates an expert. The advanced loop after Week 24 is where expertise compounds.

Default workload: 12–16 focused hours per week. If you have less time, preserve the order and stretch the calendar.

## Week 0 — Baseline

### Test
- Take Rust Baseline Exam A.
- Take AI/ML Baseline Exam A.
- Take Systems Baseline Exam A.
- Record scores without studying first.

### Setup
- Rust stable toolchain, rustfmt, Clippy, rust-analyzer.
- Python 3.12+ environment.
- Docker.
- PostgreSQL.
- GitHub Actions.
- A notes folder for learning logs.

### Deliverable
Create a progress entry with:
- current strengths,
- current weak areas,
- one-month targets,
- evidence links.

---

## Weeks 1–4 — Foundations that must become automatic

### Rust
Week 1:
- ownership, moves, Copy, Clone
- borrowing and references
- slices
- Option and Result

Week 2:
- structs, enums, pattern matching
- modules, crates, visibility
- generics and traits
- iterators and closures

Week 3:
- lifetimes
- smart pointers
- interior mutability
- error design

Week 4:
- collections
- testing
- Cargo workspaces
- idiomatic API design

### AI/ML
Week 1:
- vectors, matrices, dot products
- probability basics
- NumPy

Week 2:
- linear regression
- logistic regression
- train/validation/test splits
- metrics

Week 3:
- trees and ensembles
- bias/variance
- feature engineering
- data leakage

Week 4:
- gradient descent
- neural-network fundamentals
- PyTorch tensors and autograd

### Build
- Rust CLI application with tests.
- Implement linear regression twice: once from basic NumPy operations, once using scikit-learn.
- Write a one-page explanation of ownership without using the phrase "the compiler handles it" as the explanation.

### Gate
You may move forward when:
- you can predict common borrow-checker failures,
- you can explain precision/recall/F1,
- your projects run through CI.

---

## Weeks 5–8 — Async Rust + Deep Learning

### Rust
- threads and message passing
- Send and Sync
- Arc, Mutex, RwLock
- async/await
- Future and polling model
- Tokio tasks, channels, select, cancellation
- HTTP clients
- Axum
- Serde
- tracing

### AI
- backpropagation
- optimizers
- regularization
- embeddings
- CNN/RNN concepts
- attention
- transformer architecture
- tokenization
- Hugging Face Transformers

### Build
- concurrent Rust web crawler with bounded concurrency and retries.
- Axum API with PostgreSQL.
- PyTorch text classifier.
- implement scaled dot-product attention from scratch in PyTorch.
- write a short report comparing synchronous threads vs Tokio for one I/O-bound workload.

### Exam
Take Rust Core Exam B and AI Fundamentals Exam B.

---

## Weeks 9–12 — Systems + LLM Engineering

### Rust
- sockets and networking
- async streams
- backpressure
- graceful shutdown
- structured error taxonomy
- property-based testing
- benchmarking with Criterion

### AI
- inference vs training
- prompting and structured output
- tool/function calling
- embeddings
- RAG ingestion
- chunking
- metadata filtering
- vector search
- hybrid retrieval
- reranking
- grounding and citations

### Systems
- TCP/IP, HTTP, TLS
- Linux processes and signals
- PostgreSQL indexes and query plans
- caching
- queues
- Docker

### Build
- production-style RAG service with FastAPI.
- pgvector or Qdrant retrieval.
- evaluation set of at least 50 questions.
- report Recall@K, answer groundedness, latency, and cost.
- Rust service that consumes a queue and performs concurrent jobs.

### Application checkpoint
At the end of Week 12, begin applying if your portfolio has:
- a serious Rust repository,
- an evaluated RAG project,
- good READMEs,
- tests and CI.

Do not wait for Week 24 to apply.

---

## Weeks 13–16 — Agents, MCP, and Advanced Rust

### Rust
- Pin and Unpin concepts
- deeper Future mechanics
- macro_rules
- procedural macro concepts
- trait objects vs generics
- zero-cost abstractions
- allocations and memory layout
- flamegraphs and profiling

### AI
- agent state
- tool routing
- planner/executor patterns
- human-in-the-loop
- retries and fallback
- deterministic workflows vs autonomous agents
- agent evaluation
- prompt-injection threat modeling
- MCP architecture

### MCP
Study the current MCP specification rather than old blog examples. Implement:
- a client,
- a server,
- tools,
- resources,
- prompts,
- authentication concepts,
- safe permission boundaries.

### Build
- Rust MCP server.
- Rust MCP client using the official Rust SDK where appropriate.
- tool-call evaluation suite.
- agent trace viewer.
- approval gate for destructive tools.

### Exam
Take Agentic Systems Exam C and Rust Async/Concurrency Exam C.

---

## Weeks 17–20 — Unsafe Rust, Production AI, MLOps

### Rust
- unsafe blocks and safety invariants
- raw pointers
- MaybeUninit
- repr and layout
- FFI
- atomics basics
- lock-free concepts
- performance profiling
- allocator awareness

Never write unsafe code only to appear advanced. Every unsafe block must document its safety invariant.

### AI
- fine-tuning concepts
- LoRA/QLoRA
- quantization
- model serving
- batching
- caching
- evaluation pipelines
- experiment tracking
- drift and monitoring
- model/data versioning
- red-team tests

### Build
- fine-tune a small open model on a narrow dataset.
- compare base vs tuned model using a fixed evaluation set.
- serve a model behind an API.
- add observability to your RAG/agent project.
- implement one safe abstraction around a small justified unsafe Rust component.

---

## Weeks 21–24 — Capstone: Rust × AI Agent Runtime

Build the flagship project described in tracks/04-rust-ai-specialization.md.

Required capabilities:
- provider abstraction,
- streaming,
- structured output,
- tool registry,
- retries/timeouts/cancellation,
- MCP client and server support,
- RAG,
- state/checkpointing,
- approval policies,
- tracing,
- evaluation,
- cost/latency accounting,
- Docker,
- CI,
- production-style documentation.

### Final defense
You must:
1. demo the system live,
2. explain the architecture without notes,
3. explain three failures and how you fixed them,
4. defend why Rust is used,
5. show benchmarks where performance claims are made,
6. show eval results where AI-quality claims are made,
7. answer questions from all four tracks.

---

# Long-term expert loop: Month 7 onward

Repeat this cycle every 8–12 weeks:

1. Choose one deep topic.
2. Read a primary source/book/paper.
3. implement a minimal version.
4. build a production version.
5. benchmark/evaluate it.
6. write a technical article.
7. contribute a fix or feature to an open-source project.
8. teach the topic or present it.

Suggested deep cycles:
- Rust unsafe and memory model.
- async runtimes and schedulers.
- databases/storage engines.
- compilers and interpreters.
- distributed systems.
- CUDA/GPU fundamentals.
- transformer internals.
- inference optimization.
- representation learning.
- reinforcement learning.
- agent evaluation.
- retrieval systems.
- Rust ML/AI ecosystem.
- security engineering.

Expertise is demonstrated by sustained depth, judgment, debugging ability, and contributions—not by finishing a checklist.
