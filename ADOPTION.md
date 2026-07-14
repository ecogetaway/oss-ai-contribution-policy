# What adopting looks like

This walkthrough shows the difference between a buried prose policy and a root `ai-contribution-policy.yml`. It uses a fictional project for clarity; real worked files live in [`spec/examples/`](spec/examples/).

## Before — policy buried in CONTRIBUTING

```markdown
## AI-assisted contributions

We allow AI tools if you disclose them in the PR description.
Please make sure you understand every line and ran the tests.
Undisclosed AI-generated PRs may be closed.
```

Problems in practice:

- Contributors must *find* the paragraph (often after writing the PR)
- CI and coding agents cannot reliably parse stance, disclosure, or enforcement
- Each project reinvents incompatible wording for the same ideas
- “May be closed” is discovered in an angry thread, not declared up front

## After — one predictable file + a short CONTRIBUTING link

**1. Repository root: `ai-contribution-policy.yml`** (abbreviated)

```yaml
schema_version: "0.1"

project:
  name: "example/widgets"
  repo_url: "https://github.com/example/widgets"

stance:
  code: disclosed-allowed
  documentation: disclosed-allowed
  translations: disclosed-allowed
  media: restricted
  notes: >
    AI assistance is welcome when disclosed. Generated media needs
    maintainer pre-approval.

disclosure:
  required: true
  mechanism: pr-template
  granularity: tool-and-role

attestations:
  required:
    - understands-change
    - reviewed-output
    - ran-tests

enforcement:
  undisclosed_ai: request-disclosure
  incomplete_attestation: request-completion
  repeat_policy: maintainer-discretion

review:
  response_time_target_days: 7
  first_time_contributors: welcome

last_reviewed: "2026-07-12"
```

**2. CONTRIBUTING.md** — replace the long AI section with a pointer:

```markdown
## AI-assisted contributions

Our machine-readable policy lives at
[`ai-contribution-policy.yml`](ai-contribution-policy.yml).

In short: AI assistance is allowed when you disclose the tool and role,
attest that you understand and reviewed the change, and ran the tests.
Undisclosed AI gets a request for disclosure — not an automatic ban on
first occurrence.
```

**3. Optional PR template checkbox** (matches `disclosure.mechanism: pr-template`):

```markdown
### AI disclosure
- [ ] I used an AI tool on this PR
- Tool and role: ________
- [ ] I understand every line I submitted
- [ ] I ran the relevant tests
```

## Adoption checklist (~10 minutes)

1. Copy [permissive](spec/examples/oss-ai-contribution-policy.ai-contribution-policy.yml) or [strict](spec/examples/illustrative-strict-project.ai-contribution-policy.yml) to your repo root as `ai-contribution-policy.yml`.
2. Edit: project name/URL, per-asset **stance**, **attestations**, **enforcement**.
3. Set `last_reviewed` to today; commit.
4. Link from `CONTRIBUTING.md` (and optionally your PR template).
5. Optional: [open an issue](https://github.com/ecogetaway/oss-ai-contribution-policy/issues) if you adopt, reject, or need a schema change — early feedback shapes v0.2.

## What adoption is *not*

- Not a promise that we will police your repository
- Not a requirement to join a foundation first
- Not a ban (unless you choose `prohibited` and say so clearly)
- Not finished standards-body ratification — this remains a draft

More context: [`FAQ.md`](FAQ.md) · [`README.md`](README.md) · [schema](spec/ai-contribution-policy.schema.yml)
