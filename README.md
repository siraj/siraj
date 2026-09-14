# 👾 Siraj Razick

```text
┌──────────────────────────────────────────────────────────────┐
│ SYSTEMS ENGINEER :: LOW-LEVEL GRAPHICS :: AI :: INFRA       │
└──────────────────────────────────────────────────────────────┘
```

Systems engineer working across low-level graphics, developer tooling, distributed systems, fintech infrastructure, and AI agents.

I have been building software since the KDE 3/4 era, mostly in C and C++, with later work spanning Python, TypeScript, Go, Linux infrastructure, GPU workloads, and modern agent systems.

`[ GITHUB ]` https://github.com/siraj  ·  `[ CLOUDGPU ]` https://cloudgpu.io  ·  `[ PLEXYDESK ]` https://github.com/plexydesk

---

## 🎮 What I work on

### 🖥️ Systems and graphics

My strongest background is in systems software: desktop shells, display-server work, rendering, input, terminals, build systems, packaging, and platform integration.

```text
[ C/C++ ] [ WAYLAND ] [ X11/XWAYLAND ] [ QT ] [ GSTREAMER ] [ POSIX ]
```

Areas I have worked deeply in include:

- C and C++ systems programming
- Wayland and compositor architecture
- keyboard/input stacks
- text rendering and font shaping
- terminal emulation and PTY integration
- GPU-aware applications and runtime constraints
- Linux packaging and reproducible builds
- Qt, GStreamer, X11/Xwayland, browser-engine codebases

Today, much of that work continues around **PlexyDesk**, where I focus on display-server and desktop-system engineering.

### 🌐 Browser engines and platform code

Earlier in my career I worked inside the codebases behind **WebKit, Google Chrome / Chromium, and Firefox / Gecko**.

```text
┌─ BROWSER SYSTEMS ────────────────────────────────────────────┐
│ rendering · input · graphics · APIs · platform integration │
└──────────────────────────────────────────────────────────────┘
```

That experience was less about shipping a standalone browser and more about learning how browser engines are actually built: large C++ systems with rendering, layout, input, graphics, platform abstraction, API compatibility, performance constraints, and an enormous amount of cross-platform behaviour living in the same tree.

I worked in areas around browser APIs, rendering and compositing behaviour, UI/input handling, and platform integration. I deliberately keep the profile at that level rather than turning it into a list of individual patches.

The lasting skills from that period are still directly relevant to the work I do now:

- navigating and modifying very large C++ codebases
- understanding rendering and event pipelines end to end
- debugging behaviour that crosses framework, OS, and graphics boundaries
- maintaining compatibility across platforms and API layers
- working with mature review processes and upstream maintainers
- reasoning about performance-sensitive, user-visible systems

Browser-engine work was also an important bridge between my KDE years and the later display-server work. It reinforced my interest in the layers underneath applications: rendering, input, graphics, process boundaries, and platform plumbing.

### 🤖 AI agents and developer tooling

More recently I have been building agent runtimes and developer tools, with an emphasis on keeping the underlying systems small, understandable, and portable.

```text
[ AGENT LOOP ] → [ TOOLS ] → [ MODEL ] → [ SYSTEM ]
```

The work spans:

- agent loops and tool execution
- model-provider integration
- retrieval and context management
- local and remote inference
- native plugins and extensibility
- coding and system-administration workflows
- CLI, shell, and editor integration
- GPU-backed inference infrastructure

A lot of this work sits under the **cloudgpu.io** umbrella.

### 💾 Fintech and production infrastructure

I spent several years working on regulated financial infrastructure and Bitcoin-related systems. That work involved production services where reliability, auditability, authentication, payments, cryptography, messaging, and deployment discipline mattered more than novelty.

It gave me long-term experience with:

- payment and settlement systems
- authentication and identity flows
- cryptographic service integration
- event-driven and message-based systems
- GraphQL and service APIs
- database migrations and operational tooling
- Docker-based deployment environments
- software that has to survive security review

I keep the internal architecture and implementation details of that work private, but the engineering discipline from it still shapes how I build systems today.

---

## 🕹️ Open-source roots

I started contributing to open source during the KDE 3 and KDE 4 transition.

### 🐧 KDE / Plasma

My early work included KDE desktop components, Plasma-related code, SVG-based UI experiments, desktop launchers, build fixes, and supporting libraries.

Projects from that period include **KBFX**, **Raptor / Plasmic-Raptor**, and upstream work across KDE repositories.

That period taught me most of the habits I still value: reading unfamiliar code, working inside large projects, taking review seriously, and fixing the layer underneath the visible bug.

### 🌍 Browser-engine contributions

I also contributed upstream work around **WebKit, Chromium / Google Chrome, and Firefox / Gecko**.

Rather than listing individual bugs or patches here, I prefer to describe the engineering experience it gave me: working inside mature browser stacks, understanding rendering and input paths, dealing with cross-platform behaviour, and getting changes through established upstream review processes.

For me, that period was where desktop systems work expanded into browser systems work—and where I became comfortable operating inside codebases large enough that no single person can hold the whole architecture in their head.

### 🔧 Other systems work

Over the years I have also worked on projects involving:

- GStreamer and QNX
- XMPP libraries and services
- parser and grammar experiments
- macOS I/O Kit
- Bitcoin infrastructure
- Linux desktop tooling
- GPU utilities
- native hardware-control software

---

## 🧩 Selected public work

### 🖥️ PlexyDesk

[PlexyDesk](https://github.com/plexydesk) is where much of my current low-level systems work lives.

My work there has included areas such as input, rendering, terminal behaviour, GPU/runtime management, desktop utilities, launcher behaviour, Xwayland integration, and keeping the environment reproducible.

The interesting part for me is not any single feature. It is the interaction between all of them: input, rendering, process management, memory, latency, compatibility, and user-visible behaviour all meet in the same place.

### ☎️ GoogleVoice

[GoogleVoice](https://github.com/siraj/GoogleVoice) is an older C++ project from a very different era of the web. It involved building a native interface around a service that did not offer the kind of official integration surface developers would expect today.

### 📷 insta360link-controller

[insta360link-controller](https://github.com/siraj/insta360link-controller) is an example of the kind of software I still enjoy building: small, practical tooling that gives users direct control over hardware.

### ⚡ cloudgpu.io

[cloudgpu.io](https://cloudgpu.io) is where I am exploring GPU infrastructure, AI tooling, and agent systems.

I am especially interested in reducing the amount of framework machinery between a model and the system it is supposed to operate.

---

## 🧠 Core stack

```text
┌──────────── SYSTEMS ────────────┬──────────── SERVICES ────────────┐
│ C · C++ · Linux · Wayland      │ Python · TypeScript · Go         │
│ Qt · X11/Xwayland · GStreamer  │ PostgreSQL · GraphQL · REST      │
├──────────── INFRA ──────────────┼──────────── AGENTS ──────────────┤
│ Docker · CI/CD · packaging     │ tool calling · RAG · inference   │
│ GPU runtimes · serverless      │ context · local/remote models    │
└─────────────────────────────────┴───────────────────────────────────┘
```

I am comfortable moving between low-level and product-level work. A typical project can take me from debugging a rendering or process issue to designing an API, writing a CLI, packaging a release, or building the interface around it.

---

## 🧱 How I tend to build

```text
> understand the system first
> keep dependencies deliberate
> make behaviour observable
> prefer boring reliability
> automate releases early
> keep source → running software understandable
> use AI as a tool, not a substitute for understanding
```

---

## 🚀 Current interests

```text
[01] native AI-agent runtimes
[02] developer and sysadmin agents
[03] GPU-backed applications and inference
[04] Wayland and desktop-system engineering
[05] terminal-first tools
[06] small infrastructure products
```

I still enjoy the same class of problem I started with: software sitting close enough to the system that the abstractions eventually run out.

```text
╔══════════════════════════════════════════════════════════════╗
║                    CONTINUE?  [Y] / [N]                    ║
╚══════════════════════════════════════════════════════════════╝
```