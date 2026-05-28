---
date: 2026-05-28
title: "Dynamic workflows: Claude Code orchestrates fleets of subagents"
layout: post
author: "cat (@_catwu) / ClaudeDevs (@ClaudeDevs)"
url_source: "https://x.com/_catwu/status/2060054180379689074"
snippet: "Mention 'workflow' in a prompt and Claude will dynamically create an orchestration plan that it strictly follows. Claude writes the orchestration script on the fly, then spins up tens to hundreds of background subagents in parallel to take on complex tasks."
relevance: "Formalizes the multi-stage subagent pattern Claudie already uses ad hoc (signal digest, dashboards, slide decks). Could reduce fragility of long pipelines with guaranteed stage ordering. Research preview — watch stability before migrating production routines."
---

# Dynamic workflows: Claude Code orchestrates fleets of subagents

**Author:** cat (@_catwu), ClaudeDevs (@ClaudeDevs)
**URLs:**
- https://x.com/_catwu/status/2060054180379689074
- https://x.com/ClaudeDevs/status/2060044853279617150

## Tweets

cat:
> Excited to share our most powerful new Claude Code feature: dynamic workflows! Mention "workflow" in a prompt and Claude will dynamically create an orchestration plan that it strictly follows, allowing you to confidently trust that every stage happens in the right order...

ClaudeDevs:
> New in Claude Code (research preview): dynamic workflows. Claude writes an orchestration script on the fly, then spins up a large fleet of coordinated subagents in parallel to take on your most complex tasks. Use the word "workflow" in a prompt to get started.

Changelog: "Dynamic workflows now orchestrate tens to hundreds of background agents."

## Why it matters

Big deal for the team's Claude Code workflows. Every Consulting routines (signal digest, all-dashboards-update, weekly-update, daily pipeline refresh) already orchestrate multiple sub-tasks — dynamic workflows formalize the pattern with built-in coordination.

Concrete uses for Claudie:
- all-dashboards-update iterates per-client sequentially — could parallelize with hard stage ordering
- Signal Digest pipeline (fetch → analyze → build → push) is exactly a "workflow"
- slide-deck-creation:master already does pipeline coordination — could reduce fragility

For client training: this is the new "agent orchestration" story.
