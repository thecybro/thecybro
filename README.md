<div align="center">

# Cybro

AI · Systems · Security · Rust

I build software at the intersection of AI, systems programming, and security.

[GitHub](https://github.com/thecybro) · [Clannon Labs](https://github.com/Clannon-Labs)

</div>

---

## What I work on

- **Systems software** in Rust — concurrent runtimes, sandboxed execution, services that stay correct under real load
- **AI agent infrastructure** — orchestration, permissioned tool execution, persistent memory across sessions
- **Applied security** — cryptographic protocols, container isolation, input sanitization pipelines
- **Production-grade constraints** — bounded memory, capability-based auth, graceful failure, not demo-quality shortcuts

I'd rather build the system underneath the API than wrap one and call it a product.

## Selected projects

### [Clannon](https://github.com/Clannon-Labs/Clannon)

A multi-model AI orchestration platform. Client research briefs go in, a team of specialist agents researches them in parallel, every claim gets checked against its source before it reaches the user, and a memory layer carries context forward so the third project with a client doesn't start from zero.

Grew into a full multi-service system: a FastAPI backend, a Next.js frontend streaming a live decision log as the orchestrator works, cross-provider model routing so no single provider's quota or outage can take a run down, and its own release process, specs, and docs.

`Focus: AI orchestration · distributed systems · production infrastructure`

---

### [Vraksha](https://github.com/Clannon-Labs/vraksha)

The security-first agent runtime Clannon's pipeline is built on, distilled into a standalone CLI. Every input passes through a fixed pipeline before a model ever sees it:

```
intake → sanitizer → normalizer → verifier → orchestrator → output filter → delivery
```

ClamAV/YARA scanning, modality-aware sanitization, a small model making the final safety call, and four memory tiers (wiki, semantic, episodic, procedural) with trust ordering so user-authored facts always win. Tools and expert agents self-register through one capability registry — adding a new one is a decorated file, no wiring.

`Focus: AI agent security · orchestration · persistent memory · tool permissioning`

---

### [Clanix](https://github.com/Clannon-Labs/Clanix)

A local workbench that spins up a disposable Linux container and shows you exactly what happened inside it — real container PTY over WebSockets, timestamped process/file/network activity, and immutable workspace snapshots you can fork back into a fresh environment.

Runs on rootless Podman, capability-based auth (no passwords, no sessions — a private URL is the credential), and outbound networking disabled by default. It's careful about what it claims: sampled events are labeled as sampled, not pretended to be continuous tracing.

`Focus: systems programming · sandboxing · Rust · WebSockets · security boundaries`

---

### [GhostLayer](https://github.com/thecybro/GhostLayer)

End-to-end encryption for chat platforms that don't have it. A Chrome extension where the cryptographic core is written in Rust and compiled to WebAssembly — X25519 for key agreement, ChaCha20-Poly1305 for authenticated encryption. Keys are generated locally; there's no GhostLayer server or account.

The protocol is versioned and independent of the extension, so any client could implement GhostLayer v1 without touching this codebase. Tested end-to-end on Discord, Slack, X, and Messenger.

`Focus: Rust · WebAssembly · applied cryptography · browser internals`

**Alpha. Not audited.** Limitations are documented in-repo, not hidden.

---

### [VibeCheck](https://github.com/thecybro/VibeCheck)

A Chrome extension that filters emotionally harmful content out of your feed using a local NLP model — nothing leaves your machine. A `MutationObserver`-driven content script pulls post text, a local FastAPI service runs a RoBERTa model fine-tuned on GoEmotions, and posts crossing your sensitivity threshold get blurred with a one-click reveal.

`Focus: local inference · NLP · TypeScript · FastAPI · browser extensions`

## Engineering interests

Currently going deeper into Rust and systems programming while keeping one foot in AI infrastructure. Areas I keep coming back to:

- operating systems and kernel design
- high-performance and concurrent systems
- AI inference infrastructure
- sandboxing and isolation
- security engineering
- local-first, private AI

The common thread: understanding what's happening underneath the abstraction instead of trusting that it's magic.

## Stack

**Languages:** Rust · Python · TypeScript
**Systems:** Tokio · Axum · Podman · Linux · WebAssembly
**AI/ML:** PyTorch · Hugging Face · FastAPI

## Elsewhere

Most of my work lives across my personal repos and [Clannon Labs](https://github.com/Clannon-Labs).

[View all repositories →](https://github.com/thecybro?tab=repositories)
