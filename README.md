<!-- 
  ✨ siraj/siraj — The Work Journey ✨
  A blog-style chronicle of 17+ years of shipping software.
  🤖 This profile was generated & maintained by hola-ai-agent (hola-coder)
  → https://github.com/cloudgpu/hola-releases
-->

<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=58A6FF&center=true&vCenter=true&random=false&width=560&lines=Hi%2C+I'm+Siraj+Razick+%F0%9F%91%8B;I+build+display+servers%2C+AI+agents+%26+fintech;From+C+kernels+to+TypeScript+apps;17%2B+years+of+shipping+software" alt="Typing SVG" />
</h1>

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-siraj-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/siraj)
[![cloudgpu.io](https://img.shields.io/badge/☁️_cloudgpu.io-GPU_Cloud_Tools-9146FF?style=for-the-badge)](https://cloudgpu.io)
[![PlexyDesk](https://img.shields.io/badge/🖥️_PlexyDesk-Wayland_Display_Server-2ea44f?style=for-the-badge)](https://github.com/plexydesk)
[![Location](https://img.shields.io/badge/📍-Montreal%2C+Canada-E34F26?style=for-the-badge)](#)
[![Followers](https://img.shields.io/github/followers/siraj?style=for-the-badge&color=blue&logo=github)](https://github.com/siraj?tab=followers)

</div>

---

> ### 📖 This profile is a **work journal** — not a résumé.
> Below is the actual journey, era by era: what I built, why it mattered, and
> what each project taught me. Skip the buzzwords — this is the real work.

<br/>

```text
   Montreal, Canada  ·  GitHub since 2008  ·  155 public repos  ·  295 PRs  ·  27 orgs
   Languages I think in: C · C++ · TypeScript · Go · Python · Assembly
```

<br/>

## 🗺️ The Journey at a Glance

| Era | Years | Theme |
|---|---|---|
| 🧱 [The Systems Years](#-chapter-1--the-systems-years-20082014) | 2008–2014 | C/C++ libraries, build systems, GStreamer, QNX |
| 🏦 [The Fintech Years](#-chapter-2--the-fintech--blockchain-years-20192022) | 2019–2022 | Bitcoin infrastructure, regulated payments, PSD2 |
| 🚀 [The Product Years](#-chapter-3--the-product--app-years-20232025) | 2023–2025 | TypeScript platforms, AI-assisted workflows |
| 🖥️ [The PlexyShell Years](#-chapter-4--the-plexyshell-years-2025) | 2025– | A Wayland display server from scratch — 934 commits |
| 🤖 [The Agent Era](#-chapter-5--the-agent-era-2026) | 2026– | Hola: a C library for AI agents + cloudgpu.io |

<br/>

---

# 🧱 Chapter 1 — The Systems Years (2008–2014)

> Where it all started: **C, C++, autotools, GStreamer, and the humble
> conviction that software should build cleanly on any Unix.**

### 🔊 `gstaudiosinkqnx` — GStreamer audio sink for QNX (2013)
A **GStreamer audio sink element for QNX** — real embedded-systems work.
Writing a GStreamer element means living inside the pipeline graph: negotiating
caps, handling clock drift, and pushing buffers without stalling the chain.
Doing it for **QNX** (the RTOS that runs cars and medical devices) meant
learning a completely different audio stack from the ground up. This project
taught me that *audio latency is a systems-design problem*, not a driver problem.

### 📞 `GoogleVoice` — A C++ API to interact with Google Voice (2012)
One of my most-starred projects: a **native C++ API for Google Voice** —
before official APIs existed, this meant reverse-engineering the web
endpoints, managing session cookies, and building a clean C++ wrapper around
a moving target. It became a reference for anyone wanting to integrate
Google Voice into native applications.

### 🔌 `loudmouthcmake` — CMake build files for Loudmouth (2009)
My **first public repo**: modern CMake build files for the Loudmouth XMPP
client library. Even in 2009 I was already fixing build systems — a theme
that would return 15 years later with PlexyDesk.

### 🧪 `cssparser` — Experimental CSS parser (2012)
An **experimental CSS parser based on lex/yacc grammar specifications** —
a deep dive into formal grammars, tokenizers, and the surprisingly tricky
CSS cascade. Pure parser-theory work applied to a real-world format.

### 🖼️ `ioproxyvideofamily` — I/O Kit video family (2015)
A macOS **I/O Kit video family driver** — kernel-adjacent work on how
video devices present themselves to the operating system.

### 💬 The XMPP thread
Loudmouth → `txmpp` (a **C++ XMPP library**) → later a full **XMPP server**.
Messaging protocols became a decade-long thread through my work: presence,
streams, and the elegance of XML stanzas.

<br/>

---

# 🏦 Chapter 2 — The Fintech & Blockchain Years (2019–2022)

> Four years building a **regulated Bitcoin settlement platform** —
> where "production" means real money, real audits, and zero tolerance for bugs.

### ₿ `ArmoryDB` — Headless Bitcoin database runtime (2019–2020)
I forked **ArmoryDB** (the famous Bitcoin Armory wallet engine) and produced a
**headless runtime** that the platform's trading system fully supported.
This is a **116 MB C++ codebase**: memory-mapped blockchain parsing, Bitcoin
Core integration, and a distributed database. My work covered:

- **Producing the headless runtime** — stripping the wallet UI while keeping the full blockchain-indexing engine
- **Binary distribution** — Ubuntu PPA, Windows, and macOS builds
- **`armorydb_installer`** — a full **NSIS installer** (~50 MB of packaging work) for Windows deployments
- The delicate **memory-map contract**: ArmoryDB must run alongside a synced Bitcoin Core node on the same storage device

### 🧩 `common` — Settlement system core (2020)
The **shared code layer for the entire settlement system** (~19 MB) — the
protocol definitions, cryptographic primitives, and common utilities that
every downstream service linked against. When you touch `common`, every
service downstream feels it.

### 🔐 `login-server` — Authentication service (2021–2022)
A **Python authentication and session service** for the settlement
ecosystem — session management, secure login flows, and the supporting
test harness (`login-server-test-session`).

### 💱 `daytrader` — Trading engine (2022)
A **Python trading engine** (~600 KB) built for the platform's dealer
infrastructure — order handling and market-facing logic.

### 🏗️ The wider fintech constellation
Around this core I built and maintained the connective tissue of a regulated
financial platform — **295 pull requests** of pure engineering:

- **Merchant payment pipelines** — ~70 merged PRs across gateway services: deposit reference handling, operation IDs surfaced through GraphQL, KYC data plumbing for admin, cookie/session lifecycle, and ping/pong + channel invalidation for live connections
- **Cryptographic orchestration** — multi-party signing orchestration improvements: sign recovery, orchestrator module updates, Cap'n Proto protocol revisions with network source/destination fields, and BFX wallet integration
- **BankID & eID authentication** — yielded BankID results on async awaits, removed deprecated v6 redirect URLs, fixed mobile connection compilation, and hardened RMQ message handling
- **PSD2 open-banking infrastructure** — scaled HTTP request handling in the PSD2 proxy and stabilized its SQL watcher for reliable transaction monitoring
- **Webhook reliability** — refactored the WebhookEmitter to persist message retries across restarts, plus GC-error fixes on socket clearing
- **Payouts & migrations** — payout flows, Alembic migration setup, and account-selection new-flow work in the merchant orchestrator
- **Reproducible infrastructure** — Docker-based setup for the entire settlement stack

> 🎓 **What this era taught me:** regulated fintech is where "it works on my
> machine" goes to die. Every change is staged, audited, and signed. I learned
> to write code that survives security review — and to love it.

<br/>

---

# 🚀 Chapter 3 — The Product & App Years (2023–2025)

> Stepping out of pure infrastructure: building **complete products** with
> modern TypeScript stacks, and teaching AI to help write novels.

### 🛒 `hello-goods-market` — Marketplace platform (2025)
A **TypeScript marketplace application** (~500 KB) — the full arc of a
commerce product: listings, transactions, and the UX glue in between.

### 📈 `autobid-mobile-enhancer` — Auction tooling (2025)
A **TypeScript mobile enhancement layer** (~540 KB) for the autobid
ecosystem — bringing real-time bidding workflows to mobile clients.

### 🌒 `darktradehub` — Trading hub (2025)
A **TypeScript trading hub** (~215 KB) — dark-pool-style trading interfaces
with live market data.

### 🎙️ `audio-forge-studio-pro` — Audio production suite (2025)
A **TypeScript audio production application** (~280 KB) — a DAW-style
toolchain for recording, editing, and mastering workflows.

### 📖 `armor-protocol` — AI-assisted novel generation (2025)
One of my favourite experiments: a **Python system for AI-assisted
novel generation** — *The Armor Protocol*, a 48-chapter story about AI,
human purpose, and the need to act. This isn't a prompt wrapper — it's a
**5 MB pipeline** for chapter-by-chapter generation with continuity
tracking, character state, and narrative constraints.

### 🛠️ `hermes-daily-log` — Agent memory tracking (2026)
**Daily events, skills, and memory tracking for the Hermes agent** —
infrastructure for AI agents that need to remember what they did and
learn from it.

<br/>

---

# 🖥️ Chapter 4 — The PlexyShell Years (2025–)

> **934 commits.** A Wayland display server, a terminal, a shell — built
> from source, for GNU/Linux. This is the deepest systems work of my career.

<div align="center">

🖥️ **PlexyDesk Display Server** — *private development, public showcase: [plexydesk/plexydesk](https://github.com/plexydesk/plexydesk)*

</div>

### What PlexyShell is

**PlexyDesk is a local Wayland compositor stack** — a repo-built
`gnu-liquid-shell`, `wayland_bridge`, `plexy_term`, and `Xwayland`. The
build model is radical: **Debian provides only headers and build tools;
the entire runtime stack is built from source into the repo** — `wayland`,
`wayland-protocols`, `libdrm`, `libweston`, and `Xwayland` itself from the
`xserver/` tree. The runtime wrapper **rejects system fallbacks** when a
local replacement exists. Hermetic, reproducible, and unapologetically
hardcore.

### 🧩 My contributions — the real work

| Contribution | What it took |
|---|---|
| ⌨️ **libxkbcommon keyboard stack** | Replaced hardcoded keycode mappings with **libxkbcommon** for proper keyboard layout support — the difference between "it types" and "it types *correctly* on any layout" |
| 🎮 **GPU profile detection + VRAM budgets** | Implemented GPU profile detection, VRAM budget configuration, and **VRAM budget tracking and limits** — the compositor now knows its own memory envelope |
| ✍️ **Pango/HarfBuzz/FreeType text engine** | Implemented the full **text rendering stack**: shaping (HarfBuzz), layout (Pango), rasterization (FreeType) — complex scripts render correctly |
| 🖥️ **VT100/xterm terminal emulation** | Full **VT100/xterm compatibility with scrollback buffer** for `plexy_term` — escape sequences, cursor addressing, alternate screens, the works |
| 🔌 **PTY & shell integration** | Improved PTY and shell integration with proper **terminal modes** handling |
| 🚀 **Native fuzzy launcher (prunner)** | A **native Plexy launcher with fuzzy search** — instant app launching, zero external dependencies |
| 🧮 **pcalc — scientific calculator** | Refactored into a **native PlexyShell scientific calculator** |
| 🎨 **Cool Dock port** | Ported and refined **Cool Dock features** onto the server dock |
| 🖱️ **Xwayland game mouse grabbing** | Stability fixes for **mouse grabbing in games** running through Xwayland |
| 🧹 **Repository hygiene** | Untracked generated icons, verified `.gitignore` coverage for all build artifacts |

> 🎓 **What this era taught me:** a display server is the most unforgiving
> kind of software — every millisecond is visible, every leak is a crash,
> and the keyboard is harder than the GPU.

<br/>

---

# 🤖 Chapter 5 — The Agent Era (2026–)

> **Hola** — a small C library for building conversational AI agents.
> No Python, no Node, no framework tax. Just C, plugins, and an agent loop.

<div align="center">

🤖 **hola-ai-agent** — *private source, public binaries via [hola-releases](https://github.com/cloudgpu/hola-releases)*

</div>

### 🤖 `hola-ai-agent` — The Hola agent framework

Under **[cloudgpu.io](https://cloudgpu.io)** I designed and built **Hola** —
a **C library for building conversational AI agents**, plus reference
applications that prove the design:

- **`hola_core/`** — the library you link against: the **agent loop**, a
  **tool registry**, **prompt assembly**, providers for **OpenAI-compatible
  and local models**, **session storage**, and a **C plugin loader** — add
  new tools without rebuilding the binary
- **`hola-coder`** — an **agentic coding tool** that explores code, edits
  with search/replace, runs builds and tests, and does git operations
- **`hola-admin`** — a **sysadmin agent** that inspects systems, reads
  logs, runs safe diagnostics, and writes scripts
- **Shell + editor integration** — Zsh helpers (`hola-suggest`,
  `hola-explain`, `hola-chat`) and a **Vim/Neovim plugin**
- **Release engineering** — sandboxed Docker builds producing `.deb`,
  `.rpm`, Arch packages, macOS and Windows binaries, all published through
  a one-line installer:

```bash
# Linux / macOS / FreeBSD
curl -fsSL https://raw.githubusercontent.com/cloudgpu/hola-releases/main/install.sh | sh
```

- **Current research** — an open PR for a **token-budgeted compact
  retrieval optimizer** in the RAG pipeline: fitting maximum context value
  into a fixed token budget

### ⚡ `oxy` — GPU cloud CLI
A **command-line tool for GPU cloud access** — drive GPU instances
straight from the terminal, the cloudgpu.io way.

### 🔊 `demucs-runpod` / `demucs-server` — Serverless GPU audio
**Audio source separation on serverless GPU** — upload a track, get stems
back, pay per second. Built on RunPod with the Demucs model.

### 🎛️ `gpu_ctl_app` — Native GPU control
A **C++ application for GPU control** — the systems-programmer's answer
to GPU management.

### 🧠 Other agent-adjacent work
- **`hola-miner`** — Python mining tooling in the Hola ecosystem
- **`guc-server`** — a **multi-user image-edit server** (Tornado + React +
  Postgres + RunPod, ~2.2 MB): upload, edit with AI models, manage users
  and jobs
- **`recamera-api`** — a **serverless video re-camera API**: upload a
  monocular video, get it back from any camera angle (TrajectoryCrafter /
  ReCamMaster on RunPod)
- **`insta360link-controller`** — a **daemon, CLI, and optional firmware**
  for controlling an Insta360 Link webcam without the first-party software
  — because hardware should obey *you*

<br/>

---

# 🌍 Open Source Contributions

> Beyond my own repos: **295 pull requests** across the GitHub ecosystem —
> here are the ones that matter.

| Project | Contribution |
|---|---|
| 🖥️ **PlexyDesk Display Server** *(org: [plexydesk](https://github.com/plexydesk))* | **15 PRs, 934 commits** — libxkbcommon keyboard support, GPU/VRAM budgeting, Pango/HarfBuzz/FreeType text engine, full VT100/xterm terminal, PTY modes, fuzzy launcher, pcalc, Cool Dock |
| 💳 **Merchant payment systems** | **~70 merged PRs** — payment pipelines, deposit references, GraphQL operation IDs, KYC data plumbing, cookie/session lifecycle, channel invalidation |
| 🔑 **Cryptographic orchestration** | Multi-party signing recovery, orchestrator updates, Cap'n Proto protocol revisions, BFX wallet integration, web3 bridge |
| 🪪 **BankID / eID authentication** | Async BankID result yielding, deprecated flow removal, RMQ handling hardening, Swedish eID authentication fixes |
| 🏛️ **PSD2 open banking** | HTTP request scaling in PSD2 proxy, stable SQL transaction watcher |
| 🔁 **Webhook reliability** | WebhookEmitter refactored to persist message retries across restarts |
| 💸 **Payouts & migrations** | Payout flows, Alembic migration infrastructure, account-selection flows |
| 🤖 **AI agent framework (Hola)** | RAG token-budgeted retrieval optimizer, surveillance platform prototype |
| 🐧 **Community forks maintained** | `plymouth-themes` (80+ Android bootanimation themes ported), `Bluecurve` (Red Hat theme for GTK 3/4), `kwin-effects-forceblur` (Plasma 6 blur), `Linux-on-Samsung` (GPU-accelerated Linux on Galaxy), `MacQuake` (native Quake for Apple Silicon) |

<br/>

---

# 📊 The Numbers

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=siraj&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&count_private=true" alt="GitHub stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=siraj&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117" alt="Top languages" />

<br/>

[![GitHub Streak](https://streak-stats.demolab.com?user=siraj&theme=tokyonight&hide_border=true&background=0D1117)](https://git.io/streak-stats)

<br/>

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=siraj&theme=tokyo-night&hide_border=true&bg_color=0D1117&area=true)](https://github.com/siraj)

<br/>

🤖 **hola-ai-agent** — *private source, public binaries via [hola-releases](https://github.com/cloudgpu/hola-releases)*

[![GoogleVoice](https://github-readme-stats.vercel.app/api/pin/?username=siraj&repo=GoogleVoice&theme=tokyonight&hide_border=true&bg_color=0D1117)](https://github.com/siraj/GoogleVoice)
[![insta360link-controller](https://github-readme-stats.vercel.app/api/pin/?username=siraj&repo=insta360link-controller&theme=tokyonight&hide_border=true&bg_color=0D1117)](https://github.com/siraj/insta360link-controller)

</div>

<br/>

## 🐍 Contribution Snake

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/siraj/siraj/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/siraj/siraj/output/github-snake.svg" />
  <img alt="Contribution Snake" src="https://raw.githubusercontent.com/siraj/siraj/output/github-snake.svg" />
</picture>

<br/>

<div align="center">

![Profile views](https://komarev.com/ghpvc/?username=siraj&color=58A6FF&style=for-the-badge&label=PROFILE+VIEWS)

**"From C kernels to AI agents — the journey continues."**

🤖 *This profile was generated & is maintained by* **[hola-ai-agent](https://github.com/cloudgpu/hola-releases)** *(hola-coder)*

⭐️ From [siraj](https://github.com/siraj) — *Montreal, 2026*

</div>
