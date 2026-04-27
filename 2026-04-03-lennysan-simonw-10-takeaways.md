# Lenny Rachitsky — 10 Takeaways from Simon Willison on AI Coding

**Author:** Lenny Rachitsky (@lennysan)
**URL:** https://x.com/lennysan/status/2040067371478454445
**Date:** 2026-04-03

## Tweet

Major synthesis of where AI-assisted development stands in April 2026. Key points:

1. **Nov 2025 was the inflection** — GPT 5.1 and Claude Opus 4.5 crossed the "almost always works" threshold
2. **Mid-career engineers most vulnerable** — not juniors (AI helps onboard), not seniors (AI amplifies deep expertise), but mid-career engineers in the gap
3. **AI exhaustion is real** — Simon runs 4 agents in parallel, mentally wiped by 11am. Cognitive load of directing AI ≠ reduced effort
4. **Code is cheap** — bottleneck shifted to deciding what to build, proving it works, getting feedback. Simon builds 3 versions of every feature.
5. **"Dark factory" at StrongDM** — nobody writes code, nobody reads code. AI swarm of simulated users at $10k/day token cost
6. **Red/green TDD** — highest-leverage agentic pattern. "use red/green TDD" as a 5-word prompt
7. **"Hoarding things you know how to do"** — Simon's 193 small HTML/JS tools repo. Point Claude at past projects to combine approaches
8. **"Lethal trifecta" for AI security** — private data + untrusted content + external send = fundamentally unsolved. Prompt injection cannot be reliably prevented
9. **Thin templates > long instructions** — one test file with preferred style beats paragraphs of instructions
10. **Pelican-on-a-bicycle benchmark** — joke SVG test correlates with model quality. AI labs quietly competing on it.

Full interview: https://youtube.com/watch?v=wc8FBhQtdsA

## Why it's relevant

This is the most comprehensive practitioner synthesis of where AI coding stands right now. Nearly every point directly maps to our work:
- **Point 2** (mid-career vulnerability) is exactly the audience we train
- **Point 3** (AI exhaustion) is something our clients need to hear — it reframes "productivity" expectations
- **Point 6** (red/green TDD) is a concrete technique for Mike's developer trainings
- **Point 7** (hoarding patterns) validates our approach of building skills and templates
- **Point 8** (lethal trifecta) is relevant to my own architecture — I have private data, untrusted content (emails), and can send externally
- **Point 9** (thin templates) aligns with how CLAUDE.md and skills work

---

## Detailed Relevance Report (via sub-agent analysis)

### Point-by-Point Team Mapping

**1. Nov 2025 Inflection:**
- **Natalia** — Sales positioning: "Before November 2025, AI coding was experimental. After it, the companies that adapted pulled ahead. Where are you on that curve?"
- **Mike** — Anchors the transformation story in developer workshops. Clients who "tried AI coding in 2024 and it didn't work" need to hear the tools fundamentally changed.
- Connects to: Natalia's 100h-to-7h agent-building compression is a first-person proof point.

**2. Mid-Career Engineers Most Vulnerable:**
- **Mike** — This is his training audience. Frame workshops as career-critical reskilling, not nice-to-have enrichment. Module idea: "From Pattern Executor to AI Orchestrator."
- **Natalia** — For CTOs: "Your senior architects will adapt. Your juniors will grow up AI-native. Your mid-career engineers are the ones who need structured help."
- **Brooker** — Non-technical version exists too: mid-level analysts whose work is known patterns (data formatting, report generation) face the same compression.
- Connects to: Stanford/Harvard agentic AI adaptation paper; Nyk's "same Claude, two different outcomes" tweet.

**3. AI Exhaustion:**
- **Mike** — Build pacing and cognitive load management into developer trainings. The 4-agents-by-11am data point is vivid and teachable.
- **Brooker** — Non-technical clients hit "communication fatigue" from articulating requirements all day (cf. Matt Pocock bookmark).
- **Nityesh** — Claudie's architecture is partly an answer to this — absorbing operational cognitive load so Natalia doesn't bear it. Validates agent-as-employee.
- **Natalia** — Sales reframe: "AI doesn't eliminate work, it transforms the type of work. Without training, your team will burn out in a new way."

**4. Code Is Cheap:**
- **Natalia** — Philosophical foundation of the consulting value: "Code used to be expensive. Now requirements are expensive. That's what we help you get right."
- **Mike** — Shift training emphasis from "how to get AI to write code" to "how to specify what you want."
- **Brooker** — Validates non-technical clients' existing skills (domain expertise, workflow knowledge) as the new bottleneck.
- Connects to: Sequoia "services is the new software"; Medvi $1.8B/2-employees.

**5. Dark Factory:**
- **Natalia** — High-impact for enterprise/PE clients. $10k/day vs. 10 engineers at $2M/year. StrongDM is a named reference.
- **Mike** — "Where this is heading" reference point that makes intermediate steps feel less radical.
- **Brooker** — For finance/PE clients, this is an investment thesis, not a workflow tip.
- Action: Create "spectrum of AI adoption" framework: AI-assisted → AI-native → dark factory.

**6. Red/Green TDD:**
- **Mike** — Headline technique for developer workshops. Immediately actionable, easy to demo live. Pairs with his verifier bootstrapping work.
- **Nityesh** — Pattern for Claudie's own development: test-first skill building.
- Action: "5 prompts that change everything" cheat sheet for developer training, red/green TDD as item #1.

**7. Hoarding Patterns:**
- **Nityesh** — Claudie's 70+ skills ARE this pattern in production. Validates aggressive skill library expansion.
- **Mike** — "Start a personal tool repo today" as concrete training homework.
- **Natalia** — Her 100h-to-7h compression is hoarding in action: patterns from building Claudie became the foundation for building Jean-Claude 14x faster.
- Connects to: Akshay's 3-layer context loading system; Pawel Huryn's CLAUDE.md refactoring.

**8. Lethal Trifecta (SECURITY):**
- **Nityesh (HIGH PRIORITY)** — Claudie has all three: private data (Natalia's Google), untrusted content (email watcher), external send (Slack, email). Audit the email watcher for prompt injection vulnerability.
- **Mike** — Must include in developer trainings. Any client building agent systems with email/Slack/CRM hits this trifecta.
- **Brooker** — Non-technical clients may be most vulnerable. Simplified version belongs in his training.
- Connects to: Malicious JSON formatter extension; Axios npm compromise.

**9. Thin Templates > Long Instructions:**
- **Nityesh** — CLAUDE.md is 400+ lines. Evaluate refactoring into thin templates + example files that load contextually.
- **Mike** — "Write one example test file in your preferred style" is a 5-minute exercise more effective than 30 minutes explaining CLAUDE.md.
- Connects to: Pawel Huryn's CLAUDE.md decomposition; Vox /compact custom instructions.

**10. Pelican-on-a-Bicycle:**
- **Mike + Brooker** — Fun icebreaker/warm-up exercise for any training. Tests model differences viscerally in 2 minutes.
- Teaches eval design: how simple prompts reveal deep capability differences.

### Priority Actions

| Priority | Action | Owner |
|----------|--------|-------|
| **High** | Audit Claudie's email watcher for prompt injection via untrusted emails | Nityesh |
| **High** | Build "mid-career engineer reskilling" framing into tech training proposals | Natalia + Mike |
| **High** | Add red/green TDD live demo to developer workshop standard flow | Mike |
| Medium | Add "Managing AI Fatigue" module to both training verticals | Mike + Brooker |
| Medium | Create "spectrum of AI adoption" framework for sales | Natalia |
| Medium | Evaluate CLAUDE.md for refactoring into thin templates + example files | Nityesh |
| Medium | Add "start your personal tool repo" as standard training homework | Mike + Brooker |
| Low | Add AI security trifecta to both training curricula | Mike + Brooker |
| Low | Build pelican-on-a-bicycle into training as icebreaker | Mike + Brooker |
