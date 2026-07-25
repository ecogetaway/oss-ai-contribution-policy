# Asahi Linux — AI-contribution policy (catalogue entry)

- **Project:** [Asahi Linux](https://asahilinux.org/) ([AsahiLinux](https://github.com/AsahiLinux) organisation)
- **Policy location:** [`docs/project/policies/slop.md` — "Generative AI Policy"](https://github.com/AsahiLinux/docs/blob/09810cd311da3d354685d3673ced269a21bad05f/docs/project/policies/slop.md), added 2025-07-19 in commit [`7c295db`](https://github.com/AsahiLinux/docs/commit/7c295dbb8af7)
- **Captured on:** 2026-07-25 (pinned to `09810cd`)

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (all contributions) | prohibited — "The use of Slop Generators in _any_ contribution to the Asahi Linux project is expressly forbidden," covering code, documentation and engineering decisions |
| stance (community support) | prohibited in practice — answering others' questions with generated output is called out by name, including on third-party platforms such as Reddit |
| disclosure required? mechanism? | n/a (prohibited) |
| attestations required | n/a |
| enforcement | **Exactly one warning, then permanent ban** — "will be met with a single warning. Subsequent disregard for this policy will be met with an immediate and permanent ban from the Asahi Linux project and all associated spaces" |
| authority | Stated as "the opinion of the Board" |
| rationale | Four: intellectual-property risk (with a project-specific variant), environmental resource cost, degradation of community support, and rejection of the agent/assistant framing |
| terminology | Refuses the industry's vocabulary — LLMs are named "Slop Generators" throughout the policy text |
| first-time contributors | No separate gate documented |

## Verbatim excerpt

> "It is the opinion of the Board that Large Language Models (LLMs), herein referred to as Slop Generators, are unsuitable for use as software engineering tools, particularly in the Free and Open Source Software movement."

> "The use of Slop Generators in _any_ contribution to the Asahi Linux project is expressly forbidden. Their use in any material capacity where code, documentation, engineering decisions, etc. are largely created with the \"help\" of a Slop Generators will be met with a single warning. Subsequent disregard for this policy will be met with an immediate and permanent ban from the Asahi Linux project and all associated spaces."

> "Asahi Linux is a _highly_ specific project, working in esoteric problem spaces on publicly undocumented hardware. […] it is not impossible for them to have confidential or leaked material owned by Apple or its vendor partners in their training corpi. […] We already forbid the use of illegally acquired or leaked documentation and tooling (e.g. Apple's internal repair diagnostic tools). This also applies to regurgitated slop."

> "An emerging trend we have observed is people copying user questions or posts into a Slop Generator, then replying to the post with the generated slop. […] others also have access to the same models as you do, and if they wanted an answer from one, they could have asked it themselves."

## Notes

**The AI ban is derived from an existing provenance rule rather than written fresh.** Asahi already forbade illegally acquired or leaked Apple documentation and tooling; the policy extends that specific, pre-existing prohibition to model output on the grounds that a model trained on leaked or confidential material may regurgitate it, and that the risk scales with how esoteric the problem space is. No other catalogued policy reasons this way. It is worth recording because it suggests a project's AI stance can be an inherited consequence of its existing rules rather than an independent choice — and a schema that only captures the resulting stance loses the fact that, for Asahi, changing the AI policy would mean changing the leaked-material policy.

**A numerically specified repeat policy.** "A single warning" followed by "an immediate and permanent ban" is the only quantified escalation ladder in the catalogue apart from Rust's proposed circuit breaker. The v0.1 `enforcement.repeat_policy: maintainer-discretion` default cannot express it, and the difference matters to a contributor deciding whether to risk a judgement call: "one warning" and "maintainer discretion" are very different commitments.

**Environmental cost as a stated rationale — the first in the catalogue.** Copyright (QEMU, Bevy), quality and reviewer burden (servo, tldraw, OpenStreetMap), ethics (Gentoo) and DCO provenance (QEMU) are all represented elsewhere. Resource consumption — energy, water, land, minerals across training and inference — is new here, and it is not reducible to any of the others: a tool that resolved every copyright and quality objection would not satisfy it. Any `rationale` enum that omits it will mis-file this policy.

**Scope extends to community support on third-party platforms.** The "LMGTFY" section addresses people who answer other users' questions by pasting them into a model, explicitly including Reddit. servo's ban covers issues and comments in project spaces; Zig's covers the project's own channels; Asahi reaches conduct in venues the project does not control. If venue scope is ever modelled, this is the widest instance in the corpus.

**The terminology is itself part of the policy.** The document declines to use "AI" or "LLM" as neutral descriptors and argues at length that the agent/assistant framing is "a very deliberate attempt to manufacture consent." A catalogue mapping policies into one comparable shape should probably preserve the fact that some projects reject the shared vocabulary the mapping depends on — the schema's field names are not neutral to a project that considers the framing part of the problem.
