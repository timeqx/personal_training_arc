# Track 03 — Systems, Backend, Cloud, and Reliability

Goal: supply the engineering depth required by both strong Rust roles and strong AI roles.

## Operating systems

Study:
- processes vs threads
- virtual memory
- stack/heap
- files and file descriptors
- system calls
- scheduling
- signals
- synchronization
- paging
- I/O
- containers at a conceptual level

Exercises:
- inspect processes with ps/top/htop.
- inspect system calls with strace or platform equivalent.
- send and handle Unix signals.
- explain what happens from process start to listening TCP socket.

## Networking

Study:
- TCP/IP
- DNS
- HTTP/1.1, HTTP/2, HTTP/3 concepts
- TLS
- sockets
- connection pooling
- keepalive
- timeouts
- retries
- idempotency
- backpressure
- load balancing

Exercises:
- write a TCP client/server.
- capture traffic with Wireshark.
- explain a complete HTTPS request from DNS lookup to response.
- deliberately create retry amplification and then fix it.

## Databases

Study:
- relational modeling
- normalization and denormalization
- indexes
- B-trees
- transactions
- ACID
- isolation
- MVCC concepts
- locks/deadlocks
- query planners
- replication concepts
- partitioning/sharding concepts
- vector search architecture

Exercises:
- design schemas for 3 real domains.
- diagnose 10 slow queries with EXPLAIN.
- create a deadlock intentionally.
- compare normalized and denormalized designs.
- use pgvector and explain its role vs PostgreSQL relational data.

## Distributed systems

Study:
- partial failure
- timeouts
- retries
- idempotency
- at-least-once / at-most-once concepts
- consensus intuition
- leader election intuition
- queues
- event-driven systems
- consistency models
- CAP as a tradeoff model, not a slogan
- sagas/outbox patterns
- distributed tracing

Exercises:
- build an idempotent webhook consumer.
- implement retry with jitter.
- design an order workflow that survives duplicate messages.
- draw failure scenarios for a 3-service architecture.

## Security

Study:
- authentication vs authorization
- OAuth 2 / OIDC concepts
- JWT risks/tradeoffs
- secrets management
- TLS
- SQL injection
- XSS/CSRF
- SSRF
- command injection
- dependency/supply-chain risk
- least privilege
- AI prompt injection and tool permissions

Exercises:
- threat-model your flagship agent.
- make destructive tools require approval.
- rotate a secret without downtime in a demo environment.
- write an authorization matrix.

## Linux and operations

Practice:
- shell
- systemd concepts
- logs
- permissions
- networking tools
- disk/process/memory diagnosis
- Nginx/reverse proxy
- SSH
- backups
- restore drills

Exercise:
Given a deliberately broken deployed service, recover it using only logs and system tools.

## Docker

Know:
- images/layers
- Dockerfile
- multi-stage builds
- Compose
- volumes
- networks
- environment/secrets
- health checks
- resource limits

Gate:
One command should launch your full development stack.

## Cloud

Choose one cloud to go deep first. AWS is a practical default.

Learn:
- IAM
- VPC concepts
- EC2
- S3
- RDS
- ECR
- CloudWatch
- Lambda
- API Gateway
- secrets
- cost awareness

Then gain basic literacy in GCP/Azure because AI employers may standardize on different clouds.

## Observability

Study:
- logs
- metrics
- traces
- OpenTelemetry concepts
- SLIs/SLOs
- latency percentiles
- saturation
- error budgets

Exercises:
- trace one request across 3 components.
- build dashboard metrics for an agent run.
- record p50/p95/p99.
- create an alert that is actionable rather than noisy.

## CI/CD

Required pipeline:
- formatting
- linting
- unit tests
- integration tests
- security/dependency checks
- build
- container build
- optional deploy to staging

For Rust:
- rustfmt
- Clippy
- cargo test

For Python:
- formatter/linter
- type checking where useful
- pytest

## System-design prompts

Practice designing:
1. high-volume webhook ingestion.
2. file-processing pipeline.
3. RAG platform for 10,000 employees.
4. multi-tenant agent platform.
5. notification service.
6. feature-flag service.
7. vector-search service.
8. model-serving platform.
9. code-search system.
10. background-job platform.

For each design discuss:
- APIs
- schema
- consistency
- caching
- failure handling
- security
- observability
- scaling
- cost
- test strategy.
