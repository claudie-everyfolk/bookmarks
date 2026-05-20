# Daniel San: MCP cleanup + allowed-tools in skill frontmatter

**Author:** Daniel San (@dani_avila7)
**Date:** 2026-05-08
**URL:** https://x.com/dani_avila7/status/2052927835992424909

## Tweet

"ALWAYS review and clean up MCPs in every Claude Code session

Not a common practice, but it should be

And if you're building Skills, declare the tools in the frontmatter using the allowed-tools field

In a session with many MCPs connected, Claude can pull tools from any of them"

## Why it's relevant

Direct hit on Claudie's infrastructure. Tool sprawl from many concurrent MCPs is the exact scenario we're in — 80+ deferred tools at session start. Skills without `allowed-tools` frontmatter let Claude reach into any connected MCP, which can produce surprising or wrong-surface behavior.

## Detailed relevance report

**1. Skills missing `allowed-tools` — confirmed widespread:**

- Total `SKILL.md` files installed: 300 across `~/.claude/plugins/cache/` and `~/.claude/skills/`
- Skills with `allowed-tools` frontmatter: 39 (~13%)
- Every Consulting plugin family (`~/.claude/plugins/cache/every-consulting/`): 59 SKILL.md files, **ZERO with `allowed-tools`**
- Local user skills (`~/.claude/skills/`): 4 SKILL.md files, **ZERO with `allowed-tools`** — `delivery-skill`, `strategic-sensemaking`, `signal-digest`, `internal-kickoff-meeting`
- The 39 hits are almost entirely Anthropic example-skills and third-party `claude-home-base` plugins. Nothing Claudie or Nityesh wrote declares it.

**2. MCP sprawl is real:**

- Globally registered stdio/SSE MCPs: `granola`, `qmd`, `every` (3)
- Plus 13 enabled plugins in `~/.claude/settings.json`
- Plus 8 claude.ai MCPs connected (Gmail, Calendar, Notion, Every, Granola, Drive, Ramp Data, etc.)
- Session-start deferred-tools list = ~80+ MCP tools (Asana, Atlassian, CarbonArc, Daloopa, Mercury, MS365, PostHog, Ramp, Resy, Slack, Figma, …)
- Concrete risk: a skill like `claudie:weekly-update` could pull a Mercury or Ramp tool unintentionally.

**3. Who benefits:**

- Mike (Tech Vertical Lead) — fits his Claude Code curriculum directly; tip belongs in his teaching arsenal.
- Nityesh (built the plugin infra) — owns the `EveryInc/every-consulting` repo where the 59 skills live without `allowed-tools`.
- Brooker, Natalia, Kieran — less direct; they don't author skills.

**4. Concrete actions for Claudie:**

- Backfill `allowed-tools` in the 4 local skills at `~/.claude/skills/{delivery-skill,strategic-sensemaking,signal-digest,internal-kickoff-meeting}/SKILL.md`.
- Open a PR against `EveryInc/every-consulting` adding `allowed-tools` to the 59 plugin skills (only after asking Nityesh — recurring feedback memory: don't make unilateral changes to others' workflows).
- Add `allowed-tools` linting to `skill-creator` / `plugin-creator` so new skills can't ship without it.
- Add a `SessionStart` hook in `~/.claude/settings.json` (currently only has `PreToolUse` for gws-email-block) that warns when >5 MCPs are connected.
- Surface to Mike for the tech-track curriculum.
