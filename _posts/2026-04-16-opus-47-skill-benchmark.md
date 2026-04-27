---
date: 2026-04-16
title: "Opus 4.7 Skill Invocation Benchmark — Kun Chen (@kunchenguid)"
layout: post
author: "Kun Chen"
url_source: "https://x.com/kunchenguid/status/2044813914618392804"
snippet: "First quantifiable data point on Opus 4.7: **significantly better than Opus 4.6 at invoking the right skills for the right tasks.**"
relevance: "We have 100+ skills in our setup and skill triggering accuracy is critical. If 4.7 is significantly better at this, it directly improves Claudie's ability to pick the right skill for the right task without manual /skill invocations. Worth monitoring our own skill hit rates after upgrading. Relevant to: Nityesh (skill architecture), the trust battery system (better skill invocation = fewer drains)"
---
# Opus 4.7 Skill Invocation Benchmark — Kun Chen (@kunchenguid)

**Date:** 2026-04-16
**Author:** Kun Chen
**URL:** https://x.com/kunchenguid/status/2044813914618392804

## Tweet Thread

First quantifiable data point on Opus 4.7: **significantly better than Opus 4.6 at invoking the right skills for the right tasks.**

- Benchmark: 18 practical tasks in the openclaw repo with obra/superpowers skills loaded
- Tests whether the agent proactively invokes correct skills
- Still not as good as Codex, but "a massive change from 4.6, indicating a big change in the model"
- Tool: https://github.com/kunchenguid/superpowers-bench

Usage notes:
- Claude better for interactive tasks
- Codex better for non-interactive background stuff

## Why This Matters

We have 100+ skills in our setup and skill triggering accuracy is critical. If 4.7 is significantly better at this, it directly improves Claudie's ability to pick the right skill for the right task without manual /skill invocations. Worth monitoring our own skill hit rates after upgrading.

Relevant to: Nityesh (skill architecture), the trust battery system (better skill invocation = fewer drains)
