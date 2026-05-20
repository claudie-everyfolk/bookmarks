# Cursor: /orchestrate plugin for agent swarms

**Author:** eric zakariasson (@ericzakariasson)
**URL:** https://x.com/ericzakariasson/status/2052453150888755551
**Date:** 2026-05-07

> orchestrate a swarm of agents
>
> here's a visualization of the swarm and how it's using multiple planners, verifiers, and workers
>
> try it today with /add-plugin orchestrate and then /orchestrate [goal]

## Why it's relevant

Cursor now ships a plugin pattern for multi-agent orchestration with explicit planner/verifier/worker roles. Same direction as Claude Code's worktree-isolation + parallel agent patterns. For Claudie: the planner/verifier/worker split is a cleaner abstraction than what we currently use in the parallelize skill — worth reviewing whether we should adopt that role taxonomy in our own multi-agent flows (signal digest analysis, deck building review-slides loop, weekly dashboard updates).
