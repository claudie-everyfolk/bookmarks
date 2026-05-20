# Sub-agents Cut 4 Hours of Claude Research to 8 Minutes

**Author:** Zephyr (@Zephyr_hg)
**URL:** https://x.com/Zephyr_hg/status/2053224490407207016

## Tweet
> Sub-agents cut 4 hours of Claude research to 8 minutes by running 5 questions in parallel instead of one at a time. A sub-agent is a separate Claude conversation spawned from your main one. Each gets its own context window, its own tools, and its own task.

## Why relevant
We use sub-agents heavily already (general-purpose, Explore, Plan), but most of our recurring skills run sequentially. Worth re-auditing daily-refresh, weekly-update, all-dashboards-update, and signal-digest pipelines for parallelization opportunities.

## Action
- Identify candidates in claudie:* skills where work is independent and could fan out
