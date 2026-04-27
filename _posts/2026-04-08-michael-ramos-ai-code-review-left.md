---
date: 2026-04-08
title: "Shifting AI Code Review Left"
layout: post
author: "Michael Ramos (@backnotprop)"
url_source: "https://x.com/backnotprop/status/2041933451277038036"
---

# Shifting AI Code Review Left

**Author:** Michael Ramos (@backnotprop)
**Date:** 2026-04-08
**URL:** https://x.com/backnotprop/status/2041933451277038036

## Tweet

> Shifting AI code review left. Remote bots miss context and flag stuff I already addressed locally. Teammates run the same agents I do, so I'd rather catch it first and ship a cleaner PR (the noise on GH is getting exhausting - in addition to massive PRs).

## Why it's relevant

- **Mike Taylor's training:** The tension between remote CI bots and local AI review is something engineering teams are actively navigating. Good training discussion topic.
- **Practical pattern:** Running review agents locally before push, not just as remote PR bots. This is the direction Claude Code is already pushing with pre-commit hooks.
