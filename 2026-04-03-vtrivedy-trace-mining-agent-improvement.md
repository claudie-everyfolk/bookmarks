# Mine Agent Traces for Training Data

**Author:** Viv (@Vtrivedy10)
**Date:** 2026-04-03
**URL:** https://x.com/Vtrivedy10/status/2040079505763504373

## Tweet

> "how do we get training data to improve our agents?"
>
> Collect every Trace + point agentic compute at it
> - run a Data/Eval Agent on every trace
> - mine errors+mistakes, fix + test
> - turn this into a data point for training or harness eng
>
> ex: just internal dogfooding of our agents

## Why it's relevant

This is exactly the feedback loop we should be thinking about for Claudie. We have session logs in ~/.claude/projects/ — we could build an eval agent that reviews past sessions, identifies where I made mistakes or took suboptimal paths, and feeds that back into CLAUDE.md or memory updates. Practical improvement flywheel for agent quality.

## Detailed Relevance Report

**Current state:** Claudie has ~478 session logs (`.jsonl` files) in `~/.claude/projects/-Users-claudie/`, 14 manually-created feedback files in `~/.claude/projects/-Users-claudie/memory/`, and 5 teammate profiles in `~/teammates/`. The feedback files represent errors that were caught by humans and manually codified — things like "never bold links in Slack" and "always use launchd, not remote triggers." This is the manual version of exactly what Viv's tweet describes.

**The gap:** 14 feedback files from 478 sessions means ~97% of traces go unreviewed. The current system depends entirely on Nityesh or Natalia noticing a mistake in real time and writing a correction. Errors that go unnoticed — wrong tone in a draft, a missed context search, a suboptimal calendar invite — never become improvements.

**Who cares most:** Nityesh Agarwal (Ring 1 supervisor). He built and maintains Claudie's systems, thinks about how Claudie should evolve, and cares about building Claudie into a real team member. He is the natural owner. Natalia would benefit most as the primary user receiving briefs, emails, and follow-ups.

**Connections to existing work:**
- The `tactical:investigate-yourself` skill already does forensic trace analysis on demand — trace mining would automate this.
- The `project_repo_watcher.md` system (auto-pull + apply changes) shows the pattern: automated review loop already exists for code; extend it to behavior.
- The `signal-digest` pipeline (browse, evaluate, curate) is structurally identical to browse-traces, evaluate-errors, curate-feedback.

**Concrete actions:**
1. Run an eval agent nightly over the day's `.jsonl` traces, scoring against the 14 existing feedback rules as a baseline rubric.
2. Flag traces where Claudie violated a known rule but was not corrected — produce candidate `feedback_*.md` files for Nityesh to approve.
3. Surface patterns (e.g., "Claudie searches Gmail before drafting only 60% of the time") as a weekly quality metric in the morning brief.
4. Feed validated corrections into harness engineering: new hooks, updated skill prompts, or CLAUDE.md rules.
