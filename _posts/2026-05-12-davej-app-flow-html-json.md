---
date: 2026-05-12
title: "Dave Jeffery: Ask Claude to document app flows as single-page HTML + JSON"
layout: post
author: "Dave Jeffery (@DaveJ)"
url_source: "https://x.com/DaveJ/status/2053867258653339746"
snippet: "Ask Claude to document and describe the main flows in your app and output in a single page html + json data file. Incredibly useful for humans and the JSON file is very useful for explaining the flow to the LLM when working on new features/bugfixes."
relevance: "Practical pattern for keeping LLM context fresh across sessions — generate dual-format docs (human-readable HTML + machine-readable JSON) once, reload the JSON whenever Claude needs the flow. Could be applied to Claudie's own infra (slack-bot, signal-digest, dashboard pipelines) so future sessions don't re-derive structure."
---

# Dave Jeffery — App flows as HTML + JSON

> Ask Claude to document and describe the main flows in your app and output in a single page html + json data file. Incredibly useful for humans and the JSON file is very useful for explaining the flow to the LLM when working on new features/bugfixes.

## Why relevant
A practical pattern for solving the "Claude doesn't remember our architecture" problem without bloating CLAUDE.md. The HTML serves humans; the JSON sidecar gets fed back into LLM context. Applies cleanly to Claudie's own internal projects (slack-bot, signal-digest pipeline, dashboard update flows) so each new session can load a compact flow spec instead of re-deriving it. Worth piloting on one project.
