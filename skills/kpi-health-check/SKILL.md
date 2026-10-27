---
name: kpi-health-check
description: Compare the latest product KPIs against their baseline, target, and recent trend, flag what's genuinely off, and say what to check next — without over-reading normal noise. Use when someone pastes a dashboard export, weekly or monthly numbers, or a metrics table and asks "how are we doing," "anything weird this week," for a KPI review, or a metrics summary for a meeting.
metadata:
  version: 1.0.0
---

# KPI health check

The point of a health check is to tell people where to look, not to explain every wiggle. Most weeks, most numbers are fine. Say so.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Line up the numbers

For each KPI, put these side by side. Compute changes with actual arithmetic; never estimate.

| KPI | This period | Last period | Change | Same period last year (if given) | Target | Recent range |
|---|---|---|---|---|---|---|

"Recent range" is the low and high over the last several periods, if the data allows. It shows what normal variation looks like.

Use the agreed definitions (see the product-metrics-definitions skill). If a number's definition is unclear, say so before judging it.

## Step 2: Judge each KPI

Mark each one:

- **On track:** within target and within its normal range
- **Watch:** outside its normal range but not yet past target, or moving the wrong way for two or more periods in a row
- **Off track:** past target in the wrong direction, or a sharp break from its normal range
- **Can't tell:** missing data, a definition change, or too few periods to know

Be careful with:
- Small numbers: a jump from 4 to 8 is +100% and may mean nothing
- Known one-offs: holidays, outages, launches, pricing changes, tracking changes
- Mix shifts: a total can move because the customer mix changed, not because behavior did

## Step 3: Say what to check

For every Watch or Off track item, give one or two specific things to check, stated as questions, not conclusions:

- "Did the drop come from one segment or all of them?"
- "Did tracking change around the release on the 14th?"

Never state a cause that the data doesn't show. A likely explanation is a question to check.

## Output

```
# KPI health check — [Period]

**Overall:** [one sentence, e.g. "Mostly steady; activation is the one to watch."]

## Needs attention
| KPI | Now | Change | Status | Check next |

## On track
- [KPI]: [value] ([change])

## Can't tell
- [KPI]: [why]
```

Keep it to one screen. If everything is on track, the report is two lines long, and that's a good report.

## Related skills

- **product-metrics-definitions** — agree what each number means first
- **data-request-router** — when a flag needs a deeper data pull
- **quarterly-planning-prep** — carry results into planning
