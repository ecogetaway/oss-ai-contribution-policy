# kubernetes/kubernetes — AI-contribution policy (catalogue entry)

- **Project:** [kubernetes/kubernetes](https://github.com/kubernetes/kubernetes)
- **Policy location:** [kubernetes.dev — AI Guidance for Pull Requests](https://www.kubernetes.dev/docs/guide/pull-requests/#ai-guidance)
- **Captured on:** 2026-07-16

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | disclosed-allowed — "Using AI tools to help write your PR is acceptable," subject to disclosure and author accountability |
| stance (commit messages) | prohibited — "large AI generated PRs and AI generated commit messages are not allowed" |
| disclosure required? mechanism? | Yes — a plain statement in the PR description (e.g. "This PR was written in part with the assistance of generative AI") |
| attestations required | Implicit authorship attestation: author must be able to explain every change under review questioning |
| enforcement on non-disclosure | PR closure — "if you cannot explain why a change was made, the PR will be closed"; undisclosed AI use found in review is treated as grounds for closure |
| first-time contributors | No separate gate documented; same disclosure rule applies to all contributors |

## Verbatim excerpt
> "Using AI tools to help write your PR is acceptable, but as the author, you are responsible for understanding every change. If you used AI tools in preparing your PR, you must disclose this in the description of your PR."
>
> "Listing AI tooling as a co-author, co-signing commits using an AI tool, or using the `assisted-by`, `co-developed` or similar commit trailer is not allowed."
>
> "When responding to review comments, you must do so without relying on AI tools."

## Notes
Kubernetes explicitly bans the commit-trailer disclosure pattern (`assisted-by`/`co-developed`) that Fedora's policy explicitly recommends — direct evidence that "how to disclose" is unsettled across the ecosystem, not just "whether to disclose." Also notable: the policy extends past the PR itself, to review-comment responses ("you must do so without relying on AI tools") — an enforcement surface the v0.1 schema doesn't currently capture (it models the contribution artifact, not the ongoing review conversation). Strong v0.2 signal for a `review-interaction` stance field, separate from `code`/`docs`.
