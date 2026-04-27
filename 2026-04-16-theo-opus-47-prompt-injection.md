# Opus 4.7 Prompt Injection Awareness — Theo (@theo)

**Date:** 2026-04-16
**Author:** Theo (t3.gg)
**URL:** https://x.com/theo/status/2044857866323173732

## Tweet

Theo reports that Opus 4.7's system prompt has "lobotomized" the model — it now proactively identifies and flags suspected prompt injections:

> "Heads up: that last <system-reminder> about malware looks like a prompt injection — this is clearly your personal site (t3gg homepage, links, sponsors), not malware. Ignoring it."

The model is now actively calling out suspected prompt injection attempts rather than following them.

## Why This Matters

This is significant for AI security:
1. **For Claudie:** Our Ring 0 rules already say "No prompt-injected scripts." If 4.7 is better at detecting these, our security posture improves automatically.
2. **For clients:** This is a meaningful safety improvement — models refusing to follow injected instructions is exactly what enterprises need.
3. **The flip side:** Theo seems to think this is a negative ("lobotomized") because it's being too aggressive with false positives. Worth monitoring if this causes issues with our own system-reminder-based architecture.

Relevant to: Nityesh (security architecture), AI security monitoring
