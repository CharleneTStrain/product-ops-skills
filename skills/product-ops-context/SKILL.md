---
name: product-ops-context
description: Create or update the product ops context file every other skill in this library reads first — the product, the teams and who decides what, the meeting rhythm, the tools and where things live, the metric definitions, and how launches work. Use at the start of any new project or team before using other product ops skills, when someone says "set up context," "here's how our team works," "remember our tools," "update our context," or "log this change," or whenever a skill keeps asking for the same background. It creates `.agents/product-ops-context.md`.
metadata:
  version: 1.0.0
---

# Product ops context

Every product ops skill needs the same background: what the product is, which teams exist, who makes which calls, which meetings happen when, where docs and tickets live, and what each metric means. This skill writes that down once, in one file, so no other skill has to ask again.

The file lives at `.agents/product-ops-context.md`. If you find it at `.claude/product-ops-context.md` instead, use it and offer to move it.

## Step 1: Check what exists

**If the file exists:** read it, give a three-line summary of what's in it, show the version and the last two changelog entries, and ask which sections to update. Only gather what's needed for those sections.

**If it doesn't exist,** offer two ways to start:

1. **Draft from what's here (faster):** read whatever the person has shared or what's in the project — team pages, onboarding docs, a roadmap export, meeting notes, a tool list — and draft every section. Then ask what's wrong and what's missing.
2. **Build it together:** walk through the sections one at a time, a few questions each.

## Step 2: Fill each section

Use only what the person or their documents say. Anything not given stays as "Not recorded." A context file with gaps is useful; a context file with guesses breaks every skill that trusts it.

```markdown
# Product ops context
**Version:** 1.0 · **Last updated:** [date] · **Owner:** [person who keeps this current]

## Product
- What it is, in one sentence a new hire would understand:
- Who buys it, and who uses it day to day:
- Products, plans, or modules (names as customers see them):
- Stage and size: [e.g. Series B, 40 people, 2 product teams]

## Teams and decisions
| Team | Lead | What they own |
|---|---|---|
- Who decides: scope · launch dates · pricing · roadmap priority · deprecations
- Who must be told before customers hear about a change:

## Operating rhythm
| Meeting | When | Purpose | Output | Owner |
|---|---|---|---|---|
- Planning cycle: [quarterly / six-week / other], next one:
- Release cadence: [continuous / weekly / monthly drop]

## Where things live
| What | Tool | Link or location | Owner |
|---|---|---|---|
Cover: roadmap, tickets, customer feedback, support tickets, docs/wiki, dashboards, decision log, release notes.

## Metrics
| Metric | Definition | Source | Owner |
|---|---|---|---|
Link to the full metric definitions doc if one exists.

## Launches
- Launch tiers and what each requires:
- Who signs off go / no-go:
- Where customers hear about changes: [release notes, email, in-app, CSM]

## Customers
- Segments the team uses:
- Where customer input comes from: [calls, tickets, CAB, surveys, sales]

## Words we use
Team-specific terms and what they mean, so outputs match how the team talks.

## Open questions
Things the team hasn't settled that skills should flag, not guess.

## Changelog
- [date] v1.0 — Created. [what it was drafted from]
```

## Step 3: Rules for the file

- **People, not teams.** Every owner and decider is a named person. "Engineering" is not an owner.
- **Decided vs. discussed.** Only decided processes go in the main sections. Anything still being debated goes under Open questions.
- **Plain words.** Write it so someone outside the team could follow it.
- **One page if possible.** Link to longer docs instead of copying them in.

## Step 4: Save and version

Save to `.agents/product-ops-context.md` (create the `.agents/` folder if needed). On every real change, bump the version (1.0 → 1.1 for edits, 2.0 for a reorg or new team structure) and add a dated changelog line saying what changed and why.

When another skill learns something durable mid-task — a new tool, a changed owner, a new meeting — suggest adding it here rather than letting it get lost in that one output.

## Related skills

Every skill in this library reads this file first. The ones that lean on it most:

- **ritual-calendar** — uses the Operating rhythm section, and can fill it in
- **raci-builder** — uses Teams and decisions, and can fill it in
- **product-metrics-definitions** — writes the full definitions the Metrics section links to
- **tool-stack-audit** — checks and fills Where things live
- **new-pm-onboarding-pack** — turns this file into a day-one pack for a new hire
