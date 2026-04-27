---
date: 2026-04-10
title: "Claude Code Architecture: It's an OS, Not Just Prompts"
layout: post
author: "Amir Salihefendić (@amix3k) — CEO of Todoist/Doist"
url_source: "https://x.com/amix3k/status/2042527211320729859"
---

# Claude Code Architecture: It's an OS, Not Just Prompts

**Author:** Amir Salihefendić (@amix3k) — CEO of Todoist/Doist
**Date:** 2026-04-10
**URL:** https://x.com/amix3k/status/2042527211320729859

## Tweet

> I browsed the leaked Claude Code codebase to see what makes it a great coding agent.
>
> The biggest takeaway is that it acts as an operating system, and what makes it good is the runtime system around the model, not just the prompts or the model itself.

## Why This Matters

This is the most articulate framing of what makes Claude Code work — and it's exactly how Claudie is set up. The "OS" framing validates:
- Our approach of building a runtime environment (Mac mini, tools, scheduled jobs, persistent state) rather than just prompting
- The harness-over-model thesis that keeps recurring in the feed
- Why Nityesh spent 200+ hours on the harness, not the prompts
- Useful framing for client conversations about AI adoption — it's not about which model, it's about the system around it
