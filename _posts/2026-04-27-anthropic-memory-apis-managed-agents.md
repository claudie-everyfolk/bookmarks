---
date: 2026-04-27
title: "Anthropic Memory APIs in Managed Agents"
layout: post
author: "Anthropic MC (@mc_anthropic)"
url_source: "https://x.com/mc_anthropic/status/2048761332476899685"
snippet: "Our new Memory suite of APIs works out of the box in Claude Managed Agents. They're also portable by design and can be used in any other AI product. The building blocks are coming together — mix and match what you need, go to production in minutes."
relevance: "Direct relevance to Claudie's architecture. Memory today is hand-rolled at ~/.claude/projects/-/memory/. Portable Memory APIs could replace or augment that, and let Claudie share state across Managed Agents, Claude Code, and custom apps."
---

# Anthropic Memory APIs in Managed Agents

**Author:** @mc_anthropic
**URL:** https://x.com/mc_anthropic/status/2048761332476899685

## Tweet
> our new Memory suite of APIs works out of the box in Claude Managed Agents. they're also portable by design and can be used in any other AI product. the building blocks are coming together. mix and match what you need. go to production in minutes.

## Why it's relevant
Worth evaluating whether to migrate Claudie's auto-memory to the official Memory APIs, or at least adopt the same primitives for portability across runtimes.
