<div align="center">

# Yash Raj Pandey

### AI Agents Architect · Local-First AI Infrastructure

Building self-hosted LLM systems that run modern AI on sensitive data without that data ever leaving on-premise hardware.

[![Website](https://img.shields.io/badge/Website-yashrajpandey.com-4d9fff?style=flat&logoColor=white)](https://yashrajpandey.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yashrajpandeyy/)
[![X](https://img.shields.io/badge/X-000000?style=flat&logo=x&logoColor=white)](https://x.com/I_AM_YRP)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:yashpn62@gmail.com)

[![Resume](https://img.shields.io/badge/Download_Resume-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1raCNzPrX4p9sUYEBr-h1yvhWeiFV2Bxj/view?usp=drive_link)

</div>

---

## whoami

```python
class YashRajPandey:
    role        = "AI Agents Architect @ UF IFAS"
    based_in    = "Gainesville, Florida"
    focus       = ["local-first LLMs", "RAG", "vector search", "AI agents"]
    also_builds = "full-stack production systems"
    philosophy  = "Understand the real problem. Ship the simplest thing that works. Measure. Iterate."
```

I build AI infrastructure and production software. I'm the AI Agents Architect at the University of Florida's Institute of Food and Agricultural Sciences, where I lead a function I proposed myself: self-hosted, air-gapped AI systems built on open-weight models.

I joined UF as a Software Engineer in March 2025, was promoted to Lead Software Engineer in October 2025, and moved into the AI Agents Architect role in April 2026.

---

## What I'm building

### TurboQuant on Apple Silicon &nbsp;·&nbsp; [repo →](https://github.com/devYRPauli/turboquant-m1pro-evaluation)
Independent evaluation of TurboQuant (arXiv 2504.19874), a near-optimal LLM quantization method, ported to run CPU-only on Apple Silicon. Fixed five blocking bugs, then benchmarked long-context retrieval across an MLX path and a llama.cpp Metal path.

> **Needle-in-a-haystack retrieval: 0% → 100% at 16K tokens**, with a large KV cache memory reduction, all on a consumer M1 Pro with no dedicated GPU.

`Python` &nbsp; `MLX` &nbsp; `llama.cpp` &nbsp; `Quantization` &nbsp; `Apple Silicon`

<details>
<summary><b>Blue Omics</b> — full-stack research data platform (production, internal)</summary>

<br>

A Django, React, and PostgreSQL platform I designed and built from scratch for a research lab. It grew from zero to **5M+ live records** across 32 data models and 58 API endpoints, replaced years of manual spreadsheet workflows, and became the primary system for every lab submission.

- Tuned PostgreSQL with explicit indexing and caching to hold low-millisecond median latency under concurrent access by 30+ researchers
- Built 7 ingestion pipelines for heterogeneous formats (PDF, Excel, CSV, Word, PowerPoint)
- Automated R Markdown reporting, cutting a 2-3 hour manual process to 15-20 minutes
- Deployed on GCP with Kubernetes and Terraform; optimized the frontend from 8s to 3s load time

`Django REST` &nbsp; `React` &nbsp; `PostgreSQL` &nbsp; `GCP` &nbsp; `Kubernetes` &nbsp; `Terraform`

</details>

<details>
<summary><b>ApplyScore</b> — AI resume gap-analysis Chrome extension (shipped)</summary>

<br>

A published Chrome extension that scores how well a resume matches any job posting on the web, with evidence-linked gaps and no hallucinated fluff. [View on the Chrome Web Store →](https://chromewebstore.google.com/detail/applyscore/ibecekikdjelajpnjnmapejhahgcplim)

- Universal scraper that pierces Shadow DOM to read postings across LinkedIn, Greenhouse, Ashby, Lever, Workday and more
- Strict, evidence-based analysis: a confidence-weighted fit score with requirement-by-requirement matches linked to the exact resume bullets that prove them
- Privacy-first and bring-your-own-key (OpenAI, Anthropic, or Google), so data and model choice stay with the user

`JavaScript` &nbsp; `Chrome Extension APIs` &nbsp; `Shadow DOM` &nbsp; `LLM APIs`

</details>

---

## Stack

**AI / ML** &nbsp; Open-weight LLMs · RAG · Vector search (Qdrant) · Embeddings · Reranking · Model evaluation · vLLM · Ollama

**Backend** &nbsp; Python · Django · Django REST · FastAPI · Node.js · PostgreSQL · Redis

**Frontend** &nbsp; React · TypeScript · Modern HTML/CSS

**Infra** &nbsp; Docker · Kubernetes · Terraform · GCP · AWS · CI/CD · GitHub Actions

---

## Recognition & Education

**Herbert Wertheim College of Engineering Achievement Award** — University of Florida
Merit scholarship awarded for top academic standing.

**Education**
- M.S. Computer & Information Science & Engineering, University of Florida — GPA 3.8 / 4.0
- Semester Exchange, University of Florida — GPA 3.7 / 4.0
- B.Tech Computer Science & Engineering, Jaypee University of Engineering & Technology — GPA 9.1 / 10.0

---

## Writing

I keep playbooks on what I learn shipping local AI, over on [yashrajpandey.com](https://yashrajpandey.com):

- Self-hosting open-weight LLMs without sending data to a cloud API
- RAG that holds up in production (retrieval, reranking, and the evals that keep it honest)
- Evaluation-gated releases for LLM systems

---

## GitHub

![Yash's GitHub stats](https://github-readme-stats.vercel.app/api?username=devYRPauli&show_icons=true&hide_border=true&theme=dark&icon_color=4d9fff&title_color=4d9fff)

![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=devYRPauli&layout=compact&hide_border=true&theme=dark&title_color=4d9fff)

---

<div align="center">

**Off the clock:** football (I built [Football Hub](https://football-hub-six.vercel.app/) because I love the game), tactical FPS, story-rich RPGs, and lo-fi for flow state.

*Open to good conversations on AI infrastructure and local-first LLM systems.*

</div>
