# Bevy Organization — AI-contribution policy (catalogue entry)

- **Project:** [bevyengine/bevy](https://github.com/bevyengine/bevy) — policy is Bevy-Organization-wide, not repo-scoped
- **Policy location:** [bevy.org/learn/contribute/policies/ai](https://bevy.org/learn/contribute/policies/ai/); source at [bevy-website `content/learn/contribute/policies/ai.md`](https://github.com/bevyengine/bevy-website/blob/cd91a9582dd368a7712b66f86e8669722315c13a/content/learn/contribute/policies/ai.md), added in [bevy-website#2204](https://github.com/bevyengine/bevy-website/pull/2204) (2025-10-14); linked from [bevy CONTRIBUTING.md](https://github.com/bevyengine/bevy/blob/main/CONTRIBUTING.md)
- **Captured on:** 2026-07-25 (source pinned to `cd91a95`)

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | prohibited — "all[^1] forms of AI-generated contributions cannot be merged into repositories maintained by the Bevy Organization" |
| stance (media / game assets) | prohibited — explicitly extended to "non-code game assets (e.g. textures, audio, etc)" |
| stance (issues, PRs, Discord, social) | prohibited for automated communication "under the guise of a human"; treated as a Code of Conduct violation |
| stance (translations) | permitted — machine translation is explicitly exempted, with a recommendation to prefer concise or non-LLM output |
| scope carve-out | Trivial LLM completions (variable renames, autocompleted calls) are exempt **on the stated ground that they are "by definition not detectable"** — excludes generation of whole function blocks |
| disclosure required? mechanism? | n/a (prohibited) |
| attestations required | n/a |
| enforcement | Two-step: any triage team member may mark a suspect PR `S-Nominated-to-Close`, then a maintainer reviews for closure. Repeat submitters face blanket rejection of future contributions, **retroactive removal** of prior suspect contributions, and further CoC action if bad faith |
| stated detection criteria | The policy names its own heuristics: needlessly verbose descriptions/responses; not internally coherent or self-contradictory; demonstrates misunderstanding of what the code does |
| rationale | Copyright-first — five unresolved legal questions enumerated, plus maintainer burden |
| revisit clause | "This policy may be revisited when the legal debate has settled" |
| first-time contributors | No special gate documented |

## Verbatim excerpt

> "Erring on the side of caution in light of a openly debated legal topic, all[^1] forms of AI-generated contributions cannot be merged into repositories maintained by the Bevy Organization. This includes both code and non-code game assets (e.g. textures, audio, etc)."

> "The unsolicited use of automated systems to communicate issues, bugs, or security vulnerabilities about Bevy Organization projects under the guise of a human is considered unacceptable and a Code of Conduct violation."

> "\[^1\]: Trivial LLM generated content such as variable renames or autocompleted function calls, often branded 'predictions' or 'suggestions', that is otherwise indistinguishable from traditional methods such as a regex search/replace or an LSP autocompletion **is by definition not detectable** and can be treated like other regular IDE tools such as Intellisense. This does not include cases where the prediction generates things like entire function blocks."

> "We recognize that English may not be the primarily language for all contributors and that machine translation is an indispensable tool for proper collaboration. Therefore machine translation is not subject to the above policy."

## Notes

**The only policy in this catalogue that reasons explicitly about its own enforceability.** The `[^1]` footnote carves out trivial LLM completions *on the ground that they are "by definition not detectable"* — the scope of the ban is drawn at the limit of what anyone can observe, and the policy says so out loud. Every other prohibition in the catalogue is silent about the gap between what it forbids and what it can establish. Strong v0.2 signal: if the schema ever gains a `rationale` or `scope` qualifier, "bounded by detectability" is a distinct and defensible value, not a loophole.

**A prohibition that ships its own detection heuristics.** Verbosity, internal incoherence, and demonstrated misunderstanding are written into the policy text as triage criteria. These are human-judgement heuristics, deliberately so — but no other catalogued policy states its detection standard at all, and a schema that models `enforcement` outcomes without any notion of *how a suspicion is raised* can't express this.

**Enforcement is a two-step workflow with a named artifact.** `S-Nominated-to-Close` is a label any triage member may apply, followed by maintainer review. The v0.1 `enforcement` vocabulary (`request-disclosure` / `close` / `label-and-review`) is closest here — `label-and-review` fits — but the nominate-then-adjudicate split, and the fact that the label name is public and stable, is more structure than the field currently carries.

**Retroactive removal is a sanction no other catalogued policy has.** Enforcement fields across this corpus look forward (close this PR, ban this account). Bevy reserves the right to remove already-merged contributions. That is a different kind of consequence and probably deserves its own enumeration.

**Org-wide scope, single published location.** The policy binds "repositories maintained by the Bevy Organization" and lives on the website rather than in any repository — the linked `CONTRIBUTING.md` only points at it. Same shape as Home Assistant / Open Home Foundation: the schema's per-project granularity doesn't represent an org-level policy inherited by member repos, and a machine-readable file at one repo root would be a copy, not the source.

**Machine translation exempted, with tool guidance.** Like Fedora, translation is carved out — but Bevy goes further and recommends instructing the model to be concise or using non-LLM translation, on verbosity grounds. Translation carve-outs are now common enough across the catalogue (Fedora, Rust, Home Assistant, Bevy) to be worth a dedicated stance value rather than a note.
