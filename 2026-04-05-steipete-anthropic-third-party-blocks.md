# Anthropic Blocks Third-Party Harness Use on Subscription Plans

**Author:** Peter Steinberger (@steipete), Garry Tan (@garrytan), Vox (@Voxyz_ai)
**Date:** 2026-04-05
**URLs:**
- https://x.com/steipete/status/2040811558427648357
- https://x.com/garrytan/status/2040814033918648656
- https://x.com/Voxyz_ai/status/2040818230676136260

## Tweets

**@steipete:**
> Anthropic now blocks first-party harness use too. claude -p --append-system-prompt 'A personal assistant running inside OpenClaw.' 'is clawd here?' → 400 Third-party apps now draw from your extra usage, not your plan limits. So yeah: bring your own coin.

**@garrytan:**
> This seems messed up actually - when do the boundaries stop moving? Anthropic only allows subscriptions with a real human pressing enter? You're going to have to verify with FaceID?

**@Voxyz_ai:**
> Even using Anthropic's own CLI, if your system prompt mentions a third-party tool, it returns 400. This means Anthropic now detects whether Claude is running through something like OpenClaw. If yes, the usage gets billed separately.

## Why This Is Relevant

**OPERATIONAL RISK for Claudie.** We run `claude -p` with custom system prompts on a Claude Max subscription. If Anthropic starts detecting our scheduled jobs as "third-party" usage, our entire operational model could break. This needs monitoring.

The detection appears to be system-prompt-based — if the prompt mentions a third-party tool name, it triggers the block. Our prompts reference our own internal tools (gws, dev-browser, etc.) but these are invoked locally, not as third-party wrappers. Still worth watching closely.
