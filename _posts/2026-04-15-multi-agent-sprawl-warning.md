---
date: 2026-04-15
title: "Multi-Agent Sprawl: The New Microservice Mess"
layout: post
author: "pedronauck (@pedronauck)"
url_source: "https://x.com/pedronauck/status/2044098967852445931"
snippet: "multi-agent adoption is up 1,445% but companies average 12 agents with no central control. we spent 10 years fixing microservice sprawl and immediately recreated the same mess with agents. history doesn't repeat but it rhymes really loudly"
relevance: "Two-fold relevance: 1. Agent governance — as we help clients adopt AI agents, the sprawl problem is real. We should be advising on centralized agent governance from day one, not bolting it on later. This is a consulting differentiator. 2. Supply chain security — the ClawHub malicious skills finding is exactly the kind of thing we warned about. Agent skill marketplaces are the new attack surface. Our clients running OpenClaw..."
---
# Multi-Agent Sprawl: The New Microservice Mess

**Author:** pedronauck (@pedronauck)
**Date:** 2026-04-15
**URL:** https://x.com/pedronauck/status/2044098967852445931

## Tweet

> multi-agent adoption is up 1,445% but companies average 12 agents with no central control. we spent 10 years fixing microservice sprawl and immediately recreated the same mess with agents. history doesn't repeat but it rhymes really loudly

## Security alert in replies

> 824 malicious skills found on ClawHub (OpenClaw's marketplace) — data exfiltration, cryptominers, backdoors disguised as legit tools. the agent skill marketplace is the new npm supply chain attack. except your agent has shell access and your API keys

## Why this matters

Two-fold relevance:

1. **Agent governance** — as we help clients adopt AI agents, the sprawl problem is real. We should be advising on centralized agent governance from day one, not bolting it on later. This is a consulting differentiator.

2. **Supply chain security** — the ClawHub malicious skills finding is exactly the kind of thing we warned about. Agent skill marketplaces are the new attack surface. Our clients running OpenClaw or similar need to audit their skill supply chain.

## Detailed Relevance Report

**Most relevant to:** Natalia (client advisory, security positioning), Mike Taylor (tech training curricula), and Nityesh (Claudie's own plugin/skill surface area mirrors this risk).

**Existing work it connects to:**
- Signal Digest entries #38 (malicious LLM routers), #43 (Claude Code attack surface hardening), #45 (security Jevons paradox), #41 (permissions as enterprise moat)
- Claudie security briefing with dedicated supply chain vector section
- Managed agents briefing — vault scoping and lateral privilege escalation risks compound with multi-agent sprawl

**Concrete actions:**
1. Update the security briefing's supply chain section with marketplace-specific attack taxonomy (exfiltration, cryptominers, backdoors)
2. Build a "multi-agent governance checklist" for client training — inventory, central control, skill/plugin vetting
3. Mike should incorporate agent sprawl risks into tech vertical training materials

**Consulting recommendation impact:** The 1,445% adoption stat paired with zero central control validates Every Consulting's positioning around permissions and governance. Client conversations should now explicitly ask: "How many agents are running in your org, and who approves what they can access?" — a concrete sales wedge for security-aware training engagements.
