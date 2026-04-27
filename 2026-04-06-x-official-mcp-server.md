# X (Twitter) Releases Official MCP Server

**Source:** @XDevelopers, found via search
**Date:** 2026-04-06
**URL:** https://github.com/xdevplatform/xmcp

## Details

X/Twitter officially released XMCP — a local MCP server based on FastMCP that automatically converts the X API's OpenAPI specification into MCP tools.

AI agents can now directly read and operate the X platform via MCP: search tweets, post, view user information, manage bookmarks, send/receive DMs.

A community developer (@spideystreet) who had previously built a CLI + MCP server with 48 agent tools for X will now contribute directly to the official tools.

## Why This Matters

**Relevance to Claudie's setup:**
- We currently browse X through dev-browser (Chrome CDP) which is slow and fragile
- An official MCP server would let Claudie interact with X natively through tool calls
- Could replace the entire dev-browser workflow for X browsing, liking, bookmarking
- Would need to set up OAuth for @claudie_every account

**Action item:** Nityesh should evaluate xmcp as a replacement for dev-browser X browsing

## Detailed Relevance Report

**Who this matters to:** Nityesh (primary — he built and maintains the X browsing infrastructure) and Natalia (she benefits from the Signal Digest and bookmark intelligence Claudie produces from X).

**What it connects to:**

Claudie runs a heavyweight X browsing job (`x-browse.sh`) four times daily via launchd. Each session launches a full `claude -p` session with `--dangerously-skip-permissions`, boots Chrome with CDP, copies a Chrome profile to `/tmp/`, navigates X.com via dev-browser with Playwright Page API calls, and scrapes the feed. The logs show persistent fragility: login flow failures, selector timeouts, browser command timeouts requiring retries, and syntax errors that caused five consecutive failures across Mar 31–Apr 1. Each session consumes significant tokens just navigating DOM elements.

This is Claudie's most resource-intensive scheduled job and its most brittle. It also runs on Nityesh's copied Chrome profile, which creates a session staleness problem — if cookies expire, the whole flow breaks until the profile is re-copied.

**What an official X MCP server would change:**

- Replace dev-browser entirely for X interactions (read feed, like, bookmark, follow, check notifications). Tool calls instead of CDP/Playwright scripts.
- Eliminate Chrome setup, profile copying, login flow handling, and screenshot-based scraping.
- Dramatically reduce token consumption per browse session — no DOM navigation, no waitForTimeout loops, no retry logic.
- Remove the `--dangerously-skip-permissions` requirement if the MCP server is added as a trusted tool in settings.json.
- Make the x-browse job reliable enough to downgrade from "high-maintenance" to "just works."

**Concrete actions:**

1. Nityesh should evaluate xmcp's API coverage against the x-browse.sh requirements (read timeline, like, bookmark, follow, read notifications).
2. If coverage is sufficient, rewrite x-browse.sh to use MCP tool calls, cutting the prompt size roughly in half and eliminating all Chrome/CDP setup.
3. Reassess the platform risk note — fewer tokens per X session means lower exposure to usage limits.
