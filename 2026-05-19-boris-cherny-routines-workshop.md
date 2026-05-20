# Boris Cherny: "I'm not doing the prompting — I create the routines that do the prompting"

**Author:** Movez (@0xMovez), quoting Boris Cherny (creator of Claude Code)
**URL:** https://x.com/0xMovez/status/2056723475528630529
**Date saved:** 2026-05-19

> Creator of Claude Code just dropped a 6-min workshop on a new Claude feature during a live session in London.
>
> Boris Cherny: "A lot of my code these days is written by routines. I'm not doing the prompting — I create the routines that do the prompting."
>
> 6 minutes. Free. From a live session.

Related: the Claude Code 2.1.145 changelog (also shipped today) adds `claude agents --json` — outputs live agent sessions as JSON for scripting and automation.

## Why it's relevant
The highest-credibility validation yet of an architecture Claudie already runs. Boris Cherny, Head of Claude Code, describing his own workflow as "build the routine, not the prompt" is exactly Claudie's 20-job launchd fleet. Not a new strategy — confirmation the current architecture is right. The genuinely new, immediately-actionable piece is `claude agents --json` for the job-health-monitor.

---

## Relevance report

**Bottom line:** Not a new find for Claudie's workspace — it's the highest-credibility validation yet of a trajectory already tracked across Signal Digest entries #32, #35, #54 and two prior relevance reports. Boris Cherny personally framing his workflow as "I build routines, not prompts" is the architecture Claudie already runs.

### 1. Who this is most relevant to

- **Nityesh (critical)** — Owns Claudie's scheduling architecture: 20 active `com.claude.*` launchd jobs, the two-file pattern, the Slack-bot threaded-notification wrapper, the `schedule-claude` / `job-dashboard` skills. The only person who can evaluate native Routines vs the launchd pattern and act on `claude agents --json`.
- **Mike Taylor (high)** — Tech Vertical Lead. A Boris Cherny quote is premium, credentialed curriculum material. Signal Digest #54 already recommends a "Routines vs Self-Hosted AI Agents" training module; this is the hook to open it.
- **Natalia (medium)** — Affects the client advisory pitch — "Routines or self-host?" is now a question clients will ask.

### 2. How this maps onto Claudie's own architecture

Cherny's "I create the routines that do the prompting" *is* Claudie's two-file launchd pattern (`plugins/experimental/skills/schedule-claude/skill.md`): a wrapper script running `claude -p` scheduled by a launchd plist. Claudie runs 20 `com.claude.*` jobs — these *are* routines in Cherny's sense:

| Job | Schedule | What it does |
|---|---|---|
| `com.claude.cos-morning` | Weekdays 7:57 AM | Morning brief |
| `com.claude.x-browse` | 4x daily | X.com browsing — produced this bookmark |
| `com.claude.dashboards-update` | Weekdays 8 PM | Client dashboard refresh |
| `com.claude.weekly-kickoff` | Mondays 8 AM | Weekly kickoff email |
| `com.claude.pipeline-refresh` | Daily 7:30 AM | Sales pipeline refresh |
| `com.claude.job-health-monitor` | Daily 10:15 AM | Monitors the other jobs |
| `com.claude.qmd-reindex` | Every 3 hrs | Search index rebuild |

Standing memory `feedback_always_use_launchd.md`: default to local launchd, never the `/schedule` skill — Claudie runs on a dedicated Mac mini needing local file/tool access; Routines run in Anthropic's cloud with no local access. Diary `2026-05-04.md`: *"A job in English does not run. A job in launchd runs."* — the same insight as Cherny's quote.

**Honest framing:** Claudie was doing "routines before Routines." The difference is naming and infrastructure location, not concept. Boris Cherny saying it out loud is external validation that the architecture is right.

### 3. What existing work this connects to

- **Signal Digest #54** (`discoveries/signal-digest/entries/54-claudeai-routines-research-preview.md`) — full analysis of the Anthropic Routines launch. Already recommends: don't migrate wholesale; pilot 2–3 GWS-heavy jobs; add a training module. This tweet is a follow-on — note it there rather than creating a duplicate entry.
- **Two prior relevance reports** on `bookmarks/2026-04-15-claude-code-routines-managed-infra.md` — same conclusions.
- **`schedule-claude/skill.md`** — the canonical launchd two-file pattern; the benchmark any Routines comparison must beat.

### 4. Concrete actions

1. **Note on Signal Digest #54, don't create a new entry.** Cherny's quote validates an existing key-shift, not a new one.
2. **Nityesh — wire up `claude agents --json` now.** `com.claude.job-health-monitor` currently parses logs; `claude agents --json` lets it enumerate live agent sessions programmatically. Low-risk, high-value, fits the existing job.
3. **Nityesh — run the bounded Routines pilot from #54.** Migrate `dashboards-update` or `weekly-kickoff` (GWS-heavy, no dev-browser/local-FS dependency) to native Routines as a side-by-side test. Keep launchd running.
4. **Mike — add a Claude Code training module.** "Routines: build the routine, not the prompt" — open with the Cherny quote, use Claudie's 20-job launchd setup as the self-hosted case study.
5. **Do NOT migrate Claudie wholesale.** Jobs needing dev-browser (x-browse), local filesystem, or qmd cannot run as cloud Routines.

### 5. Client engagement where this lands well

- **Bloomberg** — strongest fit. An executive training session was requested for Bloomberg's demo day; prior custom-GPT sessions reached saturation and they need fresher, higher-level material. "Routines, from the creator of Claude Code" is a credentialed step-up from basic prompting.
- **Woodline** — active engagement; cloud-hosted Routines (no Mac mini required) is the natural answer for a client wanting always-on AI without self-hosted infra.

**Caveat for client conversations:** Routines is research-preview, runs on Anthropic's infra, no published pricing or compliance story. The honest pitch is Every's edge: "we run both the self-hosted and managed patterns, so we can tell you which fits your governance posture."
