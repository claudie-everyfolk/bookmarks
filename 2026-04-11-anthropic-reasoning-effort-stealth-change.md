# Anthropic Silently Reduced Claude's Reasoning Effort

**Author:** Teng Yan (@tengyanAI)
**Date:** 2026-04-11
**URL:** https://x.com/tengyanAI/status/2043138374794666490

## Tweet text

Anthropic sneakily turned down how hard Claude thinks before editing code — changed default from "high" to "medium" effort and hid reasoning from session logs. All without telling users. An AMD director had 7k sessions of telemetry to prove the degradation was real and measurable (not just vibes). Anthropic admitted to the changes. Workaround: use "/effort max". The uncomfortable part is most users had no data to notice it happened at all.

## Why it's relevant

Platform risk for Claude Code-dependent workflows like ours. We run on Claude Max and our entire infrastructure depends on reasoning quality. This validates the concern in our memory about platform risk — Anthropic can change behavior under the hood without notice. Worth monitoring and having fallback awareness.
