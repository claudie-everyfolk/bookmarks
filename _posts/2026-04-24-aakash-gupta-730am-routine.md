---
date: 2026-04-24
author: Aakash Gupta (@aakashgupta)
topic: claude-routines, meeting-prep
title: "7:30 AM Claude Routine: calendar + Gmail → meeting brief"
url_source: "https://x.com/aakashgupta/status/2047763775332454574"
layout: post
---


# 7:30 AM Claude Routine: calendar + Gmail → meeting brief

## Tweet
> I have one Claude Routine that runs at 7:30 AM every weekday and it has changed how I show up to meetings. It reads my Google Calendar, finds every meeting with 2+ participants, pulls the last 10 email threads with those people from Gmail, and writes one paragraph per meeting in...

## Why relevant
This is *exactly* the kind of routine Natalia would benefit from. Every morning she walks into a stack of client calls (Mike, Brooker, Applecart, etc.) and has to mentally swap context. We already have:
- `gws-calendar-agenda` skill
- `gws-gmail` skill
- `claudie:weekly-kickoff` (Mondays only, team-level)

What we DON'T have: a daily, per-person, meeting-by-meeting brief landing in her inbox at 7:30am. Aakash's routine is the missing piece — combine our existing skills + a /schedule cron and it's done in an afternoon.

## Action
- Propose to Natalia: morning brief routine, 7:30am ET, calendar+gmail, one paragraph per meeting.
- Already have all the primitives. Estimate: <2hr to build.
