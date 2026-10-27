---
name: roadmap-hygiene
description: Review a product roadmap for stale, undated, ownerless, vague, or contradictory items and produce a short cleanup list, so the roadmap people see is one they can trust. Use when someone shares a roadmap export, planning sheet, Jira or Linear view, or Productboard list and asks for a roadmap review, cleanup, audit, or "is this still accurate?"
---

# Roadmap hygiene

A roadmap loses trust one stale item at a time. This check doesn't judge what should be on the roadmap; it judges whether what's on it is clear, current, and owned.

## Step 1: Inventory

For each item, capture what the source shows:

| Item | Status | Owner | Timeframe | Last updated | Linked work | Customer-facing? |
|---|---|---|---|---|---|---|

Record "None" or "Unknown" where a field is empty. Don't fill gaps.

## Step 2: Check each item

Flag every item that has one or more of these problems:

| Problem | What it looks like |
|---|---|
| Stale | Timeframe has passed and status hasn't changed; or no update in a long time |
| No owner | Owner blank, or a team instead of a person |
| No timeframe | No date, quarter, or now / next / later placement |
| Vague | Title doesn't say what changes for customers ("Platform improvements," "Phase 2") |
| No linked work | Marked in progress, but nothing in engineering is linked |
| Contradiction | Says something different from another item, a release note, or a decision on record |
| Zombie | In "later" for many cycles with no movement; likely not happening |
| Overpromise | Customer-facing roadmap shows a date the internal roadmap doesn't support |

Use dates from the source and today's date. Show your evidence for "stale" and "contradiction."

## Step 3: Recommend one action per flagged item

- **Update:** status or date needs refreshing; name who to ask
- **Assign owner:** name who should decide
- **Rewrite:** suggest a clearer title in plain words
- **Merge:** combine with a duplicate
- **Move to later / archive:** for zombies; owner decides
- **Remove from customer-facing view:** for overpromises

Recommend only. Never change, move, or delete roadmap items yourself.

## Output

```
# Roadmap hygiene — [Roadmap name] — [Date]

**Summary:** [N] items reviewed · [N] flagged · Biggest issue: [one sentence]

## Fix before the next review
| Item | Problem | Evidence | Action | Ask |

## Lower priority
[Same table]

## Clean
- [N] items with no issues
```

Customer-facing issues (overpromises, contradictions with public release notes) always go to the top.
