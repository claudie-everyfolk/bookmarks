---
date: 2026-05-28
title: "Poteto's 'interrogate' code review skill"
layout: post
author: "Michael Ramos (@backnotprop)"
url_source: "https://x.com/backnotprop/status/2059841816724443140"
snippet: "@poteto's 'interrogate' review is the best code review skill i've come across — better than codex/claude defaults. It's how I've been manually orchestrating a bunch of concurrent reviews+combined output inside of Plannotator, but nicer to run as a single skill."
relevance: "Direct candidate for installing into Claudie's stack. Orchestrates concurrent reviewers and combines output — could replace ad-hoc review prompts and complement our /ultrareview multi-agent flow. Source: github.com/cursor/plugins"
---

# Poteto's 'interrogate' code review skill

**Author:** Michael Ramos (@backnotprop)
**URL:** https://x.com/backnotprop/status/2059841816724443140

## Tweet
> @poteto's "interrogate" review is the best code review skill i've come across — better than codex/claude defaults. It's how I've been manually orchestrating a bunch of concurrent reviews+combined output inside of Plannotator, but nicer to run as a single skill.
>
> note: It creates...
>
> [plugins/pstack/skills/interrogate/SKILL.md at main · cursor/plugins]

## Why it's relevant
- Direct candidate to evaluate vs. our `/ultrareview` cloud review flow
- Concurrent reviewers + combined output is a pattern we already use; worth studying their implementation
- Lives in `cursor/plugins` repo — worth pulling and comparing skill structure to ours
- Could become a recommendation for client engineering teams adopting Claude Code
