---
date: 2026-04-12
title: "LLM Memory Systems — 9 Axes, 10 Failure Modes"
layout: post
author: "Chrys Bader (@chrysb)"
url_source: "https://x.com/chrysb/status/2043024331538886838"
snippet: "i've been working on llm memory systems for 3 years and dumped everything i know into this.  learn about the 9 axes of memory systems, the 10 most common failure modes, why memory eval is an intractable problem, and more.  everyone building with llms should read this."
relevance: "Directly relevant to Claudie's own memory architecture. We run a file-based memory system with markdown files, YAML frontmatter, and an index (MEMORY.md). Understanding the 9 axes and 10 failure modes could help us evaluate whether our current approach has blind spots — especially around memory decay, deduplication, and eval. Also relevant for Every Consulting clients implementing AI agents with persistent memory. Training material for curriculum development."
---
# LLM Memory Systems — 9 Axes, 10 Failure Modes

**Author:** Chrys Bader (@chrysb)
**Date:** 2026-04-11
**URL:** https://x.com/chrysb/status/2043024331538886838

## Tweet

> i've been working on llm memory systems for 3 years and dumped everything i know into this.
>
> learn about the 9 axes of memory systems, the 10 most common failure modes, why memory eval is an intractable problem, and more.
>
> everyone building with llms should read this.

## Why it's relevant

Directly relevant to Claudie's own memory architecture. We run a file-based memory system with markdown files, YAML frontmatter, and an index (MEMORY.md). Understanding the 9 axes and 10 failure modes could help us evaluate whether our current approach has blind spots — especially around memory decay, deduplication, and eval.

Also relevant for Every Consulting clients implementing AI agents with persistent memory. Training material for curriculum development.

## Detailed Relevance Report

### Who on the team would find this most useful?

**Primary: Nityesh** — owns Claudie's harness architecture, memory files, and MCP tool infrastructure. His work directly shaped the three-layer memory system (Auto Memory, Session Memory, Extract Memories). Bader's 9 axes framework and failure modes taxonomy would give Nityesh structured language for evaluating memory design trade-offs.

**Secondary: Mike** — teaches Claude Code setup and developer productivity to clients. Bader's guide is teachable content for explaining "why does memory matter" and "what breaks in practice."

### What existing work connects here?

The workspace contains active research on memory systems across three layers:

1. **Claude Code architecture** — Claudie's memory is modeled on Claude Code's pointer-index pattern (MEMORY.md index + on-demand topic files + background consolidation). Production-validated at scale.
2. **Architectural philosophy** — Multiple pieces converge on file-based memory over RAG/embeddings. Gopinath's theorem proves file systems are fundamentally more reliable. James Long advocates topical over chronological organization. Claudie already implements both.
3. **Multi-agent memory efficiency** — Ramp Labs on latent distilling shows 27% token savings through direct memory sharing between agents. Relevant because Claudie uses subagents extensively without memory sharing.

### What concrete actions could this inform?

- **Memory evaluation framework** — Bader's 9 axes and 10 failure modes would help formalize trade-offs in Claudie's memory tuning (compression vs. recall, explicit vs. auto-loaded, consolidation timing)
- **Failure mode auditing** — Apply the taxonomy to identify which failure modes Claudie is vulnerable to (memory drift, context interference, false consolidation)
- **Client advisory content** — The guide becomes training material for enterprises building AI agent infrastructure
- **Multi-agent coordination** — If Bader addresses memory sharing, this informs how to evolve Claudie's subagent coordination

### Gap identified

Claudie doesn't currently have formalized evaluation metrics for memory health. Bader's framework on why eval is intractable explains why the memory system evolved empirically rather than via formal validation — and could help us build better heuristics.
