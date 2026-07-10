# llvm/llvm-project — AI-contribution policy (catalogue entry)

- **Project:** [llvm/llvm-project](https://github.com/llvm/llvm-project)
- **Policy location:** [llvm/docs/AIToolPolicy.md](https://github.com/llvm/llvm-project/blob/main/llvm/docs/AIToolPolicy.md)
- **Captured on:** 2026-07-11

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code, RFCs, issues, review comments) | disclosed-allowed — "contributors can use whatever tools they would like … but there must be a human in the loop" |
| stance (autonomous agents) | prohibited — "bans agents that take action in our digital spaces without human approval"; unattended review bots included |
| disclosure required? mechanism? | Yes for "substantial amounts of tool-generated content" — commit trailer suggested: `Assisted-by: <name of code assistant>` |
| attestations required | understands-change and reviewed-output in substance: "must read and review all LLM-generated code or text" and "be able to answer questions about their work" |
| enforcement | Not specified as a sanction; framed as review-worthiness and accountability |
| first-time contributors | Welcomed, steered to "start with small contributions"; **AI tools must not be used on `good first issue` items** |

## Verbatim excerpt
> "LLVM's policy is that contributors can use whatever tools they would like to craft their contributions, but there must be a **human in the loop**. […] Contributors are expected to **be transparent and label contributions that contain substantial amounts of tool-generated content** … use a commit message trailer like Assisted-by: <name of code assistant>."

## Notes
Closest existing policy to this project's draft schema (disclosure + attestation + trailer mechanism). Three v0.2 signals: (1) **agent vs. human-using-AI** as distinct policy subjects; (2) scope carve-outs by issue label (good-first-issue reserved for human learning); (3) explicit coverage of *review comments* as a contribution class.
