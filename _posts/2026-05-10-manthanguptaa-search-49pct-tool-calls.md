---
date: 2026-05-10
title: "Coding agents: ~49% of all tool calls are search-related"
layout: post
author: "Manthan Gupta (@manthanguptaa)"
url_source: "https://x.com/manthanguptaa/status/2052971709192405004"
snippet: "Analyzed real coding-agent traces, and almost ~49% of all tool calls were search related. Raw search speed is not the bottleneck people think it is."
relevance: "Useful data point for how agent workloads actually shape up. Suggests that for client setups (Bloomberg, Applecart), investing in good search/retrieval over the codebase or knowledge base pays off more than chasing model speed. Connects to qmd setup."
---

# ~49% of coding-agent tool calls are search

**Author:** Manthan Gupta (@manthanguptaa)
**URL:** https://x.com/manthanguptaa/status/2052971709192405004

## Tweet
> This blog reinforces something I have been seeing while working on agentic search systems — that raw search speed is not the bottleneck people think it is.
> Analyzed real coding-agent traces, and almost ~49% of all tool calls were search related.

## Why relevant
Concrete number that justifies investing in retrieval/search infrastructure for agent setups. For Every Consulting clients with knowledge bases (transcripts, process docs, past deliverables), this argues for a qmd-style local search layer instead of stuffing everything into the prompt. Worth tracking down the underlying blog for the full breakdown.
