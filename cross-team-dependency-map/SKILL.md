---
name: cross-team-dependency-map
description: Map which teams or people are waiting on which others across a project, launch, or quarter — what's needed, by when, and what's at risk — so blockers surface before they slip the date. Use when someone asks who's blocked, wants a dependency map or tracker, is planning a cross-team launch or quarter, or says work keeps stalling between teams.
---

# Cross-team dependency map

Most slipped dates aren't one team being slow. They're one team waiting on another that didn't know it was being waited on. This map makes every wait visible and owned.

## Step 1: List every dependency

Pull from the project plan, notes, tickets, or what the person describes. A dependency is one specific thing one party needs from another.

| # | Needs (team / person) | Waiting on (team / person) | What exactly | Needed by | Status | Agreed? |
|---|---|---|---|---|---|---|

Rules:
- "What exactly" is a deliverable, not a topic: "Final API spec for webhooks," not "API stuff."
- Name a person on both sides whenever the source allows.
- **Agreed?** is Yes only if the source shows the providing side accepted the ask and the date. Otherwise No or Unknown. This column catches most problems.

Status is one of: Delivered, On track, At risk, Late, Not started, Unknown.

## Step 2: Find the risks

Flag:
- **Unagreed:** the provider doesn't know or hasn't confirmed
- **Late or at risk:** needed-by date is close or passed
- **Chains:** A waits on B, who waits on C. The whole chain is only as fast as its slowest link; list the chain in order
- **Hubs:** one team or person that many others are waiting on
- **Circular:** two teams each waiting on the other
- **No date:** needed but nobody said when

## Step 3: Show it

Write the table, then offer a simple visual. A swim lane diagram (one lane per team, arrows for each dependency) or a flow diagram of the chains works well. Mark agreed dependencies solid and unagreed ones dashed.

## Output

```
# Dependency map — [Project] — [Date]

## Needs attention
| # | Needs | Waiting on | What | By | Problem | Next step |

## Chains
- [Team A] → [Team B] → [Team C]: [deliverable], earliest finish [date if known]

## Hubs
- [Team or person]: [N] teams waiting

## On track
[Short table]

## Missing information
- #[N]: [what's unknown] — ask [name]
```

Every "Needs attention" row ends with a next step and a person, usually "Confirm date with [provider]."
