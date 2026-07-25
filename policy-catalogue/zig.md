# Zig / Zig Software Foundation — AI-contribution policy (catalogue entry)

- **Project:** [ziglang/zig](https://github.com/ziglang/zig) (primary development has moved to [Codeberg](https://codeberg.org/ziglang/zig); the GitHub repository remains published)
- **Policy location:** [ziglang.org/code-of-conduct](https://ziglang.org/code-of-conduct/) § "Strict No LLM / No AI Policy". Surfaced in-repo through the issue-template chooser at [`.forgejo/ISSUE_TEMPLATE/config.yml`](https://github.com/ziglang/zig/blob/738d2be9d6b6ef3ff3559130c05159ef53336224/.forgejo/ISSUE_TEMPLATE/config.yml), which links to it under the heading "Copilot and Other LLMs". The former wiki page now redirects to the Code of Conduct.
- **Captured on:** 2026-07-25 (repo link pinned to `738d2be`; the Code of Conduct is a website page with no commit pin available)

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | prohibited — "No LLM-generated content, whether it be code or prose" |
| stance (prose, docs, issues, comments) | prohibited, including paraphrase — "No paraphrasing LLM-generated content" |
| stance (editing / proofreading) | prohibited — "No LLMs for editing, including fixing spelling or grammatical errors" |
| stance (translations) | **prohibited** — "No LLMs for translation." Accessibility is solved differently: "English is encouraged, but not required. You are welcome to post in your native language and rely on others to have their own translation tools of choice to interpret your words" |
| stance (ideation) | prohibited — "No LLMs for brainstorming and then sharing the results of that brainstorming, even if you create the prose" |
| stance (bug finding) | prohibited — "No LLMs for finding bugs" |
| stance (discussion of tools) | prohibited — "No talking about use of chatbot/LLM services" |
| disclosure required? mechanism? | n/a (prohibited) |
| attestations required | n/a |
| enforcement | Not specified as a mechanism in the policy text; the rules sit inside the Code of Conduct, so CoC processes apply |
| venue scope | The Code of Conduct governs the issue tracker, IRC and the development Zulip — the policy is space-scoped, not artifact-scoped |
| first-time contributors | No separate gate; a separate rule bars unchampioned language proposals from anyone |

## Verbatim excerpt

> "**Strict No LLM / No AI Policy**
> No LLM-generated content, whether it be code or prose.
> No paraphrasing LLM-generated content.
> No LLMs for editing, including fixing spelling or grammatical errors.
> No LLMs for translation. English is encouraged, but not required. You are welcome to post in your native language and rely on others to have their own translation tools of choice to interpret your words.
> No LLMs for brainstorming and then sharing the results of that brainstorming, even if you create the prose.
> If you use a chatbot to give you advice on a comment on the issue tracker, that comment is unwelcome.
> No LLMs for finding bugs.
> No talking about use of chatbot/LLM services."

> "Please do not use GitHub Copilot or any other LLM to write an issue." — `.forgejo/ISSUE_TEMPLATE/config.yml`

## Notes

**The strictest policy in the catalogue, and the only one that reaches upstream of the artifact.** Every other prohibition here governs what may be *submitted*. Zig also bars using an LLM to brainstorm even when the contributor writes the prose themselves, and bars acting on chatbot advice when commenting. The regulated object is the contributor's process, not the contribution. No schema field models that, and it is not obvious one should — but it marks the far end of the range any stance vocabulary has to span.

**It bans LLM translation, which four other catalogued policies explicitly permit or encourage** (Fedora encourages it, Bevy exempts it, Home Assistant accommodates it, Rust allows it with disclosure). Zig resolves the same accessibility problem in the opposite direction: post in your own language and let each reader translate for themselves. That is a substantive disagreement about *where* the translation should happen, not about whether non-English speakers are welcome — and it means a `translations` stance value cannot be read as a proxy for inclusiveness. Worth capturing the reasoning, not just the value.

**A speech rule, not a contribution rule.** "No talking about use of chatbot/LLM services" regulates discussion in the project's spaces. Nothing else in the catalogue restricts what contributors may *discuss*, as opposed to what they may submit. If the schema ever models venue scope, this is the clearest case that the unit being governed is sometimes a space rather than an artifact.

**Policy lives in the Code of Conduct.** Every other catalogued policy sits in CONTRIBUTING, a dedicated AI policy file, or governance docs. Zig puts these rules in the CoC, which changes the enforcement path (CoC process rather than PR closure) and the scope (all project spaces, not just the contribution pathway). Rust's proposal reaches for the same framing from the other end — treating non-disclosure as a CoC violation — so this is now a pattern with two instances.

**Discoverability is worth noting for a machine-readable standard's purposes.** The operative text is on the website; the repository surfaces it only as a one-line link in the issue-template chooser, and the old wiki page is a redirect. An agent reading the repository would find the pointer but not the policy. That is exactly the resolution problem a `canonical_url` field would address — the same issue Home Assistant raises from the opposite direction, where the repo holds a copy that declares itself non-authoritative.
