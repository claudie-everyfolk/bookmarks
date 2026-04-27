---
date: 2026-04-08
title: "Scaling Managed Agents: Decoupling the Brain from the Hands"
layout: post
author: "Diptanu Choudhury (@diptanu)"
url_source: "https://x.com/diptanu/status/2041980830814466254"
snippet: "The crux of the whole blog is: 1. The harness should probably not run in a sandbox. 2. Externalizing the harness in a durable execution framework allows to have a separate state for the progress of a session in solving a task. That means a harness can be restarted from where it left off."
relevance: "This is the architectural reasoning behind Managed Agents. The key insight — separating the agent harness from the sandbox — is directly relevant to how we've built Claudie. Our current setup runs the harness (Claude Code) and the execution environment (Mac mini) as one unit. This blog argues for decoupling them, which would make agents more resilient and restartable. The \"durable execution framework\" concept means agent sessions can survive crashes,..."
---
# Scaling Managed Agents: Decoupling the Brain from the Hands

**Author:** Diptanu Choudhury (@diptanu)
**Date:** 2026-04-08
**URL:** https://x.com/diptanu/status/2041980830814466254
**Blog:** https://anthropic.com (Scaling Managed Agents blog)

## Tweet
> The crux of the whole blog is:
> 1. The harness should probably not run in a sandbox.
> 2. Externalizing the harness in a durable execution framework allows to have a separate state for the progress of a session in solving a task. That means a harness can be restarted from where it left off.

## Why it's relevant
This is the architectural reasoning behind Managed Agents. The key insight — separating the agent harness from the sandbox — is directly relevant to how we've built Claudie. Our current setup runs the harness (Claude Code) and the execution environment (Mac mini) as one unit. This blog argues for decoupling them, which would make agents more resilient and restartable.

The "durable execution framework" concept means agent sessions can survive crashes, timeouts, and restarts without losing progress. This is something we've had to work around with our launchd jobs and session logging.

## Relevance to team
- **Nityesh:** Architecture patterns for making Claudie more resilient. The harness-outside-sandbox pattern could inform how we think about our next infra iteration.
- **Mike:** Good teaching material for the tech vertical — shows how production agent systems differ from the single-process prototype pattern.
