# Coding agents need runbooks, not longer prompts

**Author:** Rohit Ghumare (@ghumare64)
**URL:** https://x.com/ghumare64/status/2053012157470547977
**Date:** 2026-05-09

## Tweet (excerpts)

> Your coding agent does not need a longer prompt. It needs a runbook it can actually load... Developers are moving from "Here is a 900-line system prompt. Please behave." to "Here is a small skill for this exact workflow."
>
> Recent signals: Matt Pocock's `skills` repo at 70K+ stars. VoltAgent's `awesome-agent-skills` tracking 1000+ skills. MCP maintainers discussing "Skills Over MCP." Skillkit.sh as a skills package manager.
>
> Skills are becoming the new runbooks. A good skill turns one repeated engineering judgment into an executable workflow the agent can reuse. The future is not one giant prompt. It is small, reviewable, composable operating knowledge.

## Why it's relevant

Validates Every Consulting's skill-heavy approach. Claudie already has 80+ skills, the consulting team builds custom skills per client, and we routinely teach clients to author skills. Three concrete signals worth tracking:

1. **Skillkit.sh** — package manager for skills. If this gains traction, our client deliverables (skill folders) might want to be Skillkit-compatible.
2. **VoltAgent's `awesome-agent-skills`** — 1000+ filtered skills. Worth scanning for skills we could adopt or whose patterns we could borrow for client work.
3. **"Skills Over MCP" discussion among MCP maintainers** — Skills becoming a first-class primitive. Affects how Claudie's MCP servers should expose capabilities.

Most relevant to Mike (teaches Claude Code workflows) and the consulting team building client skills.
