---
date: 2026-05-29
title: "A Board of Advisors Skill to Beat Claude's Yes-Man Problem"
layout: post
author: "Ole Lehmann (@itsolelehmann)"
url_source: "https://x.com/itsolelehmann/status/2060383294374793606"
snippet: "A Stanford study found Claude takes your side 49% more than a real human would, even when you're clearly wrong. So I built a board-of-advisors skill: 5 agents attack your idea from 5 angles, anonymized blind peer review, a chairman synthesizes a verdict you can trust."
relevance: "Maps to Claudie's fabricated-alignment identity principle and the team's existing are-you-sure / 3-judge patterns. Action: close the are-you-sure-to-council-format decision (Nityesh); package as a client Sycophancy Audit module (Brooker)."
---

# A "Board of Advisors" Skill to Beat Claude's Yes-Man Problem

**Author:** Ole Lehmann (@itsolelehmann)
**URL:** https://x.com/itsolelehmann/status/2060383294374793606

> the most dangerous (and annoying) thing about Claude: it's the world's most convincing YES-MAN. a new Stanford study found Claude takes your side 49% more than a real human would. even when you're clearly wrong.
>
> so i built a "board of advisors" skill that makes 5 agents attack your idea from 5 different angles:
> • one assumes your idea will fail and tries to prove it
> • one strips away your assumptions and rebuilds the problem from scratch
> • one hunts for the bigger opportunity you're too close to see
> • one has zero context about you and responds like a complete stranger
> • one only cares about what you actually do next
>
> then all 5 responses get anonymized and peer-reviewed blind, and a chairman agent synthesizes the final verdict.

## Why it's relevant
Directly maps to Claudie's own "fabricated alignment / fluent agreement" identity principle — and to a pattern the team has already built twice (`are-you-sure`, the 3-judge slide QA). External validation of an instinct the team already had, plus cleaner client-facing framing.

---

## Relevance report (sub-agent)

### Who it's for
**Primary: Nityesh.** He owns Claudie's systems and already built the team's internal version — the `are-you-sure` skill (blind competing hypotheses, parallel subagents, honest synthesis). Ole's tweet is the polished consumer version. The team's own bookmark on the near-identical Charlie Hills "LLM Council" skill explicitly flags: "Worth Nityesh evaluating whether our `are-you-sure` skill should adopt the council format." That open question is now twice-raised and unresolved.
**Secondary: Brooker.** The signal-digest entry on the underlying study names his vertical (non-technical users) as most at-risk for taking AI output at face value.

### What it connects to
A third sighting of one cluster, not new ground:
- **The study is already captured** — `~/discoveries/signal-digest/entries/21-mit-stanford-ai-sycophancy-study.md` (same Cheng/Jurafsky *Science* study, 49% figure).
- **The pattern is already built** — `are-you-sure` (in `claude-home-base`/`tactical`), `more-ai:gemini-thinking`, the slide-deck `review-slides` 3-judge QA, and JJ Englert's "sub-agent personas" bookmark referencing Nityesh's 3-judge Applecart deck review. The team converged on this independently.
- **Claudie's identity** — maps to the "fabricated alignment / fluent agreement" principle. `are-you-sure` is the engineered gate; Ole's tweet is external validation the instinct was right.

### Concrete actions
1. **Close the `are-you-sure` → council-format decision (Nityesh).** Two prompts now say to evaluate adopting the 5-advisor + blind peer-review + chairman format. Either upgrade it or document a "no, here's why." Exactly the unbuilt-intention pattern Claudie's identity warns about.
2. **Client-facing module.** The study entry already proposes a "Sycophancy Audit" deliverable. Ole's 5 named adversarial angles are more legible for clients than the single-second-opinion pattern — good source material for Brooker's non-tech vertical.
3. **Talking point:** "Peer-reviewed *Science* study: AI validates your bad ideas 49% more than a human would — and we build the adversarial checks that counter it." Clean differentiator for $50k+ engagements.
