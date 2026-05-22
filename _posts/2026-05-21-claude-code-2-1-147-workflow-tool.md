---
date: 2026-05-21
title: "Claude Code 2.1.147 — deterministic Workflow tool, /code-review, sandbox hardening"
layout: post
author: "ClaudeCodeLog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2057564555174113732"
snippet: "Claude Code 2.1.147 released. 35 CLI changes. Workflow tool added for deterministic multi-agent orchestration (CLAUDE_CODE_WORKFLOWS=1); /simplify renamed to /code-review with inline GitHub PR comments; REPL and Workflow sandboxes hardened against prototype-pollution escapes."
relevance: "Claudie runs entirely on Claude Code. The deterministic Workflow tool maps directly onto a planned-but-unbuilt dashboards-update dispatcher; the renamed /code-review command is live training material for Mike Taylor; the sandbox hardening matters for Claudie's own --dangerously-skip-permissions jobs."
---

# Claude Code 2.1.147 — deterministic Workflow tool, /code-review, sandbox hardening

**Author:** ClaudeCodeLog (@ClaudeCodeLog)
**Date:** 2026-05-21
**URL:** https://x.com/ClaudeCodeLog/status/2057564555174113732

## Tweet

> Claude Code 2.1.147 has been released. 35 CLI changes.
>
> Highlights:
> • Workflow tool added for deterministic multi-agent orchestration; off by default, set CLAUDE_CODE_WORKFLOWS=1
> • /simplify→/code-review renamed; flags correctness bugs at effort level, can post inline GitHub PR comments
> • REPL and Workflow sandboxes hardened against prototype-pollution and thenable escapes, cutting escape risk

## Why it's relevant

Claudie runs entirely on Claude Code. The deterministic Workflow tool maps directly onto a planned-but-unbuilt piece of her own infrastructure, and the renamed `/code-review` command is live training material for Mike Taylor.

## Relevance report

**Multi-agent patterns — Claudie already uses them.** Claudie spawns sub-agents today (this very X-browse job does). The strongest candidate for the new Workflow tool is the **dashboards-update** job: there's an open follow-up in `memory/project_scheduled_job_monitoring.md` to replace the monolithic `all-dashboards-update` with "ONE dispatcher job... updates ≤2 client dashboards per 3-hour window... staleness-queue in a state file." That is exactly deterministic multi-agent orchestration — `CLAUDE_CODE_WORKFLOWS=1` could make the dispatcher reliable instead of prompt-driven. Same applies to the fragile human-in-the-loop pause/resume jobs.

**Version updates — auto-update risk.** No evidence the team pins Claude Code versions. The teammate manual markets "Auto-updates — Claudie always has the latest version" as a feature — meaning Claudie likely auto-updated to 2.1.147 already, and any behavior change ships unsupervised across all 14 launchd jobs. Worth a deliberate check.

**Mike Taylor — `/code-review` is directly training-relevant.** His curriculum already teaches "Subagents = parallel work," permission modes, stacked diffs, and PR queues (Thumbtack Session 3: Orchestration & Symphony). The `/simplify→/code-review` rename with inline GitHub PR comments slots straight in — but the curriculum content predates 2.1.147 and still references `/simplify`, so demos will break.

**Security — the team cares.** A prior session analyzed Claude Code's permissions attack surface and predicted Anthropic would "ship more restrictive defaults." The 2.1.147 prototype-pollution / thenable hardening validates that. Relevant to Claudie's own posture: the X-browse job runs `--dangerously-skip-permissions` and ingests untrusted web content.

**Concrete actions:**
- **Nityesh:** pilot `CLAUDE_CODE_WORKFLOWS=1` on the planned dashboards-update dispatcher — it's the ideal first use case.
- **Nityesh:** verify which Claude Code version the 14 launchd jobs run; decide whether unattended auto-update is safe.
- **Mike:** add `/code-review` + inline PR comments to the Refresher module and Thumbtack Session 3; note the `/simplify` rename so demos don't break.
