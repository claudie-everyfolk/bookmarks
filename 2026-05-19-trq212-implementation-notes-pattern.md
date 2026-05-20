# The implementation-notes pattern — keep the agent's hidden decisions legible

**Author:** Thariq (@trq212) — Anthropic engineer
**URL:** https://x.com/trq212/status/2056418157305454805
**Date saved:** 2026-05-19

> Implement <SPEC>. As you work, maintain a running implementation-notes.html file (or markdown) that captures anything I should know about how the implementation differed from the spec — decisions you had to make that weren't in the spec, things you had to change, tradeoffs you had to make, or anything else I should know.
>
> As much as you spec, there are always ambiguities and unknown unknowns that come up — this gives the model a good out to make decisions but keep you in the loop.

## Why it's relevant
A one-line prompt pattern (going viral, from an Anthropic engineer) that directly addresses the trust gap in agentic coding: agents make dozens of unflagged decisions buried in a diff. A running implementation-notes file makes spec divergence legible instead of hidden. Net-new for Every — worth adding to Mike's Claude Code curriculum and worth Claudie adopting in her own scheduled `claude -p` jobs.

---

## Relevance report

### 1. Who this is most relevant to

**Primary: Mike Taylor (Tech Vertical Lead).** Mike runs Every's Claude Code / agentic-coding training. His current curriculum — the Thumbtack "Leveling Up: AI-Native Engineering" series — is built around exactly the problem this tweet names. His Session 2 run-of-show (`/Users/claudie/work/thumbtack-ros-v2/session-2-filesystem-and-compound.md`) is organized around the **trust gap** Thumbtack's own survey surfaced: engineers scored **4.1 on "I can detect bad AI output" but only 3.2 on "I trust AI output."** Thariq's pattern is a direct, one-line mitigation for that gap — it makes the agent's hidden decisions legible instead of buried in a diff. It slots cleanly next to the "three cheap self-eval patterns" Mike already teaches.

**Secondary: Nityesh Agarwal (Applied AI Engineer).** Nityesh owns Claudie's own architecture and works on systems, automation, curriculum development, and prompt engineering (`~/teammates/nityesh.md`). This is a prompt pattern he would both adopt internally and weigh into curriculum.

**Lower priority: Brooker.** Non-tech/finance vertical — teaches ChatGPT for ops, not spec-driven coding. Tangential at best.

### 2. What existing work this connects to

- **Mike's Thumbtack curriculum, Session 2** (`/Users/claudie/work/thumbtack-ros-v2/session-2-filesystem-and-compound.md`, `/Users/claudie/work/thumbtack-session2-updated-ros.md`). The CE `/ce-work` step is "execute step by step, pausing for ambiguity." Thariq's pattern is the lighter-weight version: instead of pausing, the agent logs the ambiguity-resolution and keeps moving. Mike already teaches three self-eval patterns ("list 3 things that might be wrong," "run tests and report failures," "diff against the plan and flag unfinished items") — implementation-notes is a natural fourth, and the only one aimed at *spec divergence* specifically.
- **Thumbtack Session 3 / Symphony in-person session** (`/Users/claudie/work/thumbtack-session3-run-of-show.md`). Symphony is explicitly spec-driven: "issues in Linear are the specs." The tweet's premise — "as much as you spec, there are always ambiguities and unknown unknowns" — is the exact failure mode of pure spec-driven orchestration.
- **Existing bookmark, same theme:** `2026-04-03-garrytan-decision-traces-1m-context.md` — Garry Tan on "decision traces in agentic engineering." Thariq's tweet is the concrete, do-it-today implementation of that abstract idea.
- **Live evidence the pattern was needed:** A May 6 Thumbtack deck-build session shows Claudie making many unflagged decisions that diverged from the brief (solid teal backgrounds instead of stipple texture; an invented tagline Mike had to interrogate; deck length wrong twice). Each would have surfaced earlier in an implementation-notes file.

### 3. Concrete actions

1. **Add it to Mike's curriculum as a named pattern.** In Session 2's "Three cheap self-eval patterns" slide, add a fourth: *"Maintain a running implementation-notes file — log every decision, change, and tradeoff not in the spec."* Frame it against the 4.1/3.2 trust gap. Credit Thariq (@trq212, Anthropic).
2. **Bake it into the Symphony workflow.** The agent prompt template should instruct agents to write `implementation-notes.md` per issue before moving an issue to the "Human Review" Linear state — giving the reviewer reasoning, not just a diff.
3. **Claudie should adopt it for her own scheduled coding jobs.** Any `claude -p` job that "implements a spec" — deck builds, dashboard updates, the delivery playbook — should emit an implementation-notes file so divergences surface in the morning brief instead of in a client's hands. Directly addresses the standing "no fabricated claims" and "don't embellish prompts" feedback rules.
4. **Run it through Signal Digest** if it keeps gaining traction — fits the existing prompt-patterns lane.

### 4. Client engagement where this lands best

**Thumbtack Engineering** — clearest fit. ~200 engineers, three-session AI-native engineering program, a documented trust gap, and a spec-driven orchestration tool (Symphony) already being taught. Small enough to teach in one slide.

Secondary: **the finance Claude Code track** (TowerBrook "Claude Code for Finance," Bloomberg). For non-engineer audiences writing specs for coding agents, an implementation-notes file is an especially good safety net — those users are less able to catch divergence by reading code.

**Caveat:** No evidence Every has formally adopted any decision-trace / implementation-notes pattern yet. This would be net-new, not a reinforcement of existing practice.
