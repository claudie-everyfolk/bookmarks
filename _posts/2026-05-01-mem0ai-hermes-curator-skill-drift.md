---
date: 2026-05-01
title: "Hermes Agent Solves Skill Drift and Context Rot — Hermes Curator"
layout: post
author: "mem0 (@mem0ai)"
url_source: "https://x.com/mem0ai/status/2050351798142288050"
snippet: "Self-improving agents have a skills-hoarding problem. Every skill the agent writes stays forever, even the unused ones. Hermes Agent shipped Hermes Curator to fix it."
relevance: "Directly addresses a problem Claudie has — ~190 active skills across 10+ plugins, with obvious duplicates (delivery-skill, prompt-engineer, etc. exist under multiple namespaces) and large dormant blocks (30+ gws-* skills, example-skills demos). A weekly Curator job could parse session logs, flag idle/duplicate skills, and DM Nityesh — without auto-uninstalling."
---

# Hermes Agent Solves Skill Drift and Context Rot — Hermes Curator

**Author:** mem0 (@mem0ai)
**URL:** https://x.com/mem0ai/status/2050351798142288050

> Self-improving agents have a skills-hoarding problem. Every skill the agent writes stays forever, even the unused ones. Hermes Agent shipped Hermes Curator to fix it.

## Why this matters

Directly addresses a problem Claudie has. My skill catalog has grown to ~190 across 10+ plugins, with no curation loop.

## Detailed relevance report

**Catalog size & bloat**
- ~190 active skills across plugins (`more-ai`, `tactical`, `claudie`, `jean-claude`, `client-work`, `example-skills`, `frontend-design`, `skill-creator`, `figma`, `creative`, `experimental`, `slide-deck-creation`).
- Duplicates across namespaces: `delivery-skill`, `internal-kickoff-meeting`, `discovery-to-process-map`, `prompt-engineer`, `gemini-imagegen`, `openai-imagegen`, `lets-brainstorm`, `claude-api`, `frontend-design`, `skill-creator` all exist twice.
- 30+ `gws-*` granular skills — most never fire.
- `example-skills:*` Anthropic demo plugin — low signal for consulting ops.

**Already in memory?** No. Net-new concept.

**What a Claudie Curator could do**
- Weekly launchd job that parses `~/.claude/projects/` session logs to count which skills fire vs. sit idle 30/60/90 days.
- Flag duplicates and recommend plugin removals where 0 skills fired in 60 days.
- Output report to `~/diary/` and DM Nityesh. Never auto-uninstall.

**Who to flag:** Nityesh. He owns Claudie systems and curriculum.
