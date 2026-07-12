# FAQ — OSS AI-Contribution Policy

Short answers for maintainers, OSPOs, and contributors. This is a **draft / proposed** shape, not “the” standard.

## Is this “the” AI contribution standard?

No. It is a **draft schema (v0.1)** plus a verified catalogue of what real projects already wrote by hand. Call it a proposed standard or a candidate shape — never “the standard” until a community body and adopters say so.

## Why a YAML file instead of more CONTRIBUTING prose?

Prose policies are hard for CI, forges, and AI coding agents to read consistently. A root file next to `LICENSE`, `CODEOWNERS`, and `SECURITY.md` puts the rules in one predictable place — for humans and for tools that read the repo *before* opening a PR.

## Are you asking projects to ban AI?

No. The design is **verification over detection**, and **stance-neutral**:

- `disclosed-allowed` — AI assistance OK if disclosed and attested
- `restricted` — allowed only under stated conditions
- `prohibited` — a machine-readable “no” (more useful than a buried one)

QEMU, servo, and Gentoo’s prohibitions are catalogued with the same care as Ghostty or LLVM’s disclosure regimes.

## Why not detect AI-generated contributions?

Detection is an arms race detectors lose. False positives also hit non-native English writers and newcomers hardest. This project asks answerable questions: Did a human review the output? Run the tests? Understand the change?

## Do I have to adopt the YAML to be useful here?

No. High-value contributions include:

1. Adding a [catalogue entry](policy-catalogue/TEMPLATE.md) for a project’s existing policy (~15 minutes)
2. Critiquing a specific schema field (`schema-feedback` issues)
3. Sharing maintainer experience (`community-feedback`)

Adoption is optional; evidence and critique are the near-term goals.

## What’s actually verified today vs. aspirational?

| Claim | Status |
| --- | --- |
| Nine catalogue entries verified against primary sources | **Done** |
| Schema v0.1 + worked examples | **Done** |
| First deep case study (curl) | **Done** |
| “60+ policies” in the catalogue | **Roadmap**, not current inventory |
| Multi-repo pilots with before/after metrics | **Not yet** — see Pilot invitation in the README |

## What does “adopting” look like?

See [`ADOPTION.md`](ADOPTION.md) for a before/after walkthrough. Short version: copy an example YAML to your repo root, edit stance / disclosure / attestations / enforcement, link it from `CONTRIBUTING.md`, and optionally [tell us](https://github.com/ecogetaway/oss-ai-contribution-policy/issues).

## How is this enforced?

Two layers, honestly labeled:

1. **Social** — disclosure and attestation create accountability (DCO-like), not cryptographic proof of authorship.
2. **Technical** — the file is CI-checkable and agent-readable, so handling of undisclosed AI (`request-disclosure`, `close`, `label-and-review`) is declared up front instead of invented per PR.

## Who decides what goes in the schema?

Public issues here, with a comment period on schema changes. Fields that no real policy expresses get removed. Long-term home is intended to be an established body (OpenSSF-shaped), not this incubator forever.

## Can I still use AI when contributing *to this repo*?

Yes, if disclosed and attested. We dogfood our own [`ai-contribution-policy.yml`](ai-contribution-policy.yml). See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Where should I start?

| If you are… | Do this |
| --- | --- |
| A maintainer under AI load | [Copy a YAML example](spec/examples/) → see [ADOPTION.md](ADOPTION.md) |
| A researcher / curious reader | Read the [policy catalogue](policy-catalogue/) |
| A contributor with 15 minutes | [Add a catalogue entry](policy-catalogue/TEMPLATE.md) |
| Evaluating for an OSPO / foundation | Read this FAQ + [problem-definition.md](problem-definition.md), then open `schema-feedback` |
