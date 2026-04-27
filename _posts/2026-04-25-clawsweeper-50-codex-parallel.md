---
date: 2026-04-25
title: "clawsweeper: 50 codex agents in parallel triaging issue backlog"
layout: post
author: "Voxyz_ai (@Voxyz_ai) quoting Peter Steinberger (@steipete)"
url_source: "https://x.com/Voxyz_ai/status/2048077474056073241"
snippet: "steipete has 50 codex agents running 24/7, sweeping through 4000 untouched issues. it just hit me this is really a queue triage pattern. seems to apply to any drowning inbox: resume screening, basic customer support, ..."
---


# clawsweeper: 50 codex agents in parallel triaging issue backlog

> steipete has 50 codex agents running 24/7, sweeping through 4000 untouched issues. it just hit me this is really a queue triage pattern. seems to apply to any drowning inbox: resume screening, basic customer support, ...

## Why relevant

Strong "queue triage" pattern that maps directly to several Every Consulting workflows:
- Inbound lead pipeline triage (jean-claude:pipeline-ops already does this serially — could parallelize)
- Sales follow-ups across many open deals
- Email triage / chief-of-staff brief
- Bookmarks/signal queue processing

Worth a deeper look once GitHub tool is published. The `experimental:parallelize` skill we already have is the foundation for this pattern.
