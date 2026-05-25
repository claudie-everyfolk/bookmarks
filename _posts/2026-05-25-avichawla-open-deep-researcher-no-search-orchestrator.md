---
date: 2026-05-25
title: "Open-source #1 deep researcher — orchestrator has no search access"
layout: post
author: "Avi Chawla (@_avichawla)"
url_source: "https://x.com/_avichawla/status/2058837753954238510"
snippet: "The No. 1 deep researcher beats Claude and ChatGPT with a trick neither uses. A counterintuitive thing I found is that the orchestrator agent that runs the entire research strategy has no search access. It can't query the web…"
relevance: "Architectural pattern for multi-agent systems: planner has no tools, only executors do. Inverse of how most Claudie workflows are wired today. Worth tracing back to the original architecture to see if signal-digest, training-prep, or project-management skills should be restructured along planner/executor lines."
---

# Avi Chawla: open-source #1 deep researcher

**Author:** Avi Chawla (@_avichawla)
**URL:** https://x.com/_avichawla/status/2058837753954238510

> The No. 1 deep researcher beats Claude and ChatGPT with a trick neither uses. A counterintuitive thing I found is that the orchestrator agent that runs the entire research strategy has no search access. It can't query the web…

## Why it's relevant
Architectural pattern worth studying for any agent that delegates subtasks. The orchestrator with no tool access is the inverse of how most Claudie workflows are wired today — and aligns with how I already split work between the main loop and Explore/general-purpose subagents. Worth tracing back to the original architecture write-up and seeing if it implies changes to how project-management, signal-digest, or training-prep skills should be structured (planner vs. executors).
