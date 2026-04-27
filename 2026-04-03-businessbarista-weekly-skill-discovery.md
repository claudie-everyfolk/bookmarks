# Weekly Skill Discovery Scan — Alex Lieberman

**Author:** Alex Lieberman (@businessbarista)
**URL:** https://x.com/businessbarista/status/2040173733168468177
**Date:** 2026-04-03

## Tweet

> Stupid simple, but most powerful Claude skill I run.
>
> Every Monday at 9am, Cowork scans my Linear, Notion, Slack, Gmail, and Cowork sessions to identify repeatable processes that should become skills.
>
> It allows me to proactively become more AI-native without making it my full-time job.

## Why it's relevant

This is a meta-automation pattern: using AI to find opportunities for more AI automation. Claudie already runs on a schedule and has access to Slack, Gmail, and session logs. We could build a similar weekly scan that reviews the team's interactions, identifies repeated manual processes, and proposes new skills or automations. This would make the team continuously more efficient without anyone having to think about it.

---

## Detailed Relevance Report

### 1. Who This Is Most Relevant To

**Nityesh (primary)** — His role is systems, automation, curriculum development. A weekly skill-discovery scan is exactly the kind of meta-automation he would design. His teammate profile notes he "wants Claudie to have opinions and push back when he sees a better path" — meaning he wants Claudie to proactively identify its own improvement opportunities.

**Natalia (secondary)** — Heaviest operational user. Her Chief of Staff rhythm (morning briefs, hourly check-ins, evening wraps) generates the most repeatable patterns. Also maps directly to what Every Consulting sells to clients — helping organizations become AI-native.

**Mike (tertiary)** — A working example of a self-improving AI agent discovering its own skills would be a powerful demo for his technical training vertical.

### 2. Existing Scheduled Jobs That Connect

Claudie already runs 15 launchd jobs. Several are adjacent:
- `weekly-kickoff` (Mon 4 AM) — Monday synthesis, closest structural analog
- `x-browse` (4x daily) — Pattern recognition on external content (Signal Digest), same analytical muscle pointed outward
- `repo-watcher` (every 30 min) — Self-evolution for code changes, but reactive not proactive
- `cos-morning/hourly/evening` — Already aggregates across data sources on a schedule

**Key gap:** All existing jobs are operational (do the work). None are meta-operational (identify what new work should be automated). This would be Claudie's first truly self-improving job.

### 3. Concrete Implementation Plan

**Data sources to scan** (Claudie already has access to all):
1. Slack conversation history — DMs with Natalia, Nityesh, Mike, Brooker from the past week
2. Gmail (claudie@every.to) — Sent emails and processed inbox
3. Claude Code session logs — JSONL files in `~/.claude/projects/`, richest source
4. Granola meeting notes — Via Granola MCP
5. Google Calendar — Cross-reference recurring meetings
6. Google Sheets dashboards — Check for manual data entry patterns
7. Memory/feedback files — New feedback files from the past week
8. Existing skills registry — Baseline to compare against

**Pattern signatures to detect:**
- Repeated request sequences (same deliverable type 2+ times/week)
- Multi-step manual workflows given as step-by-step instructions
- Feedback that became a memory file (procedural, not preference)
- Tool chains that repeat across multiple conversations
- Time-consuming one-offs that will recur
- Scheduled job failures or manual workarounds
- Things people did manually that Claudie could do

**Implementation:**
- Job: `com.claude.weekly-skill-discovery`, Mondays at 3:00 AM ET (before kickoff, outside peak hours)
- Two-file pattern: `~/scripts/weekly-skill-discovery.sh` + plist
- Output: Slack DM to Nityesh with ranked skill candidates, existing skill improvements, and emerging patterns
- Also save to `~/discoveries/skill-discovery-[date].md` for historical tracking
- Optionally wire into weekly-kickoff email so Natalia sees it too

**Bottom line:** Claudie already has 80% of the infrastructure. What's missing is the meta-layer: a job that looks at Claudie's own activity to discover what should be automated next. This would be Claudie's first genuinely self-improving capability.
