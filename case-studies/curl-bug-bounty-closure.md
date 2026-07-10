# Case Study: curl — Bug Bounty Ended Under AI-Generated Report Load

## Repository / Project
[curl/curl](https://github.com/curl/curl) — the data-transfer library and CLI embedded in billions of devices; among the most widely deployed pieces of software in existence, maintained by a small team led by Daniel Stenberg.

## Event Type
Contribution-pathway closure (security-report pathway)

## What Happened
curl ran a paid bug bounty for years and became one of the earliest, most publicly documented targets of AI-generated security-report flooding: fluent, plausible-looking vulnerability reports describing problems that did not exist, each consuming priority triage attention from maintainers ("we investigate each report with priority… Fake and otherwise made up security problems effectively prevent us from doing real project work"). The maintainer had documented the pattern publicly since early 2024 ("The I in LLM stands for intelligence," daniel.haxx.se, 2024-01-02). In May 2025 the project added a formal "On AI use in curl" section to its contribution guide — a disclosure-and-verification policy, not a ban. In January 2026, the project ended the bounty entirely. The current document states the closure reason in one sentence: rewards give "too strong incentives to find and make up 'problems' in bad faith that cause overload and abuse."

## Timeline
- Pressure publicly documented: 2024-01-02 — maintainer's "The I in LLM stands for intelligence" ([daniel.haxx.se](https://daniel.haxx.se/blog/2024/01/02/the-i-in-llm-stands-for-intelligence/)), followed by continued public documentation of fabricated AI reports through 2024–2025
- Policy response (disclosure, not ban): 2025-05-15 — commit "CONTRIBUTE: add project guidelines for AI use" ([docs/CONTRIBUTE.md § On AI use in curl](https://github.com/curl/curl/blob/master/docs/CONTRIBUTE.md))
- Pathway closure: 2026-01-26 — commit "BUG-BOUNTY.md: we stop the bug-bounty end of Jan 2026"
- Current state: 2026-03-10 — BUG-BOUNTY.md retitled "No curl bug bounty"; valid reports still welcomed, rewards ended ([docs/BUG-BOUNTY.md](https://github.com/curl/curl/blob/master/docs/BUG-BOUNTY.md))

## The Policy Response
Two-stage, and the stages matter. Stage one (May 2025) was exactly the shape this project's standard proposes: mandatory disclosure ("If you asked an AI tool to find problems in curl, you **must** make sure to reveal this fact"), contributor-side verification before submission, and human-authored write-ups — expressed in CONTRIBUTE.md, human-readable only, not machine-readable, discoverable only by someone who reads the docs before reporting. Stage two (January 2026) closed the *incentive* — the bounty — while keeping the report pathway open: "We still appreciate and value valid vulnerability reports."

## Cost Accounting
- **To maintainers:** priority triage of fabricated reports, described in the project's own docs as work that "pulls us away from doing other meaningful work." The maintainer's public posts documented individual fabricated reports in detail across two years.
- **To contributors:** legitimate security researchers lost bounty compensation for curl findings — the project now states it will not even "aid security researchers to get such rewards … from other sources."
- **To downstream:** an incentive that surfaced real vulnerabilities in critical infrastructure for years no longer exists; the deterrent now bears on honest reporters, while bad-faith submission cost stays near zero.

## What a Standard Would Have Changed
Honestly: the disclosure policy curl wrote in May 2025 *is* substantively `ai-contribution-policy.yml`'s disclosure-plus-verification pathway — and eight months later curl still closed the bounty. What a standard could plausibly have changed is cost and timing, not the pressure itself: a machine-readable policy is enforceable at intake (a report form that requires the disclosure and attestation fields before submission reaches a human) rather than discoverable after a maintainer has already read the fabrication. It also would have let curl's hard-won policy shape be adopted by the next hundred projects for the cost of a file, instead of each rediscovering it. The schema fields exercised by this case: a `reports`/`issues` asset class (missing in v0.1 — this case is the argument for it), `disclosure.required`, contributor-side verification attestations, and enforcement stated at the pathway level.

## Sources
- https://github.com/curl/curl/blob/master/docs/BUG-BOUNTY.md
- https://github.com/curl/curl/blob/master/docs/CONTRIBUTE.md ("On AI use in curl")
- Commit history for both files (dates cited above): `gh api repos/curl/curl/commits?path=docs/BUG-BOUNTY.md`
- https://daniel.haxx.se/blog/2024/01/02/the-i-in-llm-stands-for-intelligence/
