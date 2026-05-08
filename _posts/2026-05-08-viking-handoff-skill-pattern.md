---
date: 2026-05-08
title: "Matt Pocock's /handoff skill: compress conversation into a handoff file"
layout: post
author: "Viking (@vikingmute)"
url_source: "https://x.com/vikingmute/status/2052660705166557535"
snippet: "/handoff is indeed a very good skill; it's really just one sentence: Compress the current conversation into a handoff file, allowing a new agent or another session to seamlessly take over. Save the file to a temporary path."
relevance: "Directly applicable to Claudie's multi-session workflows. A /handoff skill that produces a structured handoff file at session boundaries could make morning-to-followup chains much more reliable than relying on MEMORY.md alone. Worth reviewing Matt Pocock's SKILL.md and considering adding to the claudie plugin."
---

# Matt Pocock's /handoff skill: compress conversation into a handoff file

**Author:** Viking (@vikingmute), quoting Matt Pocock (@mattpocockuk)
**Date:** 2026-05-08
**URL:** https://x.com/vikingmute/status/2052660705166557535
**Source skill:** github.com/mattpocock/skills/blob/733d312884b3878a9a9cff693c5886943753a741/skills/in-progress/handoff/SKILL.md

## Tweet

> /handoff is indeed a very good skill; it's really just one sentence: Compress the current conversation into a handoff file, allowing a new agent or another session to seamlessly take over. Save the file to a temporary path.

Quoting Matt Pocock: "/handoff might be my new favourite skill"

## Why it's relevant

This pattern is directly applicable to how Claudie operates across scheduled jobs and Slack-triggered sessions. Right now context is preserved through MEMORY.md files and the auto-compaction system, but a "/handoff" skill that explicitly produces a structured handoff file at session boundaries could make multi-session workflows (e.g., a morning briefing kicked off at 7am, picked up by a follow-up at 11am) much more reliable. Worth reviewing Matt Pocock's SKILL.md format and considering whether to add a /handoff skill to the claudie plugin or to client-work plugins.

Connection: Already see related patterns in the experimental:parallelize skill (shared state via temp files). /handoff is the same idea applied to time-based handoff rather than parallel coordination.
