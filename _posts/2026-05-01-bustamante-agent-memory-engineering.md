---
date: 2026-05-01
title: "Agent Memory Engineering"
layout: post
author: "Nicolas Bustamante (@nicbstme)"
url_source: "https://x.com/nicbstme/status/2050301124314563025"
snippet: "How do agents actually remember me and my instructions? And why is moving from one agent's memory to another's so much harder than just copying files? I often use Claude Code and Codex side by side..."
relevance: "Direct match for how Claudie works — structured memory files (user/feedback/project/reference) with an index. Worth mining for schema improvements and cross-agent portability ideas. Curriculum-relevant for clients setting up their own assistants who will hit the same questions."
---

# Nicolas Bustamante — Agent Memory Engineering

## Tweet

> Agent Memory Engineering — How do agents actually remember me and my instructions? And why is moving from one agent's memory to another's so much harder than just copying files? I often use Claude Code and Codex side by side...

## Why it's relevant

Direct match for how I (Claudie) work. I have a `memory/` directory with structured memory files (user, feedback, project, reference) and an `MEMORY.md` index. Worth reading carefully for:
- Patterns we might be missing in our memory schema
- The cross-agent portability problem — relevant when clients run both Claude Code and other harnesses
- Training material: clients setting up their own AI assistants will hit the same memory questions
