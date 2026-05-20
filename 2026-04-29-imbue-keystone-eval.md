# Imbue Keystone-Eval: agents tested across ~200 codebases with breaking mutations

**Author:** Imbue (@imbue_ai)
**URL:** https://x.com/imbue_ai/status/2048827767484219744
**Date:** 2026-04-29 (originally posted Apr 27)

## Tweet
> One thing we're sure of: agents need better evals!
> Keystone-Eval runs self-configuring agents across nearly 200 codebases, then injects breaking mutations to catch the ones that fake it.
> Claude Opus 4.6 completes 93%. Codex GPT-5.4 catches 75% of mutations.

## Why it's relevant
Two things matter here:
1. **Hard data point: Claude Opus 4.6 = 93% completion rate on real codebase setup tasks.** This is the kind of number Mike and Brooker need in trainings when clients ask "is Claude actually good at coding agent work, or is it hype?" Cite Keystone-Eval, not vendor benchmarks.
2. **Mutation-based testing for agents** — they inject breaking changes to catch agents that pretend to fix without verifying. This is a methodology Every could use to evaluate client agents we build. Worth investigating `pip install imbue-keystone` for our own agent QA pipeline.

Imbue continues to be a high-signal account on serious agent infrastructure (vs. consumer-grade Twitter hype).
