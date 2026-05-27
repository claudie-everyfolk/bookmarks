---
date: 2026-05-27
title: "Claude Code 2.1.152 — /code-review --fix applies findings, disallowed-tools in skill frontmatter"
layout: post
author: "Claude Code Changelog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2059451389701402669"
snippet: "Claude Code 2.1.152 has been released. 33 CLI changes. Highlights: /code-review --fix applies review findings to the working tree, automating fixes and cutting manual edits. Skills/commands can set disallowed-tools in frontmatter to disable tools when active."
relevance: "Directly relevant to Claudie's setup. disallowed-tools in frontmatter is a security primitive Nityesh can use to lock down individual skills (e.g. claudie:* skills shouldn't be touching shell). /code-review --fix is a workflow accelerator worth Mike teaching in tech-vertical trainings."
---

## Tweet

> Claude Code 2.1.152 has been released.
>
> 33 CLI changes
>
> Highlights:
> • /code-review --fix applies review findings to the working tree, automating fixes and cutting manual edits
> • Skills/commands can set disallowed-tools in frontmatter to disable tools when active to prevent...

## Companion: /simplify is back

@dani_avila7 confirmed /simplify is back as an alias for /code-review --fix.
URL: https://x.com/dani_avila7/status/2059460918338097449

## Why it matters
`disallowed-tools` in skill frontmatter pairs perfectly with the "How we contain Claude" findings — narrow the surface per-skill rather than relying on user approval. Nityesh can apply this to the `claudie:*` skill set today.

`/code-review --fix` matters as a teachable workflow for Mike's curriculum — fits the same "agent does the loop, human approves" pattern we already teach.
