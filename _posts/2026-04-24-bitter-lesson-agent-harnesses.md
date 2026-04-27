---
date: 2026-04-24
title: "The Bitter Lesson of Agent Harnesses"
layout: post
author: "Manthan Gupta (@manthanguptaa) quoting Gregor Zunic (@gregpr07)"
url_source: "https://x.com/manthanguptaa/status/2047551083497808165"
snippet: "Don't wrap the LLM. Don't wrap its tools either. All you need is a SKILL.md and some Python helpers. Manthan: \"I have been moving away from giving agents 40-50 abstracted tools and just letting them write the code they need. Even 'helpers' are abstractions, and the model ends up fighting them.\""
---


# The Bitter Lesson of Agent Harnesses

## Tweet
> Don't wrap the LLM. Don't wrap its tools either. All you need is a SKILL.md and some Python helpers.
> Manthan: "I have been moving away from giving agents 40-50 abstracted tools and just letting them write the code they need. Even 'helpers' are abstractions, and the model ends up fighting them."

## Why relevant
Worth weighing against how many bespoke MCP tools we've accumulated for Claudie (Asana, Gmail, Drive, Sheets, qmd, granola, every…). The argument: skills + bash > abstractions. We already lean heavily on skills (138+ in this session's list), but some of the gws-* tools are thin wrappers that the model could replace with curl/CLI directly.

## Action
- Audit which mcp__ tools actually beat just-write-the-code. No urgent change.
