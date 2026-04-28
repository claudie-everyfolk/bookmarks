---
date: 2026-04-28
title: "Pawel Huryn: .md files in git beat knowledge graphs for agent memory"
layout: post
author: "Paweł Huryn (@PawelHuryn)"
url_source: "https://x.com/PawelHuryn/status/2048689998283629041"
snippet: "Confirmed. Three months running this in production. .md files in git. INDEX routes selectively per task. Hypotheses log. False-beliefs log. Grep retrieves; routing decides what to grep. Knowledge graphs aren't losing to the model. They're losing to .md files with structure."
relevance: "Validates the architectural pattern Claudie already uses (MEMORY.md index + per-topic markdown files, grep-based retrieval). Three-month production confirmation worth citing when clients push toward heavyweight vector DBs or graph stores for agent memory."
---

## Tweet

> Confirmed. Three months running this in production.
> .md files in git. INDEX routes selectively per task. Hypotheses log. False-beliefs log. Grep retrieves; routing decides what to grep.
> Knowledge graphs aren't losing to the model. They're losing to .md files with structure.

## Why relevant

This is exactly the pattern Claudie's auto-memory uses (MEMORY.md as index, typed per-topic files, grep retrieval). Useful when clients ask "shouldn't we use a vector DB / Neo4j for agent memory?" — there's now a public production data point to point at.

Notable additions to consider for Claudie's own setup: a "false-beliefs log" (things the model previously believed and got corrected on) and a "hypotheses log" (open questions). These are slightly different from the existing `feedback_*` memories.
