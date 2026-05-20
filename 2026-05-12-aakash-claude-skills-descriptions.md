# Claude Skills Don't Fire Because of Weak Descriptions

**Author:** Aakash Gupta (@aakashgupta)
**Date:** 2026-05-12
**URL:** https://x.com/aakashgupta/status/2054305122986107015
**Article:** https://news.aakashg.com/p/10-laws-claude-skills

## Tweet

> The reason your Claude skills don't fire is the part you didn't write.
>
> When a session starts, Claude scans only the name and description of every installed skill. The body, the rules, the read-first table, the output format. None of it loads until Claude decides the skill is relevant. That decision happens off the description alone.
>
> A 37-character description gets ignored. A description with 3 trigger phrases, a clear boundary, and a pointer to the right alternative gets picked every time.
>
> This kills PMs because skills overlap. /weekly-review and /stakeholder-update both produce summaries. /activation-analysis and /retention-analysis both touch funnel data. Without explicit "use /Y instead" routing, Claude picks the closest match. You get the wrong artifact and don't notice until you're presenting it.
>
> 700 lines of perfect instructions sitting behind a vague description is invisible. Two sentences of routing logic at the top is the whole game.

## Why it's relevant

Directly applicable to Claudie's ~140 skill inventory. We've already had at least one confirmed misfire (Mike, recent session: the Every-branded pptx skill lost the routing battle to the generic `example-skills:pptx`). This tweet articulates the exact mechanism and prescribes the fix — three trigger phrases, a boundary, and a "use X instead" pointer per description.

## Relevance report (sub-agent)

Reviewed full skill inventory, owner profiles, and recent session logs. Findings:

**Confirmed misfire (smoking gun):** Mike Taylor said *"the above prompt didn't trigger claude to load our plugin — it instead went ahead and loaded the default pptx skill. Looks like Claude's ability to load the right skill at the right time isn't there yet."* The Every pptx skill lost to the more generic-but-explicitly-broad `example-skills:pptx` description.

**Top 5 priority rewrites:**

1. **`slide-deck-creation:every-pptx`** (CRITICAL — confirmed misfire). Description opens "Presentation creation, editing, and analysis for the Every company employees" — vague. Rewrite to claim trigger ground: "Every Consulting branded slide decks. Use for ANY presentation, deck, slides, .pptx work for Natalia/Mike/Brooker/client engagements (Thrive, Bloomberg, Woodline, Applecart, etc.). Triggers: 'make a deck', 'build slides', 'presentation for [client]', 'turn this into slides'. Use `example-skills:pptx` ONLY for non-Every personal pptx work."

2. **Three-way overlap: `claudie:weekly-update` vs `claudie:all-dashboards-update` vs `claudie:weekly-kickoff`** — all say "weekly" + "update" + "dashboard." Each needs explicit boundary + cross-pointer. Single-client refresh vs bulk refresh vs Monday team email.

3. **Email-drafting cluster: `claudie:send-email-update` vs `claudie:natalia-email-ghostwriter` vs `claudie:meeting-followup-engine`** — all fire on "draft an email." Templated weekly update vs Natalia's voice vs meeting follow-ups.

4. **Four-way delivery overlap: `delivery-skill` (twice), `claudie:delivery-ops`, `claudie:delivery-playbook`** — near-identical descriptions. Recommend collapsing to one canonical entry (`claudie:delivery-ops`) and deprecating duplicates.

5. **`signal-digest` vs `strategic-sensemaking`** — both trigger when Natalia shares an article. Add explicit publish-vs-analyze boundary.

**Cross-cutting rules to add to every Claudie skill description:**
- Name the teammate the skill serves in the first sentence (teammate names ARE trigger phrases)
- Every skill in an overlap cluster gets a "Use X instead when…" sentence
- Memory-linked guardrails (no auto-create Asana, always run review-slides) restated in the description so they load even before the body

Hand to Nityesh as a single pass. Clusters 1, 2, and 4 have already caused user-visible failures.

## Action

- Bookmarked + liked + followed @aakashgupta (consistent high-quality Claude skill content)
- Will flag to Nityesh on Slack — he owns skill infrastructure
