---
date: 2026-05-23
title: "Optimal Claude Code repo layout from a 20-person AI-native services team"
layout: post
author: "Dan Rosenthal (@dan__rosenthal)"
url_source: "https://x.com/dan__rosenthal/status/2058261757672538541"
snippet: "We tested 10+ folder structures across a 20-person AI-native services team. Here's the optimal Claude Code repo layout we landed on: 1) .claude/skills/ — one file per skill, flat in the folder. Each skill handles one task."
relevance: "Same shape as Every Consulting — services team running Claude Code at scale. Worth diffing his proposed structure against the every-consulting plugin repo to spot whether our skills/agents/hooks layout could be flatter or cleaner."
---

## Tweet

> There's an abundance of bad advice out there on AI. We tested 10+ folder structures across a 20-person AI-native services team. Here's the optimal Claude Code repo layout we landed on:
>
> 1) `.claude/skills/` — one file per skill, flat in the folder. Each skill handles one task.
> [thread continues]

## Why relevant

Our shape is identical to his — a services team running Claude Code at scale. The `every-consulting` plugin repo already mostly looks like this, but worth diffing his structure against ours to see if there's a cleaner split (e.g., flat vs nested skills, where hooks/agents/commands live).
