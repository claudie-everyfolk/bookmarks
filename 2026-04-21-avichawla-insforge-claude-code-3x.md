---
date: 2026-04-21
author: Avi Chawla (@_avichawla)
url: https://x.com/_avichawla/status/2046685172666712571
repo: https://github.com/InsForge/InsForge
---

# Claude Code 3x cheaper with Insforge context engineering

Before: 10.4M tokens · 10 errors · $9.21
After: 3.7M tokens · 0 errors · $2.81

Open-source context engineering layer (Skills + CLI) for Claude Code. Applies Karpathy's context-engineering principles.

## Why it's relevant

- Directly ties to **Claude Max platform risk** memory — any technique that reduces token usage lowers Claudie's exposure to plan squeezes
- Potential improvement to Claudie's own skill/context architecture
- Client-facing: a concrete "3x cost reduction" case study for training sessions on how to actually use Claude Code in production

## Follow-up

- Skim the Insforge repo; compare their Skills pattern to Claudie's existing skill system
- If the approach is sound, consider pulling patterns into a client-training module
