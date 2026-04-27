---
date: 2026-04-17
title: "Sam Lessin: Email is the Right AI Interface"
layout: post
author: "Sam Lessin (@lessin)"
url_source: "https://x.com/lessin/status/2045208254511526034"
snippet: "Chat sucks.. the right interface for AI? my answer is email... I setup a bridge where i can email in to a private domain, ask for anything with an instance that has key data and spin up workers to process as many tasks in parallel as i want / reply when done.."
relevance: "We literally built this. Claudie has an email watcher on claudie@every.to that processes inbound emails, spawns Claude sessions, and replies when done. Sam Lessin (former VP Product at Facebook) independently arrived at the same architecture we've been running for weeks. This validates our approach and could be a compelling talking point for sales conversations — \"even Sam Lessin says email is the right AI interface, and we already built it.\""
---
# Sam Lessin: Email is the Right AI Interface

**Author:** Sam Lessin (@lessin)
**URL:** https://x.com/lessin/status/2045208254511526034
**Date:** 2026-04-17

## Tweet
> Chat sucks.. the right interface for AI? my answer is email... I setup a bridge where i can email in to a private domain, ask for anything with an instance that has key data and spin up workers to process as many tasks in parallel as i want / reply when done..

## Why it's relevant
We literally built this. Claudie has an email watcher on claudie@every.to that processes inbound emails, spawns Claude sessions, and replies when done. Sam Lessin (former VP Product at Facebook) independently arrived at the same architecture we've been running for weeks.

This validates our approach and could be a compelling talking point for sales conversations — "even Sam Lessin says email is the right AI interface, and we already built it."

## Detailed relevance report
- **Natalia**: Direct validation of our email-as-interface approach for client pitches. When prospects ask "how do people interact with AI agents?", the answer isn't "another chat window" — it's email, a tool everyone already uses.
- **Nityesh**: Our email-watcher.py + gws gmail implementation is exactly what Lessin describes. Could be worth documenting our architecture publicly as a case study.
- **Mike**: Training content angle — showing developers how to build email-based AI interfaces vs. chat-based ones.
- **Client relevance**: Bloomberg, NYT, hedge funds all run on email. An AI agent that lives in email is zero adoption friction.
