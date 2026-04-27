---
date: 2026-04-27
title: "AI agent destroyed production data — Simon Willison's lessons"
layout: post
author: "Simon Willison (@simonw)"
url_source: "https://x.com/simonw/status/2048598378171572332"
snippet: "The conclusions here feel wrong to me. The two lessons I see are: (1) Don't run agents anywhere they might be able to access production environment credentials — it's on you to know which credentials those are. (2) Keep tested backups that are independent from your production host."
relevance: "Concrete AI safety incident — Cursor agent + Railway API destroyed a small business's prod data. Useful framing for Every client trainings: credential scoping and independent backups are the human responsibility, not the agent's."
---

Simon Willison reframes a viral incident where Cursor's agent destroyed production data over 30 hours. Rather than blaming the model, he points to credential isolation and independent backups as the load-bearing controls. Good talking point for Claude Code / Cursor adoption trainings.
