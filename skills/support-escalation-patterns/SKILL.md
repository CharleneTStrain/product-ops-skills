---
name: support-escalation-patterns
description: Analyze support tickets and escalations to find which product areas, workflows, or customer types generate the most pain, what's driving it, and which fixes would remove the most tickets. Use when someone shares a ticket export, escalation log, or support data and asks what's causing tickets, where the product is hurting customers, which bugs matter most, or how to reduce support volume.
---

# Support escalation patterns

Support tickets are the most honest product feedback a company gets. Each pattern behind a pile of tickets is something the product, the docs, or onboarding could fix once instead of support answering it a hundred times.

## Step 1: Prepare the data

Confirm what's in the export: date range, ticket count, fields available (category, product area, priority, account, plan, resolution, time to resolve, escalated or not). Note what's missing, since it limits what you can conclude.

Count with real arithmetic. If the data is a file, compute counts in code rather than estimating.

## Step 2: Find the patterns

Group tickets by root cause, not just by the category agents chose. Read ticket text where available, because categories are often applied inconsistently.

For each pattern, classify what would fix it:

| Fix type | Meaning |
|---|---|
| Product bug | Something is broken |
| Product gap | Works as designed, but the design doesn't fit what customers need |
| Usability | Customers can't find it or understand it |
| Docs | The answer exists but help content is missing, wrong, or hard to find |
| Onboarding | Customers weren't set up right from the start |
| Account-specific | One customer's setup or data, not a product issue |

## Step 3: Size and rank

For each pattern:

| Pattern | Tickets | % of total | Escalated | Avg. time to resolve | Accounts affected | Notable accounts | Trend | Fix type |
|---|---|---|---|---|---|---|---|---|

Rank by a mix of volume, escalation rate, time to resolve, and account stakes. Say which you weighted most.

Be careful with:
- One account opening many tickets can look like a pattern
- A spike in one week may be an outage or a release, not an ongoing issue
- Low-volume patterns from high-value accounts can matter more than high-volume ones from trials

## Output

```
# Support patterns — [Date range] — [N] tickets

**Headline:** [The single pattern that would remove the most pain if fixed.]

## Top patterns
| Pattern | Tickets | Escalated | Accounts | Trend | Fix type | Suggested owner |

## What the tickets say
- **[Pattern]:** [one or two sentences, with a short example]

## Quick wins
- [Docs or onboarding fixes that need no engineering]

## Data limits
- [Missing fields, inconsistent categories, short date range]
```

Suggest owners by fix type (engineering, design, docs, onboarding), but don't promise fixes. Strip customer personal details from any examples.
