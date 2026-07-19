# Policy Catalogue

The empirical base of the standard: existing per-project AI-contribution policies, mapped into one comparable shape. Target: **60+ entries.**

Each entry is one file per project, from [`TEMPLATE.md`](TEMPLATE.md). Adding an entry is the smallest useful contribution to this repository (~15 minutes) and is deliberately structured as a single-file PR — see [CONTRIBUTING.md](../CONTRIBUTING.md).

Why this matters: schema v0.2 keeps only the fields this catalogue proves projects actually need. A field that no real policy expresses is a field we remove. The catalogue is also the honest record of how fragmented the current landscape is — dozens of incompatible, hand-rolled defenses is the problem statement, in data.

## Current entries (12 of 60+)

| Project | Stance (code) | Distinctive feature |
| --- | --- | --- |
| [Ghostty](ghostty.md) | disclosed-allowed | Vouch system for first-timers; public denouncement list; media prohibited |
| [LLVM](llvm.md) | disclosed-allowed | `Assisted-by:` trailer; autonomous agents banned; good-first-issue carve-out |
| [curl](curl.md) | disclosed-allowed | Separate, stricter rules for security reports; bug bounty ended Jan 2026 |
| [Godot](godot.md) | disclosed-allowed (agents) | Policy addressed to the AI agent itself, with prescribed disclosure format |
| [Kubernetes](kubernetes.md) | disclosed-allowed (per-asset split) | AI-assisted PRs allowed, AI-generated commit messages banned; explicitly bans the commit-trailer disclosure pattern Fedora recommends |
| [Fedora](fedora.md) | disclosed-allowed | Most translation-friendly policy catalogued — AI assistance explicitly encouraged for translation; restricts AI from governance decision-making (Council-approved 2025-10-22) |
| [NetBSD](netbsd.md) | prohibited-unless-escalated | LLM output "presumed tainted"; exception via written core approval |
| [QEMU](qemu.md) | prohibited | Ban derived from DCO/copyright provenance, not quality |
| [servo](servo.md) | prohibited | Four argued rationales; covers issues and comments; explicit revisit clause |
| [Gentoo](gentoo.md) | prohibited | Council-voted (2024-04-14); carve-out for packaging AI software |
| [tldraw](tldraw.md) | closed to external PRs | Total pathway closure, AI-pressure-driven, framed as temporary |
| [Rust](rust.md) | **proposed** — ban on creation | Policy-in-formation (rust-forge PR #1040, open since 2026-04-17); repo-scoped; first quantitative circuit-breaker enforcement rule in the catalogue |

Eleven adopted policies plus one proposal under public discussion. Counts elsewhere in this repository refer to adopted policies unless stated.

Every entry verified against the linked primary source on its capture date.
