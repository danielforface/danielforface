# Daniel Cohen

**AI Systems & Infrastructure Engineer · Systems Software · GenAI Automation**

> I build systems from user workflow down to runtime and hardware.

My work sits at the intersection of **AI implementation, infrastructure, systems software, automation, and low-level engineering**. I am strongest when a problem is broad, ambiguous, and crosses layers: requirements, architecture, implementation, debugging, validation, deployment, and technical communication.

[LinkedIn](https://www.linkedin.com/in/danielforface) · [Aura](https://github.com/danielforface/aura-lang) · [AetherOS](https://github.com/danielforface/AetherOS-Showcase) · [Engineering Evidence Index](ENGINEERING_EVIDENCE.md)

---

## Where I fit best

### AI Systems / Infrastructure / Solutions

I build and integrate AI-enabled systems across application, infrastructure, automation, and operational layers. My background includes Linux/Windows administration, hardware and networking, full-stack systems, DevOps workflows, AI-assisted engineering, and end-to-end technical troubleshooting.

Typical fit: **AI Infrastructure Engineer · AI Solutions Engineer · AI Implementation / Enablement Engineer · Forward Deployed Engineer**

### Systems Software / Runtime / Developer Tools

I also work close to the machine: Rust, x86_64, bare metal, GPU/CPU inference, compiler architecture, formal verification, native networking, and runtime/tooling design.

Typical fit: **Systems Software Engineer · Rust Engineer · Runtime / Edge AI Engineer · Compiler / Developer Tools Engineer**

---

## Selected engineering work

### [Aura](https://github.com/danielforface/aura-lang) — proof-driven systems programming platform

A substantial Rust language-platform monorepo built around the idea that program verification should live inside the normal edit → build → run workflow.

Public engineering surface includes:

- 22 Rust workspace members spanning lexer, parser, AST, semantic core, IR, verifier, runtimes, backends, package tooling, LSP, SDK and plugins
- Z3-backed verification paths, contracts, invariants, structured counterexamples and proof-oriented diagnostics
- C-oriented native backend and an evolving LLVM IR backend
- Aura Sentinel desktop IDE and language-server integration
- Android build/runtime tooling and release infrastructure
- a documented seven-workflow CI validation matrix

**Status:** active, pre-stable language platform. Public claims are intentionally bounded by implementation and validation evidence.

[Repository](https://github.com/danielforface/aura-lang) · [Project Status](https://github.com/danielforface/aura-lang/blob/main/PROJECT_STATUS.md) · [Website](https://aura.geniuses.team/)

### [AetherOS](https://github.com/danielforface/AetherOS-Showcase) — bare-metal AI inference research system

A Rust-first `#![no_std]` x86_64 AI operating system / inference research system built to explore what happens when the inference stack owns the path to silicon directly instead of sitting on a conventional host OS and user-mode GPU stack.

Publicly documented and hardware-validated areas include:

- direct Intel Gen9 RCS / GPGPU command submission
- AVX2 multi-core inference paths
- GGUF transformer execution and quantized Q4_K / Q6_K kernels
- USB/NVMe, memory, paging, telemetry, synchronization and model-residency work
- bit-exact GPU/CPU qualification methodology
- physical-hardware benchmark lineage on Intel Core i3-10110U + UHD 620
- peak verified clean 128-token end-to-end decode of approximately **3.411 tokens/s** in the public evidence set

The complete kernel implementation is private; the public repository is deliberately an **architecture, proof, validation and performance showcase**.

[Repository](https://github.com/danielforface/AetherOS-Showcase) · [Performance](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/08-performance.md) · [Proof Matrix](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/09-proof-matrix.md)

### [NexusP2P / XLINK](https://github.com/danielforface/XLINK) — native Rust remote-support engine

A Windows-focused remote-support system implemented as a Rust workspace with separate core, network, display, and input layers.

- QUIC transport
- certificate fingerprint pinning
- explicit multi-gate consent flow
- DXGI Desktop Duplication
- session-gated Win32 input injection
- native desktop GUI, connection-file and QR workflows
- production build and validation scripts

### [Telegram Cloudifier](https://github.com/danielforface/TelegramDrive) — MTProto cloud-style file environment

A Next.js / TypeScript application that turns Telegram into a cloud-style file-management environment.

- direct MTProto integration
- client-side authentication and session handling
- chat/media browsing
- virtual filesystem concepts over Telegram storage channels
- upload/download management and cloud-style organization

---

## Engineering approach

- **Evidence before claims.** Implemented, tested, hardware-verified and production-promoted are different states.
- **Architecture before surface polish.** I care about contracts, failure modes, data flow, observability and ownership boundaries.
- **Reproducible validation.** Logs, CI gates, bit-exact checks, test matrices and rollback points are part of the system, not an afterthought.
- **Cross-layer debugging.** I am comfortable moving from UI/application behavior through networking and runtimes down to OS/hardware behavior.
- **AI as an engineering accelerator.** I use modern coding agents aggressively for implementation and exploration, while retaining responsibility for architecture, debugging strategy, validation, integration and final technical claims.

---

## Technical map

**AI & automation**  
LLM integration · agentic workflows · AI-assisted engineering · evaluation/validation workflows · automation

**Systems & runtime**  
Rust · C/C++ · x86_64 · bare metal · AVX2/FMA · GPU/CPU inference · Windows API · concurrency · DMA/PCIe concepts

**Compilers & formal methods**  
lexer/parser/AST/IR · Z3/SMT · contracts/invariants · C backend · LLVM-oriented architecture · LSP/tooling

**Application & infrastructure**  
Python · TypeScript/JavaScript · Node.js · React/Next.js · REST APIs · Linux · Windows · CI/CD · Docker · Kubernetes · networking

**Hardware & operations**  
laptop/desktop diagnostics · Android devices · component replacement · OS installation/recovery · troubleshooting · user-facing technical support

---

## Professional context

Alongside independent engineering R&D, my background includes hands-on systems/IT administration, computer hardware repair and troubleshooting, and programming instruction for gifted and technical learners. That combination is useful in roles where engineering depth must connect to real users, operational environments, or customer-facing implementation.

For a fast technical review of the public evidence behind the projects above, see the **[Engineering Evidence Index](ENGINEERING_EVIDENCE.md)**.

---

## Contact

- [LinkedIn](https://www.linkedin.com/in/danielforface)
- [Aura website](https://aura.geniuses.team/)
- [GitHub](https://github.com/danielforface)
