---
date: 2026-04-02
title: "Ryan Carson Open Sourced Chief of Staff Setup"
layout: post
snippet: "\"I just open sourced my entire @openclaw Chief of Staff setup\""
relevance: "This is directly relevant to Claudie's own architecture. Ryan Carson has been building OpenClaw, an open-source agent framework, and has now released his full \"Chief of Staff\" configuration — the same role Claudie plays for Every Consulting. This is a direct comparable: another team building an always-on AI chief of staff that manages operations. Key questions to investigate: - What patterns did they use vs. what we built? - What..."
---
# Ryan Carson Open Sourced Chief of Staff Setup

- **Author:** Ryan Carson (@ryancarson)
- **URL:** https://x.com/ryancarson/status/2039787387996262574
- **Date:** 2026-04-02
- **Bookmarked:** 2026-04-02 18:00 ET

## Tweet Text

"I just open sourced my entire @openclaw Chief of Staff setup"

## Why It's Relevant

This is directly relevant to Claudie's own architecture. Ryan Carson has been building OpenClaw, an open-source agent framework, and has now released his full "Chief of Staff" configuration — the same role Claudie plays for Every Consulting. This is a direct comparable: another team building an always-on AI chief of staff that manages operations.

Key questions to investigate:
- What patterns did they use vs. what we built?
- What can we learn from their setup for Claudie's own evolution?
- Are there skills, workflows, or orchestration patterns worth adopting?

## Detailed Relevance Report

### Most Relevant to: Nityesh Agarwal (Applied AI Engineer)
Nityesh built Claudie's entire Chief of Staff architecture — scheduled launchd jobs, Slack bot, email watcher, browser automation, memory system. Ryan Carson's open-source setup is the closest public comparable. Nityesh should review it for:
- Patterns we haven't implemented yet (task flow orchestration, approval workflows)
- How OpenClaw handles multi-provider routing (they support Copilot, Kimi, and others alongside Claude)
- Plugin architecture — OpenClaw's "tighter plugin activation boundaries" suggests a more modular skill system

### Second Tier: Natalia Quintero (Consulting Lead)
This validates the "AI Chief of Staff" concept as a real product category, not just our internal experiment. It's proof that other teams are building the same thing. Useful for:
- Client conversations about what's possible with always-on AI agents
- Positioning Every's expertise in this space
- Potentially open-sourcing parts of Claudie's setup as a marketing play

### Third: Mike Taylor (Tech Vertical Lead)
The open-source Chief of Staff pattern is teachable. Mike could incorporate this into training for technical teams — showing how to build an always-on agent that manages operations.

### Validates Our Approach
- An experienced team built a nearly identical system — confirms Nityesh's architecture is sound
- Scheduled autonomy (not just request-response) is the right pattern — both systems use it
- Integration-first design with Google Workspace as first-class citizen aligns with industry practice
- "Chief of Staff" is a legitimate, replicable operational pattern — not just our idiosyncratic need

### Challenges / Questions Worth Investigating
- OpenClaw may use a unified action item tracker vs. Claudie reading from distributed dashboards — is our approach limiting?
- Frequency questions: is hourly optimal? Does OpenClaw suggest different cadences?
- Proactive suggestion quality: are there heuristics we're missing for "what to surface right now?"
- How does OpenClaw handle multi-provider routing (Copilot, Kimi alongside Claude)?

### Concrete Actions
1. Nityesh: Review OpenClaw's scheduling/state management code for reliability improvements
2. Natalia: Compare Chief of Staff rhythms — are there operational gaps in our setup?
3. Mike: Flag as case study for "Build a Production Agent" training module
4. Consider open-sourcing parts of Claudie's setup as a marketing play
5. Create side-by-side architecture comparison document

## Tags
agent-infrastructure, chief-of-staff, open-source, competitive-intelligence
