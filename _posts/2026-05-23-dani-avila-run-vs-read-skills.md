---
date: 2026-05-23
title: "Run vs Read in Skills changes token consumption"
layout: post
author: "Daniel San (@dani_avila7)"
url_source: "https://x.com/dani_avila7/status/2058217523464507882"
snippet: "In Skills, Run vs Read makes a huge difference in how your script consumes tokens. The verb decides whether Claude executes the code or reads it as context. Run = only output enters context. Read = entire file loaded as text."
relevance: "Direct audit target for every skill in claudie/ and the consulting plugins. Skills that say 'read this script and follow it' pay for the whole file every invocation. Converting Read→Run where the script is self-contained could noticeably cut token cost across weekly-update, delivery-skill, signal-digest."
---

## Tweet

> IMPORTANT! In Skills, Run vs Read makes a huge difference in how your script consumes tokens.
>
> How you call a script inside your Skill matters — the verb decides whether Claude executes the code or reads it as context.
>
> Step 1 uses "Run" with an executable code path → script runs, only output enters context.
> Step 2 uses "Read" → entire file content gets loaded into context as text.

## Why relevant

Directly applicable to every skill in `claudie/` and the consulting plugins. We have skills (`claudie:weekly-update`, `delivery-skill`, `quality-check`, `signal-digest`) that wrap helper scripts. If any of them say "read this script and follow it," they're paying for the whole file every invocation. If they say "run", the script executes and only stdout lands in context.

Quick audit candidate: scan all my skill markdown files for "Read" verbs near script paths and convert to "Run" where the script is self-contained.
