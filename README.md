# Daniel Cohen

**Systems software engineer · Programming languages · Formal verification**

I build software close to both the semantics and the hardware: compilers, proof systems, native runtimes, bare-metal systems, and developer tooling.

My current work is centered on two long-running systems projects:

## Aura

[Aura](https://github.com/danielforface/aura-lang) is a proof-driven systems programming language and developer platform built in Rust.

Current engineering areas include:

- language frontend, semantic analysis, and Aura IR
- Z3-backed program verification
- refinement types, contracts, ownership, and explicit trust boundaries
- AVM development execution and a native-oriented C backend
- LSP proof streaming and structured counterexamples
- Sentinel, a dedicated verification-focused desktop development environment
- package, FFI, Android, release, and qualification tooling

**Website:** https://aura.geniuses.team/

## AetherOS

[AetherOS](https://github.com/danielforface/AetherOS-Showcase) is a Rust-first bare-metal AI operating system / inference research system for x86_64.

The project explores:

- `#![no_std]` kernel and runtime architecture
- direct hardware ownership without a conventional host OS inference stack
- Intel Gen9 GPGPU command submission
- AVX2 multi-core inference paths
- GGUF transformer execution
- real-hardware validation, bit-exact qualification, and performance lineage

The public repository is an engineering and validation showcase; the full kernel implementation is not published there.

## Selected engineering projects

### NexusP2P
[XLINK / NexusP2P](https://github.com/danielforface/XLINK) — a Windows-focused remote-support engine in Rust using QUIC, certificate fingerprint pinning, explicit consent gates, DXGI capture, and native desktop UI.

### Telegram Cloudifier
[TelegramDrive](https://github.com/danielforface/TelegramDrive) — a Telegram/MTProto-based cloud-style file management system with virtual filesystem concepts and media organization.

## Technical focus

`Rust` · `Compiler architecture` · `Formal methods` · `SMT / Z3` · `Systems programming` · `x86_64` · `Bare metal` · `C / LLVM` · `LSP` · `Native runtimes` · `FFI` · `Concurrency`

## Engineering approach

- Evidence before claims.
- Explicit trust boundaries.
- Reproducible validation.
- Correctness and observability before optimization.
- Build the language/runtime contract, not only the demo.
- Keep experimental surfaces clearly separated from qualified ones.

## Links

- Aura: https://aura.geniuses.team/
- LinkedIn: https://www.linkedin.com/in/danielforface
- Telegram: https://t.me/danielcohen
