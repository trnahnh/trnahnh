<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=1A1210,2A1F18,E8541A,141210&height=200&section=header&text=Anh%20(Andre)%20Tran&fontSize=60&fontColor=E8E0D0&fontAlignY=35&desc=Systems%20Engineer%20%E2%80%94%20Writing%20Code%20That%20Mass%20Produces%20Money&descAlignY=55&descSize=18&animation=fadeIn" />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3500&pause=800&color=E8541A&center=true&vCenter=true&multiline=false&width=700&lines=Low-Latency+Infrastructure+Engineer;Matching+Engine+%26+HFT+Systems+Developer;AI+%2F+ML+Research+%26+Infrastructure;Quantitative+Finance+%26+Big+Tech+Candidate;Platform+Engineering+%26+Kubernetes;Building+Engines%2C+Not+Apps)](https://git.io/typing-svg)

<br/>

![University](https://img.shields.io/badge/University%20of%20Cincinnati-Computer%20Engineering-E8541A?style=for-the-badge&logo=academia&logoColor=E8E0D0)
![GPA](https://img.shields.io/badge/GPA-3.77%20%2F%204.0-2A1F18?style=for-the-badge&logo=bookstack&logoColor=E8E0D0)
![Location](https://img.shields.io/badge/Cincinnati%2C%20Ohio-United%20States-1A1210?style=for-the-badge&logo=googlemaps&logoColor=E8E0D0)

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-anhdtrn.com-E8541A?style=for-the-badge&logo=firefox&logoColor=E8E0D0)](https://anhdtrn.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anhdtran11/)
[![Email](https://img.shields.io/badge/Email-Contact-E8541A?style=for-the-badge&logo=gmail&logoColor=E8E0D0)](mailto:anhdtran.forwork@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/trnahnh)

<br/>

![Profile Views](https://komarev.com/ghpvc/?username=trnahnh&color=E8541A&style=for-the-badge&label=PROFILE+VIEWS)
![GitHub Followers](https://img.shields.io/github/followers/trnahnh?style=for-the-badge&color=2A1F18&logo=github&label=FOLLOWERS&logoColor=E8E0D0)
![GitHub Stars](https://img.shields.io/github/stars/trnahnh?style=for-the-badge&color=1A1210&logo=github&label=STARS&logoColor=E8E0D0)

</div>

---

<div align="center">

## About

</div>

```
I build systems that operate at the edge of what hardware allows.

My work lives in the space between nanoseconds and profit — low-latency matching engines,
platform engineering on Kubernetes, AI research infrastructure, and real-time systems
designed to handle production load without flinching. I treat performance as a feature,
not an afterthought.

Currently studying Computer Engineering at the University of Cincinnati (3.77 GPA),
doing AI research in Dr. Novak's lab on TruVox, and targeting quantitative finance,
AI/ML, and big tech firms for Summer 2027 co-op. My background spans systems programming
in Rust and Go, Kubernetes platform engineering with Istio and ArgoCD, ML pipelines,
and full-stack product engineering across multiple deployed applications.

I don't build apps. I build engines.
```

<div align="center">

**Open To:** Summer 2027 Co-op · Quant Finance Internships · AI/ML Research · Big Tech SWE Roles · Systems & Platform Engineering

</div>

---

<div align="center">

## Tech Stack

</div>

<div align="center">

### Languages

[![Skill Icons](https://skillicons.dev/icons?i=rust,go,cpp,c,python,typescript,javascript,java&theme=dark)](https://skillicons.dev)

### Frontend

[![Skill Icons](https://skillicons.dev/icons?i=react,nextjs,vue,nuxt,tailwind,html,css&theme=dark)](https://skillicons.dev)

### Backend & Databases

[![Skill Icons](https://skillicons.dev/icons?i=nodejs,fastapi,spring,postgres,redis,mongodb,sqlite,kafka&theme=dark)](https://skillicons.dev)

### Cloud, DevOps & Tooling

[![Skill Icons](https://skillicons.dev/icons?i=aws,docker,kubernetes,terraform,nginx,githubactions,linux,git&theme=dark)](https://skillicons.dev)

### Observability & ML

[![Skill Icons](https://skillicons.dev/icons?i=grafana,prometheus&theme=dark)](https://skillicons.dev)

</div>

---

<div align="center">

## Featured Projects

</div>

<details>
<summary><b>Kiln-IDP — Internal Developer Platform</b></summary>

<br/>

A Kubernetes-native internal developer platform that replaces ticket-and-Terraform provisioning with self-service infrastructure. Features a custom scheduler plugin, a statistically rigorous canary controller, and a fail-closed policy gate integrating 6 subsystems behind one unified path. Placed zero latency-class workloads on spot capacity, validated across 57,012 replayed placements on a 12,477-machine public cluster trace.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Go, Java (Spring Boot), Kubernetes, ArgoCD, Istio, Kafka, PostgreSQL, OpenTelemetry |
| **Cost** | 45.5% cluster spend reduction with zero SLA violations via custom Kubernetes scheduler plugin |
| **Canary** | Wald sequential probability ratio test + cumulative CUSUM · 100% regression detection at 2.8% false-rollback rate on live Istio mesh |
| **Provisioning** | Self-service path reaching Ready at 11s p50 · Replaced hours-to-day ticket-and-Terraform flow |
| **Safety** | Fail-closed policy gate integrating 6 subsystems |
| **Seeded Tests** | Caught 100% of 1,000 seeded regressions |
| **Controller** | Lifted controller-runtime 20qps/30burst limit · Cut 12-min timeout to 3m58s |
| **Repository** | [github.com/trnahnh/kiln-idp](https://github.com/trnahnh/kiln-idp) |

</div>

The custom scheduler plugin bin-packs workloads against real utilization metrics rather than requests, reclaiming stranded capacity without violating availability guarantees. The canary controller combines a Wald SPRT for early stopping with a CUSUM chart for detecting gradual drift, running on live Istio traffic splits. Provisioning collapses namespace creation, RBAC binding, secret injection, Kafka topic creation, database provisioning, and ArgoCD application registration into a single declarative request.

<br/>

</details>

---

<details>
<summary><b>Commma — Developer Activity Tracker</b></summary>

<br/>

A full-stack developer activity platform turning the editor into a logbook — pace, splits, streaks, and leaderboards as rituals of a real sport, applied to code. A VSCode/Open VSX extension captures editor activity in real time; a Hono API ingests and aggregates sessions; a React web app surfaces session detail, streaks, leaderboards, and shareable keyboard heatmap cards. Live at 100% availability over 30 days with 600+ downloads.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | TypeScript, React 19, Vite, Tailwind v4, Hono, Node.js, PostgreSQL, Redis |
| **Extension** | VSCode + Open VSX · Key-label tracking · Three privacy modes · Offline queue |
| **Privacy** | Keys-only guarantee at two layers · Extension never reads editor content · API re-derives privacy mode from Redis-cached lookup |
| **Performance** | p50 latency cut from 42ms to 13ms · Load-tested to 271K events / 4,447 sessions with zero 5xx |
| **Cost** | Replaced BullMQ/Redis with interval scanner · Redis commands near 0 against 500K/mo budget cap |
| **Auth** | GitHub OAuth · JWT access tokens · HTTP-only rotating refresh tokens |
| **Billing** | Stripe Pro/Team subscriptions · Signature-verified webhooks |
| **Deployment** | EC2 t4g (Graviton) + PM2 · S3 + CloudFront · Neon PostgreSQL · Upstash Redis · Terraform |
| **Live** | [commma.dev](https://commma.dev) |

</div>

The extension captures key labels — never key content — across three configurable privacy modes. The API aggregates raw events into session records with pace, line delta, and per-language breakdowns. The Canvas heatmap layer renders per-session key frequency as a transparent PNG exportable in three aspect ratios (9:16, 1:1, 16:9) for social sharing. Load testing traced a local connection-pool win that didn't reproduce in prod to client bandwidth, not the server.

<br/>

</details>

---

<details>
<summary><b>Ferrox — Order Matching Engine</b></summary>

<br/>

A production-grade central limit order book matching engine written in Rust, architected for sub-microsecond execution in high-frequency trading environments. Designed around zero-cost abstractions, lock-free concurrency primitives, and memory-mapped persistence with crash recovery guarantees. Deployed as a containerized service on AWS Fargate.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Rust, C++, Atomics, mmap WAL, Criterion, HdrHistogram |
| **Scale** | 4.7M orders/second sustained throughput |
| **Performance** | 500ns P99 tick-to-trade latency · Zero hot-path heap allocations |
| **Memory** | 1M-slot pre-allocated arena · Fixed-point prices · HashMap-to-BTreeMap swap trading 9-22% insert regression for 67-85% cancel latency cut |
| **Concurrency** | Lock-free SPSC ring buffer · Acquire/Release over SeqCst to avoid unnecessary fence instructions · 64B cache-line padding · 8.8x throughput gain over std::sync::mpsc |
| **C++ Port** | Ported lock-free ring buffer to C++20 · Acquire/Release elides all x86 fences vs 5.4-6.0x SeqCst penalty · Isolated Rust's 1.5-3.5x single-threaded gap to runtime bounds-check overhead |
| **Reliability** | mmap write-ahead log · Crash recovery under 1.4ms · Crash-consistency fault injection zeroing 714 failures across 92,525 records · Fixed 2 silent-corruption bugs |
| **Deployment** | AWS Fargate · NLB at 70% of total hourly cost |
| **Repository** | [github.com/trnahnh/ferrox](https://github.com/trnahnh/ferrox) |

</div>

Built to match or exceed the performance profile of institutional-grade matching engines. The design eliminates all dynamic memory allocation on the critical execution path, using a pre-allocated arena and stack-pinned message passing throughout. Ported the lock-free ring buffer to C++20, confirming Acquire/Release elides all x86 fences versus a 5.4-6.0x SeqCst penalty, then isolated Rust's 1.5-3.5x single-threaded gap to its runtime bounds-check overhead. Fixed two silent-corruption bugs via crash-consistency fault injection, zeroing 714 failures across 92,525 records. The WAL layer guarantees durability without sacrificing microsecond-level recovery windows, verified end-to-end via HdrHistogram latency measurement under Criterion benchmarks.

<br/>

</details>

---

<details>
<summary><b>Draft-Thinker — Cost-Aware LLM Gateway</b></summary>

<br/>

A high-performance LLM routing gateway written in Go that cuts inference costs by 82.9% (bootstrapped 95% CI: 79.6–86.0%) while holding accuracy at 98.1%. Routes requests dynamically using a machine learning entropy router built on top-k logprobs from the OpenAI API, executes speculative drafts via goroutines, and serves repeated semantic queries from a vector-backed cache layer under 50ms.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Go, OpenAI API, Qdrant, Redis, Prometheus, Grafana, Docker |
| **Cost Reduction** | 82.9% inference cost savings (bootstrapped 95% CI: 79.6–86.0%) |
| **Routing** | Machine learning entropy router using top-k logprobs from OpenAI API |
| **Accuracy** | 98.1% on benchmark |
| **Diagnosis** | Identified confidence-threshold baseline ceiling at 61.5% from OpenAI logprob-reporting artifact affecting 65.5% of creative prompts — entropy routing structurally avoids this |
| **Speculative Execution** | Found cancelled speculative calls would cost 80-88% of the all-heavyweight bill · Recommending speculation stay off |
| **Cache** | Vector search + TTL eviction · Cosine similarity ≥ 0.95 · Sub-50ms cache hits |
| **Observability** | Prometheus metrics · Grafana dashboards |
| **Repository** | [github.com/trnahnh/draft-thinker](https://github.com/trnahnh/draft-thinker) |

</div>

The entropy router evaluates token-level confidence distributions from the drafter model before deciding whether to escalate to a capable and expensive model. Diagnosed why a confidence-threshold baseline plateaus at a 61.5% cost-reduction ceiling from an OpenAI logprob-reporting artifact affecting 65.5% of creative prompts, which entropy routing structurally avoids. Full observability via Prometheus and Grafana covers routing decisions, cache hit rates, and per-model cost attribution.

<br/>

</details>

---

<details>
<summary><b>Inyeon — Agentic AI Git Assistant</b></summary>

<br/>

A multi-agent AI assistant for software engineering workflows, built on a LangGraph orchestration backbone with a FastAPI runtime and ChromaDB vector memory. Handles the full spectrum of developer requests through a 7-agent pipeline with 100ms median response time and 100% test coverage across 245+ cases.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Python, FastAPI, LangGraph, ChromaDB, scikit-learn, NumPy, Typer |
| **Architecture** | 7-agent orchestration pipeline with cost-optimized caching and short-circuiting |
| **Performance** | 100ms median response latency |
| **Test Coverage** | 245+ test cases · 100% unit and integration branch coverage |
| **Build Speed** | 95% Docker build time reduction (49s → 2.1s) |
| **Memory** | RAG-powered ChromaDB across 4 clustering strategies via scikit-learn |
| **Repository** | [github.com/trnahnh/inyeon](https://github.com/trnahnh/inyeon) |

</div>

Each agent in the pipeline is scoped to a discrete responsibility: intent classification, repository context retrieval, code analysis, diff generation, review synthesis, test suggestion, and response formatting. LangGraph manages state transitions and conditional routing between agents, enabling complex multi-hop workflows without brittle prompt chaining.

<br/>

</details>

---

<details>
<summary><b>KatanaID — AI Branding Toolkit</b></summary>

<br/>

A production-deployed AI branding platform written in Go, generating brand identities through high-concurrency API orchestration. Integrates Google Gemini AI for creative generation with a trust score engine and browser fingerprinting for session security, delivering complete brand packages under 200ms via concurrent goroutine execution. Validated under 2,300+ requests/day via k6 stress testing.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Go, React, Gemini AI, Ent ORM, PostgreSQL, goroutines, Railway, Vercel |
| **Concurrency** | 19+ parallel API calls per request via goroutine fan-out |
| **Performance** | Sub-200ms response times · 2,300+ requests/day in production |
| **Security** | Trust score engine · Browser fingerprinting · k6 stress tested |
| **Data Layer** | Ent ORM type-safe PostgreSQL · Zero schema-related runtime errors |
| **Deployment** | Production · [katanaid.com](https://katanaid.com) |

</div>

The fan-out architecture dispatches all generative API calls simultaneously at request ingestion, collapsing serial latency chains into a single parallel wait window. Trust scoring evaluates session signals in real time, gating generation behind lightweight anomaly detection before touching paid API quota. Ent ORM enforces strict type safety on the PostgreSQL layer, enabling reliable large-scale brand data synchronization across distributed API sources.

<br/>

</details>

---

<details>
<summary><b>Caphne — Real-Time Study Matching Platform</b></summary>

<br/>

A real-time peer study matching platform serving 400+ active users at FPT University, built on a Socket.IO event bus with PostgreSQL persistence and Redis caching. Engineered to sustain 1,700+ requests per minute under concurrent session load.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Nuxt 3, Vue 3, shadcn-vue, Tailwind, Express.js, Socket.IO, PostgreSQL, Drizzle ORM, Redis |
| **Scale** | 1,700+ requests/minute · 400+ active users · 30 days production traffic |
| **Performance** | API response time cut from 60s to 10s · Socket.IO scoped to per-match rooms |
| **Match Supply** | Deleted two speculative DB tables · Raised daily match supply 7x (3/3hr → 20/day) |
| **Infra** | EC2, CloudFront, S3, Route 53 via Terraform · OIDC-federated credentials |
| **Incidents** | Root-caused and fixed 2 production incidents same-day from raw error output |
| **Auth** | JWT · OAuth 2.0 · Typebox schema validation |
| **Deployment** | Production · [caphne.co](https://caphne.co) |

</div>

The Redis layer serves presence state and match candidates from memory, keeping the hot path away from PostgreSQL except for durable writes. Socket.IO manages bidirectional session state across the matching lifecycle, from availability broadcast through confirmation handshake to session teardown. Led 6 engineers through sprint planning and code reviews across the full product lifecycle.

<br/>

</details>

---

<details>
<summary><b>Dasi — End-to-End Encrypted Journal</b></summary>

<br/>

A privacy-first journaling application with end-to-end encryption — thoughts are encrypted on-device before leaving the client, ensuring the server never has access to plaintext content. Daily writing prompts eliminate the blank-page problem and drive consistent engagement.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Go, Chi, PostgreSQL, React, TypeScript, AWS Lambda, Resend |
| **Security** | On-device encryption before sync · Server sees only ciphertext |
| **Infrastructure** | AWS Lambda serverless compute |
| **Notifications** | Resend transactional email for daily prompts |
| **Repository** | [github.com/NauriFive/dasi-encrypted-journal](https://github.com/NauriFive/dasi-encrypted-journal) |

</div>

The encryption model ensures that even a full database compromise exposes no user content — all plaintext remains on the client. The daily prompt system is designed to reduce activation energy for writing, routing prompts through Resend at scheduled intervals to nudge users back into the habit loop.

<br/>

</details>

---

<details>
<summary><b>AnyuDock — S3 File Storage & Config Sharing</b></summary>

<br/>

A brutalist-by-design S3 file storage platform for sharing files and environment configs between machines. Private by default, public on demand — files stay locked to the owner until explicitly toggled, with share links available for public files only.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Hono, Bun, Drizzle ORM, PostgreSQL, React, TanStack Router/Query, Tailwind, Vite |
| **Storage** | Any S3-compatible provider · Privacy toggle per file · Share link generation |
| **Auth** | Email OTP via Resend · JWT session cookies |
| **API** | File upload, list, preview, download, privacy toggle, share links |
| **Deployment** | Production · [anyudock.cloud](https://anyudock.cloud) |
| **Repository** | [github.com/NauriFive/anyudock](https://github.com/NauriFive/anyudock) |

</div>

Files are private by default on upload — private files are owner-only for preview and management, while public files are downloadable by anyone with the file ID. Share links are generated only for public files, keeping accidental exposure impossible by design.

<br/>

</details>

---

<div align="center">

## Experience

</div>

**AI Researcher** · *University of Cincinnati Department of Computer Science*
`Aug 2026 – Present · Cincinnati, OH`

Building AI-driven voice modification and exercise-recommendation modules (e.g., PerMod) in Dr. Novak's lab for TruVox, a gender-affirming voice training platform, alongside its deployment infrastructure.

- Achieved 15x voice-resynthesis speedup (5.5s → 0.36s) via LPC pole-warping and LP-PSOLA
- Fixed an LPC stability bug by adding a Schur-Cohn test, preventing unstable filter coefficients
- Found 3 measurement bugs in the existing evaluation pipeline

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![AI/ML](https://img.shields.io/badge/AI%2FML-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)

---

**Founder & CTO** · *Commma* · [commma.dev](https://commma.dev) · [LinkedIn](https://www.linkedin.com/company/commma-dev/)
`May 2026 – Present · Cincinnati, OH`

Building commma.dev end-to-end — a TypeScript monorepo spanning a VSCode/Open VSX extension, a Hono/Postgres API, and a React SPA — live on AWS at 100% availability over 30 days with 600+ downloads.

- Built the VSCode extension with key-label tracking, three configurable privacy modes, and an offline queue for resilient event delivery
- Replaced BullMQ/Redis with an interval scanner, holding Redis commands near 0 against a 500K/mo budget cap
- Enforced a keys-only privacy guarantee at two layers: extension never reads editor content, API re-derives privacy mode from a Redis-cached lookup, cutting p50 latency from 42ms to 13ms
- Load-tested the live stack to 271K events / 4,447 sessions with zero 5xx, then traced a local connection-pool win that didn't reproduce in prod to client bandwidth, not the server
- Deployed on EC2 t4g (Graviton) with PM2, S3 + CloudFront for the web layer, Neon PostgreSQL, Upstash Redis, and Terraform for infra-as-code with S3-locked remote state

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Hono](https://img.shields.io/badge/Hono-E36002?style=flat-square&logo=hono&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)

---

**Lead Software Engineer** · *Caphne*
`Jan 2026 – Aug 2026 · Remote`

Led a cross-functional team of 6 engineers through sprint planning, code review, and production deploys of a full-stack study matching platform scaling to 400+ active users.

- Cut API response time from 60s to 10s by engineering a distributed, real-time chat system with Socket.IO scoped to per-match rooms, sustaining 1.7K+ requests/minute over 30 days in production
- Architected AWS infrastructure as code (EC2, CloudFront, S3, Route 53) via Terraform with OIDC-federated credentials, then root-caused and fixed 2 production incidents same-day from raw error output
- Deleted two speculative database tables from match rate-limiting, raising daily match supply 7x (3/3hr to 20/day)

![Nuxt](https://img.shields.io/badge/Nuxt-00DC82?style=flat-square&logo=nuxtdotjs&logoColor=white)
![Vue](https://img.shields.io/badge/Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=flat-square&logo=socketdotio&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)

---

**Founding Engineer** · *KatanaID*
`Dec 2025 – Present · Remote`

Co-founding and leading 5 engineers to architect a scalable AI branding intelligence platform in Go, from initial design through production deployment and ongoing operations.

- Architected a scalable end-to-end branding intelligence backend in Go, leveraging goroutines to orchestrate 19+ external API calls for real-time asset aggregation and PDF generation
- Sustained 2,300+ requests/day under production load, validated via k6 stress testing, by integrating Google Gemini AI for brand asset generation alongside a trust score engine with browser fingerprinting
- Eliminated schema-related runtime errors by leveraging Ent ORM for a strictly type-safe PostgreSQL layer, enabling reliable large-scale brand data synchronization across distributed API sources

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Gemini](https://img.shields.io/badge/Gemini%20AI-4285F4?style=flat-square&logo=google&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

**Technical Assistant Intern** · *Vietcombank*
`May 2025 – Jul 2025 · Hue, Vietnam`

Maintained banking infrastructure reliability and drove digital adoption across branch operations over a 3-month engagement.

- Maintained 99% uptime across 30+ networked branch systems by diagnosing hardware, network, and software faults in coordination with IT teams
- Reduced monthly in-branch transactions by 15% by onboarding 100+ customers biweekly onto digital banking services including mobile app setup, online payments, and account management workflows

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Networking](https://img.shields.io/badge/Networking-0078D4?style=flat-square&logo=cisco&logoColor=white)

---

<div align="center">

## Achievements

</div>

<div align="center">

| Recognition | Details |
|:---:|:---|
| GPA Honor Roll | 3.77 / 4.0 · University of Cincinnati · Computer Engineering |
| AI Research | Researcher in Dr. Novak's lab · TruVox · 15x voice-resynthesis speedup (5.5s → 0.36s) |
| Production Deployment | Commma — live at commma.dev · 100% availability over 30 days · 600+ downloads · 271K events load-tested |
| Production Deployment | KatanaID — 2,300+ req/day · AI branding platform · 5-engineer team |
| Production Deployment | Caphne — 400+ users · 1,700+ req/min · FPT University network |
| Platform Engineering | Kiln-IDP — 45.5% cluster spend reduction · 11s p50 provisioning · 100% regression detection · 57,012 replayed placements validated |
| LLM Cost Engineering | 82.9% inference cost reduction · 98.1% accuracy · Bootstrapped 95% CI |
| Systems Performance | 500ns P99 matching engine latency · 4.7M orders/sec · 8.8x throughput gain · C++20 port confirming 5.4-6.0x SeqCst penalty · 714 fault-injection failures zeroed |
| Full Test Coverage | 245+ test cases · 100% branch coverage · 95% Docker build time reduction |
| Team Leadership | Led 6-engineer team (Caphne) · 5-engineer team (KatanaID) |

</div>

---

<div align="center">

## GitHub Analytics

</div>

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=trnahnh&show_icons=true&theme=gruvbox&hide_border=true&bg_color=141210&title_color=E8541A&icon_color=E8541A&text_color=E8E0D0"/>
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=trnahnh&layout=compact&langs_count=8&theme=gruvbox&hide_border=true&bg_color=141210&title_color=E8541A&text_color=E8E0D0"/>

</div>

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com/?user=trnahnh&theme=dark&hide_border=true&background=141210&stroke=E8541A&ring=E8541A&fire=E8E0D0&currStreakNum=E8E0D0&sideNums=E8E0D0&currStreakLabel=E8541A&sideLabels=E8541A&dates=888888"/>

</div>

---

<div align="center">

## Connect

</div>

<div align="center">

[![Gmail](https://img.shields.io/badge/Gmail-anhdtran.forwork%40gmail.com-E8541A?style=for-the-badge&logo=gmail&logoColor=E8E0D0)](mailto:anhdtran.forwork@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-anhdtran11-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anhdtran11/)
[![GitHub](https://img.shields.io/badge/GitHub-trnahnh-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/trnahnh)
[![Portfolio](https://img.shields.io/badge/Portfolio-anhdtrn.com-E8541A?style=for-the-badge&logo=firefox&logoColor=E8E0D0)](https://anhdtrn.com)

</div>

---

<div align="center">

*The bottleneck is never the algorithm. It's the engineer who stops measuring.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=141210,2A1F18,E8541A,1A1210&height=120&section=footer&animation=fadeIn" />

</div>
