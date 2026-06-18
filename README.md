<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0c10,50:1a3a5c,100:4d9fff&height=200&section=header&text=Yash%20Raj%20Pandey&fontColor=ffffff&fontSize=48&fontAlignY=38&desc=AI%20Agents%20Architect%20-%20Local-First%20AI%20Infrastructure&descAlignY=58&descSize=18&animation=fadeIn" width="100%" />

![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&pause=1200&color=4D9FFF&center=true&vCenter=true&width=700&lines=Self-hosted+LLMs+that+never+leak+your+data;RAG+-+Vector+search+-+AI+agents;AI+that+runs+in+production%2C+not+in+a+demo)

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
    focus       = ["local-first LLMs", "RAG", "vector search", "AI agents"]
    also_builds = "full-stack production systems"
    philosophy  = "Understand the real problem. Ship the simplest thing that works. Measure. Iterate."
```

I build AI infrastructure and production software. I'm the AI Agents Architect at the University of Florida's Institute of Food and Agricultural Sciences, where I lead a function I proposed myself: self-hosted, air-gapped AI systems built on open-weight models.

I joined UF as a Software Engineer in March 2025, was promoted to Lead Software Engineer in October 2025, and moved into the AI Agents Architect role in April 2026.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0a0c10,100:4d9fff&height=2&width=100%" width="100%" />

## What I'm building

### TurboQuant on Apple Silicon

Independent evaluation of TurboQuant (arXiv 2504.19874), a near-optimal LLM quantization method, ported to run CPU-only on Apple Silicon. Fixed five blocking bugs, then benchmarked long-context retrieval across an MLX path and a llama.cpp Metal path.

> **Needle-in-a-haystack retrieval: 0% to 100% at 16K tokens**, with a large KV cache memory reduction, all on a consumer M1 Pro with no dedicated GPU.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![MLX](https://img.shields.io/badge/MLX-000000?style=flat-square&logo=apple&logoColor=white)
![llama.cpp](https://img.shields.io/badge/llama.cpp-4d9fff?style=flat-square)
![Quantization](https://img.shields.io/badge/Quantization-1a3a5c?style=flat-square)

[**View the repo ->**](https://github.com/devYRPauli/turboquant-m1pro-evaluation)

### Blue Omics - full-stack research data platform

A Django, React, and PostgreSQL platform I designed and built from scratch for a research lab. It grew from zero to **5M+ live records** across 32 data models and 58 API endpoints, replaced years of manual spreadsheet workflows, and became the primary system for every lab submission.

- Tuned PostgreSQL with explicit indexing and caching to hold low-millisecond median latency under concurrent access by 30+ researchers
- Built 7 ingestion pipelines for heterogeneous formats: PDF, Excel, CSV, Word, PowerPoint
- Automated R Markdown reporting, cutting a 2-3 hour manual process to 15-20 minutes
- Deployed on GCP with Kubernetes and Terraform; optimized the frontend from 8s to 3s load time

![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

### ApplyScore - AI resume gap-analysis Chrome extension

A published Chrome extension that scores how well a resume matches any job posting on the web, with evidence-linked gaps and no hallucinated fluff.

- Universal scraper that pierces Shadow DOM to read postings across LinkedIn, Greenhouse, Ashby, Lever, Workday and more
- Strict, evidence-based analysis: a confidence-weighted fit score with requirement-by-requirement matches linked to the exact resume bullets that prove them
- Privacy-first and bring-your-own-key (OpenAI, Anthropic, or Google), so data and model choice stay with the user

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Chrome](https://img.shields.io/badge/Chrome_Extension-4285F4?style=flat-square&logo=googlechrome&logoColor=white)
![LLM](https://img.shields.io/badge/LLM_APIs-1a3a5c?style=flat-square)

[**View on the Chrome Web Store ->**](https://chromewebstore.google.com/detail/applyscore/ibecekikdjelajpnjnmapejhahgcplim)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0a0c10,100:4d9fff&height=2&width=100%" width="100%" />

## Open source

I fix real bugs in the AI infrastructure I build on: inference engines, ML frameworks, and the tooling around them. 30+ merged pull requests across 20+ open-source projects, each one a root-caused fix backed by a regression test.

**LLM inference and ML frameworks**

- [**llama.cpp**](https://github.com/ggml-org/llama.cpp/pull/24305) (ggml) - fixed `rms_norm_back` producing wrong output under in-place aliasing on the CPU backend
- [**MLX**](https://github.com/ml-explore/mlx/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) (Apple) - signed-integer overflow in `roll` and `tile`; undefined behavior in `arange(step=0)`
- [**MLX-LM**](https://github.com/ml-explore/mlx-lm/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) (Apple) - server 404 on short prompts; sampler `top_k` bound fix
- [**RAGFlow**](https://github.com/infiniflow/ragflow/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) - broken language detection; Excel parser off-by-one chunking
- [**mem0**](https://github.com/mem0ai/mem0/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) - Redis, FAISS, and Weaviate crashes and filtered-search truncation

**Developer tooling**

Cost-accuracy and edge-case fixes across a suite of open-source CLI and macOS tools: pricing-unit bugs (per-token vs per-request), timezone and Unicode handling, performance regressions, and more.

[**See all merged contributions ->**](https://github.com/search?q=is%3Apr+author%3AdevYRPauli+is%3Amerged&type=pullrequests)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0a0c10,100:4d9fff&height=2&width=100%" width="100%" />

## Stack

| | |
|---|---|
| **AI / ML** | Open-weight LLMs, RAG, Vector search (Qdrant), Embeddings, Reranking, Model evaluation, vLLM, Ollama |
| **Backend** | Python, Django, Django REST, FastAPI, Node.js, PostgreSQL, Redis |
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

**Off the clock:** football (I built [Football Hub](https://football-hub-six.vercel.app/) because I love the game), tactical FPS, story-rich RPGs, and lo-fi for flow state.

*Open to good conversations on AI infrastructure and local-first LLM systems.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4d9fff,50:1a3a5c,100:0a0c10&height=120&section=footer" width="100%" />

</div>
