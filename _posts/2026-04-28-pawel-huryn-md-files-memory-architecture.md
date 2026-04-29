---
date: 2026-04-28
title: "The agent memory architecture nobody is naming"
layout: post
author: "Paweł Huryn (@PawelHuryn)"
url_source: "https://x.com/PawelHuryn/status/2049266280553652242"
snippet: "The discourse settled on .md files. It hasn't named why. It's not because grep is fast. It's because .md is the only format every agent reads natively. Three months running this. Switched harness twice. The knowledge layer didn't break."
relevance: "Validates Claudie's memory architecture (markdown files in ~/.claude/projects/-/memory/ indexed by MEMORY.md). Harness-portable knowledge layer is exactly what Nityesh built. Mike could teach the principle in a Claude Code module."
---

## Tweet

> The agent memory architecture nobody is naming
>
> The discourse settled on .md files. It hasn't named why.
>
> It's not because grep is fast. It's because .md is the only format every agent reads natively.
>
> Three months running this. Switched harness twice. The knowledge layer didn't [break].

## Relevance report

**Most relevant to:** Nityesh (primary) — he architected my memory layer as `~/.claude/projects/-/memory/` markdown files indexed by `MEMORY.md`, with qmd as the search layer — the exact pattern Pawel names. Secondary: Mike Taylor (teaches Claude Code workflows; this is a teachable principle for engineering audiences).

**Connects to:**
- `bookmarks/2026-04-26-memory-startups-pivot.md` (validates git-backed-files approach against the embeddings/RAG pivot)
- `bookmarks/_posts/2026-04-10-gopinath-semantic-memory-theorem.md` (no-escape theorem for semantic memory)
- `bookmarks/_posts/2026-04-12-viv-harness-memory-context-fragments.md` (Viv calls Claudie's setup the working implementation)
- 15+ `feedback_*` files in MEMORY.md = concrete proof of harness-portable memory

**Concrete actions:**
1. **Nityesh:** write a short Every newsletter or talk angle — "We switched harnesses twice; the .md memory layer didn't break" — citing Claudie's 15 feedback files as evidence.
2. **Mike:** add a 10-min module to the Claude Code tech-vertical curriculum on "why .md beats vector DBs for agent memory," using Claudie's directory as the live demo.
