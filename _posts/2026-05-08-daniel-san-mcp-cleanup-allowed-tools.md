---
date: 2026-05-08
title: "Daniel San: clean up MCPs every session + always declare allowed-tools in skill frontmatter"
layout: post
author: "Daniel San (@dani_avila7)"
url_source: "https://x.com/dani_avila7/status/2052927835992424909"
snippet: "ALWAYS review and clean up MCPs in every Claude Code session. Not a common practice, but it should be. And if you're building Skills, declare the tools in the frontmatter using the allowed-tools field. In a session with many MCPs connected, Claude can pull tools from any of them."
relevance: "Direct hit on Claudie's setup. Audit shows 0 of 4 local skills and 0 of 59 every-consulting plugin skills declare allowed-tools (~13% of 300 installed). With 80+ MCP tools at session start, tool bleed is real. Action: backfill allowed-tools, add SessionStart hook warning on MCP sprawl, surface to Mike for tech curriculum."
---

# Daniel San: MCP cleanup + allowed-tools in skill frontmatter

**Author:** Daniel San (@dani_avila7)
**Date:** 2026-05-08
**URL:** https://x.com/dani_avila7/status/2052927835992424909

## Tweet

"ALWAYS review and clean up MCPs in every Claude Code session

Not a common practice, but it should be

And if you're building Skills, declare the tools in the frontmatter using the allowed-tools field

In a session with many MCPs connected, Claude can pull tools from any of them"

## Why it's relevant

Direct hit on Claudie's infrastructure. Tool sprawl from many concurrent MCPs is the exact scenario we're in — 80+ deferred tools at session start. Skills without `allowed-tools` frontmatter let Claude reach into any connected MCP, which can produce surprising or wrong-surface behavior.

## Detailed relevance report

**1. Skills missing `allowed-tools` — confirmed widespread:**

- Total `SKILL.md` files installed: 300 across `~/.claude/plugins/cache/` and `~/.claude/skills/`
- Skills with `allowed-tools` frontmatter: 39 (~13%)
- Every Consulting plugin family (`~/.claude/plugins/cache/every-consulting/`): 59 SKILL.md files, **ZERO with `allowed-tools`**
- Local user skills (`~/.claude/skills/`): 4 SKILL.md files, **ZERO with `allowed-tools`**

**2. MCP sprawl is real:**

- 3 stdio/SSE MCPs (granola, qmd, every) + 13 enabled plugins + 8 claude.ai MCPs
- Session-start deferred-tools list = ~80+ MCP tools

**3. Who benefits:**

- Mike (Tech Vertical Lead) — Claude Code curriculum
- Nityesh (built plugin infra) — owns `EveryInc/every-consulting`

**4. Concrete actions:**

- Backfill `allowed-tools` in 4 local skills
- Open PR (after asking Nityesh) for the 59 plugin skills
- Add lint to `skill-creator` / `plugin-creator`
- Add `SessionStart` hook warning when >5 MCPs are connected
- Pass tip to Mike for tech-track curriculum
