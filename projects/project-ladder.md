# Project Ladder

Do not build all projects at once. Each project exists to prove a specific level.

## Project 1 — Rust CLI
**Proves:** language fundamentals, API design, testing.

Requirements:
- config,
- subcommands,
- custom errors,
- unit/integration tests,
- CI,
- documentation.

Examples:
- log analyzer,
- duplicate-file finder,
- local task database.

## Project 2 — Concurrent Rust service
**Proves:** concurrency/async/networking.

Requirements:
- Tokio,
- bounded concurrency,
- timeout/retries,
- graceful shutdown,
- tracing,
- load test.

Example:
- URL metadata crawler,
- background-job processor.

## Project 3 — Classical ML system
**Proves:** non-LLM AI fundamentals.

Requirements:
- dataset analysis,
- baseline,
- preprocessing,
- cross-validation,
- appropriate metrics,
- error analysis,
- inference API.

## Project 4 — PyTorch model
**Proves:** deep-learning competence.

Requirements:
- custom training loop,
- train/validation separation,
- checkpoint,
- experiment comparison,
- reproducibility notes.

## Project 5 — Evaluated RAG system
**Proves:** production AI application engineering.

Requirements:
- ingestion,
- chunking,
- embeddings,
- vector DB,
- reranking,
- citations,
- evaluation set,
- retrieval and answer metrics,
- cost/latency.

Suggested domain:
- software repository or technical documentation.

## Project 6 — Rust MCP server
**Proves:** Rust + agent tooling.

Requirements:
- five tools,
- schema validation,
- safe permissions,
- tests,
- logging,
- documentation.

## Project 7 — Agent evaluation harness
**Proves:** AI reliability skill.

Requirements:
- versioned task dataset,
- tool-choice metric,
- argument-validity metric,
- outcome metric,
- latency/cost,
- regression comparison.

## Project 8 — Rust AI runtime
**Proves:** specialization.

Use the requirements in tracks/04-rust-ai-specialization.md.

---

# Optional mastery projects

## Storage engine
Rust:
- WAL concepts,
- indexes,
- compaction,
- crash recovery.

## Mini async runtime
Learning-only project:
- understand Future/Waker/task scheduling.

## Compiler/interpreter
- lexer,
- parser,
- AST,
- evaluator,
- optional bytecode.

## Mini transformer
Python/PyTorch:
- tokenizer or simple tokenization pipeline,
- attention,
- transformer blocks,
- tiny training run.

## Model inference server
- batching,
- queueing,
- metrics,
- load tests.

## Distributed job system
- worker pool,
- idempotency,
- retry,
- dead letter,
- observability.

---

# Project quality checklist

Every portfolio project should have:

- [ ] problem statement
- [ ] architecture diagram
- [ ] reason for technology choices
- [ ] setup instructions
- [ ] tests
- [ ] CI
- [ ] realistic error handling
- [ ] security considerations
- [ ] observability
- [ ] benchmark or evaluation where relevant
- [ ] known limitations
- [ ] roadmap
- [ ] screenshots/demo
- [ ] concise résumé bullets

## "Not portfolio-ready" warning signs

- only one giant file,
- copied tutorial architecture,
- no tests,
- no error handling,
- secrets committed,
- no README,
- no evaluation for AI claims,
- performance claims without benchmarks,
- "multi-agent" architecture where one deterministic function would suffice,
- dozens of technologies added only for keywords.
