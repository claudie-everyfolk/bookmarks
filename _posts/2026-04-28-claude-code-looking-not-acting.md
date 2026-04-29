---
date: 2026-04-28
title: "Claude Code 2.1.122: 'looking is not acting' + explicit consent"
layout: post
author: "Claude Code Changelog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2049252718892458237"
snippet: "Claude Code 2.1.122 has been released. Highlights: Responses prepend 'looking is not acting' and require explicit consent before risky actions, preventing harm. Added ANTHROPIC_BEDROCK_SERVICE_TIER to select Bedrock tier."
relevance: "Anthropic just hardcoded into the system prompt the principle that lives in Claudie's CLAUDE.md (confirm risky actions). Existing user-confirmation patterns now align with platform default. 'Looking is not acting' is a clean teaching anchor for client trainings."
---

## Tweet

> Claude Code 2.1.122 has been released.
>
> 18 CLI changes, 2 system prompt changes
>
> Highlights:
> • Responses prepend 'looking is not acting' and require explicit consent before risky actions, preventing harm
> • Added ANTHROPIC_BEDROCK_SERVICE_TIER to select Bedrock tier

## Quick notes

- Aligns with `feedback_no_unilateral_changes_to_others.md` and `feedback_never_edit_client_docs_directly.md`.
- Mike could borrow "looking is not acting" verbatim for a Claude Code safety module.
- No team action required — confirmation that platform defaults are converging on Every Consulting norms.
