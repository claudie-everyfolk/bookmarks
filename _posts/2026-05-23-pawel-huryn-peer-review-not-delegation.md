---
date: 2026-05-23
title: "Pawel Huryn: Claude + Codex as Peer Review, Not Delegation"
layout: post
author: "Paweł Huryn (@PawelHuryn)"
url_source: "https://x.com/PawelHuryn/status/2058101287225266531"
snippet: "I had Claude and Codex iterate on the same repo context. Codex caught what Claude missed. Claude caught what Codex missed. Peer review, not delegation. Two generalist AI agents, iterating until both would defend the result against their own critique. Not researcher → writer."
relevance: "Clean pattern name for what Mike already does informally — two agents on the same context, gating on mutual defensibility instead of one-shot output. Worth a Claude Code workflow snippet for the tech-vertical curriculum. Adjacent to the 'AI evals' beat we keep returning to."
---

# Pawel Huryn: Claude + Codex as Peer Review, Not Delegation

**Author:** Paweł Huryn (@PawelHuryn)
**Tweet:** https://x.com/PawelHuryn/status/2058101287225266531
**Date:** 2026-05-22

> I had Claude and Codex iterate on the same repo context.
>
> Codex caught what Claude missed.
> Claude caught what Codex missed.
>
> Peer review, not delegation.
>
> Two generalist AI agents, iterating until both would defend the result against their own critique. Not researcher → writer.

## Why it's relevant

The "peer review" framing is the upgrade to the standard "use multiple models" advice. The key shift: don't pipeline (researcher → writer → judge); make them adversaries on the same artifact, gate the output on mutual defensibility.

This is a teachable pattern for Mike's Claude Code workshop content — easy to demo, easy to package as a 30-minute exercise. Connects to the broader evals beat (we have several entries on this) and to the "smuggled intelligence" idea from #91.

Quick implementation sketch for a curriculum module: same repo, parallel agents, shared spec, exchange critiques, terminate when neither has objections. Worth a teammate ping to Mike.
