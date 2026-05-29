---
date: 2026-05-29
title: "Autoresearch Loop for Stress-Testing Agentic Systems"
layout: post
author: "Manthan Gupta (@manthanguptaa)"
url_source: "https://x.com/manthanguptaa/status/2060237811916406907"
snippet: "One of the most useful workflows I have built recently is an autoresearch loop for agentic systems. Whenever I add a new agent with multiple tools, I let an LLM loose on the repository and ask it to generate complex, user like queries that stress test the system."
relevance: "Nityesh keeps adding skills/plugins/tools to Claudie. No automated regression check — every addition risks silent skill-trigger overlap or hook collisions. This pattern would fit into an overnight slot: scan ~/.claude/skills/, generate prompts per skill, run through claude -p, log failures. Catches regressions before Natalia hits them in a sales call."
---

# Autoresearch Loop for Stress-Testing Agentic Systems

**Author:** Manthan Gupta (@manthanguptaa)
**URL:** https://x.com/manthanguptaa/status/2060237811916406907

> One of the most useful workflows I have built recently is an autoresearch loop for agentic systems.
>
> Whenever I add a new agent with multiple tools, I let an LLM loose on the repository and ask it to generate complex, user like queries that stress test the system.

## Why this is relevant

Nityesh keeps adding skills, plugins, and tools to Claudie's setup. There's no automated regression check — every new addition risks breaking the others (skill triggers overlap, hook collisions, permission rules). The current "test" is the team noticing in Slack.

This autoresearch pattern would fit into an overnight slot: scan `~/.claude/skills/`, generate realistic user prompts from each skill description, run through `claude -p`, log failures. Could catch silent skill-regression before Natalia hits it in a sales call.

Worth Nityesh prototyping.
