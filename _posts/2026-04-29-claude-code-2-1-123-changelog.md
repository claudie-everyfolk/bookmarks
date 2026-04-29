---
date: 2026-04-29
title: "Claude Code 2.1.123 — system prompt loosens security guardrails, warns about URL hallucination"
layout: post
author: "Claude Code Changelog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2049334134586151272"
snippet: "Claude Code 2.1.123 has been released. 1 CLI change, 3 system prompt changes. Highlights: Fixed OAuth 401 retry loop when CLAUDE_CODE_DISABLE_EXPERIMENTAL_BETAS=1 is set; responses may now include generated or guessed URLs, which can point to incorrect external sites."
relevance: "URL hallucination is now an explicit Anthropic-acknowledged failure mode — clients running CC need to know fabricated links are possible (real liability in legal/finance). Security-policy reframe also worth tracking if Anthropic is loosening dual-use defaults."
---

# Claude Code 2.1.123 — system prompt loosens security guardrails, warns about URL hallucination

**Author:** Claude Code Changelog (@ClaudeCodeLog, automated by @marc_krenn)
**URL:** https://x.com/ClaudeCodeLog/status/2049334134586151272
**Date:** 2026-04-28

> Claude Code 2.1.123 has been released. 1 CLI change, 3 system prompt changes.
> Highlights:
> • Fixed OAuth 401 retry loop when CLAUDE_CODE_DISABLE_EXPERIMENTAL_BETAS=1 is set, restoring CLI authentication
> • Responses may now include generated or guessed URLs, which can point to incorrect external sites

Thread notes the system prompt no longer carries the upfront rule limiting security help to "clearly authorized contexts (pentests/CTFs/defensive)" with explicit refusal of destructive techniques, DoS, mass targeting, supply-chain compromise. CLI surface added `claude-empty-U`, removed `claude-empty-`.

## Why it's relevant

1. **URL hallucination is now an explicit Anthropic-acknowledged failure mode in Claude Code.** Every teammate / client running CC needs to know that links Claude pastes can be fabricated. Worth raising in client trainings, especially for legal/finance verticals where a hallucinated citation URL is a real liability.
2. **Security policy reframe.** The prior hard rule got softened. Could affect what we tell clients about using Claude for security tooling.
