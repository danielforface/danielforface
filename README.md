# Daniel Cohen

**Systems / AI Runtime Engineer · Bare-metal OS · GPU Compute · Rust**

> I build systems from user intent down to runtime and hardware — and I try to make the claims inspectable.

My strongest work is in **cross-layer systems engineering**: architecture, implementation, debugging, physical validation, performance instrumentation, rollback and technical communication.

[LinkedIn](https://www.linkedin.com/in/danielforface) · [AetherOS](https://github.com/danielforface/AetherOS-Showcase) · [Engineering Evidence Index](ENGINEERING_EVIDENCE.md) · [Aura](https://github.com/danielforface/aura-lang)

---

## Current engineering anchor: AetherOS

### [AetherOS](https://github.com/danielforface/AetherOS-Showcase) — bare-metal AI runtime / OS

A Rust `#![no_std]`, x86_64 bare-metal system for local LLM inference on physical hardware.

The current public evidence release documents:

- physical USB boot into AetherOS;
- GGUF model loading on the physical machine;
- custom Intel Gen9-class compute work on PCI `8086:9b41`;
- hybrid CPU / Intel iGPU inference;
- a long ROUND18 optimization and failure-analysis lineage;
- explicit physical promotion/rejection gates;
- a causal GPU register-corruption experiment and repair;
- a reviewed **7.0775 decode tok/s** steady operating point for the tested Llama 3.2 1B Instruct Q4_K_M configuration;
- a later continuous RUN01 laptop recording reproducing approximately the same ~7.08 tok/s point.

The public repository is intentionally evidence-first rather than a claim that the complete private kernel source is open.

**Start here:**  
[AetherOS README](https://github.com/danielforface/AetherOS-Showcase) · [Reviewer Guide](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/REVIEWER_START_HERE.md) · [Claims & Limits](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/CLAIMS_AND_LIMITS.md)

---

## What I want to work on

The strongest role fit for my current evidence is:

- **Systems / AI Runtime Engineering**
- **Rust / low-level systems engineering**
- **Edge / local AI inference**
- **GPU/CPU performance engineering**
- **Runtime / compiler / developer-tools engineering**
- **Forward-deployed or solutions work where deep technical debugging matters**

I am particularly useful when the problem crosses layers and cannot be solved cleanly from one abstraction level.

---

## Selected engineering work

### [Aura](https://github.com/danielforface/aura-lang) — proof-driven systems programming platform

A substantial Rust language-platform monorepo built around the idea that program verification should live inside the normal edit → build → run workflow.

Public engineering surface includes:

- lexer/parser/AST/semantic/IR layers;
- Z3-backed verification paths;
- contracts, invariants and structured counterexamples;
- C-oriented native backend and evolving LLVM IR work;
- LSP / IDE integration;
- Android build/runtime tooling;
- multi-workflow CI and explicit project-status reconciliation.

**Status:** active, pre-stable language platform.

[Repository](https://github.com/danielforface/aura-lang) · [Project Status](https://github.com/danielforface/aura-lang/blob/main/PROJECT_STATUS.md)

### [NexusP2P / XLINK](https://github.com/danielforface/XLINK) — native Rust remote-support engine

A Windows-focused remote-support system with:

- QUIC transport;
- certificate fingerprint pinning;
- explicit multi-gate consent;
- DXGI Desktop Duplication;
- session-gated Win32 input injection;
- native desktop UI and connection-file / QR flows.

### [Telegram Cloudifier](https://github.com/danielforface/TelegramDrive) — MTProto file environment

A Next.js / TypeScript system that explores a cloud-style file-management abstraction over Telegram / MTProto.

---

## Engineering approach

- **Evidence before claims.** Implemented, tested, physically observed and production-promoted are different states.
- **Mechanism before mythology.** A performance number matters less if the mechanism cannot be explained.
- **Negative results stay visible.** A candidate can be exact and faster and still be rejected.
- **Cross-layer debugging.** I am comfortable moving from application behavior through runtime, OS and hardware evidence.
- **Reproducible validation.** Logs, hashes, exactness gates, rollback points and benchmark methodology are part of the engineering.
- **AI as an engineering accelerator.** I use coding agents aggressively, while keeping architecture, debugging strategy, validation, integration and final claim boundaries as explicit responsibilities.

---

## Technical map

**Systems / runtime**  
Rust · `no_std` · x86_64 · bare metal · concurrency · memory / paging · device bring-up · Windows APIs

**AI runtime / performance**  
GGUF · transformer inference · quantized kernels · AVX2/FMA · CPU/GPU routing · performance instrumentation · A/B admission gates

**GPU / low level**  
Intel integrated-GPU experimentation · command submission · residency · synchronization · emitted instruction analysis · register/fence debugging

**Compilers / formal methods**  
lexer/parser/AST/IR · Z3/SMT · contracts/invariants · native backends · LSP/tooling

**Application / infrastructure**  
Python · TypeScript/JavaScript · Node.js · React/Next.js · networking · CI/CD · Linux · Windows

---

## AI-assisted development disclosure

I use modern AI coding agents heavily.

I do not treat generated code or project size as proof that a system works. The evidence I want reviewed is the architecture, source/binary provenance, physical behavior, debugging mechanism, validation method and the decisions to promote or reject changes.

AetherOS Public Evidence Release v1.1 is the clearest current example.

---

## Fast technical review

If you only have ten minutes:

1. Open [AetherOS](https://github.com/danielforface/AetherOS-Showcase).
2. Read the [Reviewer Guide](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/REVIEWER_START_HERE.md).
3. Inspect one of the three bounded stories: **BY**, **DV**, or **HAR**.
4. Use [ENGINEERING_EVIDENCE.md](ENGINEERING_EVIDENCE.md) for the wider project map.

---

## Contact

- [LinkedIn](https://www.linkedin.com/in/danielforface)
- [GitHub](https://github.com/danielforface)
