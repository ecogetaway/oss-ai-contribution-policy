# godotengine/godot — AI-contribution policy (catalogue entry)

- **Project:** [godotengine/godot](https://github.com/godotengine/godot)
- **Policy location:** [CONTRIBUTING.md](https://github.com/godotengine/godot/blob/master/CONTRIBUTING.md) (agent-directed notice in the document header)
- **Captured on:** 2026-07-11

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
