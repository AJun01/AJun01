# Hi there, I'm Yujun Liu 👋

<p>
  <a href="https://www.linkedin.com/in/yujun-liu-challenger/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:yujunliu150@gmail.com"><img src="https://img.shields.io/badge/Email-Say%20hi-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://ajun01.github.io/React-Portfolio/" target="_blank"><img src="https://img.shields.io/badge/Portfolio-Visit-7C3AED?style=for-the-badge&logo=react&logoColor=white" alt="Portfolio" /></a>
</p>

**AI / full-stack engineer.** I build agentic systems end to end — multi-agent orchestration, fine-tuned models, and the cloud infrastructure they run on.

- 🏢 **Forward Deployment & AI Developer @ iOffer.AI** (Cambridge, MA) — AI-native B2B SaaS for college admissions
- 🎓 MS in Computer Science, **Boston University** (2025) · BS in Information Sciences & Technology, **Penn State** (2022)
- ☁️ **AWS Certified Solutions Architect – Associate**
- 🌱 GSoC 2024 @ GFOSS — OpenAPI tooling and PII anonymization for the Flexbench traffic simulator
- ✍️ I write sci-fi, and I'm adapting my novel *SLEEPING IRON* into an HD-2D game
- 💬 Ask me about: agentic workflows, RAG, multi-tenant SaaS architecture, AWS CDK, local LLM fine-tuning

### I'm open to

- Open-source contributions
- Agentic-AI / LLM infrastructure collaborations
- Interesting full-stack and cloud problems

## Languages and Tools

<p align="center">
  <img src="https://skillicons.dev/icons?i=py,ts,js,java,go,cpp,react,nextjs,nodejs,fastapi,docker,kubernetes,aws,terraform,postgres,redis,git,githubactions,linux,godot&perline=10" alt="Languages and tools" />
</p>

**Also working with:** LangGraph / LangChain · LlamaIndex · PyTorch & MLX (QLoRA) · SQLAlchemy 2.0 · Pydantic · Supabase · Stripe · Kafka · Qdrant · Neo4j · MinIO · Prometheus / ELK · GDScript

---

## Featured Projects

### 🎬 [Backlot Film Maker](https://github.com/AJun01/Backlot-Film-Maker) — agentic film production toolchain

> A canonical **ProductionBible** acts as the single source of truth for every agent, from script breakdown to rendered shots.

- Multi-role agent pipeline (Analyst → Art → Playwright → Director → Acting Coach → VLS → Cinematographer → PM) driven by a **chat-to-DAG** workflow editor with React Flow + SSE live graph updates.
- Replaced a serial ReAct state machine with a **Redis pub/sub roundtable** — tool-enabled agents debate in parallel, moderated by operator keyword directives.
- **Aegis Asset Vault** keeps characters, props and environments consistent across shots with Qdrant prop vectors, a Neo4j continuity graph, and Pydantic-enforced schemas.
- Per-role Claude or Gemini models, Claude extended-thinking streamed into the operator UI, and a **ToolGate** that guards destructive tools.

`Python` `FastAPI` `React` `Redis` `Qdrant` `Neo4j` `MinIO` `PostgreSQL` `LlamaIndex` `Docker Compose`

### 🧠 [OW-Socrates](https://github.com/AJun01/ow-socrates) — a Socratic hint assistant that refuses to spoil

> Teaching Qwen3-8B to give hints that help stuck *Outer Wilds* players think — instead of handing them the answer.

- A **QLoRA fine-tuning** pipeline for Qwen3-8B (4-bit MLX) built to train and serve locally on a 16 GB M2 Pro — ~39 tok/s at inference.
- Four explicit Socratic strategies (counter-question / widen / challenge premise / decompose) used both as the system prompt and as training-data labels.
- Baseline harness over fixed stuck-point prompts, a raw → normalize → augment → chat-JSONL data pipeline, and MLX-free smoke tests.

`Python 3.12` `MLX-LM` `QLoRA` `Qwen3-8B`

### 📈 ZenTrade — AI trading coach that can actually stop you 🔒

> Inserts an AI coach *with enforcement power* between the impulse and the order.

- Seven risk rules (drawdown, position size, frequency, revenge trading, stop-loss, take-profit, no-trade windows) escalate from a nudge → position lock → redemption.
- Behavior profiling from imported trade history (disposition effect, overtrading, chasing) that explicitly refuses to draw conclusions from thin samples.
- LLM-proposed trading plans must pass a deterministic validation gate and human approval before they take effect; four coach personas remember your goals and evidence.
- Macro reports from FRED, plus an "information environment" layer over SEC EDGAR + GDELT / Google News with provenance badges — *"only N new things were actually said about this in 24h."*
- Exposes 10 MCP tools so external agents can plug into memory, reports, rules and market data.

`TypeScript` `Node 22` `npm workspaces` `SQLite` `Gemini / Anthropic` `React` `MCP`

### 🖥️ Computer-Use Agent Backend 🔒

> FastAPI service running many independent Claude computer-use sessions, each with its own virtual desktop.

- Typed event streams over **SSE** plus Postgres persistence that survives restarts; one desktop container per session with a pooled lifecycle and proxied VNC access.
- Reuses the upstream agent loop and tool implementations **unmodified** (vendored at a pinned commit), replacing a single-user Streamlit demo with a real multi-session backend.
- Built spec-first against FR-1..FR-9 requirements — every design decision is recorded together with the alternative it rejected — and ships with a one-command Docker Compose demo.

`Python` `FastAPI` `PostgreSQL` `Docker Compose` `Anthropic computer-use`

### 🎮 [Sleeping Iron HD-2D](https://github.com/AJun01/godot-HD-SleepingIron) — HD-2D game adapting my original novel

> A sci-fi mecha story I wrote, rebuilt as a Godot game — with a spec-driven development pipeline enforced end to end.

- Every feature starts as a **spec → design → implementation → verification** artifact; one task = one commit, and PRs are created by a verifier agent.
- Fully statically typed GDScript with data-driven `@export` / `Resource` design.
- CI runs GDToolkit lint plus headless Godot compile and scene smoke tests on every push, with AI architecture review on PRs.

`Godot 4.7` `GDScript` `GitHub Actions`

### 📄 [Resume Tailor](https://github.com/AJun01/master-resume) — conservative resume micro-tuning

> A resume that already works is a verified asset — the system's job is surgical adjustment, not a rewrite.

- A change budget caps reworded bullets at ~30%, output is a reviewable diff, and every change needs a JD-cited reason.
- ATS / HR quality gates block fabrication; numbers and metrics must survive verbatim.
- Application tracking with Gmail-driven status automation, plus a `baseline` control group to measure whether tailoring actually improves interview rate.

`TypeScript` `Next.js` `Drizzle` `PostgreSQL (Neon)` `Claude`

### 🎓 VEer — virtual educator AI 🔒

> Distills a real education consultant into a 24/7 AI that both *talks* like them and *works* like them.

- 100% infrastructure as code on **AWS CDK** (Lambda, WebSocket API, Aurora, S3) with Stripe billing and multi-tenant isolation.
- A unified chat runtime composes six capability layers — persona, guardrails, skills, knowledge, intake, jobs — that can hot-swap at the data plane without redeploying the model.
- 99-endpoint admissions-management backend plus a TanStack Start + React 19 frontend with en/zh i18n, developed across 8 written specs.

`TypeScript` `AWS CDK` `Python / FastAPI` `Aurora PostgreSQL` `React 19` `TanStack Start` `Stripe`

## More Projects

| Project | What it does | Stack |
|---|---|---|
| AI admissions platform 🔒 | Multi-tenant B2B SaaS for AI-powered college admissions: RBAC permission matrix, LangGraph ReAct agents, workflow engine with human approval gates, Postgres-native job queue | FastAPI, SQLAlchemy 2.0, LangGraph, Supabase |
| Application-autofill browser extension 🔒 | Manifest V3 extension that fills university application forms from a student profile and calls AI agents to generate content | WXT, React 18, TypeScript, Tailwind |
| Serverless file-processing pipeline 🔒 | Browser → API Gateway → presign Lambda → direct-to-S3 upload; a DynamoDB stream launches an orchestrator Lambda that boots a self-terminating EC2 worker | AWS CDK, Lambda, DynamoDB, S3, EC2, React |
| TikTok Shop print automation 🔒 | Backend that syncs TikTok Shop orders, queues label-print jobs, monitors printers and auto-fulfills shipments across multiple shops | Node.js, Express, Supabase, Firebase, Socket.io |
| [SYNAB LLC](https://github.com/AJun01/SYNAB-LLC) | Production marketing site for a cross-border commerce infrastructure firm — [live](https://synab-llc.vercel.app) | React 18, Vite 6, Tailwind v4, Framer Motion |
| [React Portfolio](https://github.com/AJun01/React-Portfolio) | Personal front-end portfolio, deployed on GitHub Pages | React, CSS |

---

## Experience

### iOffer.AI — Forward Deployment & AI Developer · *Sep 2024 – Present*

- Led **pre-sales technical discovery** for an AI-native B2B platform, designing migration workflows to onboard enterprise customers.
- Architected a **multi-tenant RBAC permission matrix** securing enterprise onboarding with **zero privilege escalation**.
- Built a **multi-agent orchestration service** (ReAct + semantic routing + unified function-calling toolchain) that reaches **96% reusable content** in counseling reports.
- Reengineered **data-ingestion tools** for the agentic pipeline around a fine-tuned knowledge base, lifting data quality by **400%**.
- Decoupled request handling from heavy multi-agent execution with a **Postgres-backed Procrastinate job queue**, smoothing bursty load into async workers for a **40+ user** platform.

### Google Summer of Code 2024 @ GFOSS — Open-Source Module Developer · *May – Aug 2024*

- Selected from **40,000+** applicants to build HTTPS traffic-simulation tooling for large-scale load testing.
- Published an **npm module** automating OpenAPI parsing, cutting configuration time to seconds with **100% endpoint coverage**.
- Built a config-driven **PII anonymization middleware** for real-time sanitization, and integrated GPT-4o for dynamic scenario generation.

### LeadershipEdge — Web Developer · *Sep 2022 – Jul 2023*

- Engineered a web survey platform with custom **PHP** hooks writing into **MySQL**, plus SQL-driven interactive charts and MBTI-style results.
- Drove a **40% weekly user increase** through SEO and feature work.

### Education & Certifications

- **AWS Certified Solutions Architect – Associate** · Jan 2026
- **Boston University** — MS, Computer Science · Sep 2023 – May 2025
- **Pennsylvania State University** — BS, Information Sciences & Technology · Aug 2018 – May 2022

## Recent Updates

- **Sep 2026** — Shipped the ZenTrade coach workspace: project/conversation workbench, per-persona context isolation, artifact system and full trading activity traces.
- **Aug 2026** — First playable *Sleeping Iron HD-2D* demo on Godot 4.7, with a spec-driven pipeline and headless CI verification.
- **Jul 2026** — Built Resume Tailor, a conservative JD-tailoring platform with ATS gates and application tracking.
- **Jun 2026** — Started OW-Socrates: QLoRA fine-tuning of Qwen3-8B on Apple Silicon.
- **Apr – May 2026** — Shipped Backlot Film Maker's multi-agent roundtable and the SYNAB LLC marketing site.
- **Jan 2026** — Passed the AWS Certified Solutions Architect – Associate exam.

## GitHub Stats

<p align="center">
  <img src="https://streak-stats.demolab.com?user=AJun01&theme=tokyonight&hide_border=true" alt="GitHub streak" />
</p>

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=AJun01&theme=tokyonight" alt="Top languages by repo" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=AJun01&theme=tokyonight" alt="Top languages by commit" />
</p>

## Connect with Me

<p align="center">
  <a href="https://docs.google.com/document/d/1N1jUcrAv7VVRQC3pCZJCyiZIdYGmIFn3kmNYF28QPcY/edit?tab=t.0" target="_blank">
    <img src="https://img.shields.io/badge/Resume-Read%20It-blue?style=for-the-badge&logo=googledrive&logoColor=white" alt="Resume" />
  </a>
  <a href="https://ajun01.github.io/React-Portfolio/" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-Visit-blueviolet?style=for-the-badge&logo=react&logoColor=white" alt="Portfolio" />
  </a>
  <a href="https://www.linkedin.com/in/yujun-liu-challenger/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Connect%20Now-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://flexivian.github.io/flexbench/docs/GSoC/2024/" target="_blank">
    <img src="https://img.shields.io/badge/GSOC%202024-Learn%20More-orange?style=for-the-badge&logo=google&logoColor=white" alt="GSoC 2024" />
  </a>
</p>

<details>
<summary><b>Earlier toy projects (2024 and before)</b></summary>

<br />

| Project | Description |
|---|---|
| [ticketmeister](https://github.com/AJun01/ticketmeister) | Mock ticket-selling app built with React. |
| [weather-app](https://github.com/AJun01/weather-app) | Weather app fetching data from the OpenWeatherMap API. |
| [Registar](https://github.com/AJun01/Registar) | Mock registration flow for yoga instructors. |
| [trade-king](https://github.com/AJun01/trade-king) | Mock stock-trading app. |
| [grocerella](https://github.com/AJun01/grocerella) | Mock grocery-shopping app in React. |
| [job-list](https://github.com/AJun01/job-list) | Mock job widget. |
| [develop-flexbench](https://github.com/AJun01/develop-flexbench) | Node.js HTTP traffic simulator (GSoC work). |
| [MIPS-PIPELINED-DATAPATH](https://github.com/AJun01/MIPS-PIPELINED-DATAPATH) · [MIPS-CACHE](https://github.com/AJun01/MIPS-CACHE) · [MIPS-DECODER](https://github.com/AJun01/MIPS-DECODER) | Computer-architecture exercises simulating pipelined datapaths, cache read/write, and instruction decoding. |

</details>
