# OpenStreetMap — AI-contribution policy (catalogue entry)

- **Project:** [openstreetmap/openstreetmap-website](https://github.com/openstreetmap/openstreetmap-website)
- **Policy location:** [`CONTRIBUTING.md` § "AI-Assisted Contributions"](https://github.com/openstreetmap/openstreetmap-website/blob/8f1c4d4116095658d24ece41efbd0a70f0b3c230/CONTRIBUTING.md#ai-assisted-contributions), added 2026-04-08 in commit [`fc1f7f2`](https://github.com/openstreetmap/openstreetmap-website/commit/fc1f7f2a0e70)
- **Captured on:** 2026-07-25 (pinned to `8f1c4d4`)

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | disclosed-allowed in effect, though disclosure is never actually requested — AI tools may be used subject to review, testing and understanding |
| **disclosure required? mechanism?** | **No.** The section imposes no disclosure obligation at all — unique in the catalogue among policies that permit AI use |
| attestations required | understands-change, reviewed-output and manual-verification in substance: "Make sure that a human has reviewed, tested, and fully understands all the code changes being submitted" |
| scope carve-out | Newcomer-labelled issues: "Issues tagged for new contributors are meant as learning opportunities… Using AI for these issues removes the opportunity to learn, both from you and other contributors" |
| enforcement | Closure on suspicion, explicitly without discussion — "if you submit a PR and the maintainers suspect that you haven't reviewed, tested, or understood the code, they may decline your PR without further discussion" |
| first-time contributors | Addressed indirectly through the newcomer-issue carve-out |

## Verbatim excerpt

> "If you choose to use AI tools to help create pull requests, you should follow these additional guidelines:
> - Make sure that a human has reviewed, tested, and fully understands all the code changes being submitted.
> - If you submit code that you don't understand, then you aren't actually helping anyone. Maintainers already have access to AI tools. If pasting the output into a PR is all that was required, then the maintainers would have done that themselves already.
> - Issues tagged for new contributors are meant as learning opportunities, not as items that need to be addressed with urgency. Using AI for these issues removes the opportunity to learn, both from you and other contributors.
> - If you submit a PR and the maintainers suspect that you haven't reviewed, tested, or understood the code, they may decline your PR without further discussion."

## Notes

**The only permissive policy in the catalogue that requires no disclosure whatsoever.** Every other disclosed-allowed entry — Ghostty, LLVM, Fedora, Kubernetes, curl, Mesa, llama.cpp, Home Assistant — asks the contributor to say something. OpenStreetMap asks only that a human reviewed, tested and understood the change, and enforces on the *absence of understanding* rather than on the presence of AI. That is this standard's "verification over detection" principle already implemented in the wild, by a project that reached it independently and did not need the word "verification" to get there. If the schema wants a worked example of a policy that skips the disclosure axis entirely, this is it — and it implies `disclosure.required: false` needs to be a first-class, non-degenerate configuration rather than an omission.

**Newcomer issues reserved for human learning — the second instance of this carve-out.** LLVM states that AI tools must not be used on `good first issue` items; OpenStreetMap makes the same carve-out with the same stated reason, that it removes a learning opportunity "both from you and other contributors." Two independent projects converging on a label-scoped exemption moves this from a quirk to a pattern, and it is a *mechanically scoped* one: the issue label is observable even though the AI use is not. A `scope.exempt_labels` style field would let both express it directly.

**Enforcement is suspicion-based and explicitly terminal.** "They may decline your PR without further discussion" forecloses the appeal step that Home Assistant offers and that this repository's own `enforcement.undisclosed_ai: request-disclosure` default assumes. The v0.1 `enforcement` vocabulary captures the action but not whether a conversation follows. Given that suspicion-based enforcement is inherently error-prone — the survey in #22 puts every "was this AI?" judgement out of reach of any deterministic check — whether the policy commits to an appeal path seems like exactly the sort of thing an adopter should have to state.

**The rationale is reviewer-economics, stated bluntly.** "Maintainers already have access to AI tools. If pasting the output into a PR is all that was required, then the maintainers would have done that themselves already." That is a distinct argument from the copyright rationale (QEMU, Bevy, Asahi), the quality rationale (servo, tldraw) and the accountability rationale (Fedora, Mesa) — it says the contribution adds no value the project could not trivially produce itself. If a `rationale` enum is added, this one deserves its own value; it is the argument most specific to the agent era.
