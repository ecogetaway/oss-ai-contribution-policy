# Home Assistant / Open Home Foundation — AI-contribution policy (catalogue entry)

- **Project:** [home-assistant/core](https://github.com/home-assistant/core) — policy is Open Home Foundation-wide, applying to all OHF projects
- **Policy location:** [`AI_POLICY.md`](https://github.com/home-assistant/core/blob/702a9cb7289e535927f5279190bcad6ffc5d3fd0/AI_POLICY.md), added [2026-07-21 (#176917)](https://github.com/home-assistant/core/pull/176917); referenced from [`CONTRIBUTING.md`](https://github.com/home-assistant/core/blob/702a9cb7289e535927f5279190bcad6ffc5d3fd0/CONTRIBUTING.md) and [`AGENTS.md`](https://github.com/home-assistant/core/blob/702a9cb7289e535927f5279190bcad6ffc5d3fd0/AGENTS.md). The file declares itself a copy: canonical version at <https://developers.home-assistant.io/docs/ai_policy>
- **Captured on:** 2026-07-25 (repo copy pinned to `702a9cb`)

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code / documentation) | disclosed-allowed in substance — "AI can be a helpful tool," but "we require a human in the loop who understands the work produced by AI" |
| stance (autonomous agents) | prohibited — "We do not allow autonomous agents to be used for contributing to our projects," including **contributions that bypass the provided issue or pull request templates** |
| stance (communication: issues, PRs, code reviews) | restricted — AI may assist writing, but "do not have tools post unreviewed content on your behalf"; answers to maintainer questions must not be AI-generated |
| stance (translations / non-native speakers) | permitted and accommodated — grammar and clarity assistance is fine; translated comments should carry the original text in a details block |
| disclosure required? mechanism? | Prescribed for AI-derived context in conversation: it "must be in a quote block (e.g., using `>`) and disclosed as such," accompanied by the contributor's own commentary; long snippets discouraged. No trailer or PR-template field for code |
| attestations required | understands-change and reviewed-output in substance: "All contributions must be reviewed and understood by the contributor before submission. You should be able to explain every change in a pull request you submit" |
| enforcement | Closure — "Contributions that do not follow this policy will be closed"; unreviewed-looking AI output closed without review; suspected autonomous comments may be marked as spam; repeat violations may result in being blocked across OHF projects; appeal by contacting a maintainer |
| **project's own AI use** | **Disclosed** — some OHF projects use AI for code review, triage and reporting; such comments "are not always correct" and maintainers have the final say |
| first-time contributors | No separate gate documented |

## Verbatim excerpt

> "**We do not allow autonomous agents to be used for contributing to our projects.** We will close any pull requests or issues that we believe were created autonomously, and may mark automated comments as spam. This includes contributions that bypass the provided issue or pull request templates."

> "If you wish to include context from an interaction with AI in your comments, it must be in a quote block (e.g., using `>`) and disclosed as such. It must be accompanied by your own commentary explaining the relevance and implications of the context. Do not share long snippets."

> "**Do not use AI to generate answers to questions from maintainers.** You should understand and be able to explain your own work. Using AI to improve grammar or clarity is fine, but the substance of your responses must be your own."

> "Some of our projects use AI tools to assist with code reviews, issue triaging, reporting, and other project management tasks. These tools may leave comments on pull requests or issues. As with any automated tooling, these comments are not always correct."

> "The canonical version of this policy is published at <https://developers.home-assistant.io/docs/ai_policy>. In case of differences, the published version applies."

## Notes

**The only catalogued policy that discloses the project's own AI use.** Every other entry regulates what contributors must reveal; Home Assistant also states that OHF projects run AI review and triage tooling, that its comments may be wrong, and how a contributor should treat them. The v0.1 schema is one-directional by construction — `disclosure` describes an obligation flowing toward the maintainers. Reciprocal disclosure is a genuinely new field candidate, and arguably the one most consistent with this standard's stated posture, since a project asking for transparency is in a stronger position having declared its own.

**Template bypass used as an observable proxy for autonomy.** "Contributions that bypass the provided issue or pull request templates" is offered as evidence of autonomous operation. Whether a contribution was autonomous is not decidable from the artifact; whether it filled in the template is. This is the same move Godot makes from the opposite direction (require a marker rather than infer one), and it is the only instance in the catalogue of a project substituting a *checkable* signal for an *unanswerable* one inside a prohibition clause. Worth flagging in any enforcement-related schema work.

**A policy file that declares itself non-authoritative.** The repository copy names an external canonical URL and states that the published version wins on conflict. For a standard whose premise is a machine-readable file at the repository root, this is a live design question: an adopter with an org-level canonical policy needs a way to say "this file is a mirror of X" so that agents and CI resolve the right text. A `canonical_url` plus an explicit precedence rule looks cheaper than the alternative of silently divergent copies.

**Org-level policy inherited by member projects.** The document is Open Home Foundation-wide; `home-assistant/core` links to it rather than owning it. Same shape as Bevy. Two of the newest policies in the catalogue are org-scoped, which suggests project-level granularity is going to be the exception rather than the rule as this matures.

**Communication is treated as a first-class asset class, with a prescribed format.** Alongside llama.cpp, this is the second catalogued policy whose real dividing line is artifact-versus-conversation rather than code-versus-docs — and the only one that prescribes a *shape* for disclosed AI content in conversation (quote block, disclosed as such, with the contributor's own commentary). Godot prescribes a marker for the contribution; Home Assistant prescribes one for the discussion around it.

**Non-native speaker provision with a concrete mechanism.** Like Fedora and Bevy, translation assistance is welcomed; unlike them, it suggests an artifact — the original text in a details block — framed as evidence of effort and as an aid to maintainers verifying the translation.
