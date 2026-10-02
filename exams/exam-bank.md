# Exam Bank

Use closed-book conditions first. Afterward, check documentation and correct yourself.

Scoring:
- 90–100: strong
- 80–89: ready to advance with minor gaps
- 70–79: repeat weak sections
- below 70: do not rush forward

For coding/design questions, correctness alone is not full credit. Include reasoning, edge cases, tests, and tradeoffs.

---

# Baseline Exam A — Rust

1. Explain ownership in your own words.
2. What is the difference between move, Copy, and Clone?
3. Why does this fail?

\`\`\`rust
let mut x = vec![1,2,3];
let y = &x[0];
x.push(4);
println!("{y}");
\`\`\`

4. What is a lifetime?
5. When would you use Box, Rc, Arc?
6. Difference between Result and Option?
7. What does Send mean?
8. What does Sync mean?
9. Mutex vs RwLock?
10. Explain async/await without saying "it makes it asynchronous."
11. What is a Future?
12. What does Pin protect?
13. Trait object vs generic?
14. What can unsafe Rust do that safe Rust cannot?
15. Why is data-race freedom not the same as race-condition freedom?

Coding:
16. Implement a generic function that returns the largest item from a slice.
17. Implement a small parser returning a custom error.
18. Build a producer/consumer queue.
19. Write three tests for an error-prone function.
20. Diagnose a provided deadlock scenario.

---

# Baseline Exam A — AI/ML

1. Training vs inference.
2. Supervised vs unsupervised learning.
3. What is overfitting?
4. Why split train/validation/test?
5. Precision vs recall.
6. What does F1 capture?
7. Explain gradient descent.
8. What is backpropagation?
9. What is an embedding?
10. Explain self-attention.
11. Token vs word.
12. What is temperature?
13. What problem does RAG solve?
14. What is cosine similarity?
15. Why can a RAG system hallucinate even with good retrieval?
16. Prompting vs fine-tuning vs RAG.
17. What makes an "agent" different from a single LLM call?
18. What is tool-calling accuracy?
19. How would you evaluate an AI feature?
20. Name three security risks of tool-using agents.

Practical:
21. Calculate precision/recall from a confusion matrix.
22. Build a train/test split without leakage.
23. Inspect five model errors and categorize them.
24. Design a retrieval eval dataset.
25. Design a tool-use eval dataset.

---

# Baseline Exam A — Systems

1. Process vs thread.
2. Stack vs heap.
3. TCP vs UDP.
4. What happens during DNS lookup?
5. What does TLS provide?
6. What makes an HTTP method idempotent?
7. What is a database index?
8. Why can too many indexes be bad?
9. Explain a database transaction.
10. What is isolation?
11. What is a deadlock?
12. Cache-aside pattern.
13. At-least-once delivery means what?
14. Why must consumers often be idempotent?
15. Timeout vs retry.
16. Why add jitter?
17. What are logs/metrics/traces?
18. Container vs VM.
19. Authentication vs authorization.
20. What is least privilege?

---

# Rust Core Exam B

## Written
1. Give three ways ownership can be transferred.
2. Explain reborrowing.
3. Explain interior mutability.
4. When is RefCell appropriate?
5. Why can Rc not normally cross threads?
6. Explain associated type vs generic trait parameter.
7. When is dyn Trait useful?
8. Explain object safety at a practical level.
9. Describe a useful newtype.
10. Design an error enum for an HTTP/database service.

## Code review
Review a 100–200 line Rust program and find:
- unnecessary clones,
- panics,
- poor errors,
- misleading names,
- bad ownership boundaries,
- missing tests.

## Build
Create a crate from scratch in 90 minutes with:
- parser,
- typed domain model,
- custom error,
- tests,
- documentation.

---

# AI Fundamentals Exam B

1. Derive MSE gradient for a linear model.
2. Explain logistic regression.
3. Bias vs variance.
4. Bagging vs boosting.
5. Cross-validation.
6. Calibration.
7. Why does normalization help some models?
8. Explain autograd.
9. Why do we need nonlinear activations?
10. What is an embedding matrix?
11. Explain query/key/value in attention.
12. Why scale dot products?
13. Why use multiple attention heads?
14. Encoder vs decoder.
15. Causal mask.
16. What is a tokenizer and why does it matter?
17. What does a context window mean?
18. Greedy vs top-p decoding.
19. Fine-tuning vs in-context learning.
20. Give an experiment that could falsify your claim that a model change improved quality.

Practical:
- implement attention from scratch,
- train a small model,
- produce an error-analysis report.

---

# Rust Async / Concurrency Exam C

1. Concurrency vs parallelism.
2. Future vs thread.
3. How does a Tokio task make progress?
4. What does await do?
5. What is cooperative scheduling?
6. What is cancellation safety?
7. When should spawn_blocking be used?
8. Explain Arc<Mutex<T>>.
9. Why can a lock across await be risky?
10. Channel vs shared state.
11. What is backpressure?
12. Semaphore use case.
13. How would you shut down 100 worker tasks cleanly?
14. What happens if a spawned task panics?
15. How would you detect starvation?

Practical:
- debug one deadlock,
- debug one runaway task,
- implement bounded concurrency,
- add graceful shutdown.

---

# Agentic Systems Exam C

1. Workflow vs agent.
2. When should a deterministic workflow replace an agent?
3. What is tool calling?
4. How do you validate tool arguments?
5. Planner/executor benefits and risks.
6. Why can multi-agent systems be worse than one agent?
7. Define durable state vs conversation history.
8. What is MCP?
9. Tool vs resource vs prompt in MCP.
10. How do permissions change agent architecture?
11. Explain prompt injection against a tool-using agent.
12. Retrieval evaluation vs generation evaluation.
13. How do you measure tool-selection accuracy?
14. How do you prevent infinite loops?
15. How do you test a nondeterministic system?
16. What should be logged?
17. What should never be logged?
18. How would you introduce human approval?
19. How should an agent behave when evidence is weak?
20. What would you put in CI for an agent repository?

Design:
Design a code-assistant agent that can inspect a private repository but cannot arbitrarily execute shell commands or expose secrets.

---

# Advanced Rust Oral Exam D

Give yourself 5 minutes per question.

1. Explain memory layout and alignment.
2. Explain what makes unsafe code sound or unsound.
3. What is undefined behavior?
4. Raw pointer vs reference.
5. Why does MaybeUninit exist?
6. What safety invariant would you write for a custom buffer?
7. What does repr(C) do and not guarantee?
8. Explain atomics and memory ordering at a conceptual level.
9. What is false sharing?
10. When can zero-copy make an API worse?
11. Describe how you would profile a Rust service.
12. Explain p99 latency.
13. Why might fewer allocations not improve end-to-end latency?
14. What does FFI boundary safety require?
15. Explain a Rust compiler error that taught you something important.

---

# Final Capstone Defense

Pass only if you can answer from your actual implementation.

1. Walk through one request end-to-end.
2. Where can it fail?
3. Which failures are retried?
4. Which failures must not be retried?
5. What makes the system safe?
6. What makes it observable?
7. What does the benchmark actually prove?
8. What does the eval actually prove?
9. What does it not prove?
10. Why these technologies?
11. What complexity would you remove?
12. How does the system degrade when the model provider is unavailable?
13. How does it behave under load?
14. How is state recovered?
15. What would you change for enterprise multi-tenancy?
