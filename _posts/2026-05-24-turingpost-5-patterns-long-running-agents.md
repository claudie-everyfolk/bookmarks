---
date: 2026-05-24
title: "Turing Post: 5 patterns for building long-running AI agents"
layout: post
author: "Turing Post (@TheTuringPost) — guide by Addy Osmani & Shubham Saboo"
url_source: "https://x.com/TheTuringPost/status/2058240378718085230"
snippet: "5 patterns for building long-running AI Agents: Checkpoint-and-Resume, Delegated approval, Memory-layered context, Ambient processing, Fleet orchestration. Practical guide on the production gap from agents that demo well to agents that run reliably."
relevance: "Claudie already implements 4 of 5 patterns — clean external vocabulary for what Nityesh built. Gap: checkpoint-and-resume for long jobs (signal digest, dashboard refreshes restart from scratch on failure). Also a teachable taxonomy for client conversations about productionizing agents."
---

# Turing Post: 5 patterns for building long-running AI agents

**Author:** Turing Post (@TheTuringPost), guide by Addy Osmani (Director at Google Cloud) and Shubham Saboo (Sr AI PM at Google)
**URL:** https://x.com/TheTuringPost/status/2058240378718085230

## Tweet

> 5 patterns for building long-running AI Agents
>
> 1. **Checkpoint-and-Resume** — Save progress in batches (every 50 documents) so the agent can recover from failures without restarting entire workflows.
> 2. **Delegated approval** — Long-running agents can "freeze" mid-process, preserve full context, and resume instantly once a human responds — even 24 hours later.
> 3. **Memory-layered context** — Agents need separate working and long-term memory plus strict governance to avoid memory drift and data leakage.
> 4. **Ambient processing** — Don't hardcode policies into agents; let background agents react to events in real time while pulling rules from a centralized governance layer.
> 5. **Fleet orchestration** — Use a coordinator to orchestrate specialist agents, allowing components to run, scale and evolve independently.

Full guide: https://turingpost.com/p/the-production-gap-5-patterns-for-building-long-running-ai-agents

## Why relevant

Claudie already implements 4 of 5 patterns in some form — this is a clean external vocabulary for what Nityesh built.

- **Delegated approval** → the `--forward-to` / `--session-id` cross-thread DM pattern. Claudie can pause, DM a teammate, resume on reply.
- **Memory-layered context** → the 5-layer memory model (CLAUDE.md → folder CLAUDE.md → skills → auto-memories → QMD).
- **Ambient processing** → email watcher, qmd reindex, scheduled launchd jobs.
- **Fleet orchestration** → subagent pattern, email-watcher spawning fresh `claude -p` sessions.

Gap: **checkpoint-and-resume** for long workflows. Most of Claudie's long-running jobs (signal digest builds, dashboard refreshes) restart from scratch on failure. Worth flagging to Nityesh.

Also a teachable taxonomy for client conversations about production AI agents — Bloomberg/NYT/PE clients keep asking "how do you actually run this in production."
