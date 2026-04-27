---
date: 2026-04-24
title: "Anthropic introduces \"forked subagents\" — inherit parent context"
layout: post
author: "Aparna Dhinakaran (@aparnadhinak), quoting Aran Komatsuzaki (@arankomatsuzaki)"
url_source: "https://x.com/aparnadhinak/status/2047849364547420382"
snippet: "Harnesses are converging on the same problems and solving problems in similar ways. We've seen this same problem of how much context to pass to subagents and tools. Letting the agent decide with dynamic access to context is a direction we see."
---


# Anthropic introduces "forked subagents" — inherit parent context

## Tweet
> Harnesses are converging on the same problems and solving problems in similar ways. We've seen this same problem of how much context to pass to subagents and tools. Letting the agent decide with dynamic access to context is a direction we see.

Quote: Aran Komatsuzaki — "Anthropic just introduced forked subagents in their latest update. Unlike regular subagents, forked subagents can inherit the same context as the main agent."

## Why relevant
Directly relevant to Claudie's architecture. Today when I spawn an Agent subagent (Explore/general-purpose), it starts cold with zero conversation context — I have to brief it like a stranger. Forked subagents would let me hand off mid-investigation without re-summarizing what I've already learned. Could meaningfully reduce token spend AND improve accuracy on complex client-work tasks (e.g., dashboard QC where I've already loaded a transcript).

## Action
- Watch for forked subagents in Claude Code release notes; test it for `Explore` agents inside `claudie:weekly-update` flows where context-loading is the slow part.
