---
name: sprint-review-summary
description: Translate what engineering shipped in a sprint or cycle into a short summary of what it means for customers and the business — what's done, what slipped, and what other teams need to know. Use when someone pastes a sprint board, completed tickets, a cycle report, or demo notes and wants a sprint recap, a stakeholder update, an engineering update for leadership, or "what did we ship?"
metadata:
  version: 1.0.0
---

# Sprint review summary

Engineering reports progress in tickets and points. Everyone else wants to know what changed, what didn't, and whether it affects them. This summary is the translation.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Sort the work

From the source, place every item in one bucket:

| Bucket | What goes here |
|---|---|
| Shipped to customers | Live and usable now |
| Done, not yet released | Complete but behind a flag, waiting on a release, or in beta |
| Carried over | Planned for this sprint and not finished |
| Dropped | Removed from the sprint on purpose |
| Internal | Tech debt, tooling, infrastructure, tests |

Use the status in the source. Don't count an item as shipped unless the source says it's live.

## Step 2: Translate

For shipped and done items, write one plain sentence each:
- What changed, for whom
- Where it shows up, if the source says

For carried-over and dropped items, say what it was and the reason, if given. Don't add reasons that aren't in the source.

Group internal work into one or two lines ("Reliability work on the reporting service"). Name it only if it has a visible effect, like faster load times, and the source says so.

Rules:
- No ticket IDs, story points, or velocity unless the reader is engineering.
- No codenames or internal team names.
- Plain verbs: "you can now," "fixed," "faster," not "implemented," "refactored," "enhanced."

## Step 3: Flag who needs to know

List anything another team should act on: support needs a new help article, sales can now say yes to something, a carried-over item affects a launch date.

## Output

```
# Sprint [N] summary — [Dates]

**In one line:** [the most important outcome]

## Shipped
- [Plain sentence]

## Done, releasing soon
- [Plain sentence] — releasing [when, if known]

## Carried over
- [Item] — [reason, if given]

## Who needs to know
- **Support:** [what]
- **Sales:** [what]
- **[Team]:** [what]

## Behind the scenes
- [One or two lines on internal work]
```

Drop any empty section. Keep the whole summary readable in under a minute.

## Related skills

- **release-notes-drafting** — turn the summary into customer-facing notes
- **roadmap-hygiene** — update the roadmap for what slipped
- **cross-team-dependency-map** — flag what other teams need next
