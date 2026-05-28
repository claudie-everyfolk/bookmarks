---
date: 2026-05-28
title: "14 Claude Code sub-agents — only 4 survived"
layout: post
author: "Mnimiy (@Mnilax)"
url_source: "https://x.com/Mnilax/status/2059737441880457369"
snippet: "14 Claude Code sub-agents I built in 60 days, 4 survived. The other 10 just burned tokens. Every sub-agent spawns with ~20K tokens of overhead before it does a single line of work."
relevance: "Directly applicable to Claudie's architecture. Sub-agent ROI is unmeasured here and the 20K spawn-cost floor is a clean rule of thumb for deciding when fan-out is wasted. Nityesh should audit parallelize callers; review-slides is already the correct adversarial pattern to copy elsewhere."
---

# 14 Claude Code sub-agents — only 4 survived

**Author:** Mnimiy (@Mnilax)
**URL:** https://x.com/Mnilax/status/2059737441880457369

## Tweet

> 14 Claude Code sub-agents I built in 60 days, 4 survived. The other 10 just burned tokens. Every Claude Code sub-agent spawns with ~20K tokens of overhead before it does a single line of work. The 20K number is buried in community write-ups, not the marketing page. Most builders never see it.

Companion thread quoting Anthropic engineers Ash Prabaker and Andrew Wilson on long-running agents:
> "self-evaluation is a trap. adversarial evaluator agents work better."
> "context compaction doesn't scale..."

## Relevance report

**Most relevant to: Nityesh** (owns Claudie's architecture). Secondary: **Mike Taylor** — exactly the "what works in production" finding he'd want for his Claude Code curriculum.

**Connections in Claudie's setup:**

1. **Sub-agent inventory is small but real.** Only `chat-history-retriever.md` exists as a dedicated agent. It just greps JSONL — almost certainly not worth 20K spawn overhead vs. a direct read.
2. **`experimental:parallelize` is the meta-skill** — doctrine of "fan out via multiple parallel agents, share state via temp files." Mnimiy's pain surface exactly: every fan-out carries an N × 20K floor.
3. **Slide QA already does it right.** `plugins/slide-deck-creation/skills/review-slides/SKILL.md` runs three independent judge subagents (spacing, data accuracy, holistic) with no shared context — the adversarial pattern Anthropic endorses. Use it as the template elsewhere.
4. **No memory of this debate.** Nothing in `~/.claude/projects/-Users-claudie/memory/` mentions evaluator agents or sub-agent ROI — architecture is intuition, not measured.

**Three concrete actions:**

1. **Audit `parallelize` callers.** Nityesh tally recent invocations: did this net >20K of useful work per subagent, or just feel parallel? Likely cut: retrieval or single-file edits that fan out.
2. **Promote `review-slides` as the template.** Refactor `quality-check` and any self-reviewing skill into adversarial-judge form.
3. **Watch the Prabaker/Wilson talk together.** Nityesh + Mike co-session — curriculum input + architecture pass before compaction strategies bake deeper.
