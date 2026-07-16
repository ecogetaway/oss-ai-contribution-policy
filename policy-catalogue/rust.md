# rust-lang/rust — AI-contribution policy (catalogue entry)

- **Project:** [rust-lang/rust](https://github.com/rust-lang/rust)
- **Policy location:** [rust-lang/rust-forge PR #1040 — "Add an LLM policy for `rust-lang/rust`"](https://github.com/rust-lang/rust-forge/pull/1040) (proposed `src/policies/llm-usage.md`)
- **Captured on:** 2026-07-16

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| status | **Proposed, not yet merged.** PR #1040 opened 2026-04-17, still open and under active discussion as of 2026-07-13. Catalogued as a signal of a policy in formation, not an adopted one. |
| stance (code) | banned by default — "It's fine to use LLMs to answer questions, analyze, distill, refine, check, suggest, review. But not to **create**" |
| stance (docs / comments) | banned — "Documentation that is originally created by an LLM," including non-trivial source comments, doc-comments, safety comments, and compiler diagnostic messages |
| stance (experimental code) | conditionally allowed under a carve-out for PRs clearly marked experimental (`S-experimental` label, `[PERF]` title, `r? ghost`) — disclosure "strongly recommended, not required" while marked experimental, **required** once the experimental marker is removed |
| disclosure required? mechanism? | Required for everything in the "⚠️ Allowed with caveats" tier (trivial changes, machine translation, LLM review bots) — no fixed trailer format specified, unlike Fedora's `Assisted-by:` convention |
| attestations required | Self-review required regardless of AI use: "An LLM review does not substitute for self-review. Authors are expected to review their own code before posting and after each change." |
| enforcement on non-disclosure | Framed explicitly as a Code-of-Conduct matter ("🔨 Violating this clause counts as a violation of the Code of Conduct") for the "Lying" category, rather than automated PR closure |
| aggregate/systemic control | Novel mechanism not seen elsewhere in this catalogue: a **circuit breaker** — if more than 50% of merged PRs in a rolling 6-week window are LLM-created, new LLM-created PRs face a moratorium with a minimum 10-day cooldown |
| first-time contributors | Explicitly held to a higher bar: "If you are a new contributor, you should expect to be scrutinized more heavily than existing contributors, since you haven't yet established trust with your reviewers." |

## Verbatim excerpt
> "Using LLMs while working on `rust-lang/rust` is conditionally allowed, when done with care. LLMs are not a substitute for thought."
>
> "Our goal is *not* to catch every violation... Instead, our goal is to remove plausible deniability: to force a choice between following the policy and intentionally violating it."
>
> "It's fine to use LLMs to answer questions, analyze, distill, refine, check, suggest, review. But not to **create**."

## Notes
Two things make this entry distinct from the rest of the catalogue. First, it's **explicitly scoped to one repository** (`rust-lang/rust` only — "excludes subtrees, submodules, and dependencies"), not the whole Rust project, which the schema's project-level granularity doesn't currently represent. Second, the **circuit-breaker mechanism** is the first quantitative, self-adjusting enforcement rule seen in this catalogue (vs. binary allowed/banned stances elsewhere) — strong v0.2 signal that "enforcement" needs a sub-field for threshold-based/dynamic rules, not just static prohibitions. The policy's own stated goal — "remove plausible deniability" rather than "catch every violation" — is also a notably different enforcement philosophy from Kubernetes' closure-on-detection approach, worth surfacing in any cross-project synthesis this catalogue eventually produces.
