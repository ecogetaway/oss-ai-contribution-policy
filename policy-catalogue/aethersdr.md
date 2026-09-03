# aethersdr/AetherSDR — AI-contribution policy (catalogue entry)

- **Project:** [aethersdr/AetherSDR](https://github.com/aethersdr/AetherSDR)
- **Policy location:** [CONTRIBUTING.md](https://github.com/aethersdr/AetherSDR/blob/e69bfaefc09948031239fc7317bd105a32f0f3e6/CONTRIBUTING.md)
- **Agent guidance:** [AGENTS.md](https://github.com/aethersdr/AetherSDR/blob/178f911efe8b28249ab227c43a229921a6ec6972/AGENTS.md)
- **Captured on:** 2026-08-01 (each source pinned at the revision shown above)

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | disclosed-allowed; Claude Code use is strongly encouraged |
| stance (docs / translations / media) | unstated |
| disclosure required? mechanism? | No disclosure requirement is stated for code contributions. AI-assisted bug and feature reports are explicitly supported through the in-app lightbulb workflow. |
| attestations required | None stated for contributors. |
| enforcement on non-disclosure | No non-disclosure enforcement is stated. Human review is required for bot-opened PRs, and signed commits are enforced by branch protection. |
| first-time contributors | Welcomed; the guide points newcomers to `good first issue` issues. |
| maintainer-only paths | Tier 1 includes governance and security files plus the AI control plane: `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, and `.claude/commands/`. |
| agent claim protocol | An agent actively reviewing, commenting, or implementing must assign itself first; an existing human or non-triage agent assignment blocks overlapping work. |
| autonomous boundaries | Agents may fix clear bugs, protocol compliance, and build/CI issues, but must not autonomously change visual design, UX behavior, architecture, feature scope, or defaults. |

## Verbatim excerpt

> Community contributions are welcome.
>
> AetherSDR is developed using [Claude Code](https://claude.com/claude-code) as the primary development environment. We **strongly encourage all contributors to use Claude Code**.
>
> Bot-opened PRs (e.g. @AetherClaude's) still require a human reviewer regardless of tier — the bot is intentionally **not** a code owner.

The pinned `AGENTS.md` adds the operational rules behind those gates: AI-instruction files are maintainer-only, commits must be signed, and an active agent must claim an issue or PR before reviewing, commenting, or implementing. It also limits autonomous agent work to clear bugs, protocol compliance, and build/CI fixes, leaving design, UX, architecture, scope, and defaults to maintainers.

## Notes

The policy distinguishes AI-assisted issue intake from code contribution policy: the lightbulb workflow is explicitly AI-assisted, while code contributions are encouraged to use Claude Code but do not have a stated disclosure or attestation requirement. Review gates are tiered by path, with human review, signed commits, maintainer-only AI control-plane files, and the claim protocol providing the main enforcement controls.
