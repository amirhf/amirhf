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

### 🧮 Credit Ledger — Fintech core / double-entry system  
**Repo:** `github.com/amirhf/creditLedger`  
Event-driven, double-entry ledger for subscription and credit platforms. Includes:

- CQRS-style write/read separation with replayable projections.
- Transactional outbox and idempotent consumers for safe, at-least-once processing.
- Distributed tracing and metrics via Jaeger/Grafana for “what happened to this credit?” journeys.

Use it as a blueprint for: **wallets, balances, credits/usage, and subscription billing systems.**

---

### 🖼️ AI Image Search / Feature Router — Multimodal search engine
**Repo:** `github.com/amirhf/imageSearch`

Local-first **captioning & embeddings** with a **scalable Go microservice** for high-throughput hybrid search. Provides:

- **Polyglot Architecture**: Python (FastAPI) for AI/Write paths + Go for high-performance Read paths.
- **Hybrid Search**: Combines **Dense Retrieval** (OpenCLIP) and **Sparse Retrieval** (FTS) using `pgvector` and `pgx`.
- **Production Engineering**: Features **Shadow Mode** for safe backend migration, **Load Testing** (Locust), and **Policy Routing** (Local vs Cloud).

Use it as a reference for **scalable e-commerce discovery**, internal media search, or any “find similar content” feature requiring high concurrency.

---

### 📚 Learning Path Designer — RAG + agent orchestration  
**Repo:** `github.com/amirhf/learningPathDesigner`  

RAG + agents demo that assembles grounded learning paths and quizzes:

- Next.js frontend with a Go gateway and Python/FastAPI services.
- Qdrant for vectors, Postgres for metadata, with migrations/seeders and Docker Compose for easy spin-up.
- Patterns for **multi-step reasoning, structured outputs, and tool orchestration**.

Use it as a template for **agentic workflows**: training, onboarding, or domain-specific copilots.

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
