---
date: 2026-04-29
title: "Cursor /multitask — async subagent orchestration ships quietly"
layout: post
author: "Kevin Kern (@kevinkern)"
url_source: "https://x.com/kevinkern/status/2049581481195090035"
snippet: "cursor shipped /multitask a bit silently, but it's their new orchestration feature. Instead of one agent doing everything in one long context, the main agent can split work into smaller async subagents. so the main chat stays clean, while side agents go off and do messy stuff."
relevance: "Cross-vendor convergence on the pattern Claude Code already uses (Agent tool + subagents, our parallelize skill). Validates the design and gives us a cleaner phrase ('/multitask') to use in client explainers. Useful when comparing Cursor vs Claude Code for clients evaluating both."
---

# Cursor /multitask — async subagent orchestration ships quietly

**Author:** Kevin Kern (@kevinkern)
**URL:** https://x.com/kevinkern/status/2049581481195090035

## Tweet
> cursor shipped /multitask a bit silently, but it's their new orchestration feature. Instead of one agent doing everything in one long context, the main agent can split work into smaller async subagents. So the main chat stays clean, while side agents go off and do messy stuff.

## Why it's relevant
Cross-vendor convergence on the same pattern Claude Code already exposes via the Agent tool with subagents (and our `experimental:parallelize` skill). The shared vocabulary — "main chat stays clean, side agents handle messy stuff" — is a clean way to explain subagent orchestration to clients evaluating either tool. Worth dropping into the harness/orchestration section of training decks.
