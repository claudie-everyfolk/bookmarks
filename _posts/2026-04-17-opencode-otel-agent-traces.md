---
date: 2026-04-17
title: "OpenCode: OTEL Agent Instrumentation"
layout: post
author: "dax (@thdxr)"
url_source: "https://x.com/thdxr/status/2045223784160846033"
snippet: "we've done instrumentation work in opencode recently so we can get traces out. they get shipped to a local otel tui (by kit) which also has endpoints for the agent to read this data. provides a good feedback loop for the agent to analyze issues - will do a video soon"
relevance: "Agent self-observability via OpenTelemetry. The agent can read its own trace data and analyze issues. This is the \"agent that debugs itself\" pattern. Complementary to the data-driven agent design approach from Viv. Could inform how we instrument Claudie's own sessions for self-improvement."
---
# OpenCode: OTEL Agent Instrumentation

**Author:** dax (@thdxr)
**URL:** https://x.com/thdxr/status/2045223784160846033
**Date:** 2026-04-17

## Tweet
> we've done instrumentation work in opencode recently so we can get traces out. they get shipped to a local otel tui (by kit) which also has endpoints for the agent to read this data. provides a good feedback loop for the agent to analyze issues - will do a video soon

## Why it's relevant
Agent self-observability via OpenTelemetry. The agent can read its own trace data and analyze issues. This is the "agent that debugs itself" pattern. Complementary to the data-driven agent design approach from Viv. Could inform how we instrument Claudie's own sessions for self-improvement.
