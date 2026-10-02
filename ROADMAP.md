# 16-Week Hiring Sprint + Long-Term Mastery

Target window: **October 2026 → January 2027**, with active applications beginning before the sprint is finished.

The sprint is optimized around current target roles:
- Applied AI
- Agentic AI
- AI-native full stack
- Python/FastAPI AI
- Rust backend
- Rust × AI infrastructure

Default workload: **12–16 focused hours/week**.

## Time allocation

Until application-ready:
- **45% flagship building**
- **25% fundamentals**
- **15% testing/evaluation/debugging**
- **10% interview practice**
- **5% documentation/GitHub**

After applications start:
- **35% flagship building**
- **20% fundamentals**
- **15% interview practice**
- **15% applications/networking**
- **10% tests/evals**
- **5% documentation**

Do not add a new technology unless it closes a target-role gap or materially improves the flagship system.

---

# Week 0 — Baseline and setup

## Exams
Take without studying first:
- Rust Baseline A
- AI/ML Baseline A
- Systems Baseline A

## Setup
- Rust stable, rustfmt, Clippy, rust-analyzer
- Python 3.12+
- PostgreSQL + pgvector
- Docker
- GitHub Actions
- project journal
- benchmark/eval folders

## Output
- baseline scores
- top 5 gaps
- current evidence links
- exact target roles
- first 4-week goals

---

# October — Rust core + working agent

## Week 1 — Rust ownership + agent skeleton

Rust:
- ownership, move, Copy, Clone
- borrowing/references
- Option/Result
- enums/pattern matching

AI:
- provider API basics
- structured outputs

Build:
- create flagship Rust agent workspace
- one provider
- structured response type
- unit tests

Proof:
- explain ownership without notes
- CI running rustfmt + Clippy + cargo test

## Week 2 — Traits, errors, provider abstraction

Rust:
- structs
- traits/generics
- error types
- iterators
- modules/crates

Build:
- LlmProvider abstraction
- second provider
- typed error taxonomy
- retries/timeouts

Exercise:
Add a provider without editing core orchestration logic.

## Week 3 — Tokio + tools

Rust:
- async/await
- Future intuition
- Tokio tasks
- channels
- Arc
- Mutex/RwLock
- Send/Sync

AI:
- function/tool calling
- tool schemas

Build:
- async tool registry
- bounded tool execution
- malformed-argument tests
- timeout handling

Proof:
- explain why/when Arc<Mutex<T>> is needed
- demonstrate bounded concurrency

## Week 4 — Axum + deployable v0

Rust:
- Axum
- Serde
- reqwest
- tracing
- graceful shutdown

Build:
- HTTP API
- streaming where feasible
- basic state
- Dockerfile
- Docker Compose
- simple dashboard or CLI trace view

### October gate
By October 31:
- agent executes a real multi-step task,
- supports at least two providers or one remote + one local provider,
- has tests,
- has CI,
- runs from Docker,
- emits structured traces.

Take Rust Core Exam B.

---

# November — RAG + MCP + real evaluation

## Week 5 — RAG foundations
Learn:
- embeddings
- chunking
- metadata
- cosine similarity
- Top-K
- context windows

Build:
- ingestion pipeline
- pgvector
- source metadata
- semantic retrieval

Create:
- first 30–50 eval questions.

## Week 6 — Retrieval quality
Learn:
- hybrid search
- reranking
- Recall@K
- MRR/nDCG intuition
- grounded answers
- abstention

Build:
- hybrid retrieval if useful
- reranker
- citations
- retrieval metrics

Proof:
Publish baseline vs improved retrieval results.

## Week 7 — MCP
Learn current MCP specification:
- host/client/server
- tools
- resources
- prompts
- transport
- schemas
- permissions

Build:
- Rust MCP server
- Rust MCP client
- Developer Workspace MCP tools
- read-only/safe tool policies

## Week 8 — Agent orchestration
Learn:
- state
- router
- planner/executor
- deterministic workflows
- checkpointing
- human approval
- fan-out/gather
- critique/review loop

Build only patterns that improve a real task:
- router → specialist
- planner → executor
- one parallel workflow
- destructive-action approval

Also:
- implement or study the equivalent workflow in LangGraph so you can discuss mainstream Python tooling.

### November gate
By November 30:
- agent is clearly beyond a chatbot,
- MCP client/server works,
- RAG is evaluated,
- at least 50 eval tasks exist,
- permissions exist,
- you can explain when **not** to use an agent.

Take Agentic Systems Exam C.

---

# December — productionize + portfolio + applications

## Week 9 — Observability
Build:
- tracing
- token accounting
- cost estimates
- tool latency
- request latency
- retries/errors
- retrieval stats

Study:
- OpenTelemetry concepts
- p50/p95/p99

Deliver:
- agent-run trace view/dashboard.

## Week 10 — Reliability and security
Build/test:
- rate limiting
- retries with jitter
- cancellation
- graceful shutdown
- secret handling
- prompt-injection tests
- path restrictions
- SQL read-only mode
- approval gates

Write:
- threat model
- failure-mode table.

## Week 11 — Cloud deployment
Learn one cloud well enough to operate the app:
- IAM
- compute
- storage
- managed DB
- secrets
- logs
- container registry

AWS is the default first choice; gain basic GCP literacy afterward.

Deploy:
- flagship app
- database/vector store
- logs/metrics

## Week 12 — Portfolio release
Required:
- polished README
- architecture diagram
- setup instructions
- screenshots
- benchmark/eval table
- limitations
- threat model
- 2–3 minute demo
- live deployment
- résumé bullets
- pinned GitHub repository

### December application gate
Start/continue serious applications.

Do **not** wait for:
- advanced unsafe Rust,
- Kubernetes depth,
- advanced fine-tuning,
- research-level ML theory.

---

# January — interview strength + deeper differentiation

## Week 13 — Python AI production depth
Strengthen:
- asyncio
- typing
- Pydantic
- FastAPI
- SQLAlchemy
- pytest
- httpx
- background work
- dependency injection

Build:
- one Python/LangGraph reference implementation or service that interoperates with the Rust system.

Purpose:
Be employable for AI roles that do not use Rust.

## Week 14 — ML/deep-learning credibility
Learn/practice:
- train/validation/test
- leakage
- precision/recall/F1/ROC-AUC
- gradient descent
- neural networks
- PyTorch
- transformers/attention/tokenization

Build:
- small scikit-learn project
- small PyTorch project
- scaled dot-product attention exercise

Purpose:
Avoid being only an LLM-wrapper engineer.

## Week 15 — Rust backend interview depth
Practice:
- lifetimes
- trait objects vs generics
- concurrency
- cancellation
- networking
- SQL
- profiling
- benchmarks
- API design

Build:
- load test
- bottleneck analysis
- one measured optimization

Take Rust Async/Concurrency Exam C.

## Week 16 — application and defense week
Do:
- 2 Rust mock interviews
- 2 AI mock interviews
- 2 system-design interviews
- final capstone defense
- revise résumé
- revise GitHub
- tailor applications by job family

Target searches:
- Applied AI Engineer
- AI Engineer
- Agentic AI Engineer
- AI Application Engineer
- AI Agent Developer
- Full Stack AI Engineer
- Generative AI Engineer
- AI-Native Software Engineer
- Python/FastAPI AI Engineer
- Junior/Mid Rust Backend Engineer
- Rust × AI Developer

---

# Parallel weekly requirements

Every week:
- 1 coding-interview session in Python
- 1 selected problem re-solved in Rust
- 1 system-design prompt
- 1 no-AI debugging block
- 1 primary-source reading session
- 1 measurable artifact shipped
- 1 progress-scorecard update

Every two weeks:
- one public technical note or strong README update
- one mock interview
- one benchmark/eval comparison

Every month:
- retake one exam
- create one demo/video/update
- review résumé keywords against actual evidence
- remove low-value backlog items

---

# February and beyond — mastery loop

Continue applications and deepen independently in Rust and AI.

## Rust expert cycles
- unsafe + memory model
- FFI
- atomics
- async runtime internals
- storage engines
- networking
- compilers/interpreters
- profiling
- open-source contributions

## AI expert cycles
- classical ML depth
- transformer internals
- fine-tuning/LoRA
- quantization
- model serving
- MLOps
- evaluation science
- research-paper reproduction
- inference optimization

## Systems expert cycles
- distributed systems
- observability
- databases
- networking
- Linux internals
- security
- cloud architecture

## Rust × AI cycles
- LLM gateway
- high-throughput embedding pipeline
- inference gateway
- agent sandbox
- evaluation platform
- local model tooling

Each 8–12 week expert cycle must end with:
1. primary-source reading,
2. implementation,
3. production version,
4. benchmark/evaluation,
5. technical write-up,
6. open-source contribution or review,
7. oral defense.

Expertise comes from repeated depth and judgment, not the number of technologies listed.
