# godotengine/godot — AI-contribution policy (catalogue entry)

- **Project:** [godotengine/godot](https://github.com/godotengine/godot)
- **Policy location:** [Changes to our Contribution Policies](https://godotengine.org/article/contribution-policy-2026/) — Godot Foundation blog (2026-06-30); the Foundation says the amended policy will be folded into the [contributing documentation](https://contributing.godotengine.org/)
- **Captured on:** 2026-09-27

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (autonomous AI agents) | prohibited — "No autonomous AI agent use or vibe coding"; such use already leads to an auto-ban from the GitHub repository |
| stance (AI-assisted code by a human contributor) | restricted — "No use of AI to generate substantial pieces of code"; all code must be human-authored; AI assistance limited to menial things (code completion, regex, find-and-replace) |
| stance (AI-generated text in human-to-human communication) | prohibited — maintainers "do not want to talk to a machine" |
| disclosure required? mechanism? | Yes, for any AI code assistance: "If you do use AI in some capacity to author code, you must disclose it in the PR discussion" |
| attestations required | Human authorship and accountability: contributors must be "able and willing to fix" their code; all PRs reviewed and approved by a human before merging |
| enforcement on non-disclosure | Auto-ban from the GitHub repository for autonomous AI agent use |
| first-time contributors | Separate gate in the same announcement: no new features or significant re-factoring from contributors with ≤3 merged PRs without explicit maintainer permission |

## Verbatim excerpt
> "No autonomous AI agent use or vibe coding — This already leads to an auto-ban from our GitHub repository and will continue to do so."
>
> "No use of AI to generate substantial pieces of code — We require all code to be human authored. AI assistance should be limited to menial things (like code completion, regex, or find and replace)."
>
> "No AI-generated text in human-to-human communication — When our maintainers volunteer their time to review your issue, PR, or proposal, they do not want to talk to a machine. This is a basic principle of respect."

## Notes
Supersedes the 2026-07-11 capture: the agent-directed 🤖 disclosure notice in `godotengine/godot`'s `CONTRIBUTING.md` is now commented out (no longer rendered), and this Foundation-level announcement replaces it. v0.2 signal: the policy grades stance by subject — prohibited for autonomous agents, restricted for human AI-assistance, prohibited for AI text in comms — which a single `stance` field strains to express.
