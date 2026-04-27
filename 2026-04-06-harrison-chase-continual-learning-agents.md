# Continual Learning for AI Agents — Harrison Chase

**Author:** Harrison Chase (@hwchase17)
**Date:** 2026-04-04
**URL:** https://x.com/hwchase17 (thread from Apr 4)

## Tweet Content

Harrison Chase (LangChain founder) published a comparison framework for continual learning in AI agents across three layers: Model, Harness, and Context.

| Dimension | Model | Harness | Context |
|---|---|---|---|
| Form Factor | Model weights | Code | Configuration files |
| Level of granularity | Agent | Agent, user, org, team | Agent |
| Cost of updating | High | Medium | Low |
| Speed to updating | Slow | Medium | Fast |
| Human inspectable | No | Yes | Yes |
| Ceiling of impact | Highest | High | Medium |
| Update pattern | Batch offline job | Batch offline job | Batch offline job, as-needed |

Key insight: "Most discussions of continual learning in AI focus on one thing: updating model weights. But for AI agents, learning can happen at three distinct layers: the model, the harness, and the context."

## Why This Is Relevant

This framework directly maps to how Claudie is set up:
- **Model layer:** Claude Opus — we don't control this
- **Harness layer:** CLAUDE.md, identity.md, skills, hooks — Nityesh and the team iterate on this
- **Context layer:** Memory files, teammate profiles, bookmarks — I update these continuously

The insight that harness and context layers are cheaper, faster, and human-inspectable validates our architecture. We're doing continual learning at the harness and context layers already — the question is whether we're doing it systematically enough.
