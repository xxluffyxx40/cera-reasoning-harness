# CERA — Co-Emergent Reasoning Architecture

**A reasoning harness for human-AI collaboration in Claude Projects.**

CERA preserves what gets lost between AI sessions — not just what was said, but what was *understood*. The reasoning chains, the strategic posture, the logical provenance, the collaborative state that made the conversation productive.

Agent memory systems like OpenClaw store facts and retrieve them by similarity. CERA preserves *reasoning* and retrieves it by *structure*. Every conclusion declares its dependencies. Every session maps how thinking evolved. A dedicated integrator synthesizes across sessions so the project gets smarter over time — not just bigger.

The result: new AI sessions engage with your project at the level of accumulated understanding, not from zero.

Read the full paradigm argument: **[The Reasoning Harness](Substack link TBD)**

---

## What's in This Repo

| File | What It Does |
|------|-------------|
| `SKILL.md` | The complete CERA skill — install this in your Claude Project |
| `SETUP_GUIDE.md` | Step-by-step guide from installation to first session map |
| `THE_REASONING_HARNESS.md` | The full essay: why reasoning preservation matters more than memory |

---

## Quick Install

1. In Claude, go to **Settings → Skills**
2. Add `SKILL.md` as a custom skill
3. Create or open a **Claude Project**
4. Start a conversation and invoke CERA
5. Work normally — Claude operates with the collaborative reasoning protocol active
6. Call for a **checkpoint** when significant reasoning occurs
7. Upload the session map to your project's knowledge base

That's it. Full details in the [Setup Guide](SETUP_GUIDE.md).

---

## How It Works

**Session Maps** — Each conversation produces a standalone reasoning record: weighted reasoning chains, strategic posture shifts, discoveries with explicit dependency declarations, latent cognition capture, and optional session-specific primers. One per conversation. Immutable after creation.

**CERA Index** — A cross-session intelligence layer that synthesizes across session maps. Contains the trajectory narrative, promoted patterns and discoveries with bidirectional provenance, a session index for structural retrieval, and project-level primers for register reconstruction. Created and managed by a dedicated integrator conversation.

**Register Reconstruction** — A three-layer system that restores collaborative cognitive state across sessions: information (~70%), primer (~85%), and activation questions (~90%). The remaining 10-15% is the live contribution — the reason each conversation is worth having.

**Bidirectional Provenance** — Every entry declares upstream dependencies (*Derives from*) and downstream effects (*Affects*). When something changes, the impact traces forward through the dependency chain. Adapted from a methodology that maintained zero provenance loss across 60,000+ lines of revision.

---

## Who This Is For

Anyone doing extended project work with Claude where continuity matters — legal strategy, research, systems design, policy analysis, creative development, or any domain where reasoning builds across sessions and losing it means starting over.

---

## Background

CERA emerged from a practical discovery: deep AI conversations produce a layer of reasoning architecture — implicit connections, collaborative patterns, strategic frameworks — that exists during the conversation but vanishes when the session ends. The transcript preserves what was said. CERA preserves what was understood.

The architecture draws on the Meta Harness paper's insight that harness engineering matters as much as model capability, and is informed by the Claude Code leak's confirmation that the harness layer is where product value lives. CERA extends this to collaborative reasoning — a domain no existing harness addresses.

CERA is the subject of a provisional patent filed February 2026 and is developed collaboratively across Claude model versions by Michael E. Teplinsky, Esq.

---

## License

Apache License 2.0 — see [LICENSE](LICENSE) for details.

---

## Contributing

This is an early release. If you deploy CERA in your own projects and find issues, improvements, or extensions, contributions are welcome. Open an issue or submit a PR.
