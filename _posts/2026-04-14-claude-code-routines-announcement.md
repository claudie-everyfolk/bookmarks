---
date: 2026-04-14
title: "Claude Code Routines — Now in Research Preview"
layout: post
author: "Claude (@claudeai)"
url_source: "https://x.com/claudeai/status/2044095086460309790"
snippet: "Now in research preview: routines in Claude Code.  Configure a routine once (a prompt, a repo, and your connectors), and it can run on a schedule, from an API call, or in response to an event.  Routines run on our web infrastructure, so you don't have to keep your laptop open."
---
# Claude Code Routines — Now in Research Preview

**Author:** Claude (@claudeai)
**Date:** 2026-04-14
**URL:** https://x.com/claudeai/status/2044095086460309790

## Tweet

> Now in research preview: routines in Claude Code.
>
> Configure a routine once (a prompt, a repo, and your connectors), and it can run on a schedule, from an API call, or in response to an event.
>
> Routines run on our web infrastructure, so you don't have to keep your laptop open.

Follow-up tweet:
> Scheduled routines let you give Claude a cadence and walk away. Try telling Claude to pull the top bug from Linear every night at 2am, attempt a fix, and open a draft PR.
>
> If you've been using /schedule in the CLI, those are routines now, and there's nothing to migrate.

## Why This Is Relevant

This is a **key shift** for how Claudie operates. We currently run on a Mac mini with launchd jobs because we need always-on scheduled execution. Claude Code Routines could potentially replace our local infrastructure — running on Anthropic's web infra instead of our Mac mini.

**Direct implications:**
- Our `/schedule` commands and launchd jobs could migrate to Routines
- Removes the dependency on the Mac mini being always-on for scheduled tasks
- BUT: increases our dependency on Anthropic's platform (connects to our Claude Max platform risk concern)
- The "from an API call, or in response to an event" part is significant — event-driven Claudie tasks become possible without our custom email watcher / webhook infrastructure

**Trade-offs to consider:**
- More reliable execution (Anthropic's infra vs our single Mac mini)
- Less control over environment, tools, and credentials
- Potential rate limit / usage concerns for heavy routines
- Need to understand what "connectors" are available vs what we have locally (gws, dev-browser, Slack bot, etc.)

## Detailed Relevance Report

### Claudie's Current Scheduling Infrastructure

Claudie runs **17 scheduled jobs** via launchd on the Mac mini. Key jobs include:
- **cos-hourly/morning/evening**: AI-driven check-ins and briefings (10+ runs/day)
- **x-browse**: 4x daily X.com signal collection (requires Chrome CDP)
- **dashboards-update, pipeline-refresh, sales-data-checkin**: Client data sync via Google Sheets
- **daily-diary**: 10 PM nightly introspective reflection
- **qmd-reindex**: Every 3 hours, local search engine maintenance
- **email-watcher/email-sweep**: Continuous email monitoring
- **weekly-kickoff**: Weekly team kickoff generation

### What Could Migrate to Routines
- **weekly-kickoff**: Pure LLM work generating Slack messages
- **trust-battery tasks**: Analysis-only work
- **dashboards-update, pipeline-refresh**: Heavy GWS usage but no local tool dependency

### What CANNOT Migrate
- **x-browse**: Requires dev-browser (authenticated Chrome CDP) — local machine only
- **qmd-reindex**: Requires local qmd CLI, Python scripts, Granola transcript downloads
- **cos-hourly/morning/evening**: Depend on local file system state
- **email-watcher/sweep**: Requires persistent background process monitoring Gmail push notifications

### Platform Risk
CLAUDE.md explicitly warns: "Never use the `/schedule` skill (remote triggers) — since you run locally on your own machine, always default to local launchd jobs." Our local-first architecture provides:
1. Independence from Anthropic API availability/pricing changes
2. Cost control (avoids per-run API charges for 4x daily browsing + hourly check-ins)
3. Data privacy (client dashboards, transcripts, team dynamics stay local)
4. Reliable sub-second response for critical jobs

### Recommendation
**Maintain local-first architecture.** Consider Routines only as a supplement for 2-3 GWS-heavy jobs (dashboards-update, weekly-kickoff) IF Anthropic stabilizes pricing and adds better logging. The team invested 200+ hours making this system reliable — trading that for Anthropic's infrastructure volatility is the wrong tradeoff. But worth tracking as the feature matures.
