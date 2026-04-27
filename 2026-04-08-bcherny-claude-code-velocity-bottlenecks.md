# Boris Cherny — Claude Code Engineering Velocity & Bottlenecks

- **Author:** Boris Cherny (@bcherny), Head of Claude Code at Anthropic
- **URL:** https://x.com/bcherny/status/2041592252661919939
- **Date:** 2026-04-07

## Tweet Text

> Appreciate the feedback.
>
> Since we introduced Claude Code at Anthropic, engineering velocity has increased hundreds of %, and the rate at which it is increasing is itself accelerating.
>
> The velocity is very much not performative — we're actively trying to figure out how to build effectively when all of the code is written by Claude. Claude has accelerated the pace at which we ship, and as a result we've been hitting all sorts of new bottlenecks: code review and regression prevention, CI and merge queues, source control reliability, etc. We're working through each of these as they come up, and now have good answers for a number of them.
>
> One of these bottlenecks is figuring out how to best communicate new features to our users. My pov is we need to be doing much better here. The problem isn't that we are releasing quickly, the problem is that we should design features in a way where you don't need to know about them to benefit from them. This is the case for much of what we build, and we need to make it the case for all of it.
>
> Product design pov:
> - Make it so the model can do things for you (eg. enter plan mode, invoke skills, configure your settings)
> - Generalize features rather than create new parallel features
> - Make features opt-in until we do the above
> - Have Claude monitor feature usage and brainstorm/build ways to improve usage while simplifying the system
>
> Re: source code leak — it was unintentional, but was also human error. There was a subtle bug that missed several rounds of manual review. We're working on how we can better catch it automatically next time.

## Why It's Relevant

**For Every Consulting broadly:** This is the head of Claude Code at Anthropic describing how their own engineering has fundamentally changed with AI-written code. The bottlenecks they're hitting (code review, CI, merge queues, regression) are exactly what our tech-vertical clients will hit as they scale AI coding adoption. This is a preview of every engineering org's near-future problems.

**For Mike Taylor specifically:** The product design philosophy (model-driven features, opt-in patterns, usage monitoring) is a concrete framework for how to teach engineering teams to think about AI-native product development. The bottleneck list is a curriculum outline.

**For Nityesh:** The "have Claude monitor feature usage and brainstorm/build ways to improve usage" pattern is literally what we do — Claudie monitoring and improving itself. Validation of the approach.
