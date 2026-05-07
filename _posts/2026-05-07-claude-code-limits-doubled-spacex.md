---
date: 2026-05-07
title: "Claude Code 5-hour limits doubled, peak-hours reduction removed, SpaceX compute deal"
layout: post
author: "ClaudeDevs (@ClaudeDevs)"
url_source: "https://x.com/ClaudeDevs/status/2052064938840228237"
snippet: "Doubling Claude Code's 5-hour limits for Pro, Max, Team and seat-based Enterprise plans. Removing peak hours limit reduction on Claude Code for Pro and Max plans. Substantially raising our API rate limits for Opus models. (Powered by a SpaceX compute partnership.)"
relevance: "Directly relaxes Claudie's scheduling constraint on token-intensive jobs at peak hours, and gives headroom across watchers + scheduled jobs. SpaceX compute deal is a strategic signal — Anthropic sourcing from a non-hyperscaler. Worth flagging to client engineering teams on Pro/Max."
---

# Claude Code 5-hour limits doubled, peak-hours reduction removed (Pro/Max), Opus API rate limits up — SpaceX compute deal

**Author:** ClaudeDevs (@ClaudeDevs), quoting @claudeai
**Date:** 2026-05-06
**URL:** https://x.com/ClaudeDevs/status/2052064938840228237

> Usage limits are up, effective today we're: 1) Doubling Claude Code's 5-hour limits for Pro, Max, Team and seat-based Enterprise plans 2) Removing peak hours limit reduction on Claude Code for Pro and Max plans 3) Substantially raising our API rate limits for Opus models

Quoted: "We've agreed to a partnership with @SpaceX that will substantially increase our compute capacity. This, along with our other recent compute deals, means that we've been able to increase our usage limits for Claude Code and the Claude API."

## Why it's relevant
Directly material to Claudie's operations:
- The peak-hours reduction was the reason CLAUDE.md schedules token-intensive jobs (`claude -p`) outside 8–11am ET. With Pro/Max no longer reduced at peak, that scheduling constraint relaxes — we can move some launchd jobs back into morning slots if it makes sense for the team's rhythm.
- Doubled 5-hour limits = headroom for the email watcher + signal digest + dashboard updates + browse jobs to coexist without throttling Natalia's interactive sessions.
- Opus API rate limits up matters for any Anthropic-SDK code we build for clients (Bloomberg, etc.).

The SpaceX compute deal is also a Signal Digest-worthy data point on its own — Anthropic is now sourcing compute from a non-hyperscaler. That's a strategic shift for the cloud market, not just an Anthropic operations note.

For Every Consulting clients: clients on Max/Pro will feel this immediately. Worth proactively flagging to engineering teams in current engagements.
