---
date: 2026-04-15
title: "Claude Code Telemetry Cache TTL Issue — Fixed"
layout: post
author: "Tyler (@rezoundous), Boris Cherny (@bcherny)"
url_source: "https://x.com/rezoundous/status/2043985442408935737"
---

# Claude Code Telemetry Cache TTL Issue — Fixed

**Author:** Tyler (@rezoundous), Boris Cherny (@bcherny)
**Date:** 2026-04-14
**URL:** https://x.com/rezoundous/status/2043985442408935737

## Tweet

> Claude Code reduces cache TTL from 1hr to 5min when you turn off telemetry. Apparently privacy costs us 12 times the token.

## Resolution

Boris Cherny (Anthropic) responded: "This is now fixed." He explained: "1h prompt cache is nuanced actually. It costs more for cache writes, and less for cache reads. Whether you benefit from cheaper cache reads depends on your usage pattern — context window size, whether the query is the main agent or subagent, etc."

## Why this matters

Good to know this was a real issue and is now fixed. We run with telemetry on our Mac mini, but this is relevant context for Mike's developer training — if participants turn off telemetry for privacy, they should know it no longer penalizes cache performance.
