# Hiring Critical Path

This file answers one question:

> **What should I do first to maximize my chances for Applied AI, Agentic AI, Rust backend, and Rust × AI roles without wasting months on lower-priority study?**

The strategy is to become independently credible in:
- Rust,
- AI engineering,
- production software,

while using **Rust × AI** as the distinctive niche.

# Tier 1 — Must have before/while applying

These deserve most of your time.

## Rust
- ownership/borrowing
- lifetimes at practical level
- traits/generics
- Result/Option and error design
- Tokio async
- tasks/channels
- Arc/Mutex/RwLock
- Send/Sync
- Serde
- reqwest
- Axum
- tracing
- Cargo workspaces
- Clippy/rustfmt
- unit/integration tests

## Applied / Agentic AI
- Python/FastAPI remains strong
- provider APIs
- structured outputs
- tool/function calling
- agent state
- deterministic workflows
- planner/executor
- retries/fallback
- human approval
- MCP client/server
- RAG
- embeddings
- vector search
- pgvector or Qdrant
- hybrid retrieval
- reranking
- citations
- agent/RAG evaluation
- latency/token/cost measurement

## Production
- Docker
- CI/CD
- PostgreSQL
- Linux
- one cloud
- authentication/permissions
- logging/tracing
- rate limiting
- graceful shutdown
- secrets
- system design

## Evidence
- flagship Rust AI runtime
- pure Rust systems project
- pure AI/ML project
- live demo
- eval report
- benchmark report
- architecture diagram
- demo video

# Tier 2 — Important, but do after Tier 1 is moving

- LangGraph working knowledge
- PyTorch fundamentals
- transformer internals
- classical ML foundations
- OpenTelemetry
- GCP literacy after one primary cloud
- distributed-system fundamentals
- open-source contributions
- deeper retrieval/search knowledge
- model serving basics

These improve interview breadth and long-term mobility.

# Tier 3 — Long-term expert depth

Do not let these delay applications.

Rust:
- deep unsafe
- provenance
- advanced atomics
- lock-free structures
- compiler internals
- advanced FFI
- custom allocators

AI:
- advanced fine-tuning
- preference optimization
- deep research math
- CUDA kernels
- large-scale distributed training
- advanced RL

Platform:
- Kubernetes depth
- multi-cloud depth
- complex microservices without a real need

# The 80/20 rule

For every 10 hours:
- 4.5 h — build flagship
- 2.5 h — fundamentals
- 1.5 h — tests/evals/debugging
- 1 h — interview practice
- 0.5 h — documentation/GitHub

Once applying, move 1.5–2 hours from building/fundamentals into applications and mock interviews.

# Stop conditions

Stop studying a topic temporarily when:
- you can explain it without notes,
- implement a useful version,
- debug common failures,
- have evidence in a project,
- can answer target-role interview questions.

Then move to the next hiring gap. Return later for expert depth.

# Anti-waste rules

Do not:
- collect certificates instead of shipping,
- build multiple generic chatbots,
- learn five agent frameworks,
- learn three clouds at once,
- add Kubernetes before you need it,
- spend weeks polishing UI before evals/testing work,
- claim Rust performance without benchmarks,
- claim AI improvement without evals,
- build multi-agent systems when a deterministic workflow is better.

# Weekly prioritization algorithm

Every Sunday:

1. Look at progress/scorecard.md.
2. Find the lowest-scoring Tier-1 capability that blocks your target roles.
3. Choose **one** learning objective.
4. Choose **one** project feature that proves it.
5. Choose **one** exam/interview drill.
6. Ship by the end of the week.
7. Record evidence.
8. Re-score.

This prevents random studying.

# Target-role evidence matrix

| Evidence | Applied AI | Agentic AI | Rust Backend | Rust × AI |
| --- | :---: | :---: | :---: | :---: |
| Python/FastAPI | ✓ | ✓ |  | useful |
| RAG + eval | ✓ | ✓ |  | ✓ |
| Tool calling | ✓ | ✓ |  | ✓ |
| MCP | useful | ✓ |  | ✓ |
| Agent orchestration | useful | ✓ |  | ✓ |
| Rust ownership/traits |  |  | ✓ | ✓ |
| Tokio/concurrency |  | useful | ✓ | ✓ |
| Axum/networking |  | useful | ✓ | ✓ |
| Docker/cloud | ✓ | ✓ | ✓ | ✓ |
| Observability | ✓ | ✓ | ✓ | ✓ |
| Pure ML project | ✓ | useful |  | useful |
| Pure Rust project |  |  | ✓ | ✓ |
| Rust AI runtime | useful | ✓ | useful | ✓ |

# Application timing

Apply before mastery.

A strong early application point is:
- flagship v1 works,
- RAG is evaluated,
- MCP works,
- Rust async/backend fundamentals are defensible,
- CI/Docker exist,
- portfolio assets are present.

Keep learning while interviewing.

The goal is not to be "finished." The goal is to have enough credible evidence that an employer can see the trajectory and trust you to perform.
