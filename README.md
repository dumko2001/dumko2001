# Hi, I'm Sidharth 👋

I'm a software engineer based in India. I work across the full stack — shipping production AI systems for clients, and contributing fixes to the open-source tools the ML and agent ecosystem runs on.

- 🔧 I find correctness bugs, silent failures, and security holes in production codebases and fix them
- 🤖 I build AI-native products — pipelines, agents, verification systems, clinical tooling
- 🌏 Open to **full-time remote roles** in Backend, Applied AI, and Full Stack Engineering

---

### 🛠 What I work with

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

### 🔨 Open source

I contribute to the internals of tools I use — compiler stacks, agent runtimes, LLM frameworks. Here's what I've shipped:

**[karpathy/autoresearch](https://github.com/karpathy/autoresearch)** — AI agent framework, 50k ⭐
- [PR #17](https://github.com/karpathy/autoresearch/pull/17) — Self-healing error recovery: agent parses its own stack traces and resumes from OOM/syntax failures without stopping. Contributed within hours of the repo going public. Shopify's CEO ran it overnight and got **53% faster rendering** from 93 automated commits. ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)
- [PR #16](https://github.com/karpathy/autoresearch/pull/16) — Eliminated ~4GB of persistent VRAM overhead per run by switching tanh to native bfloat16 — headroom that matters on a single H100 running 100+ experiments overnight. ![under review](https://img.shields.io/badge/under_review-e6a817?style=flat-square)

**[googleworkspace/cli](https://github.com/googleworkspace/cli)** — Official Google repo, Rust, 20k ⭐ in 2 weeks
- [PR #500](https://github.com/googleworkspace/cli/pull/500) — Eliminated a TOCTOU race condition in atomic writes: OAuth tokens were briefly world-readable between creation and permission enforcement. Enforced `0o600` atomically at creation, closing the leak window for **~21,000 users**. ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)
- [PR #506](https://github.com/googleworkspace/cli/pull/506) — Google Meet integration for `calendar +insert` with deterministic `requestId` hashing — eliminates duplicate Meet links on API retries. ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)
- [PR #542](https://github.com/googleworkspace/cli/pull/542) — Fixed silent auth failure: token directory errors were swallowed, credentials silently never persisted while auth appeared to succeed. ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)

**[NVIDIA/NemoClaw](https://github.com/NVIDIA/NemoClaw)** — NVIDIA agent security stack, 15k ⭐
- [PR #187](https://github.com/NVIDIA/NemoClaw/pull/187) — Enforced `0o600` on `openclaw.json` during migration — session and routing config was world-readable by default. Propagated into **3 downstream forks within 13 hours** of merge. ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)
- [PR #186](https://github.com/NVIDIA/NemoClaw/pull/186) — `chmod 600` on `.env` at sandbox startup — closed the exposure window before any agent process reads secrets. ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)
- [PR #174](https://github.com/NVIDIA/NemoClaw/pull/174) — `chmod 600` on remote `.env` post-SCP during `deploy()` — different attack surface from #186, both were unpatched. ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)

**[pytorch/pytorch](https://github.com/pytorch/pytorch)** — C++ & Python compiler stack, 63% of global model training
- [PR #169128](https://github.com/pytorch/pytorch/pull/169128) — Fixed silent data corruption in Inductor C++ kernels: OpenMP + OpenCV together silently produce wrong training outputs. No error thrown. Affects **63% of global model training**. ![approved](https://img.shields.io/badge/approved-2ea44f?style=flat-square)
- [PR #169786](https://github.com/pytorch/pytorch/pull/169786) / [#169126](https://github.com/pytorch/pytorch/pull/169126) / [#169788](https://github.com/pytorch/pytorch/pull/169788) — `torch.compile` crashes on nested autograd, Conv+BatchNorm FX graph failures, silent `index_select` out-of-bounds corruption — across **~1.57B pip installs**. ![under review](https://img.shields.io/badge/under_review-e6a817?style=flat-square)

**[langchain-ai/langchain](https://github.com/langchain-ai/langchain) & [langgraph](https://github.com/langchain-ai/langgraph)** — LLM frameworks, used by Replit, Uber, LinkedIn, GitLab
- [PR #6509](https://github.com/langchain-ai/langgraph/pull/6509) — Fixed validation crash blocking Generic type hint injection in LangGraph — unblocked `ToolRuntime[Context]` patterns in typed agent pipelines. ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)
- [PR #34046](https://github.com/langchain-ai/langchain/pull/34046) / [#34053](https://github.com/langchain-ai/langchain/pull/34053) / [#34114](https://github.com/langchain-ai/langchain/pull/34114) — Fixed silent tool-calling failures across Mistral, Groq, and Ollama. TypeErrors that caused agent workflows to silently stop on provider switch. **~500k developers monthly.** ![merged](https://img.shields.io/badge/merged-8A2BE2?style=flat-square)

**[kubernetes/kubernetes](https://github.com/kubernetes/kubernetes)** — Go, 5.6M developers, 3M+ production clusters
- [PR #135460](https://github.com/kubernetes/kubernetes/pull/135460) — Modernizing the Device Resource Allocation (DRA) API: migrating `DeviceTaint` and `AllocatedDeviceStatus` to declarative API markers across **~3M production clusters**. ![under review](https://img.shields.io/badge/under_review-e6a817?style=flat-square)

---

### ✨ Highlights

- 🏆 **3rd Place — Splunk Global Hackathon 2025** out of 1,200+ entries — OPA security add-on for real-time threat detection and privilege escalation auditing
- ⚡ **Celer AI** — voice-to-text pipeline for clinicians, medical report generation from 15 minutes to **40 seconds** (95% reduction)
- 🛡️ **Trustful** — hallucination detection layer for insurance data extraction using Gemini + Zod validation. A hallucinated policy number in insurance is a liability, not a UX bug.

---

### 📊 Stats

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=dumko2001&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=dumko2001&layout=compact&theme=tokyonight&hide_border=true&langs_count=6" />
</p>

---

### 📬 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-sidharth--rajmohan-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/sidharth-rajmohan)
[![Email](https://img.shields.io/badge/Email-dumko.raj@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:dumko.raj@gmail.com)
