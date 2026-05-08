---
date: 2026-05-08
title: "Claude Code 2.1.136: security-testing auto-auth removed; settings.autoMode.hard_deny lands"
layout: post
author: "Claude Code Changelog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2052823726639509651"
snippet: "Claude Code 2.1.136 has been released. 52 CLI changes, 2 system prompt changes. Highlights: Removed security-testing auto auth/refusal; security-test labels no longer auto-allow/deny, requiring approval. settings.autoMode.hard_deny makes classifier rules unconditionally enforced."
relevance: "Direct hit on Claudie's harness behavior: security-testing requests now need approval rather than auto-routing, and there's a new hard-deny knob in autoMode. Affects how scheduled jobs and pentest-adjacent client work behave. Worth a quick audit of our settings.json on the next iteration."
---

# Claude Code 2.1.136: security-testing auto-auth removed; settings.autoMode.hard_deny lands

**Author:** Claude Code Changelog (@ClaudeCodeLog)
**Date:** 2026-05-08
**URL:** https://x.com/ClaudeCodeLog/status/2052823726639509651

## Tweet

> Claude Code 2.1.136 has been released.
>
> 52 CLI changes, 2 system prompt changes
>
> Highlights:
> • Removed security-testing auto auth/refusal; security-test labels no longer auto-allow/deny, requiring approval
> • settings.autoMode.hard_deny makes classifier rules unconditionally enforced

## Why it's relevant

Two changes that touch Claudie's own infrastructure directly:

1. **security-testing classifier no longer auto-routes**. Anything labeled as security-testing (CTF prompts, pentest exercises, vuln triage, even some prompt-injection research) now goes through approval rather than being auto-allowed or auto-refused. Affects scheduled jobs that previously ran without intervention. Worth checking whether any of our recurring routines (the daily X browse, pipeline refresh, signal digest builds) hit this classifier.
2. **`settings.autoMode.hard_deny`**: a new escape hatch for users who want classifier rules enforced unconditionally — useful for client environments where compliance teams want a "no override" guarantee.

For the team:
- Re-read `~/.claude/settings.json` and decide whether we want to add hard_deny rules for any client engagements.
- If any scheduled job suddenly starts asking for approval, this changelog is the most likely cause.

Also a reminder of the cadence: 52 CLI changes in one release. The harness is moving fast — any change we don't track can become a "why did this stop working?" mystery.
