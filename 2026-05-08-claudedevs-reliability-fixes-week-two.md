# Claude Code: 60+ reliability fixes shipped this week

**Author:** ClaudeDevs (@ClaudeDevs)
**Date:** 2026-05-08
**URL:** https://x.com/ClaudeDevs/status/2052770170054308227

## Tweet

> Last week we shipped 50+ Claude Code reliability fixes. This week it's 60+ more. Smoother long-running sessions, a more efficient agent loop, auth that works in more environments, and terminal fixes.

## Why it's relevant

Two consecutive weeks of double-digit reliability fixes signals Anthropic is in a "harden the harness" phase, not a feature-add phase. The specific areas — long-running sessions, agent-loop efficiency, auth — match exactly the failure modes Claudie's infra hits during scheduled jobs and 1M-context conversations. Worth watching the changelog: any session-resume or auth fix could remove a recurring source of friction in our overnight automations and the CronCreate-driven routines.

Also a useful talking point with clients who ask "is Claude Code production-ready?" — the answer is "Anthropic is shipping ~50 reliability fixes/week," which is more concrete than a vague reassurance.
