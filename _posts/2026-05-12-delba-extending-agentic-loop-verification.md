---
date: 2026-05-12
title: "Extending Claude Code's Agentic Loop — Verification Workflows"
layout: post
author: "Delba Oliveira (@delba_oliveira)"
url_source: "https://x.com/delba_oliveira/status/2054264771306754072"
snippet: "You can extend every step of Claude Code's agentic loop. I've been thinking a lot about what that means for the last one. What are you doing to help Claude verify its own work? Genuinely want to hear what workflows people have."
relevance: "Anthropic DevRel asking publicly about agent self-verification workflows. Directly relevant to Nityesh — we have several gates (pre-commit hooks, simplify skill, review-slides, quality-check). Worth replying privately to with what we've built or reading the thread for ideas. Connects to ultrareview and the deck QC workflow we already enforce."
---

> You can extend every step of Claude Code's agentic loop. I've been thinking a lot about what that means for the last one.
>
> What are you doing to help Claude verify its own work? Genuinely want to hear what workflows people have.

## Why it's relevant

Delba (Anthropic DevRel) is collecting verification-workflow patterns publicly. We already have gates that fit this exactly: the `simplify` skill, `review-slides` for deck QC, `quality-check` for dashboards, ultrareview, pre-commit hooks. Worth reading the replies for ideas, and worth Nityesh writing up what we've built — this is the kind of thread Anthropic blogs about.
