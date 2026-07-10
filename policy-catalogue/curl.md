# curl/curl — AI-contribution policy (catalogue entry)

- **Project:** [curl/curl](https://github.com/curl/curl)
- **Policy location:** [docs/CONTRIBUTE.md § "On AI use in curl"](https://github.com/curl/curl/blob/master/docs/CONTRIBUTE.md) (added 2025-05-15); [docs/BUG-BOUNTY.md](https://github.com/curl/curl/blob/master/docs/BUG-BOUNTY.md)
- **Captured on:** 2026-07-11

## Policy substance (mapped to schema fields)

| Schema field | This project's position |
| --- | --- |
| stance (code) | disclosed-allowed — "We can accept code written with the help of AI," with verification and quality expectations |
| stance (security reports) | disclosed-allowed with heightened duty: AI-assisted findings must be disclosed and independently verified by the reporter before submission |
| disclosure required? mechanism? | Yes — "you **must** make sure to reveal this fact in your report"; write-up must be human-authored |
| attestations required | reviewed-output and manual verification, in substance: "double-check the findings carefully … validate that the issues are indeed existing" |
| enforcement | Bug bounty ended entirely (2026-01-26): "we stop the bug-bounty end of Jan 2026" |
| first-time contributors | No special gate documented |

## Verbatim excerpt
> "If you asked an AI tool to find problems in curl, you **must** make sure to reveal this fact in your report." — CONTRIBUTE.md
>
> "The curl project does not offer any rewards for reported bugs or vulnerabilities. […] A bug bounty gives people too strong incentives to find and make up 'problems' in bad faith that cause overload and abuse." — BUG-BOUNTY.md

## Notes
The policy distinguishes **security reports** from code contributions — an asset class the v0.1 schema doesn't have (its classes are code/docs/translations/media). Strong v0.2 signal: `reports` (or `issues`) should be a first-class stance target, since for curl that's where the flood hit. Full case study: [../case-studies/curl-bug-bounty-closure.md](../case-studies/curl-bug-bounty-closure.md).
