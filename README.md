<div align="center">

# Sidharth Rajmohan

**Trader turned engineer. I build the environments AI agents train inside.**

![Kochi](https://img.shields.io/badge/Kochi-India-2ea44f?style=flat-square)
![Polymath](https://img.shields.io/badge/Polymath-YC_W26-blue?style=flat-square)
![RL Environments](https://img.shields.io/badge/focus-RL_environments-8957e5?style=flat-square)

[![GitHub](https://img.shields.io/badge/GitHub-dumko2001-181717?style=flat-square&logo=github)](https://github.com/dumko2001)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-sidharth--rajmohan-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/sidharth-rajmohan/)
[![Email](https://img.shields.io/badge/Email-dumko.raj@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:dumko.raj@gmail.com)

</div>

---

I've landed fixes in PyTorch and LangChain. These days I build the environments that AI agents train inside. About a year and a half ago I couldn't have opened any of those PRs. I was trading stocks, options, and futures on the Indian market.

> Around January 2025 I pivoted to building software. I already used AI heavily and wanted to make things with it. Think of it as a second internet moment. I rode it hard.

<details>
<summary><b>&nbsp;How a trader ended up here &nbsp;▾</b></summary>

<br/>

I learned by shipping. An invoice tracker, my first web app. A VC deal-flow tool that sorts startups by what they do. Celer AI, which turns voice into structured medical reports. Alongside that, freelance work for local businesses and friends: websites, feedback trackers, landing pages, small automations.

Open source happened almost by accident. My first PRs landed in LangChain, back in November 2025. Then PyTorch, Kubernetes, LangGraph. A few months later a random fix to Andrej Karpathy's autoresearch got merged, and that was the turning point. People started reaching out. A referral turned into a short gig with a Cambridge professor building benchmarks for rendering efficiency in games. Then Polymath, where I found the work I love.

</details>

---

## 🚀 What I've shipped

Landed and merged, all confirmed in main.

| Project | | Landed work |
|:--|:--|:--|
| **[PyTorch](https://github.com/pytorch/pytorch/pulls?q=is%3Apr+author%3Adumko2001)** | | Silent `max_autotune` BMM correctness bug under dynamic OpenMP threads, and an `efficient_conv_bn_eval` crash. Approved by core maintainers jansel and eellison. &nbsp;·&nbsp; [#169128](https://github.com/pytorch/pytorch/pull/169128) [#169126](https://github.com/pytorch/pytorch/pull/169126) |
| **[LangChain](https://github.com/langchain-ai/langchain)** | | Provider-prefix decoupling in `init_chat_model`, kwargs override for Groq structured output, unsupported-arg fix in `ChatOllama`. &nbsp;·&nbsp; [#34046](https://github.com/langchain-ai/langchain/pull/34046) [#34053](https://github.com/langchain-ai/langchain/pull/34053) [#34114](https://github.com/langchain-ai/langchain/pull/34114) |
| **[LangGraph](https://github.com/langchain-ai/langgraph)** | | Generic type-argument support for `ToolRuntime` injection. &nbsp;·&nbsp; [#6509](https://github.com/langchain-ai/langgraph/pull/6509) |
| **[autoresearch](https://github.com/karpathy/autoresearch)** `★ 90.9k` | | Fixed an agent crash blindspot by forcing it to read the traceback before retrying. The turning point. &nbsp;·&nbsp; [#17](https://github.com/karpathy/autoresearch/pull/17) |
| **[Google Workspace CLI](https://github.com/googleworkspace/cli)** `★ 26.4k` | | Closed a TOCTOU race in atomic writes, added Meet to calendar insert, propagated auth errors on token-dir failure. &nbsp;·&nbsp; [#500](https://github.com/googleworkspace/cli/pull/500) [#506](https://github.com/googleworkspace/cli/pull/506) [#542](https://github.com/googleworkspace/cli/pull/542) |
| **[NVIDIA/NemoClaw](https://github.com/NVIDIA/NemoClaw)** `★ 20.6k` | | Five security fixes hardening file permissions across deploy, startup, migration, and auth. &nbsp;·&nbsp; [#174](https://github.com/NVIDIA/NemoClaw/pull/174) [#183](https://github.com/NVIDIA/NemoClaw/pull/183) [#186](https://github.com/NVIDIA/NemoClaw/pull/186) [#187](https://github.com/NVIDIA/NemoClaw/pull/187) [#188](https://github.com/NVIDIA/NemoClaw/pull/188) |
| **[Prime Intellect verifiers](https://github.com/PrimeIntellect-ai/verifiers)** | | Made usage tracking tolerate providers that omit `cache_write_tokens`. &nbsp;·&nbsp; [#2019](https://github.com/PrimeIntellect-ai/verifiers/pull/2019) |

> **PyTorch lands work by rebase, so those two show as "closed" on GitHub. The commits are in main.** Worth knowing when you scan the profile.

Also 17 merged fixes to [clawmetry](https://github.com/vivekchand/clawmetry) (556k+ PyPI downloads): proxy and dashboard concurrency, security, caching.

**In review** across PyTorch (Inductor and CUDA), vLLM, LangGraph, Kubernetes, Supabase, and the Anthropic Claude Agent SDK. &nbsp;[Full PR list →](https://github.com/search?q=author%3Adumko2001+type%3Apr&type=pullrequests)

---

## 🎮 Building RL environments

At Polymath we build the gyms where AI agents train. Simulated worlds for teaching agents real digital work.

> I got asked to build one. I built several. Couldn't stop.

Here's the craft, learned through fast feedback. Make the verifier behavioral, so it grades what the agent actually does. A good environment sits at the exact edge of what a model can do. Tune the difficulty so a strong model lands mid pass-rate. That's where GRPO has signal to climb. The same way people learn at the edge of what they can already do.

---

## 🧠 How I think

`first principles` &nbsp; `Feynman technique` &nbsp; `Pareto` &nbsp; `efficient frontier` &nbsp; `unknown unknowns`

First principles is the one I lean on most. I learn broadly and fast by going deep on whatever grabs me.

## 🛠 Tools I reach for

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

---

<div align="center">

![Auto-audited](https://img.shields.io/badge/auto--audited_by_AI-monthly-6f42c1?style=flat-square)

<sub>🤖 An AI agent re-checks every PR's real merge status and refreshes this page each month, so it never goes stale. Contributions verified against GitHub, PyPI, and npm. Last updated July 2026.</sub>

</div>
