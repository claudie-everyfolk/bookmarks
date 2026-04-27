---
date: 2026-04-02
title: "mngr: Open-source tool for managing 100s of parallel Claude Code sessions"
layout: post
author: "Kanjun (@kanjun) / Josh Albrecht (@joshalbrecht) — Imbue"
url_source: "https://x.com/kanjun/status/2039727392915349902 (approx)"
---

# mngr: Open-source tool for managing 100s of parallel Claude Code sessions

**Author:** Kanjun (@kanjun) / Josh Albrecht (@joshalbrecht) — Imbue
**Date:** 2026-04-02
**URL:** https://x.com/kanjun/status/2039727392915349902 (approx)

## Tweet text
"We run 100s of parallel Claude Code sessions all doing useful work at @imbue_ai. It's been wild — we just say 'for each flaky test in the past week, fix it' or 'for each Linear ticket, create a PR'. Today, we're open sourcing mngr, the CLI tool that makes it possible."

Josh Albrecht: "mngr: programmatically manage 100s of claude code sessions in parallel. open source today."

## Why it's relevant
This is directly relevant to how Claudie could scale. Right now Claudie runs single Claude Code sessions via launchd. mngr could allow parallelizing work — e.g., running quality checks across all client dashboards simultaneously, processing multiple email threads at once, or doing bulk research tasks. The "for each Linear ticket, create a PR" pattern maps directly to patterns like "for each client dashboard, run a weekly update."

## Who on the team this matters to
- **Nityesh** — could evaluate mngr for scaling Claudie's scheduled jobs. Currently each launchd job runs one claude -p session; mngr could orchestrate many.
- **Mike Taylor** — teaches AI coding workflows; mngr is a concrete tool for developer productivity training.
