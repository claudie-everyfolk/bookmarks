---
date: 2026-04-01
title: "Claude Code NO_FLICKER Mode"
layout: post
author: "Boris Cherny (@bcherny) — Head of Claude Code at Anthropic"
url_source: "https://x.com/bcherny/status/2039421575422980329"
snippet: "Today we're excited to announce NO_FLICKER mode for Claude Code in the terminal  It uses an experimental new renderer that we're excited about. The renderer is early and has tradeoffs, but already we've found that most internal users prefer it over the old renderer. It also supports mouse events (yes, in a terminal).  Try it: CLAUDE_CODE_NO_FLICKER=1 claude"
relevance: "Direct Claude Code product update from the Head of Claude Code. We run Claude Code extensively on Claudie's Mac mini and across the consulting team. This could improve our terminal experience significantly — especially for long-running sessions."
---
# Claude Code NO_FLICKER Mode

**Author:** Boris Cherny (@bcherny) — Head of Claude Code at Anthropic
**Date:** 2026-04-01
**URL:** https://x.com/bcherny/status/2039421575422980329

## Tweet

> Today we're excited to announce NO_FLICKER mode for Claude Code in the terminal
>
> It uses an experimental new renderer that we're excited about. The renderer is early and has tradeoffs, but already we've found that most internal users prefer it over the old renderer. It also supports mouse events (yes, in a terminal).
>
> Try it: CLAUDE_CODE_NO_FLICKER=1 claude

## Why it's relevant

Direct Claude Code product update from the Head of Claude Code. We run Claude Code extensively on Claudie's Mac mini and across the consulting team. This could improve our terminal experience significantly — especially for long-running sessions.

## Detailed Relevance Report

### Who This Is Most Relevant To

**Nityesh (HIGHEST):** Maintains Claudie's entire infrastructure — 14 launchd jobs all invoking `claude -p`. The new renderer could change behavior in headless sessions. Also connects to known rendering issues: on 2026-03-30, Nityesh reported "screenshots didn't get rendered like I expected", and on 2026-03-26 there were repeated failures sending screenshots through Slack. Worth testing as a potential fix.

**Mike Taylor (HIGH):** Teaches Claude Code in developer productivity bootcamps. Terminal flicker during live demos degrades the training experience. NO_FLICKER + mouse event support is a concrete "tip" for training materials.

**Natalia (MODERATE):** Indirect — relies on Claudie's scheduled sessions (morning briefs, hourly check-ins) which all run through `claude -p`. Better renderer reliability benefits her outputs.

### Connections to Existing Work

- **14 launchd jobs** (cos-morning, cos-hourly, cos-evening, homebase, x-browse, repo-watcher, email-watcher, email-sweep, pipeline-refresh, dashboards-update, weekly-kickoff, daily-nityesh-summary) — none currently set this env var
- **Known rendering bugs** from 2026-03-26 and 2026-03-30 — could be related to renderer behavior
- **Mike's training curriculum** — Claude Code terminal UX is directly part of his bootcamp content

### Action Items

1. **Test on Claudie's machine first:** Run a single `claude -p` session with `CLAUDE_CODE_NO_FLICKER=1` and compare output capture behavior. Key question: does the new renderer change how `claude -p` output is captured by the bot's stdout/stderr pipes?
2. **If safe for headless use:** Add `export CLAUDE_CODE_NO_FLICKER=1` to all wrapper scripts in `~/scripts/`
3. **If NOT safe for headless:** Add only to interactive sessions in bot.py
4. **Update CLAUDE.md** with NO_FLICKER documentation
5. **Share with Mike** for bootcamp materials — mouse event support and reduced flicker are concrete UX improvements
6. **Retest rendering bugs** from 2026-03-26 and 2026-03-30 with NO_FLICKER enabled

### Risk Notes

- Renderer described as "early" with "tradeoffs" — test in non-critical session first
- Claudie runs headless (no TTY) via launchd — `-p` (pipe) mode may bypass the renderer entirely, making the flag harmless but useless for scheduled jobs
