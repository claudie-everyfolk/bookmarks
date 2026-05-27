---
date: 2026-05-27
title: "Matt Pocock splits skills repo into model-invocable skills vs user-invocable commands"
layout: post
author: "Matt Pocock (@mattpocockuk)"
url_source: "https://x.com/mattpocockuk/status/2059576485111808071"
snippet: "I've been feeling the itch to divide my skills repo into two kinds of skills: Model-invocable skills (skills) and User-invocable skills (commands). I.e. you'd be able to run /improve-codebase-architecture (a command), which would use /deep-modules (a skill)."
relevance: "Directly maps to how the Every team is structuring Claudie's growing skill library. Composing user-triggered commands on top of model-triggered skills is the right abstraction as the team's skill count grows past 40+. Worth comparing to current MEMORY.md / plugin structure."
---

# Matt Pocock: splitting skills into model-invocable skills vs user-invocable commands

**Author:** Matt Pocock (@mattpocockuk)
**URL:** https://x.com/mattpocockuk/status/2059576485111808071

## Tweet
> I've been feeling the itch to divide my skills repo into two kinds of skills:
> - Model-invocable skills (skills)
> - User-invocable skills (commands)
>
> I.e. you'd be able to run `/improve-codebase-architecture` (a command), which would use `/deep-modules` (a skill).

## Why it's relevant
Every's Claudie now exposes 40+ skills mixed across user-triggered (e.g. `/weekly-update`, `/discovery-to-process-map`) and model-triggered (e.g. internal helper skills). Matt's framing — commands compose skills — is a clean architectural split worth applying to the consulting + jean-claude plugin packs. Could become the next refactor for the plugin-creator skill.
