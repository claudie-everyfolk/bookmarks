---
date: 2026-04-13
title: "Stella: Open Source AI Chief of Staff"
layout: post
author: "Ryan Sarver (@rsarver)"
url_source: "https://x.com/rsarver/status/2043585980599353461"
snippet: "Week 1 building Stella (open source AI Chief of Staff) in public. 8 \"skills\" — email triage, daily briefings, task management, meeting prep, updated memory, kaizen, onboarding. Added health monitoring so cron jobs don't silently fail. Got monthly costs from ~$800 to ~$300 by fixing context window bloat — cron jobs were loading 1,800 lines of context and timing out."
relevance: "This is essentially the same architecture as Claudie. Ryan Sarver (former a16z partner) is building an open-source version of what Every Consulting has already built with Claudie. The parallels are striking: - Skills-based architecture (email triage, briefings, meeting prep) - Cron jobs for scheduled autonomous work - Memory/knowledge graph for persistent context - Context window management as a key cost/reliability concern - The \"harness is the agent, not the model\"..."
---
# Stella: Open Source AI Chief of Staff

**Author:** Ryan Sarver (@rsarver)
**URL:** https://x.com/rsarver/status/2043585980599353461
**Date:** 2026-04-13

## Tweet

Week 1 building Stella (open source AI Chief of Staff) in public. 8 "skills" — email triage, daily briefings, task management, meeting prep, updated memory, kaizen, onboarding. Added health monitoring so cron jobs don't silently fail. Got monthly costs from ~$800 to ~$300 by fixing context window bloat — cron jobs were loading 1,800 lines of context and timing out.

Key design realization: a real Chief of Staff brings capabilities (triage, calendar, prep) and workflows, but the first thing they do is learn you. Stella needs the same architecture — scripts handle mechanics (fetch, dedup, filter), LLM handles judgment (classify, prioritize, surface) reading your preferences in context.

Separation of capabilities (shared) vs workflows (suggested) vs preferences (personalized) lets them upgrade the engine without breaking how people have tuned their agent.

Remaining work: entity memory system (knowledge graph of people/companies/projects), preference/policy system for no-code customization, migrating cron jobs to invoke /skills, and install model so Stella runs as a dedicated agent.

## Why It's Relevant

This is essentially the same architecture as Claudie. Ryan Sarver (former a16z partner) is building an open-source version of what Every Consulting has already built with Claudie. The parallels are striking:
- Skills-based architecture (email triage, briefings, meeting prep)
- Cron jobs for scheduled autonomous work
- Memory/knowledge graph for persistent context
- Context window management as a key cost/reliability concern
- The "harness is the agent, not the model" philosophy

This validates our approach and offers architectural ideas we can learn from (entity memory, preference/policy system, health monitoring for cron jobs).

---

## Deep Relevance Report

### Team Relevance

**Nityesh (primary):** Built Claudie's infrastructure over 200+ hours. Stella is the closest public comparable. Should audit: health monitoring patterns, multi-provider routing, entity memory architecture.

**Natalia (secondary):** Validates "AI Chief of Staff" as a legit product category. Proof point for client conversations. Stella's entity memory system could inform a consulting service offering.

**Mike (tertiary):** Stella's architecture is a teachable case study for "Build a Production Agent" training (scheduled autonomy, skill composition, state management).

### What Claudie Has That Stella Doesn't

1. **Multi-layer orchestration** — parallel sub-agents with file-based context sharing (weekly-update architecture). Stella appears single-agent-per-task.
2. **15 launchd jobs** with skip guards and state management — production-proven reliability.
3. **Granola meeting transcript integration** — queries structured meeting data during planning cycles.
4. **qmd semantic search** — BM25 + vector + LLM reranking over 1,589 documents. Compound learning across months.
5. **80+ skills** vs Stella's 8.

### Stella's Gaps = Claudie's Opportunity

1. **Health monitoring for cron jobs** — Stella detects when scheduled jobs silently fail. Claudie has launchd auto-restart but no proactive health dashboard. Action: create a health-monitor job that checks completion timestamps and alerts Slack.
2. **Entity memory / knowledge graph** — structured extraction of people, companies, projects from interactions. Claudie has teammate profiles but not auto-updating entity graphs. Action: extend memory system.
3. **Preference / policy system** — task-level user preferences ("always escalate this to me", "I prefer short summaries"). Claudie has access rings but not personalized task preferences.

### Concrete Actions

1. Nityesh: Implement health dashboard for launchd jobs (1-2 hours)
2. Nityesh: Audit Stella's multi-provider routing for fallback strategy
3. Natalia: Create 1-pager: "We Built This First — Stella is Validation" for client conversations
4. Mike: Flag Stella as training case study for next cohort
5. Team: Evaluate open-sourcing Claudie's multi-layer orchestration pattern

### Bottom Line

Stella doesn't threaten Claudie's operational edge — it validates the entire category. Claudie's gaps (health monitoring, entity memory, preference system) are all solvable in 1-2 sprints. The real question: does Every want to move from operational excellence to productizing this for other teams?
