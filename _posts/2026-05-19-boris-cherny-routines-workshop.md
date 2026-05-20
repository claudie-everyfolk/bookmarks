---
date: 2026-05-19
title: "Boris Cherny: 'I create the routines that do the prompting'"
layout: post
author: "Movez (@0xMovez), quoting Boris Cherny"
url_source: "https://x.com/0xMovez/status/2056723475528630529"
snippet: "Boris Cherny: 'A lot of my code these days is written by routines. I'm not doing the prompting — I create the routines that do the prompting.' 6-min workshop from the creator of Claude Code, live session in London."
relevance: "Highest-credibility validation yet of an architecture Claudie already runs — her 20-job launchd fleet IS 'routines' in Cherny's sense. The new claude agents --json command (2.1.145) is immediately actionable for the job-health-monitor. Premium curriculum material for Mike's Claude Code training."
---

# Boris Cherny: "I create the routines that do the prompting"

**Author:** Movez (@0xMovez), quoting Boris Cherny (creator of Claude Code)
**URL:** https://x.com/0xMovez/status/2056723475528630529

> Creator of Claude Code just dropped a 6-min workshop on a new Claude feature during a live session in London.
>
> Boris Cherny: "A lot of my code these days is written by routines. I'm not doing the prompting — I create the routines that do the prompting."

Related: the Claude Code 2.1.145 changelog (also shipped today) adds `claude agents --json` — outputs live agent sessions as JSON for scripting and automation.

## Why it's relevant
The highest-credibility validation yet of an architecture Claudie already runs. Boris Cherny, Head of Claude Code, describing his own workflow as "build the routine, not the prompt" is exactly Claudie's 20-job launchd fleet. Not a new strategy — confirmation the current architecture is right. The genuinely new, immediately-actionable piece is `claude agents --json` for the job-health-monitor.

---

## Relevance report

**Bottom line:** Not a new find — the highest-credibility validation yet of a trajectory already tracked across Signal Digest entries #32, #35, #54 and two prior relevance reports.

### 1. Who this is most relevant to

- **Nityesh (critical)** — Owns Claudie's scheduling architecture: 20 active `com.claude.*` launchd jobs, the two-file pattern, the `schedule-claude` / `job-dashboard` skills. Only person who can evaluate native Routines vs launchd and act on `claude agents --json`.
- **Mike Taylor (high)** — A Boris Cherny quote is premium curriculum material. Signal Digest #54 already recommends a "Routines vs Self-Hosted" module; this is the hook.
- **Natalia (medium)** — "Routines or self-host?" is now a client question.

### 2. How this maps onto Claudie's architecture

Cherny's "routines that do the prompting" *is* Claudie's two-file launchd pattern: a wrapper script running `claude -p` scheduled by a plist. Claudie runs 20 `com.claude.*` jobs (morning brief, x-browse, dashboards-update, weekly-kickoff, pipeline-refresh, job-health-monitor, qmd-reindex) — these *are* routines. Standing memory `feedback_always_use_launchd.md`: local launchd needs local file/tool access; Routines run in Anthropic's cloud. Diary `2026-05-04.md`: *"A job in English does not run. A job in launchd runs."*

**Honest framing:** Claudie was doing "routines before Routines." Difference is naming and infra location, not concept. Cherny saying it out loud validates the architecture.

### 3. What existing work this connects to

- **Signal Digest #54** (`discoveries/signal-digest/entries/54-claudeai-routines-research-preview.md`) — full Routines analysis; already recommends a bounded pilot + training module. Note this tweet there, don't duplicate.
- **Two prior relevance reports** on `bookmarks/2026-04-15-claude-code-routines-managed-infra.md`.
- **`schedule-claude/skill.md`** — the launchd two-file pattern any comparison must beat.

### 4. Concrete actions

1. **Note on Signal Digest #54, no new entry** — validation, not new key-shift.
2. **Nityesh — wire up `claude agents --json`** into `job-health-monitor` to enumerate live agent sessions instead of parsing logs.
3. **Nityesh — run the bounded Routines pilot** from #54: migrate `dashboards-update` or `weekly-kickoff` side-by-side; keep launchd running.
4. **Mike — add a Claude Code training module:** "Routines: build the routine, not the prompt," opening with the Cherny quote, using Claudie's launchd fleet as the self-hosted case study.
5. **Do NOT migrate Claudie wholesale** — jobs needing dev-browser, local FS, or qmd cannot run as cloud Routines.

### 5. Client engagement where this lands well

- **Bloomberg** — executive training requested for demo day; prior custom-GPT sessions saturated. "Routines, from the creator of Claude Code" is a credentialed step-up.
- **Woodline** — cloud-hosted Routines is the natural answer for a client wanting always-on AI without self-hosted infra.

**Caveat:** Routines is research-preview, Anthropic-hosted, no published pricing/compliance story. Every's edge: "we run both patterns — we can tell you which fits your governance posture."
