# Interview Bank

## Rust questions

### Junior/intermediate
- Explain ownership to a C#/Java/Python developer.
- Move vs borrow.
- &str vs String.
- Vec vs slice.
- Option vs Result.
- Box vs Rc vs Arc.
- Mutex vs RwLock.
- trait vs struct.
- generic vs dyn Trait.
- lifetime annotations.
- Send and Sync.
- why Rust prevents data races.
- async Rust execution model.
- Tokio task vs OS thread.
- error handling strategy.
- crate/workspace organization.

### Advanced
- Pin/Unpin.
- cancellation safety.
- atomics.
- memory ordering.
- unsafe invariants.
- provenance.
- FFI.
- allocation behavior.
- zero-copy tradeoffs.
- API soundness.
- semver hazards.
- performance profiling.

---

# AI engineer questions

## ML
- Describe an ML project from problem definition to deployment.
- How do you detect leakage?
- Which metric would you choose for imbalanced fraud detection?
- How do you know a model is overfitting?
- What is calibration?
- Explain gradient descent.
- Why use validation data?

## Deep learning
- Explain backpropagation.
- What problem does attention solve?
- What are Q, K, V?
- Why multi-head attention?
- What is a residual connection?
- What does tokenization affect?
- Fine-tuning vs RAG.

## LLM engineering
- How do you enforce structured output?
- How do you handle rate limits?
- How do you handle streaming failures?
- How do you choose a model?
- How do you control cost?
- How do you version prompts?
- How do you test provider changes?

## RAG
- How do you choose chunk size?
- How do you evaluate retrieval?
- Recall@K vs answer quality.
- Why hybrid search?
- What does a reranker do?
- How do you prevent unsupported answers?
- What causes stale knowledge?
- How do metadata filters help?

## Agents
- What qualifies as an agent?
- When should you not use an agent?
- How do you prevent tool abuse?
- How do you evaluate tool use?
- How do you control loops?
- State vs memory.
- Human-in-the-loop.
- MCP.
- Multi-agent benefits/costs.
- Prompt injection.

---

# Systems questions

- Explain a request from browser to backend.
- Design idempotent API.
- Design retry policy.
- Explain connection pooling.
- What causes a slow SQL query?
- Indexing strategy.
- Transaction isolation.
- Queue semantics.
- Cache invalidation strategies.
- Horizontal vs vertical scaling.
- Reverse proxy.
- Load balancer.
- Observability.
- Graceful shutdown.
- Rate limiting.
- Secret management.

---

# Coding practice categories

Practice mostly easy/medium; occasionally hard.

- arrays/strings
- hash maps/sets
- stack/queue
- linked lists
- trees
- graphs
- BFS/DFS
- heaps
- sorting
- binary search
- intervals
- recursion/backtracking
- basic DP

Rule:
Solve first in Python for interview speed. Re-solve selected problems in Rust for fluency.

---

# System-design mock prompts

1. Design a RAG assistant for 10,000 employees.
2. Design an LLM gateway for multiple providers.
3. Design a coding agent with safe tools.
4. Design an embedding ingestion pipeline.
5. Design a chat system.
6. Design a webhook platform.
7. Design a remote job queue.
8. Design an observability platform for AI agents.
9. Design a feature flag service.
10. Design a vector search API.

For each:
- clarify requirements,
- estimate scale,
- API,
- data model,
- core components,
- failure modes,
- security,
- observability,
- cost,
- tradeoffs.

---

# Behavioral bank

Prepare STAR stories for:
- hardest production bug,
- disagreement with stakeholder,
- mistake you caused,
- performance improvement,
- system you owned end-to-end,
- deployment incident,
- ambiguous requirements,
- learning an unfamiliar technology,
- QA finding that changed implementation,
- project with a deadline,
- code/design review disagreement,
- using AI tools responsibly.

Never fabricate impact. Use measurable details you can defend.

---

# Mock interview rubric

Score 1–5:
- correctness,
- communication,
- assumptions,
- tradeoffs,
- testing,
- edge cases,
- complexity,
- debugging,
- production thinking.

Pass target:
- no area below 3,
- average at least 4 for target-role topics.
