# Hi, I’m Amir Firouz — Distributed Systems & AI Engineer (PhD)

I help teams take AI prototypes and data-heavy platforms to **production-grade Go and cloud architectures**.

I’ve shipped high-impact systems at **Microsoft, AWS, Property Finder, and DataGardens** – from Editor AI in Windows Photos (+20% MAU) and RDS SQL Server features, to subscription/credit platforms that cut support tickets by 50%+ and DR/HA platforms that made cutovers predictable instead of stressful.

Today I run **AandZ.tech**, an independent AI & cloud engineering practice based in the UAE, working with global clients on AI integration, distributed systems, and event-driven architectures.

---

## What I do

**Production AI & Platforms**

- Turn **Python/PoC AI pipelines** into **reliable Go/ cloud services** (GenAI, RAG, agents, vector search).
- Design and harden **event-driven systems** (CQRS, outbox, idempotent consumers, replayable projections).
- Make AI features **fast, observable, and affordable** (local-first where possible, cloud where it counts).

**Consulting & Architecture**

- Fractional **Principal Engineer / Architect** for teams scaling from MVP to “we need this to not fall over.”
- Architecture reviews for **fintech, marketplaces, and SaaS**: consistency, invariants, and scaling plans.
- Mentoring engineers on **microservices, observability, and AI integration**.

---

## Services (how I can help)

- **Fractional Principal Engineer (Go + Cloud)**
  - Design / review event-driven and microservices architectures.
  - Focus: scalability, fault tolerance, and clear service contracts.

- **RAG & Vector Search Optimization**
  - Fix latency / quality issues in **Qdrant / pgvector** pipelines.
  - Hybrid search (keyword + vector), re-ranking, and cost/latency tuning.

- **Python → Go Migration**
  - Rewrite or peel off hot paths from Python/Node backends into Go services.
  - Goal: higher concurrency, lower cloud spend, cleaner deployment story.

- **Agentic Systems & Orchestration**
  - Design **deterministic agent workflows** (plans, tools, state, observability).
  - Genkit / LangChainGo patterns, structured outputs, and guardrails.

If you’re a CTO, founder, or lead engineer wrestling with any of these, my repos below are essentially **reference architectures** for the conversations we’ll have.

---

## Reference architectures (open source)

### 🧮 Fintech Core: Credit Ledger (Go + Kafka + Postgres)
**Repo:** `github.com/amirhf/creditLedger` • **Story:** [From Spreadsheet Chaos to Reliable Credits](https://medium.com/@amirhosseinfirouzmanesh/from-spreadsheet-chaos-to-reliable-credits-ca8fe19fbdb7)

A production-ready **reference architecture** for handling high-volume financial credits and balances. It replaces fragile "credits column" designs with an immutable, double-entry ledger that guarantees auditability.

* **Event-Driven Integrity:** Implements the **Transactional Outbox** pattern and idempotent consumers to ensure consistency across microservices without dual-write hazards.
* **CQRS & Scalability:** Decouples write logic from read patterns using **CQRS projections**, allowing for high-throughput ingestion and replayable read models.
* **Full Observability:** Pre-wired with **Jaeger and Grafana** to trace "what happened to my credit?" journeys and monitor consumer lag/latency.

**Use it as a blueprint for:** SaaS credits, marketplace wallets, usage-based billing, and loyalty point systems.

---

### 🛍️ Retail AI: Polyglot Search & Feature Router
**Repo:** `github.com/amirhf/imageSearch`

A high-concurrency **Retail Discovery Engine** combining **Go** for search orchestration and **Python** for ML inference.

- **Polyglot Architecture**: Uses **Go** on the hot path (search/fusion) for sub-100ms latency and **Python** for the rich ML ecosystem (CLIP/BLIP).
- **Hybrid Search**: Merges **Dense Vectors** (Qdrant) and **Sparse Keywords** via Reciprocal Rank Fusion (RRF) to solve the "zero results" problem in e-commerce.
- **AI Feature Router**: A "circuit breaker for intelligence" that cuts cloud costs by ~90% by dynamically routing requests to local quantized models before falling back to cloud APIs.
- **SaaS Scalability**: Features built-in **multi-tenancy**, **Shadow Mode** for safe migration validation, and full OpenTelemetry instrumentation.

Use it as a reference for: **e-commerce discovery**, hybrid search implementation, and **migrating Python prototypes to Go** systems.

---


### 🧠 Agentic Workflow Orchestrator: Learning Path Designer
**Repo:** `github.com/amirhf/learningPathDesigner`

A production-ready **reference architecture** for building deterministic AI agents in a distributed system. It replaces fragile "chatbots" with a structured planner-executor workflow grounded in domain data.

* **Planner–Executor Pattern:** Implements a multi-stage agentic workflow where a Planner proposes the learning path and an Executor decomposes it into concrete steps with verified resources.
* **Structured Outputs:** Solves non-deterministic LLM behavior by enforcing strict JSON schemas for all plans and quizzes, ensuring reliability for the UI.
* **Advanced RAG & Re-ranking:** Features a production-grade retrieval pipeline using **Qdrant** (hybrid search) and **Postgres** to ground AI responses in real documentation.
* **Polyglot Microservices:** Demonstrates a scalable layout: **Go Gateway** (orchestration & auth) managing **Python** AI services, ensuring distinct separation of concerns.

**Use it as a blueprint for:** Building robust internal training platforms, onboarding copilots, and domain-specific certification agents.

---

## Tools & stacks I like

`Go` · `Python` · `TypeScript / React / Next.js`  
`FastAPI` · `Postgres` · `MySQL` · `SQL Server` · `MongoDB`  
`Qdrant` · `pgvector` · `Kafka / Redpanda` · `RabbitMQ`  
`AWS` (Kinesis, Glue, Athena, Step Functions, RDS, S3) · `Azure`  
`Docker` · `Kubernetes` · `Grafana` · `Prometheus` · `Jaeger` · `App Insights`

---

## Work with me

- 🌍 Based in **Dubai (UTC+4)** — working **remote / global**.
- 🧩 Ideal fit: teams that **already have users and data**, and now need their AI / platform to be **reliable, observable, and scalable**.
- ✉️ Best way to reach me: check my email / links in the sidebar or visit **AandZ.tech**.

If one of my reference architectures looks close to what you’re building, that’s usually the fastest way for us to start a concrete conversation.
