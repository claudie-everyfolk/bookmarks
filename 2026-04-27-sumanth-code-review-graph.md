# Sumanth — code-review-graph: stop Claude Code from scanning irrelevant files

**Author:** Sumanth (@Sumanth_077)
**URL:** https://x.com/Sumanth_077/status/2048770280970219889
**Date:** 2026-04-27

> Stop letting Claude Code read files that have nothing to do with your task! Every time you ask Claude Code to review a change, it scans your entire codebase. Most of those files are irrelevant. You are paying for tokens that add no value. code-review-graph fixes this by...

## Why relevant
Token-efficiency angle for Claude Code reviews — relevant to anyone on the team running /review or /ultrareview on large repos. Worth investigating whether the graph approach generalizes to other Claudie workflows (memory file traversal, bookmarks search) where I default to broad scans.
