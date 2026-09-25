# rust-lang/rust — AI-contribution policy (catalogue entry)

- **Project:** [rust-lang/rust](https://github.com/rust-lang/rust)
- **Policy location:** [LLM usage policy — Rust Forge](https://forge.rust-lang.org/policies/llm-usage.html) (canonical). Adoption note: [Inside Rust, 2026-08-05](https://blog.rust-lang.org/inside-rust/2026/08/05/rust-langrust-is-adopting-an-llm-policy/) by Jynn Nelson. Originating PR: [rust-lang/rust-forge #1040](https://github.com/rust-lang/rust-forge/pull/1040) (merged 2026-08-05).
- **Captured on:** 2026-08-13 (status updated from 2026-07-16 “proposed” capture)

> **Update, 2026-09-25 (re-verified at source).** The policy now applies to **six repositories**: rust-lang/rust, rustlings, mdBook, cargo, rust-clippy and rustfmt, still "only to the teams that have ratified it". LLM-created PRs under the experimental tier are tagged with an **`llm-assisted`** label (verbatim: "LLM-created PRs must be tagged with a new `llm-assisted` label"). The core rule is unchanged: "It's fine to use LLMs to answer questions, analyze, distill, refine, check, suggest, review. But not to **create**." On machine translation (verbatim): "Posting both your original message and the translated version is always ok, but you must still disclose that machine-translation was used."

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| status | **Adopted 2026-08-05** for `rust-lang/rust` only, by five teams (compiler, libs, types, rustdoc, bootstrap, and their subteams). Not a project-wide Rust stance. Other `rust-lang` repos remain out of scope. |
| stance (code) | banned by default — "It's fine to use LLMs to answer questions, analyze, distill, refine, check, suggest, review. But not to **create**" |
| stance (docs / comments) | banned — "Documentation that is originally created by an LLM," including non-trivial source comments, doc-comments, safety comments, and compiler diagnostic messages |
| stance (experimental / LLM-created code) | Conditionally allowed under the adopted **experiment**: pre-arranged reviewer, tests required, `ai-assisted` label, private Zulip channel for those PRs. New contributors must talk to a reviewer before opening an LLM-created PR. |
| disclosure required? mechanism? | Required for the “⚠️ Allowed with caveats” tier and for LLM-created PRs (`ai-assisted` label). No `Assisted-by:` trailer — different from Fedora/LLVM and opposite of Kubernetes’ trailer ban. |
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
Verified adopted on 2026-08-13 against the Forge page and Jynn Nelson’s Inside Rust post. Two things still make this entry distinct. First, it is **explicitly scoped to one repository** (`rust-lang/rust` only — subtrees, submodules, crates.io dependencies, and other `rust-lang` repos are out of scope), which the schema’s project-level granularity does not currently represent. Second, the **circuit-breaker** survived merge: if more than half of PRs merged in a rolling 6-week window are LLM-created, new LLM-created PRs face a moratorium with a minimum 10-day cooldown — the first quantitative, self-adjusting enforcement rule in this catalogue. The adopted experiment also requires a pre-arranged reviewer and an `ai-assisted` label, which is a different disclosure shape from Fedora/LLVM `Assisted-by:` trailers and from Kubernetes’ trailer *ban*. The policy’s stated goal — “remove plausible deniability” rather than “catch every violation” — remains a different enforcement philosophy from Kubernetes’ closure-on-detection approach. Do not mail llvm-dev-style blasts; if contacting, use Jynn Nelson (`@jyn514`) about this file only.
