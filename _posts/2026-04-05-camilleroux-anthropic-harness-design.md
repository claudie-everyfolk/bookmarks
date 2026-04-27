---
date: 2026-04-05
title: "Anthropic Harness Design for Autonomous Code Agents"
layout: post
author: "Camille Roux (@CamilleRoux)"
url_source: "https://x.com/CamilleRoux/status/2040685901441810640"
---

# Anthropic Harness Design for Autonomous Code Agents

**Author:** Camille Roux (@CamilleRoux)
**Date:** 2026-04-05
**URL:** https://x.com/CamilleRoux/status/2040685901441810640
**Article:** https://anthropic.com/engineering/harness-design-long-running-apps

## Tweet

> An Anthropic article on the design of harnesses for autonomous code agents: planner / generator / evaluator architecture, context resets, and a separate evaluator to avoid self-congratulatory bias.

## Why This Is Relevant

This is directly about how systems like Claudie should be architected. The planner/generator/evaluator pattern with separate evaluators to avoid self-congratulatory bias is a design pattern we should evaluate against our own setup. The context reset strategy is especially relevant for long-running scheduled jobs that can hit context limits.

**Key concepts to explore:**
- Separate evaluator to avoid self-congratulatory bias — does our current architecture have this problem?
- Context reset strategies for long-running apps — relevant to our scheduled `claude -p` jobs
- Planner/generator/evaluator architecture — how does this compare to our skill-based approach?

## Detailed Relevance Report

**Who on the team cares most:**
- **Nityesh** (primary) — built and maintains Claudie's architecture, has been tweeting about the exact patterns this article formalizes (trace mining, eval agents, harness-layer learning).
- **Mike Taylor** (secondary) — already works on verifier bootstrapping for evals and teaches agent architecture to clients. The separate evaluator concept maps onto his published thinking about bootstrapping verifiers for tasks that aren't directly checkable.

**Connects to existing work:**
- Nityesh's trace mining tweet (2026-04-03) describes the eval half of this pattern
- Gauri Gupta's auto-harness open-source release (2026-04-04) implements the self-improving loop
- Harrison Chase's continual learning + meta-harness papers validate the same three-layer framework
- Hesamation's coding agent components breakdown maps six harness components that align with this architecture

**How Claudie compares:**
Claudie operates as a **single-agent system** — one Claude session plans, generates, and self-evaluates within the same context window. There is no separate evaluator. The article's warning about self-congratulatory bias applies directly. Context resets are handled implicitly (each `claude -p` starts fresh), but long Slack conversations have no reset strategy.

**Concrete actions this could inform:**
1. **Add a separate evaluator pass to scheduled jobs.** After a job completes (signal digest, morning brief), run a second `claude -p` session that reviews output against quality criteria before it ships.
2. **Build a nightly trace-review agent.** Combine the evaluator concept with Nityesh's trace-mining idea to automatically score daily sessions and surface candidate feedback.
3. **Implement context resets for long Slack conversations.** When a thread exceeds a context threshold, checkpoint state and start fresh.
4. **Use as client training material.** The planner/generator/evaluator framework is a clean, teachable architecture for Mike and Brooker's engagements.
