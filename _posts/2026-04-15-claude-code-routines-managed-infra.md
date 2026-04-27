---
date: 2026-04-15
title: "Claude Code Routines: Managed Agent Infrastructure"
layout: post
author: "Camille Roux (@CamilleRoux)"
url_source: "https://x.com/CamilleRoux/status/2044395343022805467"
snippet: "Claude Code Routines: define a prompt once + repositories + connectors, and let it run on Anthropic's infrastructure — triggered by schedule, webhook, or GitHub event, even with laptop closed."
relevance: "This is a direct alternative to our launchd-on-Mac-mini setup. Anthropic is now offering hosted infrastructure for exactly the pattern we built manually — scheduled Claude agents with tool access. Key implications: 1. Platform risk validation — confirms our concern about Anthropic tightening third-party access. They're building the managed version of what we do. 2. Migration path — if our Claude Max approach becomes unsustainable, Routines could be the fallback (or..."
---
# Claude Code Routines: Managed Agent Infrastructure

**Author:** Camille Roux (@CamilleRoux)
**Date:** 2026-04-15
**URL:** https://x.com/CamilleRoux/status/2044395343022805467

## Tweet

> Claude Code Routines: define a prompt once + repositories + connectors, and let it run on Anthropic's infrastructure — triggered by schedule, webhook, or GitHub event, even with laptop closed.

Camille reports running 9 routines on Anthropic's infra overnight, including a morning briefing agent that sends email at 7:30am.

Docs: https://code.claude.com/docs/en/routines

## Why this matters

This is a direct alternative to our launchd-on-Mac-mini setup. Anthropic is now offering hosted infrastructure for exactly the pattern we built manually — scheduled Claude agents with tool access. Key implications:

1. **Platform risk validation** — confirms our concern about Anthropic tightening third-party access. They're building the managed version of what we do.
2. **Migration path** — if our Claude Max approach becomes unsustainable, Routines could be the fallback (or upgrade).
3. **Client relevance** — for clients who want "always-on AI" but can't maintain a Mac mini, this is the answer. Changes our training pitch.
4. **Limitations unknown** — need to understand pricing, tool access scope, whether it supports dev-browser/MCP style integrations we depend on.

## Detailed Relevance Report

**Who this is most relevant to:**

- **Nityesh (critical):** He built and maintains Claudie's entire Mac mini infrastructure — 17 launchd jobs, the Slack bot, email watcher, and all scheduled automation. He would architect any migration or hybrid approach. He also needs to evaluate whether Routines pricing fits within Claude Max or creates a new cost line.
- **Natalia (high):** This changes the client advisory conversation. Finance and enterprise clients will ask "should we use Routines or self-host?" — Natalia needs the answer ready for sales calls and discovery sessions.
- **Mike (medium):** His tech vertical training curriculum should incorporate a "Routines vs Self-Hosted" module. Claudie's own architecture is the perfect case study.

**What existing work/concerns it connects to:**

Claudie has tracked this trajectory across Signal Digest entries #32, #35, #54 and a memory file (`project_claude_max_platform_risk.md`). The through-line: Anthropic is vertically integrating from model provider to execution platform. The April 5 memory flagged Claude Max dependency as an unmitigated risk with four action items — none yet acted on. Peter Yang analysis (#35) warned that `claude -p` programmatic access may be first to get restricted. Routines is the carrot that follows that stick.

**Concrete actions:**

1. Experiment with migrating 2-3 GWS-heavy jobs (dashboards-update, weekly-kickoff) to Routines — these don't need local filesystem or dev-browser access
2. Execute the stalled fallback plan: price out API with prompt caching, evaluate open models for low-stakes tasks
3. Build a "Routines vs Self-Hosted AI Agents" training module for client engagements
4. Track Routines pricing announcements — heavy scheduling may not fit Claude Max

**Assessment: Both threat and opportunity.** Threat because Anthropic normalizing managed agents could precede restricting local `claude -p` usage. Opportunity because Claudie's local-first architecture — with its 17 jobs, authenticated browser, local search engine, and MCP integrations — is exactly what Routines cannot yet replicate.
