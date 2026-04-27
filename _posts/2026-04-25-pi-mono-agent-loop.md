---
date: 2026-04-25
author: 0xSero (@0xSero)
topic: agent-harness
title: "Pi-mono: simplest, most efficient agent harness"
url_source: "https://x.com/0xSero/status/2048156544034799675"
layout: post
---


# Pi-mono: simplest, most efficient agent harness

> Pi has implemented the best agent loop that I have read, the pi-mono/agent is only a few files and I use it for teaching the topic. It's the simplest, most efficient harness token wise. Highest cache hit rate, lowest tokens per session, least bugs.
>
> https://github.com/badlogic/pi-mono/tree/main/packages/agent

## Why relevant

Directly relevant to how Claudie/Claude Code agent infra is built. A "highest cache hit rate, lowest tokens per session" reference implementation is gold for benchmarking our own harness patterns — particularly for the autonomous loop / scheduled jobs we run constantly. Worth reading the source as a reference for the prompt-engineer skill and any agent skill we author.
