# Siraj Razick

Systems engineer working across low-level graphics, developer tooling, distributed systems, fintech infrastructure, and AI agents.

I have been building software since the KDE 3/4 era, mostly in C and C++, with later work spanning Python, TypeScript, Go, Linux infrastructure, GPU workloads, and modern agent systems.

[GitHub](https://github.com/siraj) · [cloudgpu.io](https://cloudgpu.io) · [PlexyDesk](https://github.com/plexydesk)

---

## What I work on

### Systems and graphics

My strongest background is in systems software: desktop shells, display-server work, rendering, input, terminals, build systems, packaging, and platform integration.

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

### AI agents and developer tooling

More recently I have been building agent runtimes and developer tools, with an emphasis on keeping the underlying systems small, understandable, and portable.

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

### Fintech and production infrastructure

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

## Open-source roots

I started contributing to open source during the KDE 3 and KDE 4 transition.

### KDE / Plasma

My early work included KDE desktop components, Plasma-related code, SVG-based UI experiments, desktop launchers, build fixes, and supporting libraries.

Projects from that period include **KBFX**, **Raptor / Plasmic-Raptor**, and upstream work across KDE repositories.

That period taught me most of the habits I still value: reading unfamiliar code, working inside large projects, taking review seriously, and fixing the layer underneath the visible bug.

### WebKit and Firefox

I also contributed patches to **WebKit** and **Firefox/Gecko**, working around browser UI behaviour, APIs, rendering-related code, and platform integration.

That was my first exposure to very large C++ codebases maintained by distributed engineering teams.

### Other systems work

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

## Selected public work

### PlexyDesk

[PlexyDesk](https://github.com/plexydesk) is where much of my current low-level systems work lives.

My work there has included areas such as input, rendering, terminal behaviour, GPU/runtime management, desktop utilities, launcher behaviour, Xwayland integration, and keeping the environment reproducible.

The interesting part for me is not any single feature. It is the interaction between all of them: input, rendering, process management, memory, latency, compatibility, and user-visible behaviour all meet in the same place.

### GoogleVoice

[GoogleVoice](https://github.com/siraj/GoogleVoice) is an older C++ project from a very different era of the web. It involved building a native interface around a service that did not offer the kind of official integration surface developers would expect today.

### insta360link-controller

[insta360link-controller](https://github.com/siraj/insta360link-controller) is an example of the kind of software I still enjoy building: small, practical tooling that gives users direct control over hardware.

### cloudgpu.io

[cloudgpu.io](https://cloudgpu.io) is where I am exploring GPU infrastructure, AI tooling, and agent systems.

I am especially interested in reducing the amount of framework machinery between a model and the system it is supposed to operate.

---

## Core stack

**Systems:** C, C++, Linux, Wayland, Qt, X11/Xwayland, GStreamer, POSIX

**Application / services:** Python, TypeScript, Go, PostgreSQL, GraphQL, REST

**Infrastructure:** Docker, Linux packaging, CI/CD, GPU runtimes, serverless workloads

**AI / agents:** model APIs, local inference, tool-calling systems, RAG, context management, agent tooling

I am comfortable moving between low-level and product-level work. A typical project can take me from debugging a rendering or process issue to designing an API, writing a CLI, packaging a release, or building the interface around it.

---

## How I tend to build

A few principles have stayed consistent across very different projects:

- understand the underlying system before adding abstraction
- keep dependencies deliberate
- make behaviour observable and debuggable
- prefer boring reliability over clever fragility
- automate builds and releases early
- keep the path from source code to running software understandable
- use AI as an engineering tool, not as a substitute for understanding the system

---

## Current interests

Right now I am spending most of my time around:

- native AI-agent runtimes
- developer and sysadmin agents
- GPU-backed applications and inference
- Wayland and desktop-system engineering
- terminal-first tools
- small infrastructure products

I still enjoy the same class of problem I started with: software sitting close enough to the system that the abstractions eventually run out.