<div align="center">

# Yash Raj Pandey

**AI Agents Architect at UF IFAS**

I build local-first LLM infrastructure, agent platforms, and evaluation systems.
I reproduce new model research, publish what broke, and send the fixes upstream.

[![Portfolio](https://img.shields.io/badge/Portfolio-343a40?style=for-the-badge&logo=astro&logoColor=white)](https://yashrajpandey.com)
[![Writing](https://img.shields.io/badge/Writing-343a40?style=for-the-badge&logo=rss&logoColor=white)](https://yashrajpandey.com/writing/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-343a40?style=for-the-badge)](https://www.linkedin.com/in/yashrajpandeyy/)
[![X](https://img.shields.io/badge/@devYRPauli-343a40?style=for-the-badge&logo=x&logoColor=white)](https://x.com/devYRPauli)
[![Resume](https://img.shields.io/badge/Resume-343a40?style=for-the-badge&logo=latex&logoColor=white)](https://yashrajpandey.com/Resume_YashRaj.pdf)

</div>

## Day job

I build and run AI systems for a university research institute. One constraint
shapes everything else: lab data stays on infrastructure the university
controls.

That splits the stack in a place I like. Generation runs on the university's
shared on-premises GPU cluster, because the model is far too large to sit under
a desk. Retrieval and reranking run on a Mac Studio in the lab, because I
benchmarked both paths and hybrid retrieval with a local cross-encoder won
outright. So the commodity half runs on shared infrastructure, and the half that
decides whether an answer is right runs where I can measure it. That was a
measurement, not a preference.

The model is the easy part. You download it and it answers. The hard part is
working out what the question was before any model runs, getting clean text out
of documents that resist it, and proving an answer is right before a scientist
acts on it. A confident wrong number is worse than an error.

What that has meant in practice:

- About twenty routing rules, each correct alone, collided in production. I
  replaced them with one deterministic arbiter that can be read and tested.
- A hand-written agent loop grew until one tool failure could stop the whole
  assistant. I replaced it with a proven framework, and shipped it only after it
  beat the old one on a held-out set.
- Every number in an answer traces back to the tool result it came from.
- An alarming document-quality metric turned out to be a measurement bug, not
  damaged text. Check the alarm before you act on it.

I also lead the genomics platform for the UF blueberry breeding program: the
system of record for 30 researchers across 5 labs. I joined it at 81 source
files and took the lead seat.

Software Engineer March 2025, Lead Software Engineer seven months later, AI
Agents Architect since April 2026.

## Open source

**65 merged pull requests across 28 projects.** Each one starts with a failure I
reproduced and ends with a focused fix and a regression test.

| Project | Stars | Merged | What I fix there |
|---|---|---|---|
| [ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) | 126k | 3 | Kernels. Wrong gradients under in-place aliasing. A routing table that must not be quantized. |
| [infiniflow/ragflow](https://github.com/infiniflow/ragflow/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) | 89k | 14 | Document parsers. Dropped table cells, spliced CSV fields, crashes on valid input. |
| [mem0ai/mem0](https://github.com/mem0ai/mem0/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) | 64k | 4 | Retrieval and vector store correctness. |
| [BerriAI/litellm](https://github.com/BerriAI/litellm/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) | 57k | 3 | Billing. People pay these numbers. |
| [agno-agi/agno](https://github.com/agno-agi/agno/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) | 42k | 1 | Reader took the user id from the wrong field. |
| [ml-explore/mlx](https://github.com/ml-explore/mlx/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) | 28k | 2 | Undefined behavior in shape arithmetic. |
| [steipete/CodexBar](https://github.com/steipete/CodexBar/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) | 21k | 8 | Pricing tables, quota display, reset-date rollover, cache-token accounting. |
| [ml-explore/mlx-lm](https://github.com/ml-explore/mlx-lm/pulls?q=is%3Apr+author%3AdevYRPauli+is%3Amerged) | 6.8k | 2 | Server 404 on short prompts. |

The other 28 are spread across 20 smaller projects: oracle, poltergeist, RepoBar,
birdclaw, summarize, tokentally, and
[google-research/tabfm](https://github.com/google-research/tabfm/pull/42), where
prediction crashed on multi-device hosts. I found that one during my own
evaluation of the model.

Another 39 are open, and I have filed bug reports against
[ollama](https://github.com/ollama/ollama/issues?q=author%3AdevYRPauli),
[nanochat](https://github.com/karpathy/nanochat/issues?q=author%3AdevYRPauli) and
[mcpb](https://github.com/modelcontextprotocol/mcpb/issues?q=author%3AdevYRPauli).

[Every merged pull request](https://github.com/search?q=is%3Apr+author%3AdevYRPauli+is%3Amerged&type=pullrequests)

## Things I built

**[willitcall](https://github.com/devYRPauli/willitcall)** - the caniuse of local-model tool calling.
Most local models claim tool calling. Fewer do it twice in a row. Same suite,
every model, one matrix. Nobody had published it -> 32 rows, 3 servers.

**[looma](https://github.com/devYRPauli/looma)** - local-first memory for coding agents.
Turns Claude Code, Codex and Cursor history into resumable project context.
134 tests, zero dependencies, on [PyPI](https://pypi.org/project/looma/).

**[podium](https://github.com/devYRPauli/podium)** - verified delegation for Claude Code.
One agent hands briefed work to a roster of bots. A shell command, not a model,
decides whether the work landed.

**[mddocs](https://github.com/devYRPauli/mddocs)** - git-native collaborative Markdown, with an agent API.
Yjs multiplayer over plain files in git. An agent suggests, a person accepts,
the result is a commit. 17 releases on [npm](https://www.npmjs.com/package/@devyrpauli/mddocs).

**[world-cup-2026-picks](https://github.com/devYRPauli/world-cup-2026-picks)** - a product that shipped.
Self-hostable prediction pool. Skipped picks count as wrong, so there is no
hiding in the safe games.

## Things I broke on purpose

**[TabFM Evaluation](https://github.com/devYRPauli/tabfm-evaluation)** - I tried to break Google's
tabular foundation model, across 3 machines and 13 datasets. Four upstream
issues, one merged fix. A multi-seed check then made me demote two of my own
wins to ties, because the margins sat inside measurement noise. [Write-up](https://yashrajpandey.com/writing/breaking-google-tabfm/)

**[TurboQuant on Apple Silicon](https://github.com/devYRPauli/turboquant-m1pro-evaluation)** -
five implementation bugs across the MLX and llama.cpp paths, on a 16 GB M1 Pro.
Needle retrieval 0% -> 100% at 16K. [Write-up](https://yashrajpandey.com/writing/turboquant-on-a-16gb-macbook/)

## Stack

**Inference and agents:** vLLM, llama.cpp, MLX, Ollama, Qdrant, RAG, reranking, tool calling, eval harnesses, quantization, MCP
**Languages:** Python, TypeScript, Rust, SQL, C/C++, Bash
**Rest:** Django, FastAPI, React, Next.js, PostgreSQL, DuckDB, SQLite, Docker, Linux, GCP

## Writing

- [The Work You Don't Do: Losing Two Optimization Competitions the Same Way](https://yashrajpandey.com/writing/the-work-you-dont-do/)
- [Eight Submissions, Zero Promotions: A Week Inside mlx.fast on the Wrong Hardware](https://yashrajpandey.com/writing/eight-submissions-zero-promotions/)
- [I Tried to Break Google's New Tabular Foundation Model. Then I Fixed It.](https://yashrajpandey.com/writing/breaking-google-tabfm/)

Two of those three are about losing. The ratio is roughly right.

---

Outside work: football, tactical FPS, story-rich RPGs, and lo-fi for flow state.
