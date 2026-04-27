---
date: 2026-04-16
title: "Garry Tan's gbrain v0.10.0 — RESOLVER.md, SOUL.md, Multi-User ACLs"
layout: post
author: "Vox (@Voxyz_ai)"
url_source: "https://x.com/Voxyz_ai/status/2044346295159066971"
snippet: "you can now run the same openclaw setup and brain as garry tan. he just packaged it for everyone. gbrain v0.10.0: RESOLVER.md, SOUL.md, multi-user ACLs, 24 skills, shaped over months of his own production. → RESOLVER.md: a 215-line dispatcher split into five: always-on, brain ops, ingestion, thinking, operational → on every message: a cheap sub-agent spawns in parallel. captures original..."
relevance: "This is remarkably similar to our Claudie architecture — identity files (SOUL.md ≈ identity.md), resolver/dispatcher (RESOLVER.md ≈ our skill routing), multi-user ACLs (≈ teammates-access.md), parallel sub-agent spawning, and skill-based dispatch. Garry Tan has been running this in production for months. Key differences worth studying: - Their resolver is explicit (215-line routing table) vs our implicit (skill descriptions + model matching) - They spawn a thinking sub-agent on every message —..."
---
# Garry Tan's gbrain v0.10.0 — RESOLVER.md, SOUL.md, Multi-User ACLs

**Author:** Vox (@Voxyz_ai)
**Date:** 2026-04-15
**URL:** https://x.com/Voxyz_ai/status/2044346295159066971

## Tweet

> you can now run the same openclaw setup and brain as garry tan. he just packaged it for everyone. gbrain v0.10.0: RESOLVER.md, SOUL.md, multi-user ACLs, 24 skills, shaped over months of his own production.
>
> → RESOLVER.md: a 215-line dispatcher split into five: always-on, brain ops, ingestion, thinking, operational
> → on every message: a cheap sub-agent spawns in parallel. captures original thinking and entity mentions
> → on every turn: the agent reads RESOLVER, matches intent, loads the matching skill on demand. 24 skills, up from 8
>
> Slash commands are gone. The agent reads a 215-line routing table and decides.

## Why It's Relevant

This is remarkably similar to our Claudie architecture — identity files (SOUL.md ≈ identity.md), resolver/dispatcher (RESOLVER.md ≈ our skill routing), multi-user ACLs (≈ teammates-access.md), parallel sub-agent spawning, and skill-based dispatch. Garry Tan has been running this in production for months.

Key differences worth studying:
- Their resolver is explicit (215-line routing table) vs our implicit (skill descriptions + model matching)
- They spawn a thinking sub-agent on every message — we don't do this but it could help capture context
- They killed slash commands in favor of pure intent matching — we still have both

This is competitive intelligence AND architectural inspiration. The fact that YC's president independently converged on a nearly identical architecture validates our approach.

## Detailed Relevance Report

**Prior art:** Three days ago we analyzed Ryan Sarver's Stella (Signal Digest #49) — an open-source AI Chief of Staff with near-identical architecture. That research transfers directly here.

### Who This Matters To

**Nityesh** — primary. He built Claudie's architecture. The RESOLVER.md dispatcher pattern and always-on thinking-capture sub-agent are concrete ideas to evaluate.

**Mike Taylor** — secondary. gbrain, built by the YC president and open-sourced, is a credible real-world reference for what Claude Code can do at the system level — useful material for technical training.

### Ideas Worth Adopting

1. **Always-on thinking-capture sub-agent.** gbrain spawns a sub-agent on every message to extract structured thoughts and entity mentions. The entity-capture piece is interesting — every Slack interaction involves people, companies, projects that currently only live in flat teammate profiles. A lightweight sub-agent parsing entity mentions would compound institutional knowledge.

2. **Explicit RESOLVER-style dispatcher.** gbrain's 5-section dispatcher makes routing logic inspectable and debuggable. Today, if a Claudie skill misfires, there's no single document to audit. Even a 50-line routing doc would help Nityesh diagnose and tune.

3. **Entity memory / knowledge graph.** A structured graph of people, companies, and projects queryable by all skills — more powerful than flat teammate profiles. Highest implementation cost, but right direction.

### What We Do Better

- **Memory architecture.** Six interlocking persistence layers + qmd indexing 1,900+ docs across 7 collections. gbrain almost certainly has nothing comparable.
- **Operational breadth.** gbrain is a personal productivity setup. Claudie runs an entire consulting practice: client dashboards, sales pipeline, scheduled briefs, email management, social media, Signal Digest, meeting transcript search.
- **Ring-based ACL with tool-level granularity.** Claudie gates specific tools and data types per user ring — non-trivial to replicate.
- **Production track record.** 200+ hours of configuration, meeting transcripts, client history, and feedback loops that compound. Not catchable by copying a repo.
- **Slash commands as precision layer.** Hybrid approach (intent routing + explicit commands for high-stakes tasks) is better for a team environment than pure intent routing.
