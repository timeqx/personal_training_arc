# Track 04 — Rust × AI Specialization

Goal: create a distinctive niche on top of independent Rust and AI competence.

The specialization is **not** permission to skip Rust fundamentals or AI fundamentals. This track starts becoming valuable only when the other tracks are progressing in parallel.

## Why this niche exists

Rust is useful where AI systems need:
- predictable performance,
- low memory overhead,
- concurrency,
- long-running reliability,
- safe systems programming,
- high-performance networking,
- local inference integrations,
- infrastructure and tooling,
- sandboxing,
- developer tools.

AI engineering brings:
- model/provider integration,
- RAG,
- agents,
- evaluation,
- embeddings,
- inference,
- data pipelines,
- production AI reliability.

The intersection can include:
- agent runtimes,
- inference gateways,
- model routers,
- MCP servers/clients,
- high-throughput embedding/retrieval components,
- AI developer tools,
- local-model runtimes/tooling,
- observability and evaluation infrastructure.

---

# Flagship project — Rust Agent Runtime / Harness

## Minimum architecture

- **Core runtime:** Rust
- **API/UI layer:** Rust or FastAPI + React/Next.js
- **Database:** PostgreSQL
- **Vector search:** pgvector or Qdrant
- **Cache/queue:** optional Redis
- **Providers:** at least two remote LLM providers + one local provider when practical
- **Protocol/tool integration:** MCP
- **Observability:** tracing + OpenTelemetry-compatible traces where practical
- **Deployment:** Docker Compose, CI

## Required modules

### 1. Provider abstraction
Support:
- completion/chat,
- streaming,
- structured output,
- tool calls,
- retries,
- timeout,
- provider-specific error mapping.

Exercise:
- add a new provider without changing agent-core code.

### 2. Tool registry
Support:
- typed schemas,
- validation,
- permissions,
- timeouts,
- error handling,
- tool results,
- destructive-action approval.

Exercise:
- deliberately send malformed arguments and prove the runtime rejects them.

### 3. Agent execution loop
Support:
- state,
- bounded number of steps,
- tool invocation,
- final response,
- cancellation,
- checkpointing.

Rule:
Never permit an unbounded autonomous loop.

### 4. Workflow engine
Implement at least:
- sequential workflow,
- router → specialist,
- parallel fan-out → gather,
- planner → executor,
- review/critique loop.

Measure which patterns actually help on a fixed task set.

### 5. MCP
Build:
- an MCP client,
- an MCP server,
- at least five useful tools,
- resources,
- clear permission policy.

Suggested server:
**Developer Workspace MCP**
- list_repository_files
- search_code
- read_file
- inspect_database_schema
- explain_query
- create_issue or propose_change behind an approval gate

### 6. RAG
Implement:
- ingestion,
- chunking,
- metadata,
- embeddings,
- semantic search,
- optional lexical/hybrid retrieval,
- reranking,
- citations,
- abstention.

Evaluation:
- Recall@K,
- MRR or nDCG,
- grounded answer accuracy,
- latency,
- cost.

### 7. Memory
Separate:
- conversation state,
- durable user/project memory,
- retrieval corpus,
- execution checkpoints.

Be able to explain why these are not the same thing.

### 8. Safety and permissions
Build:
- least-privilege tool scopes,
- path restrictions,
- SQL read-only mode,
- destructive-action approval,
- prompt-injection tests,
- secret redaction,
- execution limits.

### 9. Observability
Record per run:
- model,
- input/output tokens,
- latency,
- tool sequence,
- tool duration,
- retry count,
- failures,
- cost estimate,
- retrieval stats.

### 10. Evaluation harness
Maintain a versioned dataset of tasks:
- answer-only,
- retrieval,
- tool choice,
- tool arguments,
- multi-step workflows,
- refusal/permission tests.

Every major change should have:
- before result,
- after result,
- explanation,
- regressions.

---

# Specialty exercises

1. Build an LLM streaming parser in Rust.
2. Implement provider retry/backoff with jitter.
3. Build a bounded async tool executor with Tokio.
4. Create a tool permission model using Rust types.
5. Benchmark JSON parsing and serialization choices on a realistic trace workload.
6. Build an MCP server in Rust.
7. Build an MCP client in Rust.
8. Create a pgvector-backed retrieval service.
9. Implement a reranking interface where the implementation can be swapped.
10. Add local Ollama support.
11. Implement graceful cancellation of a running agent.
12. Implement trace propagation across Rust and Python services.
13. Create deterministic replay for a recorded tool run where feasible.
14. Design a model-routing policy based on task type, latency, and cost.
15. Write an adversarial prompt-injection suite.
16. Build a small Rust inference or embedding component using a suitable ecosystem crate.
17. Benchmark Rust vs a Python implementation for one well-defined infrastructure task. Do not claim Rust is faster unless the benchmark supports it.
18. Produce a written postmortem after one serious failure.

---

# Advanced niche projects

## A. LLM Gateway
Rust service providing:
- provider routing,
- rate limits,
- retries,
- caching,
- streaming,
- cost tracking,
- observability,
- fallback.

## B. High-throughput embedding pipeline
- file ingestion,
- chunking queue,
- batched embedding calls,
- backpressure,
- persistence,
- retry/dead-letter logic.

## C. Agent sandbox
Safely expose:
- selected filesystem,
- subprocess execution,
- network allowlist,
- resource limits,
- audit logs.

## D. AI codebase explorer
- repository indexing,
- semantic + lexical search,
- code-aware chunking,
- source citations,
- MCP tools,
- architecture questions.

## E. Evaluation platform
- dataset management,
- evaluator plugins,
- result comparisons,
- regression gates in CI,
- cost/latency dashboards.

---

# Capstone graduation requirements

The flagship project is ready for your résumé when:

- CI is green.
- Core logic has unit tests.
- Provider/tool integrations have integration tests.
- At least 50 eval tasks exist; target 100+.
- You can show a baseline and an improved result.
- The architecture is documented.
- Threat model exists.
- No destructive tool executes without explicit policy.
- At least one load/performance test exists.
- The project has a demo video.
- README explains tradeoffs and limitations.
- You can answer every "defense question" below.

## Defense questions

1. Why Rust here instead of Python?
2. Which components would you still keep in Python and why?
3. What is your agent state model?
4. What stops infinite loops?
5. What is cancellation-safe in your runtime?
6. What happens when a provider times out halfway through streaming?
7. How are tool schemas validated?
8. How do you mitigate prompt injection?
9. What does MCP solve that normal HTTP APIs do not?
10. How do you evaluate tool selection?
11. How do you evaluate retrieval independently from generation?
12. What changed between your baseline and current results?
13. Where is the bottleneck under load?
14. What would fail first at 100x traffic?
15. What part would you redesign if you started again?
