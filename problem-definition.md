# Problem Definition

Open source's open-contribution model — the mechanism that built the software infrastructure the world runs on — is failing in real time. AI-assisted contribution has flooded maintainers with plausible-looking submissions they cannot cheaply verify, and projects are responding by closing pathways that took decades to open: curl ended its bug bounty, Ghostty and tldraw restricted external PRs, Jazzband dissolved. Each closure is locally rational and collectively corrosive.

## The core claim

The problem is not AI assistance itself; it is the **verification asymmetry** it creates. Generating a plausible contribution now costs minutes; verifying one still costs a maintainer's scarce, expert attention. Every project is absorbing that asymmetry alone, with hand-rolled policies that are mutually incompatible, invisible to tooling, and discovered by contributors only after they've transgressed them.

## Why detection is the wrong fix

Detection asks "was this written by AI?" — a question that gets less answerable every model generation, and whose false positives land hardest on non-native English writers and newcomers. Verification asks "has a human tested, reviewed, and understood this?" — a question whose answer stays meaningful no matter how good generation gets. A standard built on attestation of human actions does not expire; a detector does.

## The equity dimension

Blanket bans don't just filter slop — they close the on-ramp. Contributors from the Global South, students, and career-changers are precisely the people for whom AI assistance most lowers the barrier to a first contribution, and precisely the people with the least standing to argue when rejected on sight. A disclosure-and-verification pathway is what makes "welcome, with honesty" a possible policy position between "anything goes" and "no."

## What "solved" looks like

Not a tool, and not a manifesto: a **standard shape**. A machine-readable policy file any project can adopt in minutes (`ai-contribution-policy.yml`), a contributor pathway that is easier to follow than to evade, and an evidence base — catalogued policies and scored case studies — proving which policy shapes actually reduce maintainer load while keeping doors open. Success is measured in pilots: mismatched-contribution volume reaching maintainer review, and median time-to-first-review, before vs. after adoption.

## Scope boundary

This project studies and standardizes **contribution governance**, not model capability or AI ethics in general. A case study can involve excellent or terrible AI output; what we score is how the project's policy and process handled it, and what infrastructure would have made that handling repeatable.
