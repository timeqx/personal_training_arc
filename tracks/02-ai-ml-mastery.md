# Track 02 — AI / ML Mastery

Goal: become an AI engineer with foundations broad enough to work beyond agents and LLM wrappers.

## Level 1 — Math and data foundations

### Learn
Linear algebra:
- vectors and matrices
- matrix multiplication
- dot products
- norms
- eigenvalues/eigenvectors intuition
- SVD intuition

Calculus:
- derivatives
- partial derivatives
- chain rule
- gradients

Probability/statistics:
- random variables
- common distributions
- expectation and variance
- conditional probability
- Bayes rule
- likelihood
- confidence intervals
- hypothesis-testing intuition

Data:
- NumPy
- Pandas/Polars
- visualization
- data cleaning
- leakage
- sampling

### Exercises
1. Implement vector/matrix operations with NumPy.
2. Derive the gradient of mean-squared error.
3. Simulate Bayes rule with synthetic data.
4. Explain correlation vs causation.
5. Identify leakage in five deliberately flawed ML pipelines.

### Gate
Explain gradient descent mathematically and implement linear regression without scikit-learn.

---

## Level 2 — Classical machine learning

### Learn
- regression
- classification
- logistic regression
- decision trees
- random forests
- gradient boosting
- SVM intuition
- k-nearest neighbors
- clustering
- dimensionality reduction
- feature engineering
- calibration
- imbalanced datasets
- cross-validation
- hyperparameter tuning

### Metrics
- MSE/MAE
- accuracy
- precision
- recall
- F1
- ROC-AUC
- PR-AUC
- confusion matrix
- calibration metrics

### Exercises
1. Implement linear and logistic regression from basic operations.
2. Train three different models on the same dataset and justify the winner.
3. Build a reproducible sklearn pipeline.
4. Diagnose overfitting.
5. Handle class imbalance correctly.
6. Explain why accuracy is misleading for one dataset.

### Gate project
A documented end-to-end ML project:
- dataset card,
- baseline,
- experiment table,
- cross-validation,
- error analysis,
- final model,
- reproducible training script,
- inference API.

---

## Level 3 — Deep learning

### Learn
- perceptrons and MLPs
- activation functions
- backpropagation
- autograd
- optimizers
- initialization
- normalization
- regularization
- CNN concepts
- sequence models
- embeddings
- attention

### PyTorch skills
- tensors
- Dataset/DataLoader
- nn.Module
- training loops
- optimizers
- schedulers
- mixed precision concepts
- checkpointing
- inference mode

### Exercises
1. Implement a tiny neural network using NumPy only.
2. Rebuild it in PyTorch.
3. Write the training loop yourself before using high-level trainers.
4. Diagnose exploding/vanishing training behavior.
5. Perform ablation tests.
6. Track experiments and random seeds.

### Gate
Train and explain a nontrivial PyTorch model, including its failure modes.

---

## Level 4 — Transformers and NLP

### Learn
- tokenization
- embeddings
- positional information
- self-attention
- multi-head attention
- feed-forward blocks
- residual connections
- normalization
- encoder vs decoder
- causal masking
- pretraining objectives
- decoding strategies

### Exercises
1. Implement scaled dot-product attention.
2. Implement a minimal transformer block in PyTorch.
3. Train a tiny language model on a small corpus.
4. Compare greedy, temperature, top-k, and top-p decoding.
5. Inspect tokenizer behavior on code, Filipino text, numbers, and whitespace.
6. Explain KV-cache intuition.

### Gate
Give a 20-minute whiteboard explanation of a decoder-only transformer from tokens to next-token probabilities.

---

## Level 5 — LLM application engineering

### Learn
- provider APIs
- structured outputs
- function/tool calling
- streaming
- retries
- rate limits
- context management
- caching
- prompt/version management
- cost accounting
- deterministic boundaries
- safety and permissions

### Exercises
1. Implement provider abstraction across at least two model providers and one local model.
2. Build a structured-output validator and retry strategy.
3. Build a streaming endpoint.
4. Add token/cost/latency tracking.
5. Test malformed tool arguments and provider failures.

### Gate
A reliable LLM service with tests and telemetry, not merely a chat UI.

---

## Level 6 — Retrieval-Augmented Generation

### Learn
- ingestion
- parsing
- chunking
- metadata
- embeddings
- approximate nearest-neighbor search
- vector databases
- lexical/BM25 concepts
- hybrid search
- reranking
- query rewriting
- citations
- grounding
- retrieval evaluation

### Metrics
- Recall@K
- Precision@K
- MRR
- nDCG intuition
- answer correctness/groundedness
- abstention behavior

### Exercises
1. Compare 3 chunking strategies.
2. Compare semantic vs hybrid retrieval.
3. Evaluate different K values.
4. Add a reranker and measure whether it helps.
5. Build an adversarial set where retrieval should abstain.
6. Require citation/source IDs in final answers.

### Gate
A RAG system with a fixed eval set and a report showing measurable iteration.

---

## Level 7 — Agents and tool-using systems

### Learn
- agent loop
- tool schemas
- state
- planning
- routing
- memory
- checkpoints
- deterministic workflow vs agent
- planner/executor
- reflection/critique patterns
- multi-agent tradeoffs
- human approval
- tool permissions
- sandboxing
- prompt injection

### Framework literacy
Know at least one mainstream framework, but understand the primitives well enough to implement a small orchestrator yourself.

Suggested practical study:
- LangGraph
- Hugging Face Agents Course
- one provider-native agent SDK
- MCP

### Exercises
1. Build a router with deterministic tests.
2. Build planner → executor flow.
3. Add human approval to destructive tools.
4. Build a benchmark of 50 tool-use tasks.
5. Track tool-choice accuracy and argument validity.
6. Test prompt-injection attempts against tool permissions.

### Gate
An agent that has an evaluation suite and permission model.

---

## Level 8 — Fine-tuning and model adaptation

### Learn
- supervised fine-tuning
- instruction data
- PEFT
- LoRA/QLoRA
- quantization
- data quality
- catastrophic forgetting concepts
- preference optimization overview
- distillation concepts

### Exercises
1. Fine-tune a small model on a narrow task.
2. Create train/validation/test partitions.
3. Compare base and tuned models using the exact same eval set.
4. Document what got better and what regressed.
5. Compare fine-tuning with a prompt/RAG baseline.

### Gate
You can justify when fine-tuning is preferable to prompting or RAG.

---

## Level 9 — MLOps and production AI

### Learn
- experiment tracking
- model registry concepts
- dataset/version tracking
- reproducibility
- model serving
- batching
- GPU/CPU inference tradeoffs
- autoscaling concepts
- monitoring
- drift
- rollback
- canary deployment
- privacy
- security
- red-team testing
- cost/latency optimization

### Exercises
1. Reproduce a previous experiment from a clean machine/container.
2. Package inference in Docker.
3. Monitor latency, errors, and quality metrics.
4. create a rollback procedure.
5. run a simple load test.
6. create an incident postmortem for a simulated model regression.

### Gate
Deploy one model-backed service with operational documentation.

---

## Level 10 — Research literacy

### Practice
For one paper every 1–2 weeks:
1. state the research question,
2. identify the baseline,
3. identify the dataset,
4. identify the metric,
5. explain the method,
6. list assumptions,
7. list weaknesses,
8. reproduce a small part when feasible.

### Milestone
Reproduce one paper or strong open-source result closely enough to write a technical replication report.

---

# AI mastery evidence

Do not call yourself an AI expert because you can use an API.

Long-term evidence should include:
- classical ML project,
- PyTorch deep-learning project,
- transformer implementation exercise,
- production RAG system with evals,
- tool-using agent with evals,
- fine-tuning experiment,
- deployed model service,
- written technical analyses,
- ability to read papers and challenge methodology,
- ability to select simpler non-AI solutions when AI is unnecessary.
