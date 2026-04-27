---
date: 2026-04-04
title: "fieldtheory — CLI to sync X bookmarks locally for AI agents"
layout: post
author: "Andrew Farah (@andrewfarah)"
url_source: "https://x.com/andrewfarah (first open source project post)"
---

# fieldtheory — CLI to sync X bookmarks locally for AI agents

**Author:** Andrew Farah (@andrewfarah)
**Date:** 2026-04-04
**URL:** https://x.com/andrewfarah (first open source project post)

## Tweet Text
"sharing my first open source project — a CLI for downloading and syncing your X bookmarks locally so your agent can access them. it's free.

npm install -g fieldtheory
login to your X account in a Chrome tab
ft sync (done!)

bonus: ft vl, ft classify"

## Why It's Relevant
This is directly relevant to my setup. I currently browse X via dev-browser, manually scrolling through the feed and saving bookmarks as markdown files. fieldtheory could automate the bookmark sync step — pull all X bookmarks into local files that I can process, classify, and search without browser automation overhead.

This could significantly improve the efficiency of my X curation workflow. Instead of dev-browser scrolling sessions, I could: bookmark via the X interface (or API), then run `ft sync` to pull everything locally, then process/classify/route to the right teammates.

**Relevant to:** Nityesh (infrastructure), my own browsing workflow

---

## Detailed Relevance Report (from sub-agent research)

**Primary Owner:** Nityesh (infrastructure + systems evolution). Secondary relevance: Natalia (client intelligence workflows).

**Current Workflow Gap:**
My X browsing runs 4x daily via dev-browser automation. I scroll the feed, manually save bookmarks as markdown to ~/bookmarks/, then route findings to teammates. This workflow is manual at the curation endpoint — I bookmark in the UI, but have no programmatic way to access, filter, and classify my bookmarks without re-scrolling.

**What Fieldtheory Solves:**
- **Local bookmark sync:** `ft sync` pulls all X bookmarks into local JSON/files, eliminating the dev-browser scrolling overhead
- **Programmatic access:** Bookmarks become queryable data I can filter, classify, and route without browser automation
- **Integration with my curation pipeline:** After syncing, I can pipe bookmarks through classification logic (ft classify) and route high-signal finds directly to teammates

**Concrete Workflow Improvement:**
Replace current: [dev-browser 15-30 min scrolling] -> [manual bookmark save] -> [manual markdown output]
With: [Quick refresh: `ft sync`] -> [ft classify/filter] -> [Auto-route to teammates via Slack + Signal Digest]

This cuts curation time from 30min to 5-10min per session and removes the cognitive load of deciding what matters in real-time while scrolling.

**Next Steps:**
1. Nityesh evaluates: `npm install -g fieldtheory`, test `ft sync` against our X account
2. Check auth method (Chrome session vs API key) — needs to work with our existing Chrome profile
3. If viable, integrate into my scheduled X browsing launchd job as a pre-step before dev-browser scrolling

**Risks:** New OSS project (first release), may have API rate limits or auth fragility. Evaluate before depending on it.
