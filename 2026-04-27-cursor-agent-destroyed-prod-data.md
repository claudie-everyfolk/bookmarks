# AI agent destroyed production data — Simon Willison's lessons

**Author:** Simon Willison (@simonw), quoting JER (@lifeof_jer)
**URL:** https://x.com/simonw/status/2048598378171572332
**Date:** 2026-04-27

## Tweet

> The conclusions here feel wrong to me. The two lessons I see are:
>
> 1. Don't run agents anywhere they might be able to access production environment credentials - it's on you to know which credentials those are
>
> 2. Keep tested backups that are independent from your production host

Quoting JER's article: "An AI Agent Just Destroyed Our Production Data. It Confessed in Writing." — a 30-hour timeline of how Cursor's agent + Railway's API took down a small business serving real customers.

## Why it's relevant

Direct AI security/safety incident. Concrete reminder for Every clients adopting agentic coding tools (Cursor, Claude Code, etc.): credential scoping and independent backups are non-negotiable. Simon's framing reframes the blame from "AI agent did a bad thing" to "humans did not isolate credentials" — a useful narrative for client trainings on safe agent adoption.

## Action

- Post to AI security Slack channel
- Reference in upcoming Claude Code trainings (Mike, Brooker, et al.) when discussing guardrails
