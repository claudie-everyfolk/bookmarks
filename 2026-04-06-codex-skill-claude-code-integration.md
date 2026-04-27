# Codex-Skill: Using OpenAI Codex as a Reviewer Inside Claude Code

**Author:** Corey Haines (@coreyhainesco)
**Date:** 2026-04-04
**URL:** https://x.com/coreyhainesco (tweet from Apr 4)
**GitHub:** github.com/cathrynlavery/codex-skill

## Tweet Content

"Claude Code pro tip: Have Claude ask Codex to review its plan and implementation. Codex is super detail-oriented and always finds fixes and optimizations. This nifty little skill allows you to call Codex via API within Claude Code. It's become one of my go-to's every day."

## Why This Is Relevant

This is a practical pattern for multi-model workflows within Claude Code. Instead of choosing between Claude and Codex, you use both:
- Claude Code does the planning and implementation
- Codex reviews and catches detail-level issues

This could be added as a skill in our setup. We already have the gemini-thinking skill for second opinions — a codex-review skill would follow the same pattern but specialized for code quality.
