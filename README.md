<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=1A1210,2A1F18,E8541A,141210&height=200&section=header&text=Anh%20Tran&fontSize=60&fontColor=E8E0D0&fontAlignY=35&desc=Systems%20Engineer%20%E2%80%94%20Writing%20Code%20That%20Mass%20Produces%20Money&descAlignY=55&descSize=18&animation=fadeIn" />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3500&pause=800&color=E8541A&center=true&vCenter=true&multiline=false&width=700&lines=Low-Latency+Infrastructure+Engineer;Matching+Engine+%26+HFT+Systems+Developer;AI+%2F+ML+Pipeline+Architect;Quantitative+Finance+%26+Big+Tech+Candidate;Building+Engines%2C+Not+Apps)](https://git.io/typing-svg)

<br/>

![University](https://img.shields.io/badge/University%20of%20Cincinnati-Computer%20Engineering-E8541A?style=for-the-badge&logo=academia&logoColor=E8E0D0)
![GPA](https://img.shields.io/badge/GPA-3.71%20%2F%204.0-2A1F18?style=for-the-badge&logo=bookstack&logoColor=E8E0D0)
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
AI inference pipelines, and real-time infrastructure designed to handle production load
without flinching. I treat performance as a feature, not an afterthought.

Currently studying Computer Engineering at the University of Cincinnati (3.71 GPA),
targeting quantitative finance and big tech firms for Fall 2026 co-op. My background
spans systems programming in Rust and Go, ML pipelines with XGBoost and LangGraph,
and full-stack product engineering across multiple deployed applications.

I don't build apps. I build engines.
```

<div align="center">

**Open To:** Fall 2026 Co-op · Quant Finance Internships · Big Tech SWE Roles · Systems Engineering · ML Infrastructure

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

[![Skill Icons](https://skillicons.dev/icons?i=nodejs,bun,fastapi,spring,postgres,redis,mongodb,sqlite&theme=dark)](https://skillicons.dev)

### Cloud, DevOps & Tooling

[![Skill Icons](https://skillicons.dev/icons?i=aws,docker,nginx,githubactions,linux,git,vscode,vim&theme=dark)](https://skillicons.dev)

</div>

---

<div align="center">

## Featured Projects

</div>

<details>
<summary><b>Commma — Developer Activity Tracker</b></summary>

<br/>

A full-stack developer activity platform turning the editor into a logbook — pace, splits, streaks, and leaderboards as rituals of a real sport, applied to code. A VSCode extension captures editor activity in real time; a Hono API ingests and aggregates sessions; a React web app surfaces session detail, streaks, leaderboards, and shareable keyboard heatmap cards.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | TypeScript, React 19, Vite, Tailwind v4, Hono, Node.js, PostgreSQL, Redis |
| **Extension** | VSCode API · Key-label tracking · Privacy modes · Offline queue |
| **Performance** | Sub-second session ingestion · Redis sorted sets for leaderboard queries |
| **Auth** | GitHub OAuth · JWT access tokens · HTTP-only rotating refresh tokens |
| **Billing** | Stripe Pro/Team subscriptions · Signature-verified webhooks |
| **Deployment** | EC2 t4g (Graviton) + PM2 · S3 + CloudFront · Neon PostgreSQL · Upstash Redis · Terraform |
| **Repository** | [github.com/NauriFive/commma-coding-progress-tracker](https://github.com/NauriFive/commma-coding-progress-tracker) |
| **Live** | [commma.dev](https://commma.dev) |

</div>

The extension captures key labels — never key content — across three configurable privacy modes. The API aggregates raw events into session records with pace, line delta, and per-language breakdowns. The Canvas heatmap layer renders per-session key frequency as a transparent PNG exportable in three aspect ratios (9:16, 1:1, 16:9) for social sharing. Redis sorted sets back real-time weekly, monthly, and all-time leaderboards filterable by language.

<br/>

</details>

---

<details>
<summary><b>Ferrox — Order Matching Engine</b></summary>

<br/>

A production-grade central limit order book matching engine written in Rust, architected for sub-microsecond execution in high-frequency trading environments. Designed around zero-cost abstractions, lock-free concurrency primitives, and memory-mapped persistence with crash recovery guarantees.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Rust, Atomics, mmap WAL, Criterion, HdrHistogram |
| **Scale** | 4.7M orders/second sustained throughput |
| **Performance** | 500ns P99 tick-to-trade latency · Zero hot-path heap allocations |
| **Memory** | 1M-slot pre-allocated arena · Doubly linked list order book |
| **Concurrency** | Lock-free SPSC ring buffer · Acquire/Release memory ordering · 64B cache-line padding |
| **Reliability** | mmap write-ahead log · Crash recovery under 1.4ms |
| **Throughput Gain** | 8.8x improvement from lock-free SPSC design |
| **Repository** | [github.com/trnahnh/ferrox](https://github.com/trnahnh/ferrox) |

</div>

Built to match or exceed the performance profile of institutional-grade matching engines. The design eliminates all dynamic memory allocation on the critical execution path, using a pre-allocated arena and stack-pinned message passing throughout. The WAL layer guarantees durability without sacrificing microsecond-level recovery windows, verified end-to-end via HdrHistogram latency measurement under Criterion benchmarks.

<br/>

</details>

---

<details>
<summary><b>Draft-Thinker — Cost-Aware LLM Gateway</b></summary>

<br/>

A high-performance LLM routing gateway written in Go that cuts inference costs by 91.6% without degrading output quality. Routes requests dynamically using real-time Shannon entropy analysis of token logprobabilities, executes speculative drafts via goroutines, and serves repeated semantic queries from a vector-backed cache layer under 50ms.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Go, OpenAI API, Qdrant, Redis, Prometheus, Grafana, Docker |
| **Cost Reduction** | 91.6% inference cost savings · 94% of requests handled by drafter model |
| **Routing** | Real-time Shannon entropy analysis of token logprobabilities |
| **Accuracy** | 98.2% accuracy on 518-prompt benchmark |
| **Cache** | Vector search + TTL eviction · Cosine similarity ≥ 0.95 · Sub-50ms cache hits |
| **Observability** | Prometheus metrics · Grafana dashboards |
| **Repository** | [github.com/trnahnh/draft-thinker](https://github.com/trnahnh/draft-thinker) |

</div>

The entropy router evaluates token-level confidence distributions from the drafter model before deciding whether to escalate to a capable and expensive model. The semantic cache layer uses vector search to detect repeated queries above a cosine similarity threshold, eliminating redundant inference on cache-accepted responses entirely. Full observability via Prometheus and Grafana covers routing decisions, cache hit rates, and per-model cost attribution.

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

A real-time peer study matching platform serving 400+ active users at FPT University, built on a Socket.IO event bus with PostgreSQL persistence and Redis caching. Engineered to sustain 1,700+ requests per minute under concurrent session load with p50 response times under 400ms.

<div align="center">

| Attribute | Detail |
|:---|:---|
| **Stack** | Nuxt 3, Vue 3, shadcn-vue, Tailwind, Express.js, Socket.IO, PostgreSQL, Drizzle ORM, Redis |
| **Scale** | 1,700+ requests/minute · 400+ active users · 30 days production traffic |
| **Performance** | p50 median response under 400ms · 60% API response time reduction |
| **Frontend** | Vue optimistic updates · Lazy loading · Input debouncing |
| **Auth** | Email OTP via Resend · OAuth via Passport.js (Google, GitHub) |
| **Infra** | EC2 (SSM deploys) · S3 + CloudFront · Terraform · GitHub Actions CI/CD |
| **Security** | JWT · OAuth 2.0 · Typebox schema validation |
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

**Founder & CTO** · *Commma* · [commma.dev](https://commma.dev) · [LinkedIn](https://www.linkedin.com/company/commma-dev/)
`May 2026 – Present · Cincinnati, OH`

Founding and building an end-to-end developer activity tracking platform from zero — VSCode extension, REST API, and web app — shipping across the full monorepo as sole technical decision-maker. Phases 1–4 complete and live in production; Phase 5 (mobile, PWA, JetBrains/Neovim plugins, CLI, self-hosted Docker stack) in progress.

- Architected a pnpm monorepo across three apps (extension, API, web) and two shared packages (schema, DB) with strict TypeScript boundaries
- Built the VSCode extension with key-label tracking, three configurable privacy modes, and an offline queue for resilient event delivery
- Designed and implemented GitHub OAuth, JWT access tokens, HTTP-only rotating refresh tokens, and Stripe Pro/Team billing with webhook signature verification
- Engineered Canvas-based keyboard heatmap rendering with PNG export in three aspect ratios for social sharing, plus a server-side OG image variant via sharp
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
`Jan 2026 – Present · Ho Chi Minh, Vietnam`

Leading 6 engineers building an end-to-end distributed real-time messaging and study-matching platform across the full product lifecycle, from architecture to production operations.

- Engineered a distributed real-time messaging system using Socket.IO, PostgreSQL, and Redis, cutting average API response times by 60% and sustaining 1,700+ requests/minute over 30 days of production traffic
- Scaled the backend study-matching platform to 400+ active users through sprint planning and code reviews using Nuxt 3 and Node.js
- Achieved p50 median response times under 400ms by architecting a Vue-based frontend with optimistic updates, lazy loading, and input debouncing, hardened with JWT, OAuth 2.0, and Typebox schema validation

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
| GPA Honor Roll | 3.71 / 4.0 · University of Cincinnati · Computer Engineering |
| Production Deployment | Commma — live at commma.dev · EC2 t4g + S3 + CloudFront + Terraform · Phases 1–4 complete |
| Production Deployment | KatanaID — 2,300+ req/day · AI branding platform · 5-engineer team |
| Production Deployment | Caphne — 400+ users · 1,700+ req/min · FPT University network |
| LLM Cost Engineering | 91.6% inference cost reduction · 98.2% accuracy · 518-prompt benchmark |
| Systems Performance | 500ns P99 matching engine latency · 4.7M orders/sec · 8.8x throughput gain |
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

## Contribution Activity

</div>

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=trnahnh&bg_color=141210&color=E8E0D0&line=E8541A&point=E8E0D0&area=true&area_color=2A1F18&hide_border=true)](https://github.com/ashutosh00710/github-readme-activity-graph)

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
