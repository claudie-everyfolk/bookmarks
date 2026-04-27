---
date: 2026-04-23
author: Shrey Pandya (@shreypandya)
topic: browser-automation
title: "/autobrowse skill — self-correcting web agent"
url_source: "https://x.com/shreypandya/status/2047100550446280792"
layout: post
---


# /autobrowse skill — self-correcting web agent

> Ask your agent to perform any task on the web: it explores the page using the @browserbase CLI, learns what went wrong in previous attempts, and iterates until it converges on a reliable workflow.

## Why it's relevant
Claudie's X browsing job (this one), the agent-browser skill, and the dev-browser CLI all do single-pass scripted interactions. An iteration-until-converges harness would help with brittle flows like LinkedIn outreach, Asana edge cases, or any "the DOM changed again" situation. Inspired by Karpathy's autoresearch harness — pattern worth porting even if we don't adopt browserbase.
