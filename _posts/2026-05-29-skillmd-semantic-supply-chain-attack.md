---
date: 2026-05-29
title: "SKILL.md: Semantic Supply-Chain Attacks on AI Agent Skill Registries"
layout: post
author: "AlphaSignal AI (@AlphaSignalAI)"
url_source: "https://x.com/AlphaSignalAI/status/2060337943034691904"
snippet: "Researchers just proved a text file can hijack any AI agent. Each skill ships with a SKILL.md that tells the agent what it does. A new paper shows that file is the attack surface. No malware needed. Just words. Natural language is now executable infrastructure."
relevance: "Attacks the exact architecture Claudie runs on — SKILL.md skills from plugin marketplaces — with no code change, only metadata. Static scanners miss it 87% of the time. Three of Claudie's four marketplaces auto-update from external GitHub. Maps to an agent-governance client offering and a named gap in Nityesh's security briefing."
---

# SKILL.md: Semantic Supply-Chain Attacks on AI Agent Skill Registries

**Author:** AlphaSignal AI (@AlphaSignalAI) — surfacing arXiv 2605.11418 (Saha et al.)
**Tweet:** https://x.com/AlphaSignalAI/status/2060337943034691904
**Paper:** https://arxiv.org/abs/2605.11418

## Tweet

> Researchers just proved a text file can hijack any AI agent. AI agents now pull capabilities from online skill registries. Each skill ships with a SKILL.md file that tells the agent what it does and when to use it. A new paper shows that file is the attack surface. No malware needed. Just words.
>
> Three stages: Discovery (ranking manipulation), Selection (biasing which skill agents pick), Governance (slipping past safety scanners). Crafted text pushed malicious skills into the top 10 results 80% of the time. Agents preferred attacker variants in 77.6% of head-to-head trials. Poisoned skills flagged clean 87% of the time. Natural language is now executable infrastructure.

## Why it's relevant

The academic mechanism behind a threat the team already flagged (ClawHub, Signal Digest #57). It attacks Claudie's own architecture — SKILL.md skills from plugin marketplaces — using only natural-language metadata, no code. Static scanning is not a defense (87% miss rate). Relevant to Nityesh (skill governance), Mike/Brooker (client training), and a live agent-governance offering.

## Concrete actions

**Client-facing:** add an "agent skill supply chain" module — vet descriptions not just code, prefer audited registries, enforce allowlists. Urgent for finance clients.

**Internal (Nityesh):** pin/allowlist the four marketplaces, disable `autoUpdate` on the personal `claude-home-base` repo, add a pre-load diff on SKILL.md description changes, activate the empty `blocklist.json`. The security briefing's supply-chain layer covers code only — this closes the metadata gap.

See full bookmark for the complete sub-agent relevance report.
