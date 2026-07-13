<div align="center">

# Yash Raj Pandey

**AI Agents Architect at UF IFAS**

I build local-first LLM infrastructure, production AI agents, evaluation systems, and developer tools.

[![Website](https://img.shields.io/badge/Website-yashrajpandey.com-1f6feb?style=flat-square)](https://yashrajpandey.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Yash_Raj_Pandey-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yashrajpandeyy/)
[![X](https://img.shields.io/badge/X-@I__AM__YRP-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/I_AM_YRP)
[![Resume](https://img.shields.io/badge/Resume-PDF-4285F4?style=flat-square)](https://yashrajpandey.com/Resume_YashRaj.pdf)

</div>

## What I work on

At the University of Florida's Institute of Food and Agricultural Sciences, I proposed and now lead a function for self-hosted, local-first AI. I build on-premises LLM infrastructure, RAG and tool-calling systems, and evaluation gates for production workflows with sensitive data.

I joined UF as a Software Engineer in March 2025, was promoted to Lead Software Engineer seven months later, and moved into the AI Agents Architect role in April 2026. Outside work, I build developer tools, run independent model evaluations, and contribute root-caused fixes upstream.

## Featured work

### [Baton](https://github.com/devYRPauli/baton) - reliable coding-agent delegation

A standalone kit that installs an orchestrator-to-executor workflow into Claude Code. Detached Codex jobs survive session end; disciplined briefs, explicit permissions, durable results, and independent verification keep delegated code work auditable.

[Project page](https://yashrajpandey.com/work/baton/) | [Technical write-up](https://yashrajpandey.com/writing/baton-the-tool-that-built-itself/)

### [Looma](https://github.com/devYRPauli/looma) - local-first memory for coding agents

Turns Claude Code, Codex, and Cursor history into resumable project context: active work, decisions, blockers, files, commits, and next steps. The zero-dependency Python default reaches F1 0.86; an optional local LLM reaches 0.95. Published on PyPI with 134 passing tests.

[Project page](https://yashrajpandey.com/work/looma/) | [PyPI](https://pypi.org/project/looma/)

### [TabFM Evaluation](https://github.com/devYRPauli/tabfm-evaluation) - independent foundation-model evaluation

Reproduced Google Research's TabFM across three machines and 13 TabArena datasets, compared it with XGBoost, random forest, linear models, and TabPFN, and analyzed memory and latency scaling. The work surfaced four upstream issues, including a multi-GPU crash fix merged into google-research/tabfm.

[Technical write-up](https://yashrajpandey.com/writing/breaking-google-tabfm/)

### [TurboQuant on Apple Silicon](https://github.com/devYRPauli/turboquant-m1pro-evaluation) - quantization systems debugging

Root-caused five implementation problems across MLX and llama.cpp paths. The fixed configuration restored needle retrieval from 0% to 100% at 16K tokens on a 16 GB M1 Pro while reducing KV-cache memory 3.5x.

[Technical write-up](https://yashrajpandey.com/writing/turboquant-on-a-16gb-macbook/)

### [mddocs](https://github.com/devYRPauli/mddocs) - git-native collaborative Markdown with an agent API

A local-first Markdown editor with Yjs multiplayer, comments, suggestions, provenance, and a token-gated HTTP API for AI agents. Published on npm, shipped across eight semver releases, and reduced 87% in package size with esbuild.

[npm](https://www.npmjs.com/package/@devyrpauli/mddocs) | [Project page](https://yashrajpandey.com/work/mddocs/)

### [World Cup 2026 Picks](https://github.com/devYRPauli/world-cup-2026-picks) - a shipped full-stack product

A self-hostable prediction pool with authentication, Row Level Security, live scoring, group and knockout picks, leaderboards, fixture syncing, and scheduled result updates. Built with Next.js, TypeScript, Supabase, and Vercel.

[Live app](https://world-cup-2026-picks.vercel.app) | [Project page](https://yashrajpandey.com/work/world-cup-2026-picks/)

## Open source

I have contributed **45+ merged pull requests across 30+ projects**, spanning LLM inference, ML frameworks, RAG systems, vector stores, and developer tools. Each contribution starts with a reproduced failure and ends with a focused fix and regression coverage.

- [llama.cpp](https://github.com/ggml-org/llama.cpp/pull/24305): fixed incorrect CPU gradients under in-place aliasing
- [Apple MLX](https://github.com/ml-explore/mlx/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged): core-operation correctness and undefined-behavior fixes
- [Google Research TabFM](https://github.com/google-research/tabfm/pull/42): fixed prediction on multi-GPU hosts
- [mem0](https://github.com/mem0ai/mem0/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged), [LiteLLM](https://github.com/BerriAI/litellm/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged), and [RAGFlow](https://github.com/infiniflow/ragflow/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged): reliability, pricing, retrieval, and parser fixes

[See all merged contributions](https://github.com/search?q=is%3Apr+author%3AdevYRPauli+is%3Amerged&type=pullrequests)

## Stack

- **AI systems:** vLLM, Ollama, llama.cpp, MLX, RAG, vector search, reranking, tool-calling agents, evaluation harnesses, quantization
- **Engineering:** Python, TypeScript, JavaScript, SQL, C/C++, Bash, Django, FastAPI, React, Next.js
- **Infrastructure:** PostgreSQL, DuckDB, Redis, SQLite, Docker, Kubernetes, Terraform, GCP, AWS, Linux, GitHub Actions

## Writing

- [Baton: I built a tool for delegating code to an AI, then used it to build itself](https://yashrajpandey.com/writing/baton-the-tool-that-built-itself/)
- [I tried to break Google's new tabular foundation model. Then I fixed it.](https://yashrajpandey.com/writing/breaking-google-tabfm/)
- [From 0% to 100%: debugging a KV-cache compression algorithm on a 16 GB MacBook](https://yashrajpandey.com/writing/turboquant-on-a-16gb-macbook/)

Outside work: football, tactical FPS, story-rich RPGs, and lo-fi for flow state.
