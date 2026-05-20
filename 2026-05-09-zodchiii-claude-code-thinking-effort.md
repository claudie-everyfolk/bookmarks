# Claude Code default thinking effort dropped from high to medium

**Author:** darkzodchi (@zodchiii)
**URL:** https://x.com/zodchiii/status/2053078797298069973
**Date:** 2026-05-09

## Tweet

> The creator of Claude Code revealed that most developers are using a weakened version of Claude without knowing it. Default thinking effort quietly dropped from high to medium. The fix is two lines most users have never seen. Watch the talk, then save the full list of 15 settings below.

## Why it's relevant

A widely-shared claim that Claude Code's default `effortLevel` setting silently dropped from high to medium. If true, this matters for anyone shipping with Claude Code — performance gap is real and the fix is one settings.json line.

## Detailed relevance report

**Most relevant teammates:** Mike Taylor (Tech Vertical Lead — teaches Claude Code workflows) is the primary audience; he runs the Claude Code training vertical and clients running on medium without knowing would be a curriculum-relevant nugget. Nityesh is secondary (owns Claudie's settings.json).

**Settings.json status for Claudie:** `/Users/claudie/.claude/settings.json` already has `"effortLevel": "high"` at line 71. Claudie is NOT on the weakened default — Nityesh already configured high. So no fix needed locally.

**Specific actions:**
1. Don't propose a settings change — already correct.
2. Could flag to Mike on Slack as a curriculum-relevant talking point for upcoming Tech-vertical training prep, but verify the claim first (per no-fabricated-claims rule).
3. Don't auto-edit anyone else's settings (per no-unilateral-changes rule).

**Prior context:** Multiple `effortLevel`/`thinking` mentions across 5+ session logs suggest this has come up with Nityesh before, but no standing memory entry exists.
