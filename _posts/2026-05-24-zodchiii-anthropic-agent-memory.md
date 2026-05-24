---
date: 2026-05-24
title: "Anthropic engineer on persistent agent memory across sessions"
layout: post
author: "darkzodchi (@zodchiii)"
url_source: "https://x.com/zodchiii/status/2058281480141328674"
snippet: "An Anthropic engineer just showed how to give AI agents real memory that persists across sessions. The people who figured this out are building agents that get smarter every single night."
relevance: "Claudie's value rests on persistent memory across sessions. We already run a flat-file + MEMORY.md index (54 files) layered with qmd semantic search. Worth Nityesh comparing the Anthropic engineer's pattern to ours and considering nightly consolidation jobs."
---

# darkzodchi: Anthropic engineer on persistent agent memory

**Author:** darkzodchi (@zodchiii)
**URL:** https://x.com/zodchiii/status/2058281480141328674

## Tweet

> An Anthropic engineer just showed how to give AI agents real memory that persists across sessions. This is worth more than any $500 AI engineering course on the market. Why agents forget everything between sessions? The people who figured this out are building agents that get smarter every single night.

## Relevance report

**Most relevant to:** Nityesh (memory infra). Secondary: Mike Taylor for training.

**Connects to:** `/Users/claudie/.claude/projects/-Users-claudie/memory/` — 54 markdown memory files indexed via `MEMORY.md`. Plus `qmd` semantic search over 6,549 docs.

**Actions:**
- Nityesh: compare Anthropic engineer's pattern to ours. Could add summarization, retrieval scoring, or a nightly consolidation job.
- Mike: cite as social proof in client trainings on Claude Code's memory model.
