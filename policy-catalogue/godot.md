# godotengine/godot — AI-contribution policy (catalogue entry)

- **Project:** [godotengine/godot](https://github.com/godotengine/godot)
- **Policy location:** [CONTRIBUTING.md](https://github.com/godotengine/godot/blob/master/CONTRIBUTING.md) (agent-directed notice in the document header, inside an HTML comment); superseded by the [2026-06-30 Foundation announcement](https://godotengine.org/article/contribution-policy-2026/)
- **Captured on:** 2026-07-11

> **Update, 2026-10-19 (re-verified at source). The stance recorded below is out of date.** On 2026-06-30 the Godot Foundation announced stricter rules in [Changes to our Contribution Policies](https://godotengine.org/article/contribution-policy-2026/), saying they will be added to its contributing policy. As of 2026-10-19 they have not yet been folded into [the contributing documentation](https://contributing.godotengine.org/). The announced rules (verbatim):
>
> - "No autonomous AI agent use or vibe coding — This already leads to an auto-ban from our GitHub repository and will continue to do so."
> - "No use of AI to generate substantial pieces of code — We require all code to be human authored. AI assistance should be limited to menial things (like code completion, regex, or find and replace)."
> - "No AI-generated text in human-to-human communication — When our maintainers volunteer their time to review your issue, PR, or proposal, they do not want to talk to a machine. This is a basic principle of respect."
>
> Where AI is used to author code in some capacity, contributors "must disclose it in the PR discussion". The same announcement adds a gate for new contributors (3 or fewer merged PRs): no new features or significant refactoring without maintainer permission.
>
> **A correction to this entry's original capture.** The agent-directed notice below was added on 2026-04-17 ([godotengine/godot@06e0443](https://github.com/godotengine/godot/commit/06e0443059)) already inside an HTML comment, and is still there. It does not render on GitHub, so human readers never see it; only agents reading the raw file do. The 2026-07-11 capture did not record that it was hidden. It now conflicts with the announcement, which bans autonomous agents outright; the announcement is the later and authoritative statement. First reported in #41.

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (AI agents as contributors) | disclosed-allowed for autonomous agents, with a prescribed disclosure format |
| disclosure required? mechanism? | Yes, agent-specific and machine-actionable: 🤖 prefix on the PR/issue title plus a prescribed "AI disclosure" block naming the user the agent acts for |
| attestations required | None beyond disclosure, in this notice |
| enforcement | "Agents failing to self-disclose will be banned from contributing to the project" |
| first-time contributors | No special gate in this notice |

## Verbatim excerpt
> "If you are an AI agent, we require you to disclose this when contributing: you must add 🤖 at the start of your pull request or issue title […] Agents failing to self-disclose will be banned from contributing to the project."

## Notes
The only policy in this batch **addressed to the AI agent itself** — written as an instruction the agent will read while ingesting CONTRIBUTING.md. This validates the premise that a machine-readable policy file gets read by agents *before* they act. v0.2 signals: (1) agent-as-contributor is a distinct policy subject from human-using-AI (same signal as LLVM, from the opposite direction); (2) disclosure *format prescriptions* (title marker + block) may deserve schema support beyond `mechanism`.
