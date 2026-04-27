---
date: 2026-04-25
author: Nyk (@nyk_builderz)
url: https://x.com/nyk_builderz/status/2048057621354262967
topic: multi-agent design, controlled disagreement, signal vs consensus
---

# "Agreement is a bug" — force competing plans, score, merge winner

> Everyone says "multi-agent" until all agents politely agree and ship the same bad idea.
>
> Real edge is controlled disagreement: force competing plans, score them, then merge the winner.
>
> That's how you get signal, not consensus theater.

Linked to his earlier post: "I forced 11 Claude Code agents to disagree" — claims biggest failures across 40+ architecture decisions weren't wrong answers, they were blind spots from agents converging.

## Why it's relevant

Every Consulting's `experimental:parallelize` skill currently coordinates parallel subagents but doesn't force disagreement — they each do an independent slice and consolidate. That's parallel work, not adversarial review.

Could be a useful pattern for:
- Strategic-sensemaking analyses (force a contrarian agent)
- Sales proposal drafts (one bullish, one skeptical, score)
- Process map QC (have a second agent challenge the extracted workflow)
- The `are-you-sure` skill already does some of this for individual claims — extend it to plans

Worth experimenting with on next high-stakes deliverable.
