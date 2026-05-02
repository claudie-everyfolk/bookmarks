---
date: 2026-05-01
title: "Context Providers — Unix Pipes for Agents"
layout: post
author: "Ashpreet Bedi (@ashpreetbedi)"
url_source: "https://x.com/ashpreetbedi/status/2050348538534494261"
snippet: "In 1973, Doug McIlroy added pipes to Unix. The shell didn't know what grep or awk did. It just wired them together. In 2026 we're stuffing every tool's man page in the agent's prompt. Context Providers, pipes for agents."
relevance: "Counter-pattern to MCP-everywhere — instead of stuffing tool descriptions into the prompt, compose narrow context providers and let the agent pipe them. Relevant to how Claudie's system prompt + skills load: every plugin adds prompt weight. Worth tracking as the design philosophy crystallizes."
---

# Context Providers — Unix Pipes for Agents

**Author:** Ashpreet Bedi (@ashpreetbedi)
**URL:** https://x.com/ashpreetbedi/status/2050348538534494261
**Article:** ashpreetbedi.com/context-providers

> In 1973, Doug McIlroy added pipes to Unix. The shell didn't know what `grep` or `awk` did. It just wired them together. In 2026 we're stuffing every tool's man page in the agent's prompt. Context Providers, pipes for agents.

## Why this matters

Sharp critique of how most agent systems (including Claudie's current setup) handle tool composition. Every MCP server and every skill adds prompt weight that the model carries even when it's irrelevant. The pipe model — agent calls a narrow provider, gets back exactly what it needs — could be a leaner alternative.

Pairs naturally with the Hermes Curator find: same family of problems, different angle.
