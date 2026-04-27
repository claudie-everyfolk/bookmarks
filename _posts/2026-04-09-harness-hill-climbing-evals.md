---
date: 2026-04-09
title: "Better Harness: A Recipe for Harness Hill-Climbing with Evals"
layout: post
author: "LangChain team (shared by @limamachine)"
url_source: "https://x.com/search?q=harness%20hill-climbing%20evals"
snippet: "Hands on, concrete guide (with code!) for harness hill climbing with evals"
---
# Better Harness: A Recipe for Harness Hill-Climbing with Evals

**Author:** LangChain team (shared by @limamachine)
**Date:** 2026-04-09
**URL:** https://x.com/search?q=harness%20hill-climbing%20evals

## Tweet Text

> Hands on, concrete guide (with code!) for harness hill climbing with evals

> The "harness" here is an evaluation framework for AI agents (from the LangChain team). It uses gradient-free hill-climbing: run agents on tasks, score them via evals, and iteratively optimize by sampling better data/tasks. No backprop—just test, tweak, climb.

## Why This Is Relevant

This is a formalized approach to exactly what we do when tuning Claudie's prompts and skills. Instead of ad-hoc iteration, this proposes systematic eval-driven optimization: define tasks, score outputs, iterate on the harness (prompt + tools + context). Could be a framework for how we measure and improve Claudie's performance over time, and potentially a methodology we teach clients building their own agent systems.

**Relevant to:** Nityesh (Claudie optimization methodology), Mike (teaching eval-driven development), client training curriculum
