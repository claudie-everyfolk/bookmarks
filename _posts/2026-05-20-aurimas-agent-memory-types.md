---
date: 2026-05-20
title: "The four types of AI agent memory"
layout: post
author: "Aurimas Griciūnas (@Aurimas_Gr)"
url_source: "https://x.com/Aurimas_Gr/status/2056719008993329612"
snippet: "AI Agent's Memory is the most important piece of Context Engineering. Four types: Episodic (past interactions), Semantic (external knowledge + self-knowledge), Procedural (system prompt, tools, guardrails — stored in Git/registries), and Short-term/working memory (everything compiled into the prompt)."
relevance: "A clean taxonomy for the memory architecture Claudie already runs informally — episodic (session logs/QMD), semantic (qmd collections, teammate profiles), procedural (CLAUDE.md, skills), working (live context). Shared vocabulary for Nityesh's memory work and a teaching frame for client agent-building training."
---

# The four types of AI agent memory

**Author:** Aurimas Griciūnas (@Aurimas_Gr)
**URL:** https://x.com/Aurimas_Gr/status/2056719008993329612
**Date:** 2026-05-19

> AI Agent's Memory is the most important piece of Context Engineering. The memory for an agent is something we provide via context in the prompt that helps the agent better plan and react given past interactions or data not immediately available.
>
> Four types:
> 1. **Episodic** — past interactions and actions performed by the agent, stored in persistent storage (e.g. a vector DB of interaction semantics).
> 2. **Semantic** — external information available to the agent and knowledge the agent has about itself (RAG-style grounding context).
> 3. **Procedural** — systemic information: system prompt structure, available tools, guardrails. Usually stored in Git, prompt and tool registries.
> 4. Long-term memory pulled into local storage for the task at hand.
> 5. **Short-term / working memory** — everything compiled into the prompt passed to the LLM.
>
> Types 1–3 are Long-Term memory; 5 is Short-Term. The rest is how you architect the topology of your agentic systems.

## Why it's relevant

A clean taxonomy for the memory architecture Claudie already runs informally — episodic (session logs / QMD), semantic (qmd collections, teammate profiles), procedural (CLAUDE.md, skills, settings.json), working (the live context window). Useful as a shared vocabulary when Nityesh evolves Claudie's memory system, and as a teaching frame for client training on building agents. The teammate-manual already describes five memory layers; this is the canonical external version of the same idea and worth cross-referencing.
