---
date: 2026-04-29
title: "The harness as the context manager"
layout: post
author: "Tony Gentilcore (@tonygentilcore)"
url_source: "https://x.com/tonygentilcore/status/2049482833111232694"
snippet: "Harnesses, the execution logic that surrounds models, are producing gains in long-running agent performance across the industry. LangChain improved Terminal-Bench by +13.7 points through harness work alone — no model swap. The harness decides how to break a request into steps, which tools to call, what to remember, when to stop."
relevance: "Frames Claudie's whole stack — CLAUDE.md memory loop, skills, MCP, slack-bot wrapper — as a harness, i.e. the context manager. +13.7 Terminal-Bench gain from harness alone is a strong client data point: model selection is not the lever; harness engineering is. Useful framing for Mike's training and Brooker's enablement work."
---

# The harness as the context manager

**Author:** Tony Gentilcore (@tonygentilcore)
**URL:** https://x.com/tonygentilcore/status/2049482833111232694

## Tweet
> Harnesses, the execution logic that surrounds models, are producing gains in long-running agent performance across the industry. LangChain improved Terminal-Bench by +13.7 points through harness work alone.

## Why it's relevant
Directly speaks to Claudie's architecture. The whole Claudie infrastructure IS a harness. This article frames the harness as the *context manager* — useful framing for client-facing explanation of why Every's "AI integration" work is more about scaffolding than picking models.
