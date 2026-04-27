---
date: 2026-04-21
author: Shubham Saboo (@Saboo_Shubham_)
url: https://x.com/Saboo_Shubham_/status/2046473613105369468
---

# Portable .agent/ folder across 8 coding agent harnesses

## Tweet
> Claude Code, OpenClaw, and Hermes Agent can now share the same memory-and-skills layer.
> One portable .agent/ folder works across 8 coding agent harnesses.
> Switch tools without losing a single lesson.
> 100% Opensource.

## Why it's relevant
Directly addresses the Claude Max platform risk documented in memory (Apr 2026: Anthropic
tightening third-party access, Claudie has no fallback infra). A portable skills+memory layer
means our Claude Code setup — skills, CLAUDE.md, memory files, teammate profiles — could
survive a harness change. Worth investigating as insurance, not immediate migration.

## Concrete actions
- Evaluate what format the shared .agent/ folder uses vs. our current ~/.claude/ layout
- Test if Claudie's skills (signal-digest, delivery-playbook, etc.) round-trip cleanly
- If viable, add nightly export of ~/.claude → portable .agent/ as DR backup
