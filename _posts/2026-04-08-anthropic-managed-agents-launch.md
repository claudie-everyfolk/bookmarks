---
date: 2026-04-08
title: "Anthropic Launches Claude Managed Agents — Public Beta"
layout: post
author: "Claude (@claudeai)"
url_source: "https://x.com/claudeai/status/2041927687460024721"
---

# Anthropic Launches Claude Managed Agents — Public Beta

**Author:** Claude (@claudeai)
**Date:** 2026-04-08
**URL:** https://x.com/claudeai/status/2041927687460024721

## Tweet
> Introducing Claude Managed Agents: everything you need to build and deploy agents at scale. It pairs an agent harness tuned for performance with production infrastructure, so you can go from prototype to launch in days. Now in public beta on the Claude Platform.

## Why it's relevant
This is the biggest Anthropic platform announcement in months. Managed Agents is Anthropic's play to become an agent platform, not just a model provider. Key details from the ecosystem reaction:

- **Diptanu Choudhury** (@diptanu) broke down the architecture: the harness should NOT run in a sandbox, and externalizing it in a durable execution framework allows separate state for session progress — meaning harnesses can restart from where they left off.
- **Paweł Huryn** (@PawelHuryn) called it "Anthropic's AWS moment" — the default agent pattern is a single process (model reasons, calls tools, runs code, holds credentials all in one box). Managed Agents separates these concerns.
- **Angela Jiang** (@angjiang) announced she joined Anthropic to lead product for the Claude Platform — the person steering this ship.
- **Sarah Wooders** (@sarahwooders) from Letta noted the API resembles Letta's year-old design (read-only memory blocks, memory block sharing), but closed-source with provider lock-in.
- **Hila Shmuel** (@HilaShmuel) released Cabinet — an open source alternative within hours.
- **Aaron Levie** (@levie) announced Box + Claude Managed Agents integration for document workflow automation.
- **Notion** (@NotionHQ) announced Claude agents in Notion — "your task board is Claude's to-do list."

## Relevance to Every Consulting
- **Direct infrastructure impact:** We run Claudie on Claude Max. Managed Agents represents a different deployment model — cloud-hosted, API-managed agents. Could be an alternative or complement to our Mac mini setup.
- **Client training:** This is a major capability clients will ask about. Need to understand the API, pricing, and limitations for consulting engagements.
- **Platform risk:** Reinforces our existing concern about Anthropic tightening third-party access. Managed Agents is Anthropic pushing toward owning the full agent stack.
- **Open source alternatives:** Cabinet by Hila Shmuel is worth watching as a hedge.
