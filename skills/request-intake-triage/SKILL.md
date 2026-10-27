---
name: request-intake-triage
description: Sort incoming feature requests, asks, and "can we just" messages by source, theme, urgency, and next step, so nothing gets lost and nothing jumps the line without a reason. Use when someone pastes a batch of requests from sales, support, customers, or leadership, asks to triage a backlog or intake queue, or wants to know which asks to act on first.
metadata:
  version: 1.0.0
---

# Request intake triage

Triage is not prioritization. Its job is to make sure every request is understood, sorted, and routed to the right next step, so the people who do prioritize are working from a clean list.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Restate each request

For every item, write one line that says what the requester actually needs, in plain words. Separate the need from the solution they proposed.

| Field | What to capture |
|---|---|
| Request | What they asked for, as written |
| Underlying need | The problem behind it, if the source says |
| Requester | Person and team |
| Source | Sales call, support ticket, customer email, exec, internal |
| Customer(s) | Named accounts affected, if any |
| Evidence | Quotes, ticket counts, revenue at stake, as given |

If the need isn't clear from the source, write "Unclear — ask requester" instead of guessing.

## Step 2: Sort

Tag each request with:

- **Type:** new capability, improvement, bug, question (already possible), out of scope
- **Theme:** the product area or workflow it touches
- **Urgency:** see below
- **Duplicate of:** another request in the batch or backlog, if it is one

Urgency comes only from evidence in the source:

| Urgency | When |
|---|---|
| Now | Blocking a live customer, a signed deal, or a legal/security issue |
| Soon | Named revenue or a renewal at risk, with a date |
| Later | Valid, but no deadline or named stakes |
| Unknown | Requester said it's urgent but gave no reason |

"The VP asked" is not by itself a reason for Now. Mark it Unknown and note who to ask.

## Step 3: Route

Every request gets exactly one next step and one owner:

- **Answer:** it's already possible; send how-to
- **Fix:** it's a bug; route to the team that owns that area
- **Add to backlog:** valid, merge with any duplicate, attach the evidence
- **Clarify:** need more from the requester; say what to ask
- **Decline:** out of scope; say why in one sentence

## Output

```
# Intake triage — [Date] — [N] requests

## Act now
| Request | Need | Requester | Evidence | Next step | Owner |

## Route
[Same table for Fix, Answer, Clarify]

## Add to backlog (grouped by theme)
- **[Theme]** — [N] requests, [accounts]. Merged: [list]

## Decline
- [Request] — [reason]

## Questions to send back
- To [requester]: [exact question]
```

Never promise a delivery date or say something "will be built." Triage records the ask; it doesn't commit to it.

## Related skills

- **duplicate-request-merging** — merge the sorted asks into the backlog with accurate counts
- **feedback-tagging** — use the same tags across requests and feedback
- **data-request-router** — when the ask is really for a number
