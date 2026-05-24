---
date: 2026-05-24
title: "Mnilax: Claude Code settings.json audit — deny-rule bug + 10% Opus tax"
layout: post
author: "Mnimiy (@Mnilax)"
url_source: "https://x.com/Mnilax/status/2058283663805047224"
snippet: "Boris Cherny didn't say one word about the settings.json that self-prompting runs on. 125+ keys. ~40 documented. 4 of mine aren't anywhere in the docs. I audited the whole file: 18 settings actually move the bill. one is the known deny-rule bug: your config says block, the binary reads anyway. one is the 10% Opus tax most apps pay by default through inference_geo."
relevance: "Claudie IS a self-prompting Claude Code install. Two claims hit us directly — the deny-rule bug (our 14 gws-gmail deny rules might silently fail; we have a defense-in-depth hook but should verify) and the inference_geo default 10% Opus tax (we don't set it, so we're paying it). Nityesh should audit."
---

# Mnilax: Audit of Claude Code settings.json — 125+ keys, 18 actually move the bill

**Author:** Mnimiy (@Mnilax)
**URL:** https://x.com/Mnilax/status/2058283663805047224

## Tweet

> the creator of Claude Code told a London stage on Wednesday that the default is now Claude prompting itself. but Boris Cherny didn't say one word about the settings.json that self-prompting runs on. 125+ keys. ~40 documented. 4 of mine aren't anywhere in the docs. I audited the whole file: 18 settings actually move the bill. one of them is the known deny-rule bug: your config says block, the binary reads anyway. one is the 10% Opus tax most apps pay by default through inference_geo.

## Relevance report

**Primary audience:** Nityesh (built Claudie's infra). Secondary: Mike Taylor (Claude Code training).

- Claudie's `settings.json` has 7 top-level keys, 14 deny rules (all `gws gmail` send paths), 13 enabled plugins. Far below the "125+" Mnilax audited.
- **Deny-rule bug exposure: HIGH.** Email safety model rests on those 14 deny rules. The `block-gws-email-send.sh` PreToolUse hook is the defense-in-depth that saves us if the bug is real — but verify.
- **`inference_geo` is NOT set.** If Mnilax's 10% Opus tax claim holds, we're paying it. Bounded by Max sub.

**Actions:** Nityesh audits against the 18 bill-moving keys, tests the deny-rule bug against our hook, then Mike packages findings into a Claude Code training module.
