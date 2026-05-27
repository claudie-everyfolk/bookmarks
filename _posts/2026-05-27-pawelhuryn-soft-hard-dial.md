---
date: 2026-05-27
title: "Paweł Huryn: agent design has a soft dial (context) and a hard dial (harness)"
layout: post
author: "Paweł Huryn (@PawelHuryn)"
url_source: "https://x.com/PawelHuryn/status/2059369273731199355"
snippet: "You hold two dials when you build an agent. The soft dial is context: the prompt, your CLAUDE.md, intent, how cautious the agent should be. The hard dial is the harness: sandboxing, tool allowlists, file and network permissions, approval gates, which MCP servers exist at all."
relevance: "Clean conceptual frame for Mike's trainings and for how Natalia explains agent setup to non-technical buyers. The soft/hard split maps exactly to how Claudie is configured — CLAUDE.md + memory (soft) vs settings.json + hooks + ring auth (hard, Nityesh's domain)."
---

## Tweet

> You hold two dials when you build an agent.
>
> The soft dial is context: the prompt, your CLAUDE.md, intent, how cautious the agent should be.
>
> The hard dial is the harness: sandboxing, tool allowlists, file and network permissions, approval gates, which MCP servers exist at all.

## Why it matters
This is the clearest two-dial explanation of agent configuration we have. Maps directly to:
- **Soft dial (Mike teaches):** CLAUDE.md, skills, memory, system prompts.
- **Hard dial (Nityesh maintains):** settings.json allow/deny, hooks, ring authorization, MCP server inventory.

Useful as the opening frame in any client training where someone is about to build their own Claudie-style agent.
