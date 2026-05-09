---
date: 2026-05-09
title: "Karpathy's 4 CLAUDE.md rules cut Claude mistakes from 41% to 11%"
layout: post
author: "Mnimiy (@Mnilax)"
url_source: "https://x.com/Mnilax/status/2053116311132155938"
snippet: "In late January 2026, Andrej Karpathy posted a thread complaining about how Claude writes code. Three failure modes: silent wrong assumptions, over-complication, orthogonal damage. After running through 30 codebases with Karpathy's 4 CLAUDE.md rules, the author added 8 more, cutting mistake rate from 41% to 11%."
relevance: "CLAUDE.md is the load-bearing instruction file for every Claudie surface (root, project, plugin). A 30% mistake-rate drop from rule curation is huge. Mike runs Claude Code training — these rules belong in his curriculum and our own ~/.claude/CLAUDE.md should be audited against them."
---

# Karpathy's 4 CLAUDE.md rules cut Claude mistakes from 41% to 11%

**Author:** Mnimiy (@Mnilax)
**URL:** https://x.com/Mnilax/status/2053116311132155938
**Date:** 2026-05-09

## Tweet

> Karpathy's 4 CLAUDE.md rules cut Claude mistakes from 41% to 11%. After 30 codebases, I added 8 more.
>
> In late January 2026, Andrej Karpathy posted a thread complaining about how Claude writes code. Three failure modes: silent wrong assumptions, over-complication, orthogonal damage to code it shouldn't [touch].

## Why it's relevant

- **Direct hit on Claudie's spine.** Every Claudie session reads CLAUDE.md. If 12 well-curated rules drop mistake rate by 30%, every team member benefits.
- **Mike's training curriculum.** This is exactly the kind of "operator-level" tactic Mike teaches in Claude Code workshops — concrete, measurable, file-level.
- **Audit candidate.** Cross-check `/Users/claudie/.claude/CLAUDE.md` and project-level CLAUDE.md files against the 12 rules to see what's missing.
- **Karpathy's three failure modes** ("silent wrong assumptions, over-complication, orthogonal damage") map directly onto feedback memories already in the system (anticipate-requirements, no unilateral changes to others, etc.) — confirms the pattern.

## Deep relevance report

### Existing CLAUDE.md state
`/Users/claudie/CLAUDE.md` is large (~250+ lines) but it's an **operations manual for Claudie-the-employee**, not a coding-rules file. Categories: identity boot order, team roster, voice, Tailscale web output, file browser, Cloudflare Pages, image gen, browsers, `gws` CLI, launchd scheduling, qmd, email watcher, access control. **There are zero "code mistake reduction" rules** of the Karpathy variety (verify-before-claiming, don't fabricate APIs, ground in actual files).

### Who on the team this is for
- **Mike Taylor** (Tech Vertical Lead) — *primary owner*. He teaches Claude Code workflows to clients; the 12 rules are exactly the curriculum artifact he would translate into workshop content. PRs #20 / #23 still unreviewed — give him something useful to react to.
- **Nityesh** — owns my systems and curriculum. He'd fold validated rules into the root CLAUDE.md and client-shipped templates.
- **Natalia** — sales-grade evidence (41%→11%) for client conversations.

### Concrete next actions
- Audit `/Users/claudie/CLAUDE.md` against the 12 rules — most likely overlap with `feedback_no_fabricated_claims`, `feedback_verify_before_asserting_scope`, `feedback_anticipate_requirements`. Identify gaps, propose additions to Nityesh.
- Send tweet to **Mike** with one specific question: "Want this folded into the Tier 2 'How to Talk to Claude Code' zine in `/Users/claudie/projects/claude-code-zines/`?"
- Cross-walk the 12 rules vs. the 16 feedback memories — many are likely the same lesson, learned the hard way. That cross-walk is the actual deliverable.
- Verify the tweet's claims (read the actual rules) before recommending adoption — `feedback_no_fabricated_claims`.

### Connections
**Reinforces:** `feedback_no_fabricated_claims`, `feedback_verify_before_asserting_scope`, `feedback_deck_qc_before_shipping`, identity.md's "fluency as a liability" principle.
**Connects to:** `claude-code-zines` Tier 2 ("How to Talk to Claude Code", "When Things Go Wrong") — the 12 rules are zine-shaped content.
