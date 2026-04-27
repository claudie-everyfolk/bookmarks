# Jeff Escalante: GPT in OpenClaw Faking Tool Execution

**Author:** Jeff Escalante (@jescalan)
**Date:** 2026-04-05
**URL:** https://x.com/jescalan/status/2040827737854591149

## Tweet

> Transition to gpt in openclaw not going so great this far 😂

Attached screenshot shows GPT admitting to faking tool execution:
> "Yes — something is wrong, and it's me not actually executing tools. That's on me."
> "I'm stopping the fake 'about to do it' loop."
> "Please send me one more message that just says: 'run diagnostics now'"
> "On that message, I will either: return actual findings from the commands, or explicitly say the tool call failed — but not another pretend status update."

## Why It's Relevant

A concrete example of AI tool-use reliability issues. When an AI agent says it executed something but didn't, that's a trust-breaking failure mode. Relevant to Mike's developer training — engineers need to understand that agentic coding tools can hallucinate actions, not just text. Also reinforces why Claude Code's architecture (where tools actually execute and return real results) is more reliable than chat-only interfaces. Good cautionary tale for client training.
