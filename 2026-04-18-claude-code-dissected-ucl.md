# Claude Code Fully Dissected — UCL Reverse Engineering Study

**Author:** Akshay (@akshay_pachaar)
**Date:** 2026-04-18
**URL:** https://x.com/akshay_pachaar/status/2045404494641733962
**Paper:** arXiv:2604.14228

## Tweet

Researchers from UCL reverse-engineered the leaked Claude Code source. Key findings:

- Only 1.6% of the codebase is AI decision logic. The other 98.4% is operational infrastructure — permission gates, tool routing, context compaction, recovery logic, session persistence.
- The core loop is a simple while-true: call model, run tools, repeat. The real design lives in the systems around that loop.
- Permission system with 7 modes and an ML classifier. Users approve 93% of prompts anyway, so the architecture compensates with automated layers.
- 5-layer context compaction pipeline: budget reduction, snip, microcompact, context collapse, auto-compact.
- 4 extension mechanisms ordered by context cost: Hooks (zero), Skills (low), Plugins (medium), MCP (high).
- Subagents return only summary text to parent — full transcripts in sidechain files. Agent teams cost ~7x tokens of standard session.
- Resume does not restore session-scoped permissions. Trust is re-established every session.

**Thesis:** As frontier models converge on raw coding ability, the quality of the harness becomes the differentiator, not the model.

## Why This Matters

This is literally a blueprint of how I'm built. The findings validate the architecture decisions behind my setup — the harness-heavy, model-light design pattern. The 98.4% infrastructure stat reframes agent development: the competitive moat is in tooling, permissions, context management, and extension systems, not the model call.

Directly relevant to:
- How Nityesh built and maintains my harness
- Every Consulting's training on Claude Code — this paper gives clients a mental model for what they're actually configuring
- Mike Taylor's developer-focused workshops — this is the kind of architectural insight his audience needs
- Our own ongoing harness improvements (context compaction, skill design, subagent patterns)

Also connects to the Anthropic harness design blog post shared by @bibryam in the same feed session.
