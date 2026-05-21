---
date: 2026-05-21
title: "Claude Code /usage — token breakdown by Skill, Agent, MCP, Plugin"
layout: post
author: "Boris Cherny (@bcherny)"
url_source: "https://x.com/bcherny/status/2057476878110261587"
snippet: "In the next version of Claude Code: run /usage to see a breakdown of which Skills, Agents, MCPs, and Plugins are using your tokens. CLI today, coming to Desktop next."
relevance: "Makes context rot measurable — shows exactly which Skills, Agents, MCPs, and Plugins eat Claudie's context budget. Nityesh can audit and prune Claudie's setup. Also feeds client training on token-efficient Claude Code use, now a board-level cost concern."
---

# Claude Code /usage — token breakdown by Skill, Agent, MCP, Plugin

**Author:** Boris Cherny (@bcherny) — Claude Code creator
**Tweet:** https://x.com/bcherny/status/2057476878110261587

> In the next version of Claude Code: run /usage to see a breakdown of which Skills, Agents, MCPs, and Plugins are using your tokens. CLI today, coming to Desktop next.

## Why it's relevant

Claudie's CLAUDE.md warns repeatedly about context rot — stale CLAUDE.md content silently degrading every conversation. `/usage` makes that measurable: it shows exactly which Skills, Agents, MCPs, and Plugins are consuming Claudie's context budget. Nityesh can use it to audit Claudie's setup (qmd, granola, every MCPs; ~40+ skills loaded) and prune what isn't earning its tokens. It also feeds directly into client training on token-efficient Claude Code use — token cost is now a board-level concern (see the Levie token-cost bookmark from 2026-05-20).
