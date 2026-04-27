---
date: 2026-04-04
title: "auto-harness: Self-improving agentic systems with auto-evals (open-sourced)"
layout: post
author: "Gauri Gupta (@gauri__gupta), Co-founder NeoSigma, previously early @o1, PhD dropout @mit"
url_source: "https://x.com/gauri__gupta/status/2040251309782409489"
snippet: "Releasing auto-harness: an open source library for our self improving agentic systems with auto-evals. We got a lot of responses from people wanting to try the self-improving loop on their own agent. So we open-sourced our setup. Connect your agent and let it cook over the weekend! brrrrr! auto-harness: Self improving agentic systems with auto-evals (open-sourced!) Connect your agent and..."
relevance: "This is a self-improving loop for AI agents: automatically find failures, generate evals from them, then fix the agent. Open-sourced. Directly relevant to how we build and improve Claudie and client agent deployments. The model-harness training loop is something Nityesh has been talking about — this is an open-source implementation of exactly that pattern."
---
# auto-harness: Self-improving agentic systems with auto-evals (open-sourced)

**Author:** Gauri Gupta (@gauri__gupta), Co-founder NeoSigma, previously early @o1, PhD dropout @mit
**URL:** https://x.com/gauri__gupta/status/2040251309782409489
**Date:** 2026-04-03

## Tweet

> Releasing auto-harness: an open source library for our self improving agentic systems with auto-evals. We got a lot of responses from people wanting to try the self-improving loop on their own agent. So we open-sourced our setup.
>
> Connect your agent and let it cook over the weekend! brrrrr!
>
> auto-harness: Self improving agentic systems with auto-evals (open-sourced!)
> Connect your agent and let it cook over the weekend. We just open-sourced our auto-harness — a self-improving loop that finds your agent's failures, turns them into evals, and fixes them. All...

## Why It's Relevant

This is a self-improving loop for AI agents: automatically find failures, generate evals from them, then fix the agent. Open-sourced. Directly relevant to how we build and improve Claudie and client agent deployments. The model-harness training loop is something Nityesh has been talking about — this is an open-source implementation of exactly that pattern.

## Deep Relevance Report

**Direct connection to Nityesh's thinking:** On Apr 2, Nityesh (@Vtrivedy18) tweeted the exact same concept: "Collect every Trace + point agentic compute at it — run a Data/Eval Agent on every trace, mine errors+mistakes, fix + test, turn this into a data point for training or harness eng." Auto-harness is an open-source implementation of what he described.

**Who it's most relevant to:**
- **Nityesh (primary):** He owns Claudie's systems and has been thinking about this pattern. ~478 session logs and only 14 feedback files — 97% of traces go unreviewed. Auto-harness could automate the feedback loop he envisioned.
- **Mike Taylor:** For technical training engagements, this is a teachable framework — "configure agents that improve themselves."
- **Natalia:** As the primary recipient of Claudie's output, she benefits most from improved quality. Also relevant for sales: "we deploy self-improving AI systems" is a concrete differentiator.

**What it connects to internally:**
- The `tactical:investigate-yourself` skill already does forensic trace analysis on demand — auto-harness would automate this continuously.
- The Signal Digest entry on Pawel Huryn's "Quality Gate" framework identified the same gap: agents praise their own mediocre work without structured evaluation.
- The `skill-creator` skill already has eval/benchmark capabilities — auto-harness could feed its output.
- Our existing `project_repo_watcher` pattern (automated review loop for code) is structurally identical.

**Concrete actions:**
1. **Evaluate auto-harness for Claudie's own improvement.** Point it at session logs, score against the 14 existing feedback rules, surface new failure patterns for Nityesh to approve.
2. **Add to consulting deliverables.** Post-engagement, configure auto-harness on client agent deployments so they keep improving after we leave — justifies retainers.
3. **Build a training module.** "Self-improving agent loops" pairs naturally with the CLAUDE.md configuration work Mike and Nityesh already teach.
