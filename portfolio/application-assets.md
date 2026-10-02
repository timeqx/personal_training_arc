# Application Assets

Technical skill that is invisible to recruiters has low application value. Convert work into evidence.

# GitHub profile

Pin at most 4 high-value repositories:

1. **Rust AI Agent Runtime** — flagship
2. **Pure Rust Systems Project**
3. **AI/ML Project**
4. Existing strongest shipped application

Avoid pinning unfinished tutorial repositories.

Suggested profile positioning:

> Software Engineer • Applied AI • Rust  
> Building production-oriented AI agents, MCP integrations, RAG systems, high-performance Rust services, and cross-platform applications.

Only list technologies you can defend.

# Flagship README

Required sections:

## Problem
What problem does the system solve?

## Architecture
Diagram plus request lifecycle.

## Why Rust
Explain where Rust creates value and where Python remains a better choice.

## Agent lifecycle
- input
- state
- planning/routing
- tools
- retrieval
- response
- checkpoint

## MCP
- client/server
- tools/resources
- permissions

## RAG
- ingestion
- chunking
- embeddings
- retrieval
- reranking
- citations

## Evaluation
Show:
- dataset size
- retrieval metrics
- tool accuracy
- groundedness/correctness methodology
- latency
- cost

## Reliability
- retries
- timeout
- cancellation
- rate limit
- graceful shutdown

## Security
- threat model
- approval gates
- prompt-injection considerations
- secret handling

## Performance
Only make claims supported by benchmarks.

## Run locally
Provide one clear Docker Compose path.

## Limitations
Be explicit.

# Demo video

Target: **2–3 minutes**.

Show:
1. problem,
2. architecture in one sentence,
3. real task,
4. tools/RAG/MCP executing,
5. trace view,
6. evaluation/benchmark result,
7. GitHub link.

No long intro.

# Architecture diagram

Must show:
- UI/client
- API boundary
- Rust runtime
- providers
- tool registry
- MCP
- RAG/vector store
- PostgreSQL
- observability
- deployment boundary

Also have a simplified interview version you can draw in under 2 minutes.

# Metrics table

Keep a versioned result table:

| Metric | Baseline | Current |
| --- | ---: | ---: |
| Recall@5 | | |
| Grounded answer rate | | |
| Tool selection accuracy | | |
| Tool argument validity | | |
| Task success | | |
| Avg latency | | |
| p95 latency | | |
| Avg request cost | | |

Never fabricate results.

# Résumé positioning

Near-term headline can move toward:

> Full-Stack / Applied AI Engineer — Python, FastAPI, Rust, React/Flutter

Possible AI section, only after evidence exists:

**AI Engineering:** LLM Agents, Tool Calling, MCP, RAG, Embeddings, Vector Search, Agent Evaluation, Prompt/Context Engineering, Local LLMs

**Rust:** Tokio, Axum, Serde, Reqwest, Cargo, Async/Concurrency, Tracing

Do not add a keyword because it appeared in a job description.

# Flagship résumé bullet template

Replace placeholders with real numbers.

- Designed and built a provider-independent AI agent runtime in Rust supporting multi-step tool execution, structured outputs, asynchronous orchestration, retries, and cancellation.
- Implemented MCP client/server integrations and permission-controlled tools for repository/database workflows.
- Built an evaluated RAG pipeline using embeddings, vector retrieval, metadata filtering, reranking, and citations, improving **[real metric]** from **[baseline]** to **[result]**.
- Added distributed tracing and dashboards measuring latency, token usage, cost, tool-call accuracy, and retrieval performance.

Use only 2–4 bullets on the final résumé.

# Pure Rust résumé proof

Good evidence:
- Tokio concurrency
- bounded queues
- graceful shutdown
- networking
- PostgreSQL
- profiling
- benchmark result
- load test
- error design

Example:
> Built a Tokio-based background job service with bounded concurrency, retry/dead-letter handling, graceful shutdown, PostgreSQL persistence, and load-tested throughput of **[real result]**.

# Pure AI/ML résumé proof

Show methodology:
- clean split
- baseline
- metric
- experiment
- error analysis
- inference/deployment

This prevents your profile from looking like only "LLM API integration."

# Application package checklist

Before applying to a strong target:

- [ ] résumé tailored to job family
- [ ] portfolio links work
- [ ] flagship demo works
- [ ] GitHub README is clear
- [ ] no leaked keys/secrets
- [ ] CI badge is green
- [ ] current architecture diagram
- [ ] current eval/benchmark table
- [ ] 2-minute project explanation ready
- [ ] 10-minute deep dive ready
- [ ] one Rust failure story
- [ ] one AI evaluation story
- [ ] one production/deployment story
- [ ] one disagreement/decision story
- [ ] salary target and notice period prepared

# Open-source credibility

Long-term target:
- 3–5 meaningful merged PRs.

Choose projects close to your specialization:
- Rust MCP tooling
- Rust LLM clients
- Tokio/Axum ecosystem
- Qdrant/vector tooling
- agent/evaluation libraries

Quality matters more than count.

# Application iteration loop

Track:
- company
- role
- date
- source
- skills matched
- skills missing
- résumé version
- response
- interview stage
- questions asked
- rejection/feedback themes

Every 10–15 applications:
1. inspect response rate,
2. identify repeated skill gaps,
3. adjust one project/readiness item,
4. revise résumé wording based on evidence,
5. continue.

Do not rebuild your entire roadmap because of one rejection.
