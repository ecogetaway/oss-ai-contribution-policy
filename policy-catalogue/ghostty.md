# ghostty-org/ghostty — AI-contribution policy (catalogue entry)

- **Project:** [ghostty-org/ghostty](https://github.com/ghostty-org/ghostty)
- **Policy location:** [AI_POLICY.md](https://github.com/ghostty-org/ghostty/blob/main/AI_POLICY.md) (dedicated file), reinforced in [CONTRIBUTING.md](https://github.com/ghostty-org/ghostty/blob/main/CONTRIBUTING.md)
- **Captured on:** 2026-07-11

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | disclosed-allowed — "Using AI to write code is fine," with mandatory disclosure and understanding |
| stance (docs / issues) | disclosed-allowed with "full human-in-the-loop": AI content must be reviewed *and edited* by a human |
| stance (media) | prohibited — "No AI-generated media is allowed (art, images, videos, audio)" |
| disclosure required? mechanism? | Yes — "All AI usage in any form must be disclosed," naming the tool and extent |
| attestations required | understands-change, in strong form: contributor must be able to explain all edge cases without AI aid |
| enforcement on non-disclosure | "Bad AI drivers will be denounced" — a public denouncement list blocking future contributions, shareable with other projects |
| first-time contributors | Vouch system: first PR requires a maintainer `!vouch`; unvouched PRs auto-closed |

## Verbatim excerpt
> "All AI usage in any form must be disclosed. You must state the tool you used (e.g. Claude Code, Cursor, Amp) along with the extent that the work was AI-assisted. […] If you can't explain what your changes do and how they interact with the greater system without the aid of AI tools, do not contribute to this project."

## Notes
Richest policy in the batch. Three things the v0.1 schema cannot express: (1) a **trust-bootstrapping mechanism** (the vouch system) as a first-contributor gate; (2) a **cross-project shareable blocklist** as an enforcement outcome; (3) maintainers explicitly **exempted** from the policy. The policy is explicitly pro-AI in rationale ("Our reason … is not due to an anti-AI stance") — stance labels need to capture that a strict policy and a welcoming posture can coexist.
