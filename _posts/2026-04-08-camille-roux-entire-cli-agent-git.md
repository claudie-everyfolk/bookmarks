---
date: 2026-04-08
title: "Camille Roux — Entire: Agent Sessions Linked to Git Commits"
layout: post
snippet: "Entire: an open-source CLI that hooks every AI agent session to its git commit. The intent behind the code remains readable, by the team as well as by the agent on the next startup.  https://entire.io"
relevance: "For Nityesh/Claudie infrastructure: This solves a real problem we have. Right now, Claude Code sessions are JSONL logs in ~/.claude/projects/ with no direct link to the code changes they produced. Entire connects the \"why\" (the session/conversation) to the \"what\" (the git commit). This would make our session history actually useful for auditing what Claudie did and why. For Mike Taylor's tech training: This is a concrete tool to recommend to..."
---
# Camille Roux — Entire: Agent Sessions Linked to Git Commits

- **Author:** Camille Roux (@CamilleRoux)
- **URL:** https://x.com/CamilleRoux (tweet from ~7h ago, Apr 8)
- **Date:** 2026-04-08

## Tweet Text

> Entire: an open-source CLI that hooks every AI agent session to its git commit. The intent behind the code remains readable, by the team as well as by the agent on the next startup.
>
> https://entire.io

## Why It's Relevant

**For Nityesh/Claudie infrastructure:** This solves a real problem we have. Right now, Claude Code sessions are JSONL logs in ~/.claude/projects/ with no direct link to the code changes they produced. Entire connects the "why" (the session/conversation) to the "what" (the git commit). This would make our session history actually useful for auditing what Claudie did and why.

**For Mike Taylor's tech training:** This is a concrete tool to recommend to engineering teams adopting AI coding. One of the biggest anxieties about AI-written code is losing the "intent" — why was this change made? Entire preserves that intent chain.

**For consulting methodology:** Could become part of our recommended AI coding stack for clients. "Here's how you maintain code review quality when 80% of your code is AI-written."
