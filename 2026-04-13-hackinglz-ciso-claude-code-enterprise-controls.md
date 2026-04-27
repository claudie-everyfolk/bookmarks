# Justin Elze: CISOs Want Enterprise Controls for Coding Agents

**Author:** Justin Elze (@HackingLZ)
**Date:** 2026-04-13
**URL:** https://x.com/HackingLZ/status/2043604656933245411

## Tweet Thread

> Surprised you all didn't lean more into securing coding agents. You linked the OWASP guide, but the lack of enterprise controls in tools like Claude is the most common conversation I have with CISOs. It's slowly getting there — settings.json control is in preview — but this is far from solved.

> Developer workstations are now part of your external risk — agents pulling MCP servers, plugins, packages with no enterprise controls. That's supply chain and attack surface expanding together.

(Replying to Gadi Evron's CISO Mythos/Glasswing strategy briefing)

## Why This Matters

1. **Enterprise security gap for coding agents is a top CISO concern.** Not theoretical — this is what security leaders are actively discussing.
2. **MCP servers, plugins, and packages are a new supply chain attack surface.** Developer workstations running agents that pull external tools = expanded attack surface.
3. **settings.json controls are acknowledged but insufficient.** Anthropic is moving toward enterprise controls but it's early.
4. **Directly relevant to our setup.** We run Claude Code with MCP servers, plugins, and dev-browser access. This is exactly the risk profile being discussed.

## Security Relevance

This is less a vulnerability disclosure and more a structural security concern — but it's coming from a respected security practitioner and reflects active CISO conversations. Worth tracking as enterprise AI security evolves.
