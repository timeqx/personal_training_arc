# Track 01 — Rust Mastery

Goal: become a strong Rust engineer independently of AI.

## Level 1 — Language fluency

### Read
- The Rust Programming Language, current stable edition.
- Rust By Example alongside the relevant chapters.
- Cargo Book sections on packages, workspaces, features, profiles, and publishing.

### Must know
- variables, mutability, scalar/compound types
- ownership and moves
- Copy vs Clone
- borrowing
- mutable vs shared references
- slices
- structs and enums
- pattern matching
- Option and Result
- modules and visibility
- collections
- iterators
- closures
- generics
- traits
- associated types
- lifetimes
- smart pointers
- interior mutability

### Exercises
1. Predict whether 30 short ownership snippets compile before running them.
2. Rewrite a clone-heavy program to use borrowing where appropriate.
3. Implement a generic in-memory repository using traits.
4. Build a parser returning meaningful custom errors.
5. Implement an iterator over your own data structure.
6. Create a type whose API prevents invalid state.
7. Explain covariance/invariance at a practical level using references and mutable references.
8. Refactor a large single-file program into a workspace with two library crates and one binary.

### Oral questions
- What exactly moves when a value is moved?
- Why can many immutable references exist but only one mutable reference?
- When is Clone the right answer instead of fighting the borrow checker?
- What does a lifetime annotation describe?
- Trait object or generic parameter: how do you decide?
- What is interior mutability and why does Rust allow it?

### Gate project
Build a production-quality CLI:
- subcommands,
- configuration,
- structured errors,
- logging,
- tests,
- documentation,
- CI,
- zero panicking on expected user errors.

---

## Level 2 — Idiomatic Rust and API design

### Topics
- newtype pattern
- builder pattern
- typestate concepts
- From, Into, TryFrom
- Display and Error
- iterator composition
- zero-copy parsing
- feature flags
- library vs binary boundaries
- public API stability
- documentation tests
- property-based testing
- fuzzing basics

### Exercises
1. Design an API where an unauthenticated client cannot call authenticated-only methods.
2. Replace a boolean-parameter-heavy API with types.
3. Implement conversions using From/TryFrom.
4. Write property tests for a parser.
5. Fuzz a boundary parser and fix any crash/panic.
6. Review one popular Rust crate and identify five API-design decisions worth copying.

### Gate
Publish a small reusable crate or maintain it as if it were public:
- semver-aware API,
- documentation,
- examples,
- unit/integration/doc tests,
- changelog,
- Clippy clean.

---

## Level 3 — Concurrency

### Read
- Rust Book concurrency chapter.
- Rustonomicon sections on Send, Sync, races, and concurrency.

### Topics
- OS threads
- channels
- Arc
- Mutex
- RwLock
- atomics
- Send
- Sync
- race conditions vs data races
- deadlocks
- lock ordering
- work queues
- graceful shutdown

### Exercises
1. Implement a thread pool.
2. Create a bounded producer/consumer system.
3. Intentionally create a deadlock, diagnose it, then redesign it.
4. Build a concurrent cache.
5. Explain why a type is or is not Send/Sync.
6. Compare channel-based ownership transfer with shared-state locking.

### Gate
Build a multithreaded job processor with:
- bounded queue,
- graceful shutdown,
- retries,
- timeout handling,
- metrics,
- stress test.

---

## Level 4 — Async Rust

### Read
- Tokio tutorial.
- Async Rust material from official/community primary documentation.
- Revisit Future, Pin, Waker after building practical systems.

### Topics
- async fn
- Future
- polling
- Waker
- task scheduling
- Tokio runtime
- spawn
- select
- channels
- cancellation
- backpressure
- blocking work in async systems
- streams
- timeouts
- structured concurrency concepts
- Pin/Unpin

### Exercises
1. Build a TCP echo server.
2. Build an async HTTP client with retries and exponential backoff.
3. Limit concurrency with a semaphore.
4. Demonstrate why holding a blocking mutex across await can be harmful.
5. Implement cancellation-safe behavior for one workflow.
6. Write a small Future manually for learning purposes.
7. Explain the difference between concurrency and parallelism.

### Gate
Build an Axum service with:
- PostgreSQL,
- async background work,
- timeouts,
- tracing,
- graceful shutdown,
- load test,
- no unbounded task spawning.

---

## Level 5 — Systems programming

### Topics
- memory representation
- stack vs heap
- alignment and padding
- bytes and encodings
- file I/O
- mmap concepts
- sockets
- protocols
- serialization
- process management
- signals
- FFI
- OS primitives

### Exercises
1. Write a binary protocol encoder/decoder.
2. Implement a tiny TCP protocol.
3. Use strace or equivalent to inspect system calls.
4. Compare buffered vs unbuffered I/O.
5. Build a Unix-style pipeline utility.
6. Call a C library through FFI and wrap it safely.

### Gate
Implement one:
- small key-value store,
- mini Redis-like server,
- binary log processor,
- file indexer/search engine.

Document consistency, durability, and failure tradeoffs.

---

## Level 6 — Unsafe Rust

### Read
- Rustonomicon.
- Rust Reference sections relevant to every unsafe feature you use.

### Topics
- unsafe contracts
- raw pointers
- aliasing
- provenance concepts
- MaybeUninit
- repr
- unions
- FFI safety
- Send/Sync unsafe implementations
- panic/unwind safety
- memory-model awareness

### Rules
- Do not use unsafe merely for speed.
- Every unsafe block must state a safety invariant.
- Prefer a small unsafe core behind a safe API.
- Use Miri when relevant.

### Exercises
1. Wrap a C API safely.
2. Implement a small arena or buffer abstraction.
3. Find the soundness bug in deliberately broken unsafe examples.
4. Use Miri to catch undefined-behavior examples.
5. Write a safety section explaining assumptions and invariants.

### Gate
Code review defense: another engineer should be able to audit every unsafe block and understand why it is sound.

---

## Level 7 — Performance

### Topics
- asymptotic complexity
- allocations
- copying
- cache locality
- branch behavior
- zero-copy techniques
- batching
- SIMD concepts
- profiling
- flamegraphs
- Criterion
- throughput vs latency
- tail latency

### Exercises
1. Benchmark before and after every optimization.
2. Remove an unnecessary allocation from a hot loop.
3. Compare HashMap strategies only with measurements.
4. Profile CPU and allocation hotspots.
5. Explain why one "optimization" made performance worse.

### Gate
Publish a benchmark report that includes:
- methodology,
- hardware,
- dataset/workload,
- warmup,
- sample size,
- p50/p95/p99 if applicable,
- before/after,
- limitations.

---

## Level 8 — Architecture and open source

### Practice
- read source code from Tokio, Axum, Serde, tracing, and other mature crates.
- contribute documentation/tests first, then code.
- review PRs.
- maintain compatibility.
- learn semver and release discipline.

### Graduation evidence
You should have:
- at least 3 substantial Rust projects,
- one networked/async service,
- one performance investigation,
- one justified unsafe/FFI exercise,
- several meaningful open-source contributions,
- ability to debug compiler/lifetime/concurrency problems without immediately asking an AI agent.
