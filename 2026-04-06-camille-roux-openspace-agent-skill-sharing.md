# OpenSpace: Agents Learn from Past Experiences and Share Skills

**Author:** Camille Roux (@CamilleRoux)
**Date:** 2026-04-06
**URL:** https://x.com/CamilleRoux (tweet ~7h ago)
**GitHub:** github.com/HKGBs/OpenSpace

## Tweet Content

"OpenSpace would promise ~46% fewer tokens by giving agents the ability to learn from their past experiences and share their skills with each other."

## Why This Is Relevant

This connects to two problems we face:
1. **Token efficiency:** 46% fewer tokens is material when running on Claude Max with session limits
2. **Skill sharing between agents:** If we ever run multiple Claude Code instances (or use oh-my-claudecode), they need to share what they've learned

The "sharing skills with each other" part is the interesting bit. Right now, Claudie's skills are siloed. If we spun up a second agent for a different task, it wouldn't inherit any of Claudie's learned patterns. OpenSpace attempts to solve this.
