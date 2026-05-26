---
date: 2026-05-25
title: "GitHub-labels as agent triggers"
layout: post
author: "Matt Pocock (@mattpocockuk)"
url_source: "https://x.com/mattpocockuk/status/2059008544477757887"
snippet: "Playing with a GitHub labels-based approach to spinning up agents. Add a label, trigger an action. agent:implement, agent:update-branch, agent:review, agent:to-issues, etc. Tried this 6 months ago but I didn't like it. Pure skill issue on my part, it actually rocks."
relevance: "Lightweight pattern for routing work to agents without a custom UI — useful for the every-consulting GitHub repo where Nityesh currently lands skill PRs by hand. Labels like agent:review or agent:update-branch could automate the cycle. Cheap to prototype."
---

# GitHub-labels as agent triggers

**Author:** Matt Pocock (@mattpocockuk)
**URL:** https://x.com/mattpocockuk/status/2059008544477757887
**Date:** 2026-05-25

## Tweet

> Playing with a GitHub labels-based approach to spinning up agents.
>
> Add a label, trigger an action.
>
> `agent:implement`, `agent:update-branch`, `agent:review`, `agent:to-issues`, etc.
>
> Tried this 6 months ago but I didn't like it. Pure skill issue on my part, it actually rocks.

## Why it's relevant

The `every-consulting` plugin repo and Claudie's own infra repos currently rely on Nityesh manually shepherding PRs. Labels-as-triggers is a cheap pattern to automate routine actions (review, branch-update, issue-grooming) without building a UI. Worth prototyping on one repo to see how it feels.
