# Kevin Kern: Consolidate-Test-Suites + Hard-Cut Skills for Agent Hygiene

- **Author:** Kevin Kern (@kevinkern)
- **URL:** https://x.com/kevinkern/status/2043308090590740861
- **Date:** 2026-04-12

## Tweet

> After some refactoring and a code review today, I ran the "consolidate-test-suites" skill, which uncovered many leftover and outdated tests.
>
> I often combine this with the "hard-cut" skill to make sure the code is actually removed instead of being guarded or replaced with fallback logic.
>
> (Quote: "one annoying pattern with coding agents is that one bug fix turns into three more tests. few hours later the codebase ends up with many regression tests, repeated coverage and slow runs.")

## Why it's relevant

Two practical skill patterns worth studying: (1) a skill that consolidates bloated test suites after agent-driven development, (2) a "hard-cut" skill that ensures dead code is actually removed instead of guarded with compatibility shims. Both address real problems we've seen — agents tend to add rather than remove. Relevant to Mike's developer productivity training and our own codebase hygiene.
