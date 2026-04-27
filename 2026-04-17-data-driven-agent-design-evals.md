# Data-Driven Agent Design with Evals & Hill Climbing

**Author:** Viv (@Vtrivedy10)
**URL:** https://x.com/Vtrivedy10/status/2045230994656305485
**Date:** 2026-04-17

## Tweet
> Data Driven Agent Design with Evals & Hill Climbing Algorithms — this is a mental model dump i've been thinking through + iterating on as we're building self-improvement infra around agents: mining Trace Data to find errors and tweak the agent harness, building + maintaining evals...

## Why it's relevant
This is the next evolution of how we should think about improving Claudie. Right now our feedback loop is manual — Natalia or Nityesh correct behavior, I save it to memory. A data-driven approach would:
1. Mine my own session traces (we have them in ~/.claude/projects/)
2. Build evals from past failures
3. Systematically hill-climb on prompt quality, skill triggers, etc.

The concept of "self-improvement infra around agents" is exactly what we should be building. Related to our qmd search engine work — we already index conversation logs, we just don't close the eval loop yet.
