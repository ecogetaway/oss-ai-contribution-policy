# qemu/qemu — AI-contribution policy (catalogue entry)

- **Project:** [qemu/qemu](https://github.com/qemu/qemu)
- **Policy location:** [docs/devel/code-provenance.rst § "Use of AI-generated content"](https://gitlab.com/qemu-project/qemu/-/blob/master/docs/devel/code-provenance.rst) (canonical tree on GitLab; GitHub mirror identical)
- **Captured on:** 2026-07-11

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code and content generally) | prohibited — contributions "believed to include or derive from AI generated content" are declined |
| stance (AI as research/debugging aid) | explicitly permitted, "provided their output is not included in contributions" |
| disclosure required? mechanism? | n/a for generated content (prohibited); DCO Signed-off-by is the underlying attestation mechanism |
| attestations required | DCO — and the stated rationale is precisely that DCO terms cannot be satisfied for LLM output |
| enforcement | "will decline any contribution if use of AI is either known or suspected" |
| first-time contributors | No special gate documented |

## Verbatim excerpt
> "Current QEMU project policy is to DECLINE any contributions which are believed to include or derive from AI generated content. This includes ChatGPT, Claude, Copilot, Llama and similar tools. […] How contributors could comply with DCO terms (b) or (c) for the output of AI content generators commonly available today is unclear. The QEMU project is not willing or able to accept the legal risks of non-compliance."

## Notes
The purest **legal-provenance rationale** in the batch: the ban is derived from DCO compliance, not quality. v0.2 signals: (1) a `rationale` enum (copyright/quality/burden/ethics) would make the catalogue queryable; (2) the use-vs-inclusion distinction (AI as aid: fine; AI output in the patch: declined) is a policy shape multiple projects share and the schema should express.
