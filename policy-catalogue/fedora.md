# Fedora Project — AI-contribution policy (catalogue entry)

- **Project:** [Fedora Project](https://fedoraproject.org/) (distribution-wide, not repo-scoped)
- **Policy location:** [Fedora Community Blog — "Council Policy Proposal: Policy on AI-Assisted Contributions"](https://communityblog.fedoraproject.org/council-policy-proposal-policy-on-ai-assisted-contributions/) (2025-09-25); formally approved by Fedora Council 2025-10-22 (per Pagure ticket #542); canonical text intended for [docs.fedoraproject.org/en-US/council/policies/](https://docs.fedoraproject.org/en-US/council/policies/) (page currently sits behind Anubis bot-challenge and could not be fetched directly — Community Blog announcement used as the verified primary source instead)
- **Captured on:** 2026-07-16

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | disclosed-allowed — contributor remains full author, AI output treated as suggestion only |
| stance (docs / translations) | disclosed-allowed and explicitly **encouraged** for translation — a stronger stance than any other catalogued project takes on this asset class |
| disclosure required? mechanism? | Required only when AI assistance is "significant" (undefined threshold); mechanism is a commit trailer, `Assisted-by: <name of code assistant>` |
| attestations required | None beyond disclosure — contributor is "always the author and is fully accountable" |
| enforcement on non-disclosure | Not specified as automatic (no stated closure-on-detection rule, unlike Kubernetes); enforcement instead framed around downstream review burden — "unverified or low-quality machine-generated content... creates an unfair review burden on the community and is not an acceptable contribution" |
| out-of-scope / prohibited decisions | AI/ML tools explicitly **banned** from scoring or evaluating Code of Conduct matters, funding requests, conference talks, or leadership positions — a governance-process carve-out no other catalogued project states this explicitly |
| infrastructure protection | Aggressive scraping of Fedora infrastructure prohibited; user-facing AI features require opt-in consent |
| first-time contributors | No special gate documented |

## Verbatim excerpt
> "The contributor is always the author and is fully accountable for their contributions."
>
> "When a contribution has been significantly assisted by an AI tool, we encourage you to note this in your pull request description, commit message, or wherever authorship is normally indicated... For instance, use a commit message trailer like `Assisted-by: <name of code assistant>`."
>
> "Using AI tools to translate your thoughts or overcome language barriers is a welcome and encouraged practice."
>
> "AI/ML tools **must not** be used to score or evaluate submissions for things like code of conduct matters, funding requests, conference talks, or leadership positions."

## Notes
Fedora is the most translation-friendly policy catalogued so far — directly relevant to this project's i18n thesis, since it frames machine-assisted translation as removing a barrier rather than as a quality risk to be gated. It's also the only catalogued policy that explicitly restricts AI from **governance decision-making** (CoC, funding, leadership), a category the v0.1 schema has no field for at all — the schema currently only models contribution artifacts (code/docs/translations/media), not process/governance uses. Recommend a `governance-use` stance as a v0.2 addition. Also directly contradicts Kubernetes' explicit ban on commit-trailer disclosure — Fedora recommends the exact `Assisted-by:` pattern Kubernetes prohibits, reinforcing the "how to disclose" fragmentation noted in the [rust.md](rust.md) entry.
