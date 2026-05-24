---
date: 2026-05-24
title: "Gregor Zunic: Browser Harness reverse-engineered LinkedIn's API on its own"
layout: post
author: "Gregor Zunic (@gregpr07)"
url_source: "https://x.com/gregpr07/status/2058255904131486196"
snippet: "Browser Harness is unreal. Told it to pull every profile viewer from the last year into a CSV. Realized scrolling would take forever, started reverse engineering the LinkedIn API, wrote a script to call it directly, handed me a clean CSV. I didn't tell it how — harness figured out the smart path itself."
relevance: "Direct analogue to Claudie's dev-browser work — same CDP-driven Chrome approach but with stronger 'stop scrolling, script the API' instinct. Pattern worth baking into Claudie's dev-browser skill, and a great live demo for Mike's tech vertical bootcamps."
---

# Gregor Zunic: Browser Harness reverse-engineered LinkedIn's API on its own

**Author:** Gregor Zunic (@gregpr07)
**URL:** https://x.com/gregpr07/status/2058255904131486196

## Tweet

> Browser Harness is unreal. Told it to pull every profile viewer from the last year into a CSV. What it did on its own:
>
> > realized scrolling would take forever
> > started reverse engineering the LinkedIn API
> > wrote a script to call it directly
> > handed me a clean CSV of everyone who viewed my profile
>
> I didn't tell it how. Harness figured out the smart path itself

## Why relevant

Direct analogue to Claudie's `dev-browser` — same idea (drive a real Chrome via CDP) but with stronger autonomous reasoning about when to stop browsing and start scripting an API call. Claudie's current X.com browsing scrolls the DOM; if it hit a 10K-tweet backfill it would just keep scrolling.

Two uses:

1. **Claudie's own browsing jobs** could benefit from an "if scrolling is slow, look at the network tab" instinct. Worth baking into the dev-browser skill.
2. **Mike's tech vertical bootcamps** — perfect live demo of what "agent figures out the smart path" actually looks like in practice. Better story than another todo-app demo.
