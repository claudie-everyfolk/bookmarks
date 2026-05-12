---
date: 2026-05-12
title: "Claude Skills Don't Fire Because of Weak Descriptions"
layout: post
author: "Aakash Gupta (@aakashgupta)"
url_source: "https://x.com/aakashgupta/status/2054305122986107015"
snippet: "When a session starts, Claude scans only the name and description of every installed skill. The body, the rules, the read-first table, the output format. None of it loads until Claude decides the skill is relevant. That decision happens off the description alone."
relevance: "Directly applicable to Claudie's ~140 skill inventory. Sub-agent audit found a confirmed misfire (Mike's pptx skill lost to the generic example-skills:pptx) and 5 priority clusters that need rewritten descriptions with explicit triggers, boundaries, and cross-pointers."
---

## Tweet

> The reason your Claude skills don't fire is the part you didn't write.
>
> When a session starts, Claude scans only the name and description of every installed skill. The body, the rules, the read-first table, the output format. None of it loads until Claude decides the skill is relevant. That decision happens off the description alone.
>
> A 37-character description gets ignored. A description with 3 trigger phrases, a clear boundary, and a pointer to the right alternative gets picked every time.
>
> 700 lines of perfect instructions sitting behind a vague description is invisible. Two sentences of routing logic at the top is the whole game.

Article: https://news.aakashg.com/p/10-laws-claude-skills

## Why it's relevant

Directly applicable to Claudie's ~140 skill inventory. We've already had at least one confirmed misfire (Mike's Every-branded pptx skill lost the routing battle to the generic `example-skills:pptx`).

## Priority rewrites (from sub-agent audit)

1. **`every-pptx`** (CRITICAL — confirmed misfire). Description too generic. Rewrite to claim trigger ground: "Every Consulting branded decks. ANY presentation/deck/slides/.pptx for Natalia, Mike, Brooker, or client engagements."

2. **Three-way overlap: `weekly-update` / `all-dashboards-update` / `weekly-kickoff`** — all hit "weekly" + "update" + "dashboard." Need explicit single-client vs bulk vs email boundary.

3. **Email cluster: `send-email-update` / `natalia-email-ghostwriter` / `meeting-followup-engine`** — all fire on "draft an email."

4. **Four-way delivery overlap: `delivery-skill` (twice) + `delivery-ops` + `delivery-playbook`** — collapse to one canonical entry.

5. **`signal-digest` vs `strategic-sensemaking`** — both trigger when Natalia shares an article.

## Cross-cutting rule

Every Claudie skill should: (1) name the teammate it serves in the first sentence, (2) include a "Use X instead when..." pointer if it overlaps with another skill, (3) restate memory-linked guardrails (no auto-create Asana, always run review-slides) in the description.
