---
date: 2026-05-10
title: "Claude Code's architecture, mapped"
layout: post
author: "Akshay (@akshay_pachaar)"
url_source: "https://x.com/akshay_pachaar/status/2053480693733433797"
snippet: "Claude Code is one of the most powerful agent harnesses out there — six layers (Input, Knowledge, Execution, Integration, Multi-Agent, Observability), and the model is just one node inside the loop. Harness intelligence lives outside the weights. Master agent loop: perception → action → observation. Not magic — harness engineering."
relevance: "Direct map of the system Claudie runs on. Useful as internal reference for debugging Claudie's behavior and as client-training material — when explaining how Claude Code works under the hood, this six-layer model is cleaner than what's currently in the curriculum. Worth pulling into Jean Claude's curriculum updates."
---

# Claude Code's architecture, mapped

**Author:** Akshay (@akshay_pachaar)
**URL:** https://x.com/akshay_pachaar/status/2053480693733433797
**Date:** 2026-05-10

## Tweet

> Claude Code's architecture, mapped. Six layers, and the model is just one node inside the loop.
>
> **Input Layer:** session management, permission gating, YAML-based trust tiers.
>
> **Knowledge Layer:** skill registry, context compressor (3-layer, 92% threshold), task graph, cross-session memory store. Harness intelligence lives outside the weights.
>
> **Execution Layer:** tool dispatch through a typed registry. Streaming runtime, prompt cache reuses stable prefixes at 10% cost.
>
> **Integration Layer:** MCP runtime to external servers. Memory writes outward to agent_memory.md.
>
> **Multi-Agent Layer:** subagent spawner, teammate mailboxes over redis pub/sub, FSM protocol, autonomous board with atomic locks, worktree isolation.
>
> **Observability Layer:** event bus with lifecycle hooks, background executor running daemon threads non-blocking.
>
> Master agent loop: perception → action → observation. A "dumb loop" where the model reasons and the harness mediates. Not magic — harness engineering.

## Why it's relevant

Direct map of the system Claudie runs on. Useful both as internal reference for debugging Claudie's behavior and as client-training material. The six-layer model is cleaner than what's currently in the curriculum — worth pulling into Jean Claude's curriculum updates.
