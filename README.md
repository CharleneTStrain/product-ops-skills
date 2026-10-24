# Product Ops Skills

A library of Claude skills for product operations work: the launches, decisions, docs, and processes that keep product teams running.

Each skill lives in its own folder with two files:
- `SKILL.md` — the instructions Claude follows
- `README.md` — the problem it solves and what you get

## Skills

| Skill | What it does |
|---|---|
| [Release notes drafting](release-notes-drafting/) | Turns tickets and changelogs into customer-facing release notes |
| [Launch readiness checklist](launch-readiness-checklist/) | Runs a cross-functional go / no-go check with an owner on every gap |
| [Decision log](decision-log/) | Pulls real decisions out of notes and threads, separated from what was only discussed |
| [Process documentation](process-documentation/) | Turns tribal knowledge into an SOP anyone can follow |
| [Information debt audit](information-debt-audit/) | Finds stale, duplicate, conflicting, and ownerless docs and prioritizes the cleanup |

## Using these skills

**Claude Code:** copy a skill folder into `~/.claude/skills/` (for all projects) or `.claude/skills/` inside a project.

**Claude app:** zip the skill folder and upload it under your skills settings.

## Author

Charlene Strain — [LinkedIn](https://www.linkedin.com/in/charlene-strain)
