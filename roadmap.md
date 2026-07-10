# Roadmap

## Phase 1 — Evidence (current)
- [ ] Policy catalogue: map 60+ existing per-project AI-contribution policies into a comparable shape ([`policy-catalogue/`](policy-catalogue/)).
- [ ] 5–8 anchor case studies of real collisions — curl's bug-bounty closure, Ghostty and tldraw's PR restrictions, and Jazzband's dissolution are the opening candidates ([`case-studies/`](case-studies/)).
- [ ] Field report drawing the trendline, publishable in the same venues as the companion projects' work (CACM Blog, DevOps.com).

## Phase 2 — Standard
- [x] Schema v0.1 drafted ([`spec/ai-contribution-policy.schema.yml`](spec/ai-contribution-policy.schema.yml)) with two worked examples, including this repository's own.
- [ ] Schema v0.2: every field validated against the catalogue — a field survives only if it maps to something real projects already do by hand.
- [ ] Contributor-pathway specification: disclosure, attestation vocabulary, and evidence expectations as a portable document.
- [ ] Validator tool (CI-runnable) for the policy file.

## Phase 3 — Pilots
- [ ] 2–3 repositories adopt `ai-contribution-policy.yml` with a documented baseline.
- [ ] Measure: mismatched-contribution volume reaching maintainer review, and median time-to-first-review, before vs. after. Published quarterly, negative results included.
- [ ] 10–20 contributors complete the disclosed-and-verified pathway end-to-end — evidence the standard keeps doors open rather than just filtering.

## Phase 4 — Institution
- [ ] Working-group proposal to an established standards home (OpenSSF-shaped).
- [ ] Forge-level conversation: native surfacing of the policy file, the way SECURITY.md is surfaced today.
- [ ] Agent-side adoption: at least one AI coding tool reads the file before opening PRs.

## Principles that govern the roadmap
Evidence before standard; standard before pilots; pilots before institutionalization. Each phase's output is public regardless of how flattering it is.
