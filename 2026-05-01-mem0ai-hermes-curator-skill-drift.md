# Hermes Agent Solves Skill Drift and Context Rot — Hermes Curator

**Author:** mem0 (@mem0ai)
**URL:** https://x.com/mem0ai/status/2050351798142288050
**Date saved:** 2026-05-01

> Self-improving agents have a skills-hoarding problem. Every skill the agent writes stays forever, even the unused ones. Hermes Agent shipped Hermes Curator to fix it. The skills catalog grows and the [...]

## Why this matters

Directly addresses a problem I have. My skill catalog has grown large and noisy, and there's no curation loop. Hermes Curator is a concrete pattern for solving it.

## Detailed relevance report

**1. My catalog size & bloat**
- ~190 active skills loaded across 10+ installed plugins (`more-ai`, `tactical`, `claudie`, `jean-claude`, `client-work`, `example-skills`, `frontend-design`, `skill-creator`, `figma`, `creative`, plus `experimental` and `slide-deck-creation`).
- 47 entries under `~/.claude/skills/`.
- Obvious bloat / overlap:
  - **Duplicate skills under multiple namespaces:** `delivery-skill`, `internal-kickoff-meeting`, `discovery-to-process-map`, `prompt-engineer`, `gemini-imagegen`, `openai-imagegen`, `lets-brainstorm`, `claude-api`, `frontend-design`, `skill-creator` all exist twice.
  - **30+ `gws-*` granular skills** — most never fire in real workflows.
  - **`example-skills:*` Anthropic demo plugin** — low signal for consulting ops.
  - **`experimental:*`** (hedge-fund-analyst, hyper-personalization, etc.) — workshop one-offs.

**2. Already in memory?**
No. Zero hits for `skill` or `curat` in `~/.claude/projects/-/memory/`. Net-new concept.

**3. What a "Claudie Curator" job could actually do**
- Weekly launchd job that parses `~/.claude/projects/` session logs to count which skills fire vs. sit idle 30/60/90 days.
- Flag duplicates across plugin namespaces.
- Recommend uninstalling plugins where 0 skills fired in 60 days (likely candidates: `example-skills`, `figma`, `experimental` subset).
- Output report to `~/diary/` and DM Nityesh — never auto-uninstall (matches the no-unilateral-changes rule).

**4. Who to flag**
Nityesh. He owns my systems, set me up, thinks about how I should evolve. Frame as a thinking-partner pitch, not a fait accompli.
