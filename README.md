Open source's open-contribution model is closing in real time. AI-assisted contribution has flooded maintainers with plausible-looking submissions they cannot cheaply verify — and projects are responding by shutting doors that took thirty years to open.

This repository defines a machine-readable standard — **`ai-contribution-policy.yml`** — that lets a project declare its AI-contribution policy once, in a form readable by humans, CI, forges, and AI coding agents themselves. It is built on one design decision: **verification, not detection.**

# OSS AI-Contribution Policy

This is the third application of an evidence-first method already published for internationalization (CACM, DevOps.com) and in progress for accessibility: document how the problem actually plays out in real repositories, then build the smallest piece of infrastructure the evidence says is missing.

**Provenance.** Part of the **OSS Infrastructure Initiative** (Sanjay C. and Aniruddh Raghavendra) — an evidence-first portfolio applying one method across three under-served open source contribution domains: internationalization, accessibility, and AI contribution. First published July 2026. Full portfolio under [Companion Projects](#companion-projects) below.

_Status: early-stage — schema v0.1 drafted, nine verified catalogue entries, and the first case study complete._

## Terminology used in this repo

- **the policy file** = `ai-contribution-policy.yml`, the machine-readable standard this project defines
- **disclosure** = a contributor stating what role AI played in a contribution
- **attestation** = a contributor affirming specific verification steps ("I ran the tests," "I understand every line")
- **catalogue** = the mapped corpus of existing per-project AI-contribution policies
- **case studies** = structured write-ups of real projects' collisions with AI-assisted contribution

---

## The Problem

Maintainers are the load-bearing humans of digital infrastructure, and AI-generated contribution volume is now a leading driver of their burnout. The visible casualties are public and accumulating: curl ended its bug bounty under a flood of AI-generated reports; Ghostty and tldraw restricted external pull requests; Jazzband dissolved. Each closure removes a pathway by which the commons renews itself.

The damage lands on three groups at once:

1. **Maintainers** — a few thousand people carrying disproportionate load for software embedded in banking, healthcare, government, and communications, now spending their scarcest resource (review attention) triaging plausible-looking noise.
2. **Good-faith contributors, especially new ones** — without a disclosure-and-verification standard, responsible AI-assisted work is rejected on sight alongside the slop. Contributors from the Global South, students, and career-changers are precisely the people who benefit most from AI assistance and suffer most from blanket bans.
3. **Everyone downstream** — closed contribution pipelines degrade the security and maintenance of software effectively everyone uses.

Projects are defending themselves anyway — with dozens of incompatible, hand-rolled policies buried in CONTRIBUTING files, issue templates, and blog posts. The defense exists. The **standard shape** for it does not.

## Why Now

- The trendline is active: every month of delay is another project that closes external contribution rather than manage it.
- The consensus fix already exists in fragments — disclosure plus human verification — but has no machine-readable primitive to run on.
- A remediation market has already emerged downstream: commercial services now charge five figures per engagement to refactor AI-generated codebases back to maintainability (e.g., [Slopfix](https://odra.dev/slopfix/), a three-engineer consultancy priced at ~$10k/week against measured code-reduction targets; captured 2026-07-11). When the *cure* is already being sold, the case for standardizing *prevention at the contribution boundary* — where the cost is a policy file and a review pathway — makes itself.
- AI coding agents increasingly read repository files before acting. A standard policy file is the first defense that works *before* the pull request is generated, not after.
- Institutional money and attention (OpenSSF's AI-integrity commitments, forge-level interest) arrived with this problem. The window for an evidence-backed, community-owned standard — rather than a vendor-owned one — is open now.

---

## Adopt in 10 Minutes

1. Copy a worked example that matches your posture — [permissive](spec/examples/oss-ai-contribution-policy.ai-contribution-policy.yml) or [strict](spec/examples/illustrative-strict-project.ai-contribution-policy.yml) — to your repository root as `ai-contribution-policy.yml`.
2. Edit four things: your project name, your per-asset **stance**, the **attestations** you require, and what happens on **non-disclosure**.
3. Set `last_reviewed` to today and commit. Link it from CONTRIBUTING.md.

That's the whole adoption cost. Your policy is now in one predictable place — for contributors, for CI, and for AI agents that read repository files before acting. If you adopt it, [tell us](../../issues) — early adopters shape schema v0.2.

---

## The Proposed Standard

Three artifacts, in dependency order:

### 1. `ai-contribution-policy.yml`
A file at the repository root — sibling to LICENSE, CODEOWNERS, and SECURITY.md — declaring:
- the project's **stance** per asset class (code, docs, translations, media): disclosed-allowed, restricted, or prohibited
- what **disclosure** is required and how it's expressed (PR checkbox, commit trailer)
- which **attestations** a contributor must make (tests run, change understood, output reviewed line-by-line)
- what happens on **non-disclosure**, stated plainly rather than discovered in an angry comment thread

Draft schema: [`spec/ai-contribution-policy.schema.yml`](spec/ai-contribution-policy.schema.yml), with worked examples in [`spec/examples/`](spec/examples/).

### 2. The contributor pathway
A specification for how a good-faith contributor complies: disclose role, attest verification, provide evidence. Designed so that following it is *easier* than evading it, and so a first-time contributor can succeed without reading a debate thread.

### 3. The evidence base
A catalogue mapping 60+ existing per-project policies ([`policy-catalogue/`](policy-catalogue/)) and 5–8 deep case studies of real collisions ([`case-studies/`](case-studies/)) — so the schema encodes what projects actually need, not what sounds plausible.

First nine catalogued (every entry verified against its primary source on the capture date):

| Project | Stance | Distinctive feature |
| --- | --- | --- |
| [Ghostty](policy-catalogue/ghostty.md) | disclosed-allowed | Vouch system; public denouncement list; AI media prohibited |
| [LLVM](policy-catalogue/llvm.md) | disclosed-allowed | `Assisted-by:` trailer; autonomous agents banned |
| [curl](policy-catalogue/curl.md) | disclosed-allowed | Stricter rules for security reports; bug bounty ended Jan 2026 → [case study](case-studies/curl-bug-bounty-closure.md) |
| [Godot](policy-catalogue/godot.md) | disclosed-allowed (agents) | Policy addressed to the AI agent itself |
| [NetBSD](policy-catalogue/netbsd.md) | prohibited-unless-escalated | LLM output "presumed tainted"; core-approval exception |
| [QEMU](policy-catalogue/qemu.md) | prohibited | Ban derived from DCO/copyright provenance |
| [servo](policy-catalogue/servo.md) | prohibited | Four argued rationales; explicit revisit clause |
| [Gentoo](policy-catalogue/gentoo.md) | prohibited | Council-voted 2024; packaging carve-out |
| [tldraw](policy-catalogue/tldraw.md) | closed to external PRs | Total pathway closure, framed as temporary |

**Why verification, not detection:** every detection-based approach is an arms race the detectors lose. Attestation of human review, testing, and understanding stays meaningful no matter how good the models get. That single decision is what keeps this standard from being obsolete on arrival.

---

## Who Benefits

| Group | What changes for them |
| --- | --- |
| Maintainers | One declared policy replaces per-PR arguments; mismatched contributions filtered before they consume review attention |
| Good-faith contributors | A visible, achievable pathway — disclose and verify — instead of guessing or being rejected on sight |
| New contributors | The on-ramp stays open; blanket bans are replaced by explicit, meetable expectations |
| AI coding tools | A file their agents can read *before* generating a PR, making policy compliance automatic |
| Forges and foundations | A standard shape to surface natively, the way SECURITY.md is surfaced today |
| Downstream users | Contribution pipelines that stay open and reviewed, instead of closed or overwhelmed |

## What This Is / What This Is Not

| What this is | What this is not |
| --- | --- |
| A machine-readable policy standard and contributor pathway | An AI-detection tool or arms-race participant |
| An evidence base: catalogued policies and scored case studies | A think-piece or one project's opinion generalized |
| Community-owned, Apache-2.0, built toward a standards body | A vendor wedge or a paid gate in front of contribution |
| A way to keep contribution pathways open under AI pressure | A ban on AI assistance — or an endorsement of undisclosed use |

---

## Maintainer Principles

The standard is built by and for maintainers, on three commitments:

1. **Verification over detection.** We never ask "was this written by AI?" — an unanswerable question. We ask "has a human verified this?" — an answerable one. Attestations are of human actions: tests run, behavior checked, every line understood.
2. **Clarity over complexity.** The policy file must be writable in ten minutes and readable in one. Any field that requires a lawyer or a committee to fill in is a field we remove.
3. **Openness over gatekeeping.** The measure of success is not how much the standard filters out but how many good-faith contributors it lets through. A policy file that only says "no" is a failure of this standard, even if it is syntactically valid.

---

## Roadmap

**Phase 1 — Evidence (current).** Catalogue 60+ existing AI-contribution policies; write 5–8 anchor case studies (curl, Ghostty, tldraw, Jazzband among the candidates); publish the field report that makes the pattern undeniable.

**Phase 2 — Standard.** Schema v0.1 (drafted here) hardened against the catalogue: every field must earn its place by mapping to something real projects already do by hand. Contributor-pathway spec alongside it.

**Phase 3 — Pilots.** 2–3 repositories adopt the policy file; measure mismatched-contribution volume reaching maintainer review and median time-to-first-review, before vs. after. Published quarterly, negative results included.

**Phase 4 — Institution.** Propose a working group in an established standards home (OpenSSF-shaped) so the standard outlives this repository. Forge-native surfacing of the file is the endgame.

## How to Contribute

Start small — every pathway below begins with a single-file, easily reviewable PR:

1. **Add a policy to the catalogue** (smallest): one file documenting one project's existing AI-contribution policy, with a link and a date. Label: `policy-catalogue`.
2. **Nominate or draft a case study**: a real project's collision with AI-assisted contribution, using [`case-studies/TEMPLATE.md`](case-studies/TEMPLATE.md). Label: `case-study-candidate`.
3. **Critique the schema**: open an issue against a specific field of [`spec/ai-contribution-policy.schema.yml`](spec/ai-contribution-policy.schema.yml) — what's missing, what's unclear, what would stop *your* project from adopting it. Label: `schema-feedback`.
4. **Share maintainer experience**: what AI-contribution load actually looks like in your queue. Label: `community-feedback`.

Disclosure expectations for contributing *here* follow our own draft standard — see [`CONTRIBUTING.md`](CONTRIBUTING.md). We dogfood what we propose.

## Pilot Invitation

If you maintain a repository that receives AI-assisted contributions — welcome, unwelcome, or undisclosed — we want 2–3 pilot projects to adopt `ai-contribution-policy.yml` and let us measure what changes. Pilots get: help writing their policy file, a documented baseline, and public credit as co-designers of the standard. Open an issue with the `pilot` label, or see the pinned pilot issue.

## Governance and Next Steps

- **License:** Apache-2.0. The standard stays open and community-owned; that is a design constraint, not a preference.
- **Decisions:** documented in public issues in this repository, with a comment period on schema changes. As the maintainer panel forms (compensated maintainer co-design is part of the funded roadmap), schema authority shifts to it.
- **Long-term home:** this repository is the incubator, not the destination. Phase 4 proposes the standard into an established body (OpenSSF-shaped working group) once pilots produce evidence worth standardizing.
- **Next concrete steps:** policy catalogue to 60+ entries; first two case studies drafted; schema v0.1 field-by-field review issue open for comment.

## Anticipated Questions

**Isn't this just another opinion about AI and open source?**
No — it's a catalogue first. Nine projects' policies verified against live primary sources, one deep case study, and a schema whose every field must map to something real projects already do by hand. Where the evidence is thin, the documents say so. Opinions are cheap in this debate; the [policy catalogue](policy-catalogue/) is the part you can check.

**Why not just detect AI-generated contributions?**
Because detection is an arms race the detectors lose — accuracy degrades with every model generation, and false positives land hardest on non-native English writers and newcomers. Attestation of *human actions* (tests run, change understood, output reviewed) stays meaningful no matter how good generation gets. That single design decision is why this standard doesn't expire.

**Does disclosure actually reduce the burden?**
Honestly: measuring that is the point of the pilots. What the catalogue already shows is that the projects that kept their doors open (Ghostty, LLVM, curl, Godot) all converged independently on disclosure-plus-verification — and that curl's disclosure policy alone wasn't sufficient to save its bug bounty. We publish pilot results either way, negative findings included.

**What about projects that prohibit AI contributions entirely?**
The standard is stance-neutral. `prohibited` is a first-class value, and a machine-readable "no" is more useful than a buried one — an AI coding agent that reads the file can decline to generate the PR at all. QEMU, servo, and Gentoo's positions are documented in the catalogue with the same care as the permissive ones.

**How would this ever be enforced?**
Two layers, honestly labeled. Social: a self-certified pathway, like DCO — attestations create accountability, not proof. Technical: the file is CI-checkable and agent-readable, so undisclosed-AI handling (`request-disclosure`, `close`, `label-and-review`) is declared before the argument starts instead of invented per-PR. Enforcement that requires proving what wrote the code is exactly the arms race we refuse (see detection, above).

**Who decides what goes in the standard?**
For now: public issues in this repository, with a comment period on schema changes and a field-survival rule — a field no real policy expresses gets removed. The roadmap's endgame is handing the spec to an established standards home (OpenSSF-shaped working group) once pilots produce evidence worth standardizing. This repo is the incubator, not the throne.

## Related Work

- The arXiv taxonomy of AI-contribution policies and RedMonk's policy cataloguing describe the space — neither owns a machine-readable primitive. This project builds the primitive, citing both.
- DCO and CLA workflows prove that per-contribution attestation at scale works in open source.
- SECURITY.md's history is the adoption model: a simple file, a clear shape, then forge-native surfacing.

## Companion Projects

Three repositories, one method: document how a contribution domain actually fails in real repositories, then build the smallest machine-readable piece of infrastructure the evidence says is missing. Each domain's adoption compounds the others' credibility.

| Domain | Repository | What it builds | Maturity |
| --- | --- | --- | --- |
| Internationalization | [oss-language-inclusion](https://github.com/ecogetaway/oss-language-inclusion) | Translated-string contribution evidence + `i18n-security-lint` CI tooling | Most developed; method published in CACM Blog and DevOps.com |
| Accessibility | [oss-accessibility-inclusion](https://github.com/ecogetaway/oss-accessibility-inclusion) | How accessibility PRs are reviewed; review rubric + draft `a11y-signals.yml` | Active |
| AI contribution | [oss-ai-contribution-policy](https://github.com/ecogetaway/oss-ai-contribution-policy) | Machine-readable `ai-contribution-policy.yml` standard (verification over detection) | Early evidence-gathering |

---

Licensed under Apache-2.0.
