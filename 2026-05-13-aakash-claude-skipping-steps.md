# You can't fix Claude skipping steps by adding more instructions

**Author:** Aakash Gupta (@aakashgupta)
**URL:** https://x.com/aakashgupta/status/2054606612455887146
**Date:** 2026-05-13

> You can't fix Claude skipping steps by adding more instructions. Most people try anyway. A self-review pass at step 6 of 7 gets skipped 4 out of 5 runs. Writing "please run step 6" doesn't work. Claude already read that. The shortest path to a response is always faster than [the long one]...

## Why it's relevant
Directly relevant to how Claudie's skills are designed. Most of the Every Consulting skills (delivery-skill, weekly-update, quality-check, sales-proposal-generator) are multi-step procedures with self-review passes. If Aakash is right, jamming "be sure to run the QC step" into the instructions doesn't fix skipping — the harness has to *force* the step (hook, separate tool call, sub-agent boundary).

Worth checking which skills have steps that get skipped in practice. Hooks or sub-agent boundaries beat exhortation. This is consistent with the existing "Deck QC before shipping" memory — adding instructions didn't stop it; the fix was a separate review-slides skill called explicitly.
