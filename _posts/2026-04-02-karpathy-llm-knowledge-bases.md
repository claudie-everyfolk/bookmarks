---
date: 2026-04-02
title: "Karpathy: LLM Knowledge Bases"
layout: post
author: "Andrej Karpathy (@karpathy)"
url_source: "https://x.com/karpathy/status/2039805659525644595"
---

# Karpathy: LLM Knowledge Bases

**Author:** Andrej Karpathy (@karpathy)
**URL:** https://x.com/karpathy/status/2039805659525644595
**Date:** 2026-04-02

## Tweet

> LLM Knowledge Bases
>
> Something I'm finding very useful recently: using LLMs to build personal knowledge bases for various topics of research interest. In this way, a large fraction of my recent token throughput is going less into manipulating code, and more into manipulating knowledge.

## Why it's relevant

Karpathy — one of the most respected voices in AI — is signaling a shift in how top practitioners use LLMs: from code generation to knowledge synthesis and management. This is directly relevant to:

1. **How Claudie is set up** — our memory system, knowledge base, and bookmark curation pipeline is exactly this pattern
2. **Client training** — we can teach clients to build personal knowledge bases with LLMs, not just use them for code/writing
3. **Agent architecture** — the idea that agents should maintain persistent, growing knowledge bases (not just respond to queries) aligns with how we've built Claudie

---

## Deep Relevance Report (sub-agent analysis)

### How Karpathy's Approach Compares to Claudie's System

Claudie already operates a multi-layer knowledge system strikingly close to what Karpathy describes:

| Karpathy's Pattern | Claudie's Implementation |
|---|---|
| Using LLMs to build knowledge bases | Structured bookmark files with analysis during 4x daily X browsing |
| Personal research topics | Bookmarks filtered through "relevant to Every Consulting" lens |
| Manipulating knowledge, not code | The bookmark → Signal Digest pipeline is pure knowledge synthesis |
| Persistent, growing knowledge | Memory files accumulate behavioral corrections; bookmarks grow daily |

**The gap:** Karpathy likely means something more interactive — extended conversations with an LLM where it maintains evolving understanding. Claudie's system is more one-directional (browse → bookmark → digest) than bidirectional. No mechanism today to revisit old bookmarks, connect them to new ones, or build evolving position papers.

### Who This Is Most Relevant To

- **Nityesh (Primary)** — Architecturally his territory. The gap between Claudie's current pipeline and a true bidirectional knowledge base is the next evolution he could build. Cross-referencing bookmarks, weekly knowledge synthesis, and searchable knowledge graphs are all natural next steps.
- **Mike Taylor (High)** — Perfect teaching moment for technical training: reframes what developers should do with LLMs beyond code. Pairs with the Obsidian-as-agent-wiki pattern for practical workshop takeaways.
- **Natalia (Strategic)** — "LLM Knowledge Bases" could become a new service offering. Clients in finance and media sit on massive institutional knowledge that's poorly structured. Teaching them knowledge synthesis vs. task automation is a natural extension.
- **Brooker (Applicable)** — For non-technical audiences: you don't need to code to build an LLM knowledge base. Finance clients could use this for investment research, market analysis, or regulatory tracking.

### Concrete Actions

1. **New training module**: "You're using AI to write emails. Karpathy is using it to build knowledge bases. Here's how to do the same for your domain."
2. **Improve Claudie**: Add cross-referencing in bookmarks (today's Karpathy bookmark doesn't reference related Obsidian/memory stack bookmarks), weekly knowledge synthesis jobs, and bidirectional knowledge conversations.
3. **Enhance file browser**: Add search and auto-generated "related entries" links to turn the flat bookmark directory into a linked knowledge graph.

### The Bigger Picture

This connects to a thesis Every Consulting is already living but hasn't fully articulated: **the highest-value use of AI is not automation — it's augmented knowledge work.** The teams that win aren't the ones with the best AI tools — they're the ones who build the best knowledge systems on top of AI tools. Claudie is the living proof of concept.
