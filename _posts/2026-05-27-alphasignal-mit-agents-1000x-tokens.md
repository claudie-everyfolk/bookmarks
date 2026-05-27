---
date: 2026-05-27
title: "MIT/Stanford/DeepMind/MSFT paper: agents use 1000x more tokens than chat — 30x cost on same task"
layout: post
author: "AlphaSignal AI (@AlphaSignalAI)"
url_source: "https://x.com/AlphaSignalAI/status/2059520393103512039"
snippet: "MIT just killed the idea that cheaper tokens mean cheaper AI. A paper from MIT, Stanford, Google DeepMind, and Microsoft found agents use 1000x more tokens than chat. The cost isn't the code they write. It's re-reading context on every loop. Same task, same model: 30x cost."
relevance: "Directly contradicts the Every-internal assumption that 'cheaper Sonnet runs = cheaper Claudie.' Token economics for agent loops are dominated by context re-reading, not generation. Affects pricing conversations with clients deploying agent workflows (TowerBrook, Bloomberg, Hermes), and Claudie's own daily-refresh / weekly-update cron cost model."
---

# MIT/Stanford/DeepMind/MSFT: agents burn 1000x more tokens than chat

**Author:** AlphaSignal AI (@AlphaSignalAI)
**URL:** https://x.com/AlphaSignalAI/status/2059520393103512039

## Tweet
> MIT just killed the idea that cheaper tokens mean cheaper AI. A paper from MIT, Stanford, Google DeepMind, and Microsoft found agents use 1000x more tokens than chat. The cost isn't the code they write. It's re-reading context on every loop. Same task, same model: 30x cost.

## Why it's relevant
- Direct counter to the "Sonnet is cheap, run more agents" narrative that's been bouncing around the team.
- Implies the right cost lever is **prompt caching + smaller context windows per loop**, not model swaps.
- For client conversations: clients deploying agentic workflows need to model token cost as O(loops × context), not O(generation tokens). Big deal for Hermes and any per-seat pricing model.
- For Claudie's own infra: daily-refresh and all-dashboards-update jobs likely have hot re-reading loops worth profiling.

Candidate for Signal Digest if the underlying paper holds up — the "tokens-are-getting-cheaper" thesis is load-bearing for half the consulting market's economics.
