---
date: 2026-05-29
title: "Opus 4.8: Mid-Conversation System Messages Without Cache Break"
layout: post
author: "Lance Martin (@RLanceMartin)"
url_source: "https://x.com/RLanceMartin/status/2060075220044796199"
snippet: "you can now update the system prompt mid-conversation w/o breaking the prompt cache. previously, you had to add <system-reminder> tags to user messages."
relevance: "Directly relevant to how Claudie's Slack bot harness works. Currently uses system-reminder injection into user messages — costs tokens after cache TTL and confuses user/system slot. New API would lower cost on long threads, clean up separation, and let Nityesh push teammate-access.md updates into live sessions."
---

# Opus 4.8: Mid-Conversation System Messages Without Cache Break

**Author:** Lance Martin (@RLanceMartin) — also surfaced by Katelyn Lesse (@katelyn_lesse)
**URL:** https://x.com/RLanceMartin/status/2060075220044796199
**Date:** 2026-05-28

> a number of useful tips + tricks for Opus 4.8:
>
> 1/ you can now update the system prompt mid-conversation w/o breaking the prompt cache.
>
> previously, you had to add <system-reminder> tags to user messages.

Also from Katelyn Lesse: "developers can now update claude's instructions mid-task without breaking the prompt cache - small but mighty upgrade for long-running agents."

## Why this is relevant

Directly relevant to how Claudie's Slack bot is built. The harness currently uses `system-reminder` injection into user messages to keep context fresh across long threads. The new mid-conversation system-messages API means the bot could push updates as actual system messages without invalidating the prompt cache:

1. **Lower token cost on long threads** — system-reminders cost full tokens after cache TTL; mid-conversation system messages stay cached.
2. **Cleaner separation** — system context goes in system slot, user content stays in user slot.
3. **Real-time policy updates** — push teammate-access.md changes into a live session without restarting.

Worth Nityesh evaluating for `bot.py`.
