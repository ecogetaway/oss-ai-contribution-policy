# Mesa — AI-contribution policy (catalogue entry)

- **Project:** [mesa/mesa](https://gitlab.freedesktop.org/mesa/mesa) (canonical tree on freedesktop GitLab)
- **Policy location:** [`docs/submittingpatches.rst` § "Expectations on contributors"](https://gitlab.freedesktop.org/mesa/mesa/-/blob/7a6f5690575edc7113ff0da4281d8a646114be28/docs/submittingpatches.rst)
- **Captured on:** 2026-07-25 (pinned to `7a6f569`)

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | disclosed-allowed — tool choice is the contributor's, but "no tool can substitute actual understanding," and the submitter carries full responsibility including MIT-licensability |
| stance (autonomous agents) | prohibited — "It is not allowed to use autonomously acting tools to submit any contributions"; extends to autonomous interaction with GitLab issues and MRs; "Do not under any circumstances wire up any review bot or similar tools" |
| disclosure required? mechanism? | **Required whenever AI was involved in the creative process**, via commit trailers, with a two-tier vocabulary: `Assisted-by: TOOL (OPTIONAL: MODEL)` when AI helped make decisions or generated parts, `Generated-by: TOOL (OPTIONAL: MODEL)` when almost all the code was generated. `Co-authored-by:` is explicitly reserved for humans and must not be used |
| disclosure exemptions | Two, both drawn at the limit of distinguishability: changes too trivial to be copyrightable regardless of AI involvement (e.g. a `min` function), and mechanical changes whose result "would be the same regardless of what tooling was used" (autocomplete, variable renames). Disclosure is still *recommended* in the second case |
| granularity | tool, optionally model, plus a degree tier — the finest disclosure granularity in the catalogue |
| attestations required | understands-change in substance: the submitter "needs to understand what code they are changing, what the change does, and justify that change in the commit messages" |
| enforcement | Not specified as a sanction; framed as responsibility and reviewability. Tooling adoption is a community/maintainer decision |
| first-time contributors | No special gate documented |

## Verbatim excerpt

> "The submitter is responsible for the code change, regardless of where that code change came from, whether they wrote it themselves, used an \"AI\" or other tool, or got it from someone else. That responsibility includes making sure that the code change can be submitted under the MIT license that Mesa uses."

> "It is not allowed to use autonomously acting tools to submit any contributions, that is every contributions needs explicit oversight and your review. This includes interactions with GitLab issues or MRs in any autonomous way through such tools. […] Do not under any circumstances wire up any review bot or similar tools."

> "Disclosure is always required when \"AI\" was involved in the creative process of coming up with the code, except in the following cases:
> - Trivial or small changes that wouldn't be copyrightable regardless of \"AI\" involvement. For example something like a \"min\" function fit this category.
> - Mechanical changes where the expected result is obvious and not up to interpretation, ie. when it would be the same regardless of what tooling was used."

> "We suggest the following scheme to disclose the level \"AI\" tooling was involved:
> - `Assisted-by: TOOL (OPTIONAL: MODEL)` for when \"AI\" was involved in making decisions or also generated parts of the code.
> - `Generated-by: TOOL (OPTIONAL: MODEL)` for when almost all the code was generated through \"AI\".
> Do not use the `Co-authored-by` tag as this one is reserved for human co-authors."

## Notes

**The only graduated disclosure vocabulary in the catalogue.** Fedora and LLVM each specify a single `Assisted-by:` trailer; Mesa distinguishes `Assisted-by:` from `Generated-by:` by how much of the change the model produced, and invites naming the model as well as the tool. The v0.1 schema's `granularity: tool-and-role | role-only | binary` is close but doesn't reach this: Mesa's scheme is tool **and** model **and** a degree tier, expressed in a fixed trailer grammar. If any single catalogued policy should drive the shape of a disclosure field, it is probably this one — it is the most machine-readable disclosure convention in the corpus and needs no new infrastructure to adopt.

**`Co-authored-by:` is reserved for humans — the third project to legislate on this trailer, and the three do not agree.** Fedora recommends `Assisted-by:`; Kubernetes forbids `assisted-by`/`co-developed` and AI co-authorship outright; Mesa mandates `Assisted-by:`/`Generated-by:` while banning `Co-authored-by:` for tools. Same mechanism, three incompatible conventions, all mechanically checkable. This is the sharpest available argument that the fragmentation this catalogue documents is not merely rhetorical — it is already encoded in commit metadata that CI could enforce today, differently in each project.

**Exemptions drawn at the limit of distinguishability, reached from the permissive side.** Mesa exempts changes that "would be the same regardless of what tooling was used." Bevy's `[^1]` footnote exempts trivial completions because they are "by definition not detectable." One policy allows AI and one bans it, and both scope the rule to what an observer could in principle distinguish. Two independent arrivals at the same boundary is a strong signal that the boundary is real and belongs in the schema's vocabulary rather than in each project's prose.

**Copyrightability used as the exemption test, not as a rationale.** QEMU and Bevy invoke copyright to justify prohibition; Mesa invokes it to define where disclosure stops mattering. The same legal concept doing opposite work in two directions is worth noting if a `rationale` enum is added — rationale and scope-test are different roles for the same idea.

**Review bots are banned by name.** Alongside LLVM ("unattended review bots") and Home Assistant, this is the third policy to prohibit automated review tooling from contributors — while Mesa simultaneously reserves the right for the project itself to adopt such tooling ("It will be decided by the community and maintainers which and how such tooling will be used"). That asymmetry — contributors may not, the project may — matches the reciprocal-disclosure signal in the Home Assistant entry and suggests the schema is missing a project-side dimension entirely.
