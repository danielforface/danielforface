# Engineering Evidence Index

This is a technical-review shortcut for Daniel Cohen's public engineering work.

The objective is to distinguish what is **implemented**, **publicly inspectable**, **physically/CI validated**, **experimental**, and **private**.

---

## 5-minute review path

### 1. AetherOS — low-level AI/runtime depth

Start with the [AetherOS Public Evidence Release](https://github.com/danielforface/AetherOS-Showcase).

Then use:

- [Reviewer Start Here](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/REVIEWER_START_HERE.md)
- [Claims & Limits](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/CLAIMS_AND_LIMITS.md)
- [Benchmark Methodology](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/BENCHMARK_METHODOLOGY.md)
- [BY causal repair](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/BY.md)
- [DV local-vs-E2E rejection](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/DV.md)
- [HAR steady qualification](https://github.com/danielforface/AetherOS-Showcase/blob/main/evidence/release-v1.1/HAR.md)

### 2. Aura — code-backed compiler / formal-methods work

Review the [Aura README](https://github.com/danielforface/aura-lang) and [PROJECT_STATUS.md](https://github.com/danielforface/aura-lang/blob/main/PROJECT_STATUS.md).

### 3. NexusP2P / XLINK — practical native Rust product engineering

Review [XLINK](https://github.com/danielforface/XLINK).

### 4. Telegram Cloudifier — full-stack / protocol integration

Review [TelegramDrive](https://github.com/danielforface/TelegramDrive).

---

# 1. AetherOS

**Repository:** [danielforface/AetherOS-Showcase](https://github.com/danielforface/AetherOS-Showcase)  
**Category:** bare metal · AI inference · GPU/CPU runtime · x86_64 · Rust  
**Public source depth:** bounded evidence slices; complete kernel private  
**Physical evidence depth:** high

AetherOS is a Rust-first `#![no_std]`, x86_64 bare-metal AI operating system / inference runtime.

## Current reviewed public evidence

- physical x86 boot into AetherOS;
- external USB / GGUF model loading;
- Intel compute device PCI `8086:9b41`;
- custom Gen9-class backend in a hybrid CPU/iGPU route;
- ROUND18 source/binary provenance;
- promotion/rejection gates;
- raw physical serial telemetry;
- causal register-corruption experiment;
- rejected optimizations preserved as evidence;
- reviewed HAR steady decode point of **7.0775 tok/s** for the tested Llama 3.2 1B Instruct Q4_K_M configuration;
- later continuous RUN01 physical reproduction at approximately **7.08 tok/s**.

## Three strongest review stories

### BY — causal register corruption

A predicted SIMD write-footprint overwrite was reproduced on physical execution, then removed by a narrow scalar-write repair. The unsafe full kernel produced exactly 2048 mismatches with the predicted row pattern; repaired execution reached 8192/8192 exact.

### DV — 7.768x local result rejected

A controlled B=8 Q4 multicolumn kernel reached 7.768x while remaining exact. The complete FFN graph did not gain enough, so production promotion remained off.

### HAR — benchmark methodology corrected

After identifying one-time code-install contamination in the predecessor qualification, HAR separated warm-up from balanced measured pairs without weakening the gate. The fixed 128-token matrix closed at 7.0775 tok/s steady.

## Claim boundary

The evidence is internally produced. It is not presented as independent third-party certification.

The public release does **not** claim:

- pure-GPU inference;
- 100% GPU offload;
- zero-copy USB execution;
- universal 7 tok/s performance;
- cross-hardware reproducibility;
- semantic-answer certification;
- competitive superiority over another runtime.

## What AetherOS demonstrates

- low-level Rust systems integration;
- x86/bare-metal architecture;
- CPU/GPU inference integration;
- physical performance engineering;
- mechanism-level debugging;
- benchmark-methodology discipline;
- rollback and rejection decisions;
- ability to coordinate AI-assisted engineering while retaining an inspectable evidence chain.

---

# 2. Aura

**Repository:** [danielforface/aura-lang](https://github.com/danielforface/aura-lang)  
**Category:** programming languages · formal methods · compiler/runtime tooling  
**Public-code depth:** high

Aura is an active Rust language-platform project with lexer/parser/AST/IR, Z3-backed verification, contracts/invariants, native backend work, LSP/IDE integration and CI/release tooling.

Best review links:

- [README](https://github.com/danielforface/aura-lang)
- [Project Status](https://github.com/danielforface/aura-lang/blob/main/PROJECT_STATUS.md)
- [Architecture](https://github.com/danielforface/aura-lang/blob/main/ARCHITECTURE.md)

The repository explicitly distinguishes implemented capabilities from evolving/pre-stable surfaces.

---

# 3. NexusP2P / XLINK

**Repository:** [danielforface/XLINK](https://github.com/danielforface/XLINK)  
**Category:** Rust · Windows · networking · native desktop

Public implementation includes QUIC transport, certificate fingerprint pinning, explicit consent gates, DXGI Desktop Duplication, session-gated Win32 input injection and native desktop workflows.

---

# 4. Telegram Cloudifier

**Repository:** [danielforface/TelegramDrive](https://github.com/danielforface/TelegramDrive)  
**Category:** TypeScript · Next.js · MTProto · file management

This project demonstrates third-party protocol integration, authentication/session workflows, chat/media browsing, upload/download management and filesystem-style abstraction.

---

# Engineering ownership and AI-assisted development

I use modern AI coding agents heavily.

The engineering ownership I want evaluated is:

- problem decomposition;
- architecture and interface boundaries;
- experimental design;
- debugging and fault isolation;
- integration across layers;
- test / validation design;
- telemetry and benchmark interpretation;
- rollback / promotion decisions;
- technical claim boundaries;
- ability to explain and reproduce the mechanisms.

Generated code by itself is not used as evidence.

---

# Role alignment

The strongest current public evidence aligns most directly with:

- Systems / AI Runtime Engineering
- Rust / Native Systems Engineering
- Edge / Local AI Runtime
- GPU/CPU Performance Engineering
- Compiler / Developer Tools Engineering
- Forward Deployed / Solutions Engineering where deep technical debugging is central

[Back to GitHub profile](https://github.com/danielforface)
