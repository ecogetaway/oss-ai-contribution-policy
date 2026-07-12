# Contributing

This project practices the standard it proposes. Contributions are welcome — including AI-assisted contributions, disclosed and attested. Our own policy file is [`ai-contribution-policy.yml`](ai-contribution-policy.yml) at the repository root.

New here? Start with [`FAQ.md`](FAQ.md) and the adoption walkthrough in [`ADOPTION.md`](ADOPTION.md).

## Start small

Every pathway begins with a single-file, easily reviewable PR. In rough order of effort:

### 1. Add a policy to the catalogue (~15 minutes)
One file in [`policy-catalogue/`](policy-catalogue/) documenting one project's existing AI-contribution policy. Copy [`policy-catalogue/TEMPLATE.md`](policy-catalogue/TEMPLATE.md), fill in the project, the policy's substance, a link, and the date you captured it. This is the highest-value low-effort contribution: the schema is only as good as the corpus it's tested against.

### 2. Nominate or draft a case study
A structured write-up of a real project's collision with AI-assisted contribution — a closure, a restriction, a policy fight, or a success story. Open an issue with the `case-study-candidate` label first (so effort isn't duplicated), then draft against [`case-studies/TEMPLATE.md`](case-studies/TEMPLATE.md). Claims must trace to public records: issues, PRs, blog posts, commit history.

### 3. Critique the schema
Open an issue with the `schema-feedback` label naming a **specific field** of [`spec/ai-contribution-policy.schema.yml`](spec/ai-contribution-policy.schema.yml): what's missing, what's ambiguous, what would prevent your project from adopting it. "This field would never survive contact with my repo because…" is exactly the input v0.2 needs.

### 4. Share maintainer experience
Open an issue with the `community-feedback` label describing what AI-contribution load looks like in your review queue. Anonymized is fine. This shapes the enforcement and review sections of the schema.

## Disclosure and attestation (we dogfood)

When you open a PR here, the template asks you to:

- **Disclose** whether and how AI assisted the contribution (tool and role — e.g., "drafted with an AI coding assistant, restructured by hand").
- **Attest** that you understand the change and reviewed the full output before submitting.

Non-disclosure isn't punished with closure here — you'll simply be asked to complete it, exactly as our policy file's `enforcement.undisclosed_ai: request-disclosure` says. We want the experience of complying with this standard to be visibly reasonable, because we're asking other projects to adopt it.

## Review expectations

This is a small, part-time-maintained project. Target first response: 14 days (declared in our policy file). If a contribution requires expertise we lack, we'll say so in the thread rather than let it stall silently.

## Style

- Case studies and catalogue entries: evidence over adjectives. Link the primary source for every claim.
- Schema changes: propose in an issue before a PR; schema fields are removed as eagerly as they're added (see Maintainer Principles in the README).
- License: Apache-2.0. By contributing you agree your contribution is licensed under it.
