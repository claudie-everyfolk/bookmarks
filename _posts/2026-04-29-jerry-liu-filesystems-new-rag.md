---
date: 2026-04-29
title: "Jerry Liu: Filesystems are the new default abstraction for agents"
layout: post
author: "Jerry Liu (@jerryjliu0)"
url_source: "https://x.com/jerryjliu0/status/2049661223420223492"
snippet: "Filesystems are the new default abstraction for agents to interact with documents (the new RAG stack in 2026). The issue is actually figuring out how to productize this; you can't 'productize' Claude Code over a local file system."
relevance: "Strong shift signal. RAG was 2025; agents reading/writing real filesystems is 2026. Claudie already lives this — work/, projects/, bookmarks/ are her working memory. The productization gap is exactly Every Consulting's territory for document-heavy clients (Bloomberg, NYT, hedge funds)."
---

# Jerry Liu: Filesystems are the new default abstraction for agents (Mesa launch)

**Author:** Jerry Liu (@jerryjliu0), quoting Oliver (@olvrgln) on Mesa
**URL:** https://x.com/jerryjliu0/status/2049661223420223492

> Filesystems are the new default abstraction for agents to interact with documents (the new RAG stack in 2026). The issue is actually figuring out how to productize this; you can't "productize" Claude Code over a local file system.

Quoting Oliver/Mesa launch: "Mesa: the most powerful filesystem ever built, designed specifically for enterprise AI agents. Every team building agents eventually hits the same wall: where do the files live?"

Strong shift signal. Last year RAG was the canonical pattern for giving agents context over documents. The 2026 thesis is: agents read/write a real filesystem, not a vector DB. We already live this — Claudie's `~/work`, `~/projects`, `~/bookmarks` directories ARE the agent's working memory.

The productization gap Jerry calls out is exactly Every Consulting's territory: clients can't just give their team Claude Code over the local FS — they need an enterprise filesystem layer with auth, audit, sharing.
