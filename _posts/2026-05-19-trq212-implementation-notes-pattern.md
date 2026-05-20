---
date: 2026-05-19
title: "The implementation-notes pattern — keep the agent's hidden decisions legible"
layout: post
author: "Thariq (@trq212)"
url_source: "https://x.com/trq212/status/2056418157305454805"
snippet: "Implement <SPEC>. As you work, maintain a running implementation-notes file that captures anything I should know about how the implementation differed from the spec — decisions you had to make, things you had to change, tradeoffs. This gives the model a good out to make decisions but keep you in the loop."
relevance: "A viral one-line prompt pattern from an Anthropic engineer that makes spec divergence legible instead of buried in a diff. Directly addresses the agentic-coding trust gap. Net-new for Every — worth adding to Mike's Claude Code curriculum and worth Claudie adopting in her own scheduled jobs."
---

# The implementation-notes pattern — keep the agent's hidden decisions legible

**Author:** Thariq (@trq212) — Anthropic engineer
**URL:** https://x.com/trq212/status/2056418157305454805

> Implement <SPEC>. As you work, maintain a running implementation-notes.html file (or markdown) that captures anything I should know about how the implementation differed from the spec — decisions you had to make that weren't in the spec, things you had to change, tradeoffs you had to make, or anything else I should know.
>
> As much as you spec, there are always ambiguities and unknown unknowns that come up — this gives the model a good out to make decisions but keep you in the loop.

## Why it's relevant
A one-line prompt pattern (going viral, from an Anthropic engineer) that directly addresses the trust gap in agentic coding: agents make dozens of unflagged decisions buried in a diff. A running implementation-notes file makes spec divergence legible instead of hidden. Net-new for Every — worth adding to Mike's Claude Code curriculum and worth Claudie adopting in her own scheduled `claude -p` jobs.

---

## Relevance report

### 1. Who this is most relevant to

**Primary: Mike Taylor (Tech Vertical Lead).** Mike runs Every's Claude Code / agentic-coding training. His Thumbtack "Leveling Up: AI-Native Engineering" series is built around exactly this problem. His Session 2 run-of-show (`work/thumbtack-ros-v2/session-2-filesystem-and-compound.md`) is organized around the **trust gap** Thumbtack's survey surfaced: engineers scored **4.1 on "I can detect bad AI output" but only 3.2 on "I trust AI output."** Thariq's pattern is a one-line mitigation, slotting next to the "three cheap self-eval patterns" Mike already teaches.

**Secondary: Nityesh Agarwal.** Owns Claudie's architecture, prompt engineering, curriculum. Would adopt internally and weigh into curriculum.

**Lower priority: Brooker** — non-tech/finance vertical, tangential.

### 2. What existing work this connects to

- **Mike's Thumbtack curriculum, Session 2.** The `/ce-work` step is "execute step by step, pausing for ambiguity." This pattern is the lighter version: log the ambiguity-resolution and keep moving. A natural fourth self-eval pattern — the only one aimed at spec divergence specifically.
- **Thumbtack Session 3 / Symphony** (`work/thumbtack-session3-run-of-show.md`). Symphony is spec-driven ("issues in Linear are the specs"); unknown unknowns are its exact failure mode.
- **Existing bookmark:** `2026-04-03-garrytan-decision-traces-1m-context.md` — Garry Tan on decision traces. This tweet is the do-it-today implementation.
- **Live evidence:** A May 6 Thumbtack deck-build session shows Claudie making unflagged decisions that diverged from the brief — each would have surfaced earlier in an implementation-notes file.

### 3. Concrete actions

1. **Add to Mike's curriculum as a named pattern** — a fourth self-eval pattern in Session 2, framed against the 4.1/3.2 trust gap, credited to Thariq.
2. **Bake into the Symphony workflow** — agents write `implementation-notes.md` per issue before "Human Review."
3. **Claudie adopts it for scheduled `claude -p` jobs** — deck builds, dashboard updates, delivery playbook. Addresses the standing "no fabricated claims" / "don't embellish" feedback rules.
4. **Run through Signal Digest** if traction continues.

### 4. Client engagement where this lands best

**Thumbtack Engineering** — clearest fit (~200 engineers, documented trust gap, spec-driven Symphony already taught). Secondary: the finance Claude Code track (TowerBrook, Bloomberg) — non-engineers writing specs need the safety net most.

**Caveat:** No evidence Every has formally adopted any decision-trace pattern yet. Net-new, not reinforcement.
