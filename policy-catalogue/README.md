# Policy Catalogue

The empirical base of the standard: existing per-project AI-contribution policies, mapped into one comparable shape. Target: **60+ entries.**

Each entry is one file per project, from [`TEMPLATE.md`](TEMPLATE.md). Adding an entry is the smallest useful contribution to this repository (~15 minutes) and is deliberately structured as a single-file PR — see [CONTRIBUTING.md](../CONTRIBUTING.md).

Why this matters: schema v0.2 keeps only the fields this catalogue proves projects actually need. A field that no real policy expresses is a field we remove. The catalogue is also the honest record of how fragmented the current landscape is — dozens of incompatible, hand-rolled defenses is the problem statement, in data.

## Current entries (20 of 60+)

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
| [llama.cpp](llama-cpp.md) | disclosed-allowed | First loosening in the catalogue (ban → allow, 2026-07-22, rationale: model quality); prohibits AI for PR descriptions, commit messages and all reviewer/issue communication; instructs autonomous agents to remove the project from their own target list |
| [Home Assistant](home-assistant.md) | disclosed-allowed; autonomous agents prohibited | Only policy that discloses the **project's own** AI use; bypassing the issue or PR template is the observable proxy for autonomy; org-level, inherited by member repositories |
| [Mesa](mesa.md) | disclosed-allowed; autonomous agents prohibited | Only graduated disclosure vocabulary in the catalogue — `Assisted-by:` vs `Generated-by:` with tool and optional model — while banning `Co-authored-by:` for tools; third project to legislate on commit trailers, and incompatible with both Fedora and Kubernetes |
| [OpenStreetMap](openstreetmap.md) | disclosed-allowed in effect, disclosure never requested | The only permissive policy that asks for no disclosure at all: it enforces on the **absence of understanding** rather than the presence of AI — verification-over-detection, arrived at independently |
| [FreeBSD](freebsd.md) | restricted by channel rather than banned | Only policy protecting the project **as training data** ("or use pull request interactions to train AI or LLM systems"); its AI clause is a routing rule — wrong channel — rather than a stance |
| [Bevy](bevy.md) | prohibited, extended to game assets | Only policy that reasons about its own enforceability, exempting trivial LLM completions because they are "by definition not detectable"; retroactive removal as a sanction; ships its own detection heuristics |
| [Zig](zig.md) | prohibited, including paraphrase | Strictest in the catalogue and the only one reaching upstream of the artifact — bans LLM brainstorming and discussion of LLM services; bans LLM **translation** where four other policies permit or encourage it |
| [Asahi Linux](asahi-linux.md) | prohibited | The only stance **derived from a pre-existing rule** rather than written fresh: its existing ban on leaked Apple material is extended to model output; one warning then permanent ban; first to cite environmental cost |

Nineteen adopted policies plus one proposal under public discussion. Counts elsewhere in this repository refer to adopted policies unless stated.

Every entry verified against the linked primary source on its capture date.
