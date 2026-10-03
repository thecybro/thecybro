Hey there 👋 Cybro here.

Let me introduce myself by telling me what I am interested in and what I work on; instead of telling my name again.

I am particularly interested in working at the intersection of AI, systems programming, and security. 

You can find my projects here;
[GitHub](https://github.com/thecybro)  [Clannon Labs](https://github.com/Clannon-Labs)

---

## What I work on

I am quite mostly focused on rust nowadays, so any upcoming project of mine will most probably be rust largely/only.

- **Systems software**: OS/kernel, bare metal programming etc.. This is the most favorite field of mine; cuz why not?
   I am actively learning to eventually get into building my own OS from scratch.
- **Infrastructure software**: This the field I am actively learning to work at even lower level day-by-day.
   Take devops and containerization & orchestration platforms for example.
   I am working on controlled execution tools and media indexing tools right now.
- **AI Agent infrastructure**: Even though nowadays, I am actively trying to get close to operating system level, I
    have made some interesting projects. They are the top 2 in the projects section below.
    I have built projects related to orchestration, permissioned tool execution and system that persists memory across
    sessions.
- **Applied security**: This is field I want to work on intersection of; with my other interests of and I am actively
  learning towards making that a reality.

I'd rather build the system underneath the API than wrap one and call it a product.

## Selected projects

### [Clannon](https://github.com/Clannon-Labs/Clannon)

A multi-model AI orchestration platform. Client research briefs go in, a team of specialist agents researches them in parallel, every claim gets checked against its source before it reaches the user, and a memory layer carries context forward so the third project with a client doesn't start from zero.

Grew into a full multi-service system: a FastAPI backend, a Next.js frontend streaming a live decision log as the orchestrator works, cross-provider model routing so no single provider's quota or outage can take a run down, and its own release process, specs, and docs.

---

### [Vraksha](https://github.com/Clannon-Labs/vraksha)

The security-first agent runtime Clannon's pipeline is built on, distilled into a standalone CLI. Every input passes through a fixed pipeline before a model ever sees it:

```
intake → sanitizer → normalizer → verifier → orchestrator → output filter → delivery
```

ClamAV/YARA scanning, modality-aware sanitization, a small model making the final safety call, and four memory tiers (wiki, semantic, episodic, procedural) with trust ordering so user-authored facts always win. Tools and expert agents self-register through one capability registry — adding a new one is a decorated file, no wiring.

---

### [Claven](https://github.com/Clannon-Labs/Claven)

A local workbench that spins up a disposable Linux container and shows you exactly what happened inside it — real container PTY over WebSockets, timestamped process/file/network activity, and immutable workspace snapshots you can fork back into a fresh environment.

Runs on rootless Podman, capability-based auth (no passwords, no sessions — a private URL is the credential), and outbound networking disabled by default. It's careful about what it claims: sampled events are labeled as sampled, not pretended to be continuous tracing.

---

### [OmniClan](https://github.com/Clannon-Labs/Omniclan)

A tool/platform that lets you upload all your media, transcribes and indexes them and lets you search them as if you were
googling them. It can direct you to the relevant sections that your search most resembles and eventually my goal is to
make it explain things to you instead of merely being a search tool only.

Development still on progress

---

### [GhostLayer](https://github.com/thecybro/GhostLayer)

End-to-end encryption for chat platforms that don't have it. A Chrome extension where the cryptographic core is written in Rust and compiled to WebAssembly; X25519 for key agreement, ChaCha20-Poly1305 for authenticated encryption. Keys are generated locally; there's no GhostLayer server or account.

The protocol is versioned and independent of the extension, so any client could implement GhostLayer v1 without touching this codebase. Tested end-to-end on Discord, Slack, X, and Messenger.


**Alpha.** Limitations are documented in-repo.

---

### [VibeCheck](https://github.com/thecybro/VibeCheck)

A Chrome extension that filters emotionally harmful content out of your feed using a local NLP model — nothing leaves your machine. A `MutationObserver`-driven content script pulls post text, a local FastAPI service runs a RoBERTa model fine-tuned on GoEmotions, and posts crossing your sensitivity threshold get blurred with a one-click reveal.

## Stack

**Languages:** Rust • C • C++ • Python • TypeScript
**Systems:** Tokio · Axum · Podman · Linux · WebAssembly
**AI/ML:** PyTorch · Hugging Face · FastAPI

## Elsewhere

Most of my work lives across my personal repos and [Clannon Labs](https://github.com/Clannon-Labs).

[View all repositories →](https://github.com/thecybro?tab=repositories)
