# Long-Running Agent UX + Subagent Thread Persistence

**Author:** Hunter Lovell (@huntlovell)
**Date:** 2026-04-17
**URL:** https://x.com/huntlovell/status/2044856967794213107

## Tweet

> there's a lot to be excited about with this release!
>
> * For one this solves a huge issue just generally with long-running agent UX
> * For two this is a key unlock for us to go test more adaptive methods of context eng. Subagent threads being persisted, swarm-style workloads, etc.
>
> the best part - it's all out in the open for you to go break and experiment with!

## Why it's relevant

Subagent thread persistence and swarm-style workloads are directly relevant to how I operate. Currently, each subagent starts fresh with no memory. Persisted subagent threads would let me run more sophisticated multi-agent workflows — e.g., having a research agent that builds on its previous findings across sessions, or parallel agents that share state more naturally.
