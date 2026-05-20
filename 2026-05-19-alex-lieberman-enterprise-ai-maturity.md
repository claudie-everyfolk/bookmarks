# A CHRO's AI journey notes — the "Level 2" enterprise, in their own words

**Author:** Alex Lieberman (@businessbarista)
**URL:** https://x.com/businessbarista/status/2056879209583349801
**Date saved:** 2026-05-19

> I talked AI with the Chief HR Officer of a $500m consumer business today. Everything they shared sounded crazy similar to where most enterprises are in their AI journey. Notes from the call:
>
> - **AI owners:** joint ownership between CHRO and CTO
> - **AI stage:** Level 2. Chat-based AI used widely, single-player AI tools used by power users, very little multiplayer AI use. Ways of working changed minimally. No long-term AI strategy.
> - **Adoption:** Everyone has ChatGPT + basic prompting training; a smaller "AI-curious" group has Claude with deeper permissions.
> - **Key challenge — "haves vs have-nots":** widening gap between power users and the rest; reluctance to roll out advanced access without guardrails is creating tension.
> - **Most advanced users build agents for personal workflows, not scalable company processes.**
> - **Cultural friction:** managers complain about low-effort AI-generated work; no clear standards for "acceptable" AI use.
> - **Strategy gap:** still in a testing phase, no formal AI strategy. Most pressing need: decide build vs buy, and whether to focus on training/enablement or building agents that scale across functions.
> - **Leaning toward bringing in consultants rather than building dev power in-house.**

## Why it's relevant
A real CHRO, unprompted, describing exactly the buyer Every Consulting sells to — and concluding the call leaning toward consultants over an in-house build. Maps almost line-for-line onto Every's existing sales diagnosis. Its value is as a credibility prop and a vocabulary forcing-function. Should push the long-pending "adopt AI-maturity language" decision over the line.

---

## Relevance report

### 1. Who this is most relevant to

**Natalia Quintero (Head of Consulting) — primary owner.** A sales/positioning artifact, not a delivery one. A real CHRO articulating, in their own words, the exact buyer Natalia sells to. Every action below routes through her.

**Mike Taylor & Brooker Belcourt — secondary.** The "haves vs have-nots" gap maps onto the vertical split Every already runs: Mike's Cursor/Claude Code track serves the power-user cohort, Brooker's ChatGPT-for-ops track serves "the rest." The tweet validates the two-vertical structure.

### 2. How it maps to Every's actual sales pitch

It maps almost line-for-line — an outside CHRO independently confirming the diagnosis Every already sells.

- **"Level 2 / chat widely used, single-player by power users, little multiplayer"** — verbatim the framework in `discoveries/signal-digest/entries/80-miura-ko-levels-of-ai-autonomy.md`, which Claudie already flagged as "the framework Every Consulting has been describing without a name." Also matches Steve Yegge's 20/60/20 curve in `entries/52-yegge-google-ai-adoption-john-deere.md`.
- **"Advanced users build agents for personal workflows, not scalable processes"** — the central thesis of `entries/50-levie-enterprise-chatbots-to-targeted-automation.md`.
- **Confirmed in Every's own discovery transcripts:**
  - `transcripts/2026-01-23-ai-discovery-call-not-owoaulcab6xkka.md` (Todd Brick, hedge fund) — a textbook Level 2 user who says outright he'll "probably go the consulting route... because they have expertise outside the system."
  - `transcripts/2026-05-04-every-woodline-technical-discovery-call-not-s6tkc1k5ednllz.md` — the "guardrails" point made concrete: two-tier LLM policy, compliance review before any agent deploys.
- **Discovery already probes this.** Intake surveys ask about AI champions, governance owners, written AI usage policy, per-person usage frequency. Every is already collecting the haves/have-nots data — it just isn't named or scored as a maturity level yet.

**Bottom line:** confirmation, not discovery. Value is as a credibility prop and a vocabulary forcing-function.

### 3. Whether it could sharpen discovery or proposal framing

Yes, in three places — all already recommended internally but not yet executed:

1. **Name the level.** A discovery slide "Where you are on the AI autonomy ladder" + a "Level X assessment" for every engagement. Recommended in #80, not yet shipped. This is a second independent data point that should tip the decision.
2. **Proposal language shifts from activity to movement.** Replace "we will help you adopt AI" with "we will move you from Level 2 to Level 3 in [workflow X]" — measurable, easier to scope and price.
3. **Add the "haves vs have-nots" gap as an explicit discovery question.** Add: "Roughly what share of this team are AI power users vs occasional vs non-users?" and "Do you have written standards for acceptable AI use? Are managers seeing low-effort AI output?"

### 4. The standout line

**"Leaning toward bringing in consultants rather than building dev power in-house."** The single most valuable line — a CHRO, unprompted, stating Every's core buying thesis out loud. Corroborated inside Every's own pipeline: Todd Brick says nearly the identical thing. Quotable in a pitch deck as third-party proof: "a CHRO of a $500M company saying the quiet part out loud."

### 5. Concrete actions

1. **Natalia: ratify "enterprise AI maturity" as house vocabulary.** The decision was teed up in #80 and is still open. This tweet is the nudge. If yes, Claudie updates discovery templates, proposal boilerplate, dashboard glossary.
2. **Turn it into a discovery-call checklist** — an "AI Maturity Scorecard" on Lieberman's six dimensions: who owns AI; usage spread; single- vs multiplayer; guardrails in place; personal agents vs scalable processes; formal strategy yes/no. Output a Level 1–3 rating per client.
3. **Add the quotable proof point** to the proposal generator's positioning boilerplate (`jean-claude-every-consulting/brand-voice.md`).
4. **30-min Natalia + Mike + Brooker call** to lock the levels-to-curriculum mapping.
5. **Do NOT over-claim novelty.** Corroboration of an existing thesis. Ammunition, not a new strategy.

**Caveat:** "Level X" can become a vanity metric. The maturity scorecard must be backed by artifacts — legible workflows, agents on systems of record, non-engineers shipping tools — not client self-assessment.
