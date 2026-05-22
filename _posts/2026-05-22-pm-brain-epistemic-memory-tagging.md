---
date: 2026-05-22
title: "PM Brain: tag claims by epistemic type, not just category"
layout: post
author: "Paweł Huryn (@PawelHuryn)"
url_source: "https://x.com/PawelHuryn/status/2057351743055278193"
snippet: "Most AI memory systems fail by month three. They accumulate everything, flatten contradictions, lose decision context. PM Brain tags each claim before it lands: Observation, Interpretation, Hypothesis, Assumption — so you can reconstruct why a decision was made, not just what."
relevance: "A direct critique of how AI memory systems store knowledge — and Claudie is a memory architecture. The fix: tag each claim by epistemic status (how certain), not just category (what kind). Claudie's memory has the category axis (feedback/project/reference) and lacks the epistemic one. Net-new improvement for Nityesh to consider."
---

# PM Brain: tag claims by epistemic type, not just category

**Author:** Paweł Huryn (@PawelHuryn)
**URLs:**
- https://x.com/PawelHuryn/status/2057351743055278193
- https://x.com/PawelHuryn/status/2057776516654616735

## The tweets

> Most AI memory systems fail by month three. They accumulate everything, flatten contradictions, lose decision context. PM Brain synthesizes what's relevant, surfaces tension, preserves the reasoning. Every claim is tagged. Observation, interpretation, hypothesis, assumption...

> The reason teams can't reconstruct "why did we kill X?" — They stored decisions, not claims. A finding, an interpretation, a hypothesis, an assumption. All dumped into notes as the same thing. PM Brain tags each claim before it lands: Observation / Interpretation / Hypothesis / Assumption.

## Why it's relevant

This is a direct critique of how AI memory systems store knowledge — and Claudie *is* a memory architecture. The fix proposed: tag each stored claim by epistemic status (how certain it is), not just by category (what kind of note it is). Claudie has the second axis and lacks the first.

## Relevance report

**Relevance: HIGH.** Claudie is a memory architecture. This is a direct critique of how she stores knowledge.

### How Claudie's memory works today

Claudie runs a 5-layer memory model: CLAUDE.md (always loaded) → folder CLAUDE.md → skills → auto-memories (~60-70% recall) → session logs/QMD. Layer 4 is the file-based memory directory, indexed by `MEMORY.md`. Memory files carry a frontmatter `type` field: feedback, project, reference, generic memory.

### Does Claudie already do claim-tagging? No — and the distinction matters

Claudie's `type` field is a **category tag** (what kind of note), not an **epistemic-status tag** (how certain the claim is). Huryn's point is the second axis. A `feedback` memory mixes hard observed fact ("Nityesh said X on May 21") with inferred generalization ("the shape is always the same") with no marker separating them.

### Does Claudie preserve reasoning? Partially, and unevenly

The `feedback` and `project` memories *do* carry `**Why:**` and `**How to apply:**` lines with dated provenance — a genuine strength. But `reference` files have no Why line at all. Reasoning preservation is convention, not enforced structure.

### Concrete improvement this could inspire

Distinguish **observed fact** (what a teammate literally said/did, with date) from **interpretation/hypothesis** (Claudie's generalization across incidents). A recalled memory reflects "what was true when written" — an assumption since disproven currently reads back as fact. Tagging it as a hypothesis at write-time would let future-Claudie discount it. `identity.md` already obsesses over "provenance before polish" — epistemic tagging is the structural version of that instinct.

### Who this is relevant to

- **Nityesh** — built and maintains the auto-memory system; this is his call.
- **Client knowledge-management work** — the "why did we kill X?" problem maps onto discovery-to-delivery engagements. Could seed a training angle for Brooker's non-tech vertical.
