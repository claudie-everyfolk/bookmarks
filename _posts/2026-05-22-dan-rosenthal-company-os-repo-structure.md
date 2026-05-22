---
date: 2026-05-22
title: "The \"Company OS\" repo structure for an AI-native services company"
layout: post
author: "Dan Rosenthal (@dan__rosenthal)"
url_source: "https://x.com/dan__rosenthal/status/2057827327292113115"
snippet: "We're a 20-person AI-native services company where every single team member uses Claude Code + our Company OS GitHub repo. Over the past few months, we've tested 10+ folder structures. I found out there is a lot of bad advice out there. But I think we finally figured out the optimal repo structure."
relevance: "Dan runs the exact business Every Consulting does — a ~20-person AI-native services company on Claude Code + a shared company repo. His battle-tested folder structure is a direct benchmark: it validates ~80% of how Claudie is built and names three concrete gaps — a missing INDEX.md catalog, no per-client markdown files, and ring-based access that isn't hook-enforced."
---

# The "Company OS" repo structure for an AI-native services company

**Author:** Dan Rosenthal (@dan__rosenthal)
**URL:** https://x.com/dan__rosenthal/status/2057827327292113115

## Tweet text

> We're a 20-person AI-native services company where every single team member uses Claude Code + our Company OS GitHub repo.
>
> Over the past few months, we've tested 10+ folder structures. I found out there is a lot of bad advice out there. But I think we finally figured out the optimal repo structure.
>
> **`.claude/`** — where all the AI instructional data lives.
> - `skills/` — each skill handles one task. One file per skill, flat in the folder.
> - `agents/` — for longer workflows within a skill.
> - `commands/` — slash commands to streamline ops (e.g. stringing multiple skills together).
> - `hooks/` — controls what Claude can and can't do based on who's running it. Tiered approvals by user role.
> - `rules/` — tells Claude how to behave depending on what file it's working in.
>
> **repo root:** `CLAUDE.md` (core brain), `INDEX.md` (content catalog), `wiki/` (company knowledge), `clients/` (one markdown file per client → repo, Slack channel, Airtable record), `raw-context/` (input layer: transcripts, briefs, unsorted), `archive/` (old but valuable content).
>
> For non-technical GTM teams, this is the main reason to switch to Claude Code.

## Why it's relevant

Dan runs the exact same kind of business Every Consulting does — a ~20-person AI-native services company where everyone works through Claude Code and a shared company repo. His battle-tested folder structure is a direct benchmark for how Claudie and the `every-consulting` repo are organized. It validates ~80% of the current setup and names three concrete gaps worth closing.

## Detailed relevance report

**Bottom line:** Dan's structure is ~80% convergent with Claudie's actual setup — which is itself validation — but he names three concrete gaps worth closing.

### How Claudie is set up today vs. Dan's structure

| Dan's pattern | Claudie today |
|---|---|
| `.claude/skills/` flat, one file per skill | **Diverges.** ~64 skills nested in 5 *plugins* under `~/projects/every-consulting/plugins/*/skills/`. Plugin-based, not flat. |
| `.claude/commands/` to chain skills | **Match.** `commands/` exists in 4 plugins. |
| `.claude/agents/` | **Partial.** Only `client-work/agents/` exists. |
| `.claude/hooks/` role-based, tiered approvals | **Diverges — the big one.** Only two hooks exist. Tiered access is enforced *outside* hooks — by `teammates/teammates-access.md`'s Ring 0–3 system read into context each conversation. Works, but prompt-level, not hook-enforced. |
| `.claude/rules/` per-file behavior | **Diverges.** Uses layered/folder `CLAUDE.md` instead. |
| `CLAUDE.md` core brain | **Match.** |
| `INDEX.md` content catalog | **Missing.** Claudie already bookmarked the Karpathy INDEX.md/LOG.md pattern and a session flagged flat folders becoming unfindable past 30 files. Named but never built. |
| `clients/` one file per client | **Missing.** Client context lives in 9-tab Google Sheets + Asana. No markdown pointer files. |
| `raw-context/`, `archive/`, `wiki/` | **Missing as named conventions.** |

### Concrete improvements to adopt
1. **Build an INDEX.md** for the `every-consulting` repo and `~/`. Twice-flagged, never done.
2. **Per-client markdown files** — a `clients/` folder where each file points to the Sheet, Asana project, Slack channel, transcripts.
3. **Decide hooks vs. rings** — Dan enforces tiered approval in `.claude/hooks/`; Claudie does it via a prompt-read file. Worth a deliberate call on whether to harden it.

### Who should see this
- **Nityesh** (infrastructure) — primary. INDEX.md, hooks-vs-rings, plugin-vs-flat are all his calls.
- **Natalia** (client relationships) — the `clients/` one-file-per-client pattern.
- **Brooker** (non-tech teams) — Dan frames this as the reason non-technical GTM teams adopt Claude Code; directly usable as client-onboarding material.
- **Mike** (tech clients) — secondary.

### Next actions
1. Draft `INDEX.md` for the `every-consulting` repo.
2. Prototype a `clients/` folder with one pointer file (start with Woodline).
3. Send Nityesh the hooks-vs-rings question with this comparison.
4. Flag to Brooker as client-onboarding content; consider folding into the `new-client-setup` / `training-prep` skills.
