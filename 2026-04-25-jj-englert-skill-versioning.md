---
date: 2026-04-25
author: JJ Englert (@JJEnglert)
url: https://x.com/JJEnglert/status/2048017933495046399
topic: skill versioning, shared AI skills, change management
---

# Shared AI skills need version updates and changelogs

> If your team shares AI skills across an organization, version updates are not just a technical detail. They are how people know what changed, when it changed, and whether they are using the right version.
>
> Every shared skill should include:
> - Current version number
> - A clear changelog
> - What was fixed, added, or improved
> - The date of the update
> - Why the update matters
>
> We handle this with an official Skill Updater at @tenex_labs. When we want to improve a skill, we can trigger /skill-updater to apply the change, which automatically follows an internal versioning policy, and writes a changelog directly inside the skill folder.
>
> Version history turns invisible changes into visible context. It helps teams trust the skills they are using, adopt updates faster, and stay aligned as shared workflows improve.

## Why it's relevant

Every Consulting ships a lot of skills to clients (claudie:, jean-claude:, client-work:, plus client-specific plugins). We currently don't version them or track changelogs. As clients install + sync these, "is mine up to date?" is going to be a real question — especially for non-technical end users at Applecart, Thrive, etc. who can't read git diffs.

A `/skill-updater` slash command that bumps version + writes changelog into the skill folder would be a small, useful add. Worth probing what tenex_labs ships.

## Concrete actions

- Add a `version:` field + `CHANGELOG.md` convention to skills under `~/skills/` and the consulting plugins
- Pitch this to Nityesh as a workflow improvement before the next major skill rollout to clients
- Look at what tenex_labs publishes — possibly a reusable pattern
