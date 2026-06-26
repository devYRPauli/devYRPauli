<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0c10,50:1a3a5c,100:4d9fff&height=200&section=header&text=Yash%20Raj%20Pandey&fontColor=ffffff&fontSize=48&fontAlignY=38&desc=AI%20Agents%20Architect%20-%20Full-Stack%20-%20Systems%20-%20Open%20Source&descAlignY=58&descSize=18&animation=fadeIn" width="100%" />

![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&pause=1200&color=4D9FFF&center=true&vCenter=true&width=760&lines=Self-hosted+LLMs+that+never+phone+home;I+fix+the+open-source+tools+I+depend+on;Postgres+query+plan+by+day%2C+Metal+kernel+by+night;Yes%2C+I+built+apps+for+my+football+habit;Three+job+titles+in+13+months%2C+and+yes+I+sleep;If+it+hallucinates%2C+it+does+not+ship)

[![Website](https://img.shields.io/badge/Website-yashrajpandey.com-4d9fff?style=for-the-badge)](https://yashrajpandey.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yashrajpandeyy/)
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/I_AM_YRP)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yashpn62@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1raCNzPrX4p9sUYEBr-h1yvhWeiFV2Bxj/view?usp=drive_link)

</div>

<br>

### `whoami`

```python
class YashRajPandey:
    role        = "AI Agents Architect @ UF IFAS"
    based_in    = "Gainesville, Florida"
    builds      = ["AI infrastructure", "full-stack products",
                   "developer tools", "native + CLI apps"]
    languages   = ["Python", "TypeScript", "Swift", "Java", "C/C++"]
    open_source = "35+ merged PRs across 25+ projects, 4 ecosystems"
    philosophy  = "Find the real problem. Ship the simplest thing that works. Measure. Iterate."
```

I build AI infrastructure and production software. I'm the AI Agents Architect at the University of Florida's Institute of Food and Agricultural Sciences, where I lead a function I proposed myself: self-hosted, air-gapped AI systems built on open-weight models.

The work is end to end: open-weight models served on-prem, retrieval that pairs dense vector search with reranking, agents that call real tools, and evaluation gates that decide what ships. None of it leaves the building, and it holds up under real users rather than a demo.

That is the day job, not the whole picture. I ship full-stack products end to end, contribute fixes upstream to the inference engines and ML frameworks I run, and build native macOS and CLI tools in Swift. The throughline is range: in a given week I might tune a Postgres query plan, debug a Metal quantization kernel, and wire up a TypeScript CRDT.

I joined UF as a Software Engineer in March 2025, was promoted to Lead Software Engineer in October 2025, and moved into the AI Agents Architect role in April 2026.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0a0c10,100:4d9fff&height=2&width=100%" width="100%" />

## A year in

- **Promoted twice in ~13 months** - Software Engineer to Lead Software Engineer to AI Agents Architect
- **35+ merged open-source pull requests across 25+ projects**, spanning Apple's MLX, ggml / llama.cpp (C/C++), Python ML frameworks, and the TypeScript / Node ecosystem
- **A full-stack platform I built solo grew to 5M+ live records** and became the primary system for 30+ researchers
- **Shipped software people actually use** - a Chrome Web Store extension, a published npm package, and several deployed web apps
- **Herbert Wertheim College of Engineering Achievement Award**, alongside an M.S. in CISE (GPA 3.8)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0a0c10,100:4d9fff&height=2&width=100%" width="100%" />

## What I build

### AI infrastructure and local LLMs

**TurboQuant on Apple Silicon** - independent evaluation of TurboQuant (arXiv 2504.19874), a near-optimal LLM quantization method, ported to run CPU-only on Apple Silicon. Fixed five blocking bugs, then benchmarked long-context retrieval across an MLX path and a llama.cpp Metal path.

> **Needle-in-a-haystack retrieval: 0% to 100% at 16K tokens**, with a large KV cache memory reduction, all on a consumer M1 Pro with no dedicated GPU.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![MLX](https://img.shields.io/badge/MLX-000000?style=flat-square&logo=apple&logoColor=white)
![llama.cpp](https://img.shields.io/badge/llama.cpp-4d9fff?style=flat-square)
![Quantization](https://img.shields.io/badge/Quantization-1a3a5c?style=flat-square)
&nbsp;[**Repo ->**](https://github.com/devYRPauli/turboquant-m1pro-evaluation)

**Looma** - a local-first command-line tool that turns Claude Code, Codex, and Cursor history into resumable project context: active work, decisions, blockers, the commits and files in flight, and the next likely step. No cloud, no API keys, zero third-party dependencies.

- Reconstructs structured WorkItems (features, bugfixes, refactors, migrations) from raw agent transcripts, instead of keyword-searching logs
- Emits token-budgeted context packs so one agent can hand off to another without replaying the whole history
- Honest by design: every reconstruction carries a confidence score and shows alternatives instead of guessing

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-1a3a5c?style=flat-square)
&nbsp;[**Repo ->**](https://github.com/devYRPauli/looma)

**mddocs** - a git-native, self-hostable editor for Markdown: real-time multiplayer, inline comments, and accept/reject suggestions, plus a first-class HTTP API so AI agents read, edit, and review documents the same way people do. Published on npm.

- Local-first and git-native: every change is a commit, no central database to run
- Real-time collaboration backed by a CRDT (Yjs) document model that merges concurrent edits without conflicts
- Agent-facing HTTP API with per-agent tokens and rate limits, so automated writers are first-class collaborators, not bolt-ons

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
[![npm](https://img.shields.io/npm/v/@devyrpauli/mddocs?style=flat-square&logo=npm&label=npm&color=CB3837)](https://www.npmjs.com/package/@devyrpauli/mddocs)
&nbsp;[**Repo ->**](https://github.com/devYRPauli/mddocs)

### Full-stack and product

**Blue Omics** - a Django, React, and PostgreSQL research data platform I designed and built from scratch for a research lab. It grew from zero to **5M+ live records** across 32 data models and 58 API endpoints, replaced years of manual spreadsheet workflows, and became the primary system for every lab submission.

- Tuned PostgreSQL with explicit indexing and caching to hold low-millisecond median latency under concurrent access by 30+ researchers
- Built 7 ingestion pipelines for heterogeneous formats: PDF, Excel, CSV, Word, PowerPoint
- Automated R Markdown reporting, cutting a 2-3 hour manual process to 15-20 minutes
- Deployed on GCP with Kubernetes and Terraform; optimized the frontend from 8s to 3s load time

![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

> _Private repository - a walkthrough is available on request._

**ApplyScore** - a published Chrome extension that scores how well a resume matches any job posting on the web, with evidence-linked gaps and no hallucinated fluff.

- Universal scraper that pierces Shadow DOM to read postings across LinkedIn, Greenhouse, Ashby, Lever, Workday and more
- Strict, evidence-based analysis: a confidence-weighted fit score with requirement-by-requirement matches linked to the exact resume bullets that prove them
- Privacy-first and bring-your-own-key (OpenAI, Anthropic, or Google), so data and model choice stay with the user

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Chrome](https://img.shields.io/badge/Chrome_Extension-4285F4?style=flat-square&logo=googlechrome&logoColor=white)
![LLM](https://img.shields.io/badge/LLM_APIs-1a3a5c?style=flat-square)
&nbsp;[**Chrome Web Store ->**](https://chromewebstore.google.com/detail/applyscore/ibecekikdjelajpnjnmapejhahgcplim)

**Football Hub and World Cup 2026 Picks** - two deployed web apps I built because I love the game: a football data hub, and a self-hostable World Cup 2026 prediction pool with scoring, leaderboards, and shareable rooms for small groups.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
&nbsp;[**Football Hub ->**](https://football-hub-six.vercel.app/) &nbsp; [**World Cup 2026 Picks ->**](https://world-cup-2026-picks.vercel.app)

### Open source and systems

I fix real bugs in the software I build on and the tools I use every day, across four ecosystems. **35+ merged pull requests across 25+ open-source projects**, each one a root-caused fix backed by a regression test.

**LLM inference and ML frameworks**

- [**llama.cpp**](https://github.com/ggml-org/llama.cpp/pull/24305) (ggml, C/C++) - fixed `rms_norm_back` producing wrong output under in-place aliasing on the CPU backend
- [**MLX**](https://github.com/ml-explore/mlx/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) (Apple) - signed-integer overflow in `roll` and `tile`; undefined behavior in `arange(step=0)`
- [**MLX-LM**](https://github.com/ml-explore/mlx-lm/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) (Apple) - server 404 on short prompts; sampler `top_k` bound fix
- [**RAGFlow**](https://github.com/infiniflow/ragflow/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) - language detection, Excel cell handling, and CJK-safe text splitting
- [**mem0**](https://github.com/mem0ai/mem0/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) - Redis, FAISS, and Weaviate crashes and filtered-search truncation

**Native macOS and Swift**

- Status-model logic, terminal-rendering width invariants, and cost / timezone / Unicode correctness across several macOS menu-bar and TUI developer tools - each fix paired with a Swift Testing regression test.

**Developer tooling**

- Cost-accuracy and edge-case fixes across a suite of open-source CLI tools: pricing-unit bugs (per-token vs per-request), timezone and Unicode handling, performance regressions, and more.

[**See all merged contributions ->**](https://github.com/search?q=is%3Apr+author%3AdevYRPauli+is%3Amerged&type=pullrequests)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0a0c10,100:4d9fff&height=2&width=100%" width="100%" />

## Stack

| | |
|---|---|
| **Languages** | Python, TypeScript, Swift, Java, C/C++, SQL |
| **AI / ML** | Open-weight LLMs, vLLM, Ollama, RAG, hybrid retrieval, Qdrant, rerankers, embeddings, agents and tool use, quantization, evaluation harnesses |
| **Backend** | Django, Django REST, FastAPI, Node.js, PostgreSQL, Redis |
| **Frontend** | React, TypeScript, Modern HTML/CSS |
| **Infra** | Docker, Kubernetes, Terraform, GCP, AWS, CI/CD, GitHub Actions |

## Recognition and education

**Herbert Wertheim College of Engineering Achievement Award**, University of Florida. Merit scholarship awarded for top academic standing.

- M.S. Computer and Information Science and Engineering, University of Florida - GPA 3.8 / 4.0
- Semester Exchange, University of Florida - GPA 3.7 / 4.0
- B.Tech Computer Science and Engineering, Jaypee University of Engineering and Technology - GPA 9.1 / 10.0

## Writing

I keep playbooks on what I learn shipping local AI, over on [yashrajpandey.com](https://yashrajpandey.com):

- Self-hosting open-weight LLMs without sending data to a cloud API
- RAG that holds up in production: retrieval, reranking, and the evals that keep it honest
- Evaluation-gated releases for LLM systems

<br>

<div align="center">

**Off the clock:** football (so much that I built apps for it, above), tactical FPS, story-rich RPGs, and lo-fi for flow state.

*Open to good conversations on AI infrastructure, systems, and building things that ship.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4d9fff,50:1a3a5c,100:0a0c10&height=120&section=footer" width="100%" />

</div>
