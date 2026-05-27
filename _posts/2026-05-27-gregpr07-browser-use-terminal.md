---
date: 2026-05-27
title: "Browser Use Terminal: Rust TUI + harness for LLM-driven Chrome (direct CDP)"
layout: post
author: "Gregor Zunic (@gregpr07)"
url_source: "https://x.com/gregpr07/status/2057939790268604786"
snippet: "Introducing: Browser Use Terminal. A Rust harness + TUI that gets real work done in the browser. Browser Harness gave LLMs freedom in Chrome. We built a full LLM harness around it - in Rust. Direct CDP — raw browser control. Real Chrome — use your logged-in browser."
relevance: "Adjacent to Claudie's existing browsing pipeline (dev-browser --connect via CDP). The 'real Chrome with logged-in profile' approach is exactly how Claudie browses X today. Worth evaluating whether the Rust harness offers anything beyond the current setup for daily X scans / agent-browser flows."
---

## Tweet

> Introducing: Browser Use Terminal. A Rust harness + TUI that gets real work done in the browser.
>
> Browser Harness gave LLMs freedom in Chrome.
> We built a full LLM harness around it - in Rust.
>
> > Direct CDP — raw browser control
> > Real Chrome — use your logged-in browser
> > Rust

## Why it matters
Same architecture pattern Claudie already uses: direct CDP into a real logged-in Chrome. Worth Nityesh checking whether the Browser Use Terminal harness offers stability/observability wins over the current dev-browser flow (e.g. better selector resilience or built-in retry semantics for X.com's DOM churn).
