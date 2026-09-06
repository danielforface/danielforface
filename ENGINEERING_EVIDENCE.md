# Engineering Evidence Index

This page is a **technical-review shortcut** for Daniel Cohen's public engineering work.

The goal is not to make every project sound production-ready. It is to make it easy to distinguish **what is implemented, what is publicly verifiable, what has hardware/CI evidence, and what remains experimental or private**.

---

## 5-minute review path

If you only have a few minutes:

1. **Aura — code-backed systems/compiler work**  
   Start with the [Aura README](https://github.com/danielforface/aura-lang) and [PROJECT_STATUS.md](https://github.com/danielforface/aura-lang/blob/main/PROJECT_STATUS.md).

2. **AetherOS — low-level AI/runtime depth**  
   Start with the [AetherOS README](https://github.com/danielforface/AetherOS-Showcase), then [Performance](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/08-performance.md) and the [Proof Matrix](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/09-proof-matrix.md).

3. **NexusP2P — practical native product engineering**  
   Review the [README](https://github.com/danielforface/XLINK) and [Cargo workspace](https://github.com/danielforface/XLINK/blob/main/Cargo.toml).

4. **Telegram Cloudifier — full-stack/API integration**  
   Review the [README](https://github.com/danielforface/TelegramDrive) and [package.json](https://github.com/danielforface/TelegramDrive/blob/master/package.json).

---

# 1. Aura

**Repository:** [danielforface/aura-lang](https://github.com/danielforface/aura-lang)  
**Category:** programming languages · formal methods · compiler/runtime tooling  
**Public-code depth:** high

Aura is a proof-driven systems programming language and developer platform written primarily in Rust.

### Public evidence

- Rust workspace with **22 members**
- separate lexer, parser, AST, semantic-core and IR components
- Z3-backed verification path
- contracts, assertions, invariants and structured counterexample workflows
- AVM/development execution
- C-oriented backend
- evolving LLVM IR backend
- runtime and native-runtime components
- package tooling
- LSP and editor/IDE integration
- Android build/runtime tooling
- deterministic release tooling
- public project-status reconciliation document
- documented seven-workflow CI validation matrix

### Useful review links

- [README](https://github.com/danielforface/aura-lang)
- [Project Status](https://github.com/danielforface/aura-lang/blob/main/PROJECT_STATUS.md)
- [Workspace Cargo.toml](https://github.com/danielforface/aura-lang/blob/main/Cargo.toml)
- [Architecture](https://github.com/danielforface/aura-lang/blob/main/ARCHITECTURE.md)
- [Verification Model](https://github.com/danielforface/aura-lang/blob/main/VERIFICATION_MODEL.md)
- [GitHub Actions](https://github.com/danielforface/aura-lang/actions)

### Claim boundary

Aura is best described as an **active, pre-stable language platform**. It should not be read as a claim of a formally verified compiler, universally frozen semantics, or universal production readiness. The repository explicitly separates code-backed capabilities, evolving surfaces, targets, and non-claims.

### What it demonstrates

- large multi-crate systems architecture
- compiler pipeline reasoning
- formal-methods integration
- developer tooling and protocol design
- CI/release discipline
- ability to maintain explicit trust and claim boundaries

---

# 2. AetherOS

**Repository:** [danielforface/AetherOS-Showcase](https://github.com/danielforface/AetherOS-Showcase)  
**Category:** bare metal · AI inference · GPU/CPU runtime · x86_64  
**Public-code depth:** architecture/evidence showcase; full kernel private  
**Hardware evidence:** high

AetherOS is a Rust-first x86_64 bare-metal AI operating system / inference research system.

### Publicly documented engineering areas

- `#![no_std]` kernel/runtime architecture
- direct Intel Gen9 Render Command Streamer / GPGPU execution
- GGTT and GPU command paths
- AVX2/FMA multi-core inference
- GGUF model ingestion
- transformer runtime
- Q4_K / Q6_K optimized execution paths
- USB mass-storage and NVMe/storage work
- paging, memory ownership and model residency
- cycle-level and serial telemetry
- bit-exact qualification gates
- real-hardware benchmark lineage

### Public hardware snapshot

- Intel Core i3-10110U
- Intel UHD 620 / Comet Lake GT2
- Llama-3.2-1B-Instruct class model
- public evidence reports a peak verified clean 128-token end-to-end decode of approximately **3.411 tokens/s**

### Useful review links

- [README](https://github.com/danielforface/AetherOS-Showcase)
- [Architecture](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/01-architecture.md)
- [Gen9 GPU Compute](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/05-gen9-gpu-compute.md)
- [CPU / AMP](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/06-cpu-amp.md)
- [Transformer Runtime](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/07-transformer-runtime.md)
- [Performance](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/08-performance.md)
- [Proof Matrix](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/09-proof-matrix.md)
- [Validation Methodology](https://github.com/danielforface/AetherOS-Showcase/blob/main/docs/10-validation-methodology.md)

### Claim boundary

The complete AetherOS kernel is **not public**. The repository is an intentionally bounded architecture, proof, validation and performance showcase. Public documentation should not be interpreted as proof that every experimental path is production-promoted.

### What it demonstrates

- low-level debugging and hardware reasoning
- performance engineering under severe constraints
- GPU/CPU execution design
- model/runtime knowledge below framework level
- disciplined hardware validation
- long-running iterative optimization and rollback methodology

---

# 3. NexusP2P / XLINK

**Repository:** [danielforface/XLINK](https://github.com/danielforface/XLINK)  
**Category:** Rust · Windows · networking · native desktop  
**Public-code depth:** practical public implementation

NexusP2P is a Windows-focused remote-support engine written in Rust.

### Public engineering surface

- multi-crate Rust workspace:
  - core
  - network
  - display
  - input
- QUIC transport
- certificate fingerprint pinning
- out-of-band access IDs
- QR / connection-file workflows
- explicit multi-gate permission/consent model
- DXGI Desktop Duplication
- session-gated Win32 `SendInput`
- native desktop GUI
- release configuration and production validation scripts

### Useful review links

- [README](https://github.com/danielforface/XLINK)
- [Cargo.toml](https://github.com/danielforface/XLINK/blob/main/Cargo.toml)

### What it demonstrates

- native application architecture
- networking and security boundaries
- Windows APIs
- user-consent design
- modular Rust engineering
- build/release discipline

---

# 4. Telegram Cloudifier

**Repository:** [danielforface/TelegramDrive](https://github.com/danielforface/TelegramDrive)  
**Category:** TypeScript · Next.js · API integration · file management  
**Public-code depth:** application/integration project

Telegram Cloudifier explores a cloud-style file-management model over Telegram / MTProto.

### Public engineering surface

- Next.js / React / TypeScript
- direct MTProto interaction
- authentication/session workflows
- chat and media browsing
- upload/download management
- app-managed storage channels
- virtual filesystem concepts
- global media organization

### Useful review links

- [README](https://github.com/danielforface/TelegramDrive)
- [package.json](https://github.com/danielforface/TelegramDrive/blob/master/package.json)

### Claim boundary

The repository documentation includes both implemented and planned/evolving capabilities. Reviewers should use the current code and explicit implementation notes as the source of truth for feature state.

### What it demonstrates

- third-party protocol/API integration
- full-stack application structure
- product-state management
- authentication and file workflows
- translating an existing platform into a new user-facing abstraction

---

# Engineering ownership and AI-assisted development

I use modern AI coding agents heavily.

I do **not** treat generated code as proof that a system works. My engineering ownership is centered on:

- problem decomposition
- architecture and interface boundaries
- choosing implementation direction
- debugging and fault isolation
- integration across components
- test and validation design
- benchmark/telemetry interpretation
- release and rollback discipline
- technical documentation
- deciding which claims are supported by evidence

For complex projects, AI is an implementation and exploration accelerator. Validation remains a separate engineering responsibility.

---

# Why these projects belong together

At first glance, a compiler platform, a bare-metal inference system, a remote-support engine and a Telegram file environment look unrelated.

The common thread is **cross-layer systems ownership**:

```text
user / organization need
        ↓
application behavior
        ↓
protocols + APIs
        ↓
runtime / infrastructure
        ↓
OS / native interfaces
        ↓
hardware
```

My strongest work tends to appear where a problem crosses several of these layers and requires both fast learning and direct technical ownership.

---

# Role alignment

The public evidence above is most relevant to:

- AI Infrastructure Engineering
- AI Solutions / Implementation Engineering
- Forward Deployed Engineering
- Systems Software Engineering
- Rust / Native Runtime Engineering
- Edge / Local AI Runtime
- Compiler / Developer Tools Engineering

[Back to GitHub profile](https://github.com/danielforface)
