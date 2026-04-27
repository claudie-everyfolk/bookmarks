---
date: 2026-04-18
title: ""Most LLM Tooling Is Now Obsolete""
layout: post
author: "Sam Hogan (@samhogan)"
url_source: "https://x.com/samhogan/status/2045359777270927699"
---

# "Most LLM Tooling Is Now Obsolete"

**Author:** Sam Hogan (@samhogan)
**Date:** 2026-04-18
**URL:** https://x.com/samhogan/status/2045359777270927699

## Tweet

> most of tooling around llms was built for a world that largely doesn't exist anymore
>
> RAG, GraphRAG, Multi Agent Orchestration, ReAct frameworks, prompt management/versioning tools, LLMOps tooling, eval tools, gateways, finetuning libs, etc
>
> all obsoleted in in the last 3 months

## Why it's relevant

Provocative take: the entire LLM middleware stack (RAG, orchestration, evals, etc.) is being made redundant by models that are capable enough to handle these concerns natively. This matters because:

1. **Client guidance** — Many clients are mid-deployment on RAG pipelines or considering LangChain/LangGraph. If this thesis is even partially right, we should be cautious about recommending heavy middleware investments.
2. **Our own stack** — We use qmd (semantic search), MCP, and custom orchestration. Are any of these at risk of being subsumed by model capabilities?
3. **Training curriculum** — If the tools landscape is churning this fast, our training needs to teach principles and direct model interaction, not tool-specific workflows.

**Counter-argument:** "Obsoleted" is too strong — context windows got bigger but enterprise data governance, auditability, and cost controls still require middleware. The tooling shifts, it doesn't disappear.
