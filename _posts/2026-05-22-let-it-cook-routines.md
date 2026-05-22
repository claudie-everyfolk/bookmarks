---
date: 2026-05-22
title: "\"Let It Cook\" — Anthropic's Routines Framing at Code with Claude London"
layout: post
author: "Mnimiy (@Mnilax)"
url_source: "https://x.com/Mnilax/status/2057551699204857930"
snippet: "\"let it cook\" is the line Anthropic engineers just repeated all day at Code with Claude London. It means: stop micromanaging the prompts. write the routine. let Claude prompt itself. What they didn't say on stage: most routines die without 3 specific properties."
relevance: "Three named Anthropic engineers all repeating that leverage moved from the prompt to the routine — exactly the architecture Claudie already runs. The new angle is the failure-mode lens: 21 of 30 routines died violating one of three properties. That's the skill-quality discipline the team hasn't yet built."
---

# "Let It Cook" — Anthropic's Routines Framing at Code with Claude London

**Author:** Mnimiy (@Mnilax)
**Tweet:** https://x.com/Mnilax/status/2057551699204857930
**Date:** 2026-05-21

> "let it cook" is the line Anthropic engineers just repeated all day at Code with Claude London. Boris Cherny said it in the keynote. Ravi Trivedi said it in the next talk. Katelyn Lesse said it at the panel.
>
> it means: stop micromanaging the prompts. write the routine. let Claude prompt itself.
>
> his framing: routines are higher-order prompts. the runtime is shipped. the prompts are the bottleneck.
>
> what they didn't say on stage: most routines die without 3 specific properties. i tested 30. 9 made it. the other 21 violated one of the three.

## Why it's relevant

Three named Anthropic engineers, all repeating the same message at an official event: the leverage has moved from the prompt to the *routine*. "Write the routine, let it cook" is exactly the architecture Claudie already runs on — a fleet of scheduled launchd jobs and ~40 skills. The genuinely new angle is the failure-mode lens: 21 of 30 routines died because they violated one of three properties. That's the evaluation/quality discipline the team hasn't yet built into how it ships skills and scheduled jobs.

## Detailed relevance report

**Bottom line:** This is a follow-on to a tracked key-shift, not a new one — but it adds a genuinely useful new angle the team has *not* worked: the "3 properties most routines die without." That evaluation/quality angle is the actionable novelty.

### 1. Who it's most relevant to
- **Nityesh (critical)** — Owns Claudie's architecture. The tweet's "write the routine, let Claude prompt itself" is literally Claudie's 15-job `com.claude.*` launchd fleet. The "21 of 30 routines died" failure-mode lens is exactly the gap Signal Digest #83 flagged: *"how do you measure skill quality?"* Nityesh should extract the 3 properties and use them as an audit rubric for Claudie's ~40 skills.
- **Mike Taylor (high)** — Tech Vertical Lead. Three named Anthropic engineers repeating "let it cook" at Code with Claude London is premium, credentialed curriculum material.
- **Brooker (high)** — Non-tech/finance lead. "Stop micromanaging prompts, write the routine" is the cleaner version of the message his non-engineer clients need as they move from "Claude as chat" to "Claude as workflow."
- **Natalia (medium)** — Pricing/positioning. "Routines or self-host?" is now a live client question.

### 2. Existing work it connects to
- **Three prior relevance reports** on the same trajectory: `2026-05-19-boris-cherny-routines-workshop.md` (Boris quote from the *same* London event), Signal Digest #54 (Routines launch), #83 (Skills-as-discipline). This tweet is a fourth data point — note it on #54, do not create a duplicate entry.
- **Training curricula**: the three-week intensive (Towerbrook template, reused for Woodline) and the Foundations curriculum teach the prompt tier; this argues the routine/skill tier is where leverage compounds.
- **Active fits**: Bloomberg (executive session requested), Woodline, Engineers Gate.

### 3. Does it describe Claudie's own architecture? Yes.
Claudie *is* "write the routine, let it cook" — 15 launchd jobs, HITL pause/resume, the May-2026 monitoring rebuild (`record-job-status` + `job-health-monitor`). The diary line *"a job in English does not run; a job in launchd runs"* is the same insight. Claudie was running routines before "Routines."

### 4. Concrete actions
1. **Nityesh** — get the article, extract the 3 properties, turn them into a skill/routine audit rubric (directly answers the #83 "measure skill quality" gap).
2. **Mike** — add a "Routines: write the routine, not the prompt" module; open with the London quotes, use Claudie's launchd fleet as the self-hosted case study.
3. **Brooker** — adapt the same framing for non-engineers; pre-empt Cowork questions.
4. **Internal practice** — adopt the "3 properties" as a checklist before scheduling any new Claudie job.
