---
date: 2026-04-21
author: Philippe Laban (@PhilippeLaban)
url: https://x.com/PhilippeLaban/status/2046615120332124450
topic: ai-safety, delegated-work, reliability
---

# New paper: "LLMs Corrupt Your Documents When You Delegate"

## Tweet

> LLMs are enabling a new way of working: delegated work, where users supervise an LLM as it edits documents on their behalf. Delegation requires trust: does the LLM complete tasks without introducing errors? We simulate…

## Why relevant

Every Consulting trains clients on delegating document work to AI. This paper is exactly the counter-evidence clients will cite (or that we should proactively cite, given the feedback memory "no fabricated claims"). We need the methodology + numbers before recommending heavy delegation patterns like auto-edit-in-place. Directly shapes guardrails in Natalia's training: "always diff-review, never blind-accept."

## Action

- Read the paper, extract headline error rates by task type
- If rates are material, add a "delegated editing guardrail" slide to training decks
- Feed findings back to Claudie's own behavior: when editing client dashboards, always show the diff
