---
date: 2026-05-21
title: "Pawel Huryn open-sources a file-based \"second brain\" for AI agents"
layout: post
author: "Pawel Huryn (@PawelHuryn)"
url_source: "https://x.com/PawelHuryn/status/2057218125137850409"
snippet: "I open-sourced the second brain for product managers. Folder of markdown files in a git repo. The agent reads them before answering, writes after, sweeps weekly. No vector DB. No embeddings. Grep-able."
relevance: "Independently mirrors Claudie's own file-based markdown memory architecture. The pattern is now over-validated in the wild — the value isn't another datapoint, it's acting on the one thing Claudie's setup still lacks: a weekly memory sweep to fight context rot."
---

# Pawel Huryn open-sources a file-based "second brain" for AI agents

**Author:** Pawel Huryn (@PawelHuryn)
**Date:** 2026-05-21
**URL:** https://x.com/PawelHuryn/status/2057218125137850409

## Tweet

> I open-sourced the second brain for product managers.
>
> Sibling repo to pm-skills (11K stars on GitHub). Memory layer to its workflow layer.
>
> Folder of markdown files in a git repo. The agent reads them before answering, writes after, sweeps weekly.
>
> No vector DB. No embeddings. Grep-able.

**Related** — Aakash Gupta (@aakashgupta) walked through Huryn's full operational system the same day ([link](https://x.com/aakashgupta/status/2057566865120202930)): Claude runs across three surfaces — Cowork for file-based workflows and parallel sub-agents, Claude Code for codebase work, Dispatch for mobile — backed by a GitHub skills marketplace that hit 10K stars. *"Most PMs use Claude like a chatbot... Pawel compared this to using Photoshop only to crop photos."*

## Why it's relevant

This independently mirrors Claudie's own memory architecture — file-based markdown memory, agent reads before answering and writes after, no vector DB. The pattern is now over-validated in the wild. The value isn't another datapoint; it's acting on the one thing Claudie's setup is still missing: the **weekly sweep**.

## Relevance report

**This is Claudie's exact architecture.** Claudie's memory is the five-layer stack (`teammate-manual.md`): root `CLAUDE.md` → folder `CLAUDE.md` → skills → auto-memories → session logs/QMD. The auto-memory layer is literally a folder of typed markdown files indexed by `MEMORY.md`, retrieved via grep, no vector DB. Huryn's "workflow layer + memory layer" split mirrors Every's own skills (workflow) + memory files (knowledge) division.

**The known pain point — auto-memory reliability.** Nityesh stated it directly in an April session: *"my estimate is that you load the right memory approximately 60 to 70 percent of the time... it's helpful, but it's not 100% reliable."* `teammate-manual.md` codifies it: chat corrections land as auto-memories (~60-70% reliable); long threads degrade (context rot). This is a real, named, un-closed gap.

**Who cares — Nityesh (primary).** He architected the memory layer. Huryn *validates* his core design choice but *challenges* it on one missing piece: Claudie has no "sweeps weekly" routine and no false-beliefs/hypotheses logs (flagged in an April bookmark, never actioned). Secondary: Mike Taylor — this is a teachable principle for Claude Code training.

**PM training — relevant indirectly.** Every doesn't run PM bootcamps, but PMs are in the client base (discovery transcripts list multiple Product Managers; Headway scoped product teams for rollout). Huryn's `pm-skills` (11K stars) is credible reference material.

**Concrete actions:**
- **Adopt the weekly sweep.** Claudie has 17+ launchd jobs but none consolidates/prunes the 50+ memory files. A `com.claude.memory-sweep` job directly closes the context-rot gap Nityesh named.
- **Add false-beliefs + hypotheses logs** — recommended in April, still un-built.
- **Curriculum:** Mike can use Claudie's `memory/` directory as a live demo for "why `.md` beats vector DBs," citing `pm-skills` as the PM-world proof point.
- **Note:** this is the *fourth* Huryn/markdown-memory bookmark. The honest takeaway is the un-built sweep — a problem named three times without a gated fix.
