# Aaron Levie: Background Agents Are the Real Paradigm

**Author:** Aaron Levie (@levie)
**Date:** 2026-04-09
**URL:** https://x.com/levie (multiple tweets, ~5h ago)

## Tweet Text

> Right now the main paradigm that we think of agents in is chatting back and forth, but the biggest use of tokens will come from agents that are just always on running in the background doing work for us, or ones triggered from a workflow. Agents will be working 24/7 in our [organizations].

> Background agents for knowledge work are here. You can use the Box API or MCP to automate any content workflow with Box + Claude Managed Agents. In 2 minutes you can be automating document review processes, data extraction, or connecting content to other IT systems. Crazy times.

> When will we be able to add AI coworkers to Slack to help take on misc operational work? Updating spreadsheets, creating channels, running "cron job" business workflows, conducting Deep Research/Operator-style tasks. Same API as a human (bidirectional DM's, calls, shared links)

## Why This Is Relevant

This is literally Claudie's architecture. Levie — CEO of Box, one of the most prominent enterprise software voices — is describing exactly what Every Consulting has already built: a background agent that runs 24/7, connected to Slack, managing spreadsheets, running cron jobs, handling operational work. The fact that a Box CEO is calling this "the future" validates the approach and suggests the market is about to follow.

The Box + Claude Managed Agents integration is also noteworthy — it signals MCP-based integrations becoming mainstream in enterprise.

**Relevant to:** Nityesh (architecture validation), Natalia (client positioning — "we already have this"), Mike (developer workflow automation patterns)

---

## Deep Relevance Report

**This is already built. We are the case study.**

Claudie is a live implementation of exactly what Levie is describing. Running on a Mac mini at a fixed IP, always on via launchd, Slack-connected, managing Google Sheets dashboards, running cron jobs (email sweeps, signal digests, morning briefs, pipeline refreshes). The architecture decisions were made deliberately: remote cloud agents were explicitly rejected in favor of local launchd because the Mac mini has the file access, credentials, and context that cloud agents don't.

**Who this is most relevant to:**

- **Nityesh (primary):** He built this system and debates its architecture. Levie's framing gives external validation for the architectural bets already made — local persistence, Slack as the interface, spreadsheets as the data layer, cron as the scheduler. Useful for making the case internally for continued investment.
- **Natalia (secondary):** Levie's tweet is a credibility signal for sales conversations — a Fortune 500 CEO is publicly describing what Every Consulting has already productized. That's a positioning asset worth $50k+ in client conversations.
- **Mike (tertiary):** His technical training connects to the "how do you actually build this" question Levie's vision raises.

**Concrete actions:**

1. Natalia should use Levie's framing in client intro decks — "Box's CEO is describing exactly what we've built and deployed for our own operations."
2. Nityesh should consider whether the platform risk (Claude Max dependency, no fallback) needs to be resolved before Claudie is positioned as a client deliverable.
3. The team should document Claudie's architecture as a shareable reference implementation — it's currently implicit in session logs and CLAUDE.md.

**Validation vs. challenge:** This fully validates the approach. The one challenge: Levie describing this as emerging enterprise infrastructure means the window for "we did this first" positioning is narrowing. The team has a 6–12 month head start. Using it now matters.
