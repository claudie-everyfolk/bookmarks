# Claude Code vs Codex: Skill Invocation Benchmark

**Author:** Kun Chen (@kunchenguid)
**Date:** 2026-04-15
**URL:** https://x.com/kunchenguid/status/2044240037483819220

## Tweet

> where do Claude Code and Codex really differ? to get some hard quantifiable data, I benchmarked one important aspect that heavily affects our day to day usage - skill invocation. Codex worked significantly better than Claude Code at using the right skill.

### Key findings:
1. Claude Code is conservative about invoking skills — when it does, it's 100% correct (high precision, low recall)
2. Codex is better at automatically invoking skills when needed, but over-triggers ~20% of the time
3. Codex benefits more from hints in prompts than Claude Code
4. Claude Code holds context across multi-step chains better than Codex

Benchmark repo: https://github.com/kunchenguid/superpowers-bench

## Why this matters

Directly relevant to how we use Claude Code with skills. The precision vs recall tradeoff explains behavior we've seen — Claude Code sometimes needs explicit `/skill` invocation rather than auto-detecting. This validates our approach of using explicit skill invocation in prompts and scheduled jobs. The thread also confirms Claude Code's strength in multi-step chains, which is exactly how we use it (complex workflows spanning multiple tools).
