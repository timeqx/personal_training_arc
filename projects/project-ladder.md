# Project Strategy — Minimum Projects, Maximum Evidence

The optimized portfolio uses:

1. **One flagship Rust × AI system**
2. **One pure Rust/backend systems project**
3. **One pure AI/ML project**
4. Small exercises kept inside an exercises area rather than turned into shallow portfolio repos.

This gives independent Rust proof, independent AI proof, and the differentiated Rust × AI niche.

# Project A — Flagship Rust AI Agent Runtime

This is the primary portfolio project.

It should absorb:
- provider abstraction,
- Tokio async,
- Axum API,
- structured output,
- tool calling,
- MCP,
- RAG,
- pgvector/Qdrant,
- orchestration,
- evaluation,
- observability,
- security,
- Docker,
- cloud,
- frontend trace/dashboard,
- CI/CD.

Do **not** split MCP, RAG, agent eval, and observability into separate shallow repositories unless they become genuinely reusable standalone libraries.

## Required evidence

- [ ] two LLM providers or one remote + one local provider
- [ ] streaming
- [ ] typed structured outputs
- [ ] tool registry
- [ ] retries/timeouts
- [ ] bounded execution
- [ ] cancellation
- [ ] MCP client
- [ ] MCP server
- [ ] RAG
- [ ] citations
- [ ] retrieval evaluation
- [ ] agent/tool evaluation
- [ ] human approval
- [ ] prompt-injection tests
- [ ] tracing
- [ ] token/cost tracking
- [ ] p50/p95 latency
- [ ] Docker
- [ ] CI
- [ ] live deployment
- [ ] architecture diagram
- [ ] demo video
- [ ] benchmark/eval report

# Project B — Pure Rust Systems Project

Purpose: prove your Rust ability is not limited to AI APIs.

Choose one:

## Option 1 — Background job system
- Tokio worker pool
- bounded queue
- retry/dead-letter behavior
- idempotency
- graceful shutdown
- metrics
- PostgreSQL

## Option 2 — Mini key-value store
- binary protocol
- persistence/WAL concepts
- concurrency
- indexes
- crash-recovery reasoning
- benchmarks

## Option 3 — High-performance crawler/indexer
- bounded concurrency
- deduplication
- backpressure
- persistent state
- retry
- profiling

Required proof:
- tests
- benchmark
- error model
- tracing
- load test
- architecture write-up
- at least one postmortem or failure analysis

# Project C — Pure AI/ML Project

Purpose: prove you understand AI beyond LLM wrappers.

Build one compact end-to-end project containing:
- data exploration
- train/validation/test split
- baseline
- classical ML model
- correct metrics
- error analysis
- PyTorch extension or comparison
- reproducibility
- inference API

Good domains:
- text classification
- anomaly/fraud-style synthetic problem
- forecasting with careful leakage handling
- tabular classification

Then add one transformer learning exercise:
- implement scaled dot-product attention
- optionally train a tiny language model

This repository can be smaller than the flagship, but the methodology must be clean.

# Exercises — not portfolio clutter

Keep these as folders/notebooks/crates rather than separate repositories.

Rust:
- borrow-checker drills
- lifetimes
- custom iterator
- parser
- thread pool
- manual Future exercise
- unsafe/Miri exercises

AI:
- linear/logistic regression from scratch
- metrics
- PyTorch training loop
- attention
- embedding experiments
- retrieval comparison

Systems:
- TCP server
- SQL EXPLAIN drills
- retry/idempotency exercises
- Docker drills

# Open-source work

After the flagship stabilizes, target **3–5 meaningful merged PRs** over time.

Good areas:
- Rust AI libraries
- MCP SDK/tooling
- LLM clients
- Qdrant/pgvector ecosystem
- Tokio/Axum ecosystem documentation/tests
- agent/evaluation libraries

Start with docs/tests/bugs. Progress to implementation changes.

# Portfolio quality gate

Every portfolio project must have:

- [ ] clear problem statement
- [ ] architecture diagram
- [ ] reason for technology choices
- [ ] setup instructions
- [ ] tests
- [ ] CI
- [ ] realistic error handling
- [ ] security considerations
- [ ] observability
- [ ] benchmark/evaluation where relevant
- [ ] known limitations
- [ ] roadmap
- [ ] screenshots
- [ ] short demo
- [ ] résumé bullets
- [ ] at least one failure/postmortem note

## Not portfolio-ready

- copied tutorial architecture,
- generic chatbot,
- no tests,
- no evals,
- no error handling,
- no measurable result,
- performance claims without benchmark,
- multi-agent design without a reason,
- unnecessary microservices,
- dozens of technologies added for keywords.
