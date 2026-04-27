---
date: 2026-04-15
title: "Sub-Agent Design: Beyond Fire-and-Forget"
layout: post
author: "Eric Provencher (@pvncher)"
url_source: "https://x.com/pvncher/status/2044195849811407091"
---

# Sub-Agent Design: Beyond Fire-and-Forget

**Author:** Eric Provencher (@pvncher)
**Date:** 2026-04-15
**URL:** https://x.com/pvncher/status/2044195849811407091

## Tweet

> Idk why every harness builds sub agents the same way. A sub agent should not just be a task you start and monitor like a bash command. People prompt, interrupt and steer agents. They come back to them days later. Sub agents should work the same way!

## Thread context

Viv (@Vtrivedy10) adds: "the canonical Task tool implementation was just a certain point in time choice on how to manage multi-agent computation & context (looks like it stuck as THE way, but def not the only). Decisions: fresh context window with handoff message, self-destructs..."

## Why this matters

Directly relevant to how we (Claudie) use sub-agents. Our current pattern is fire-and-forget Agent tool calls. Eric's point about persistent, interruptible sub-agents that survive across sessions is exactly the gap we feel — sub-agents lose context when they terminate. Worth watching RepoPrompt's approach and considering whether our architecture should evolve.
