---
name: launch-readiness-checklist
description: Check whether a feature or product launch is actually ready to ship across every team, and produce a go / no-go readout with owners on every gap. Use when someone asks "are we ready to launch," wants a launch checklist, a readiness review, a pre-launch audit, or is prepping for a go / no-go meeting.
---

# Launch readiness checklist

A launch is ready when every team that touches a customer knows what's changing and has what they need. Engineering finishing the build is one row, not the whole answer.

## Step 1: Size the launch

Ask (or infer from what's given) which tier this is. The tier decides how many rows apply.

| Tier | What it looks like | Rows that apply |
|---|---|---|
| 1, major | New product, pricing change, or something customers must act on | All rows |
| 2, notable | Meaningful new feature for existing customers | All except press and analyst |
| 3, minor | Small improvement or fix | Product, docs, support, release notes |

## Step 2: Walk the checklist

For each row that applies, mark **Ready**, **At risk**, **Not started**, or **Not needed**, and name an owner. Only mark Ready when there's evidence (a link, a date, a confirmation), not an assumption.

**Product and engineering**
- Feature complete and tested in a production-like environment
- Rollout plan set (everyone at once, percentage, or flag)
- Rollback plan exists
- Tracking in place for the metric that defines success

**Documentation**
- Help center article written or updated
- Release notes drafted
- Internal FAQ for customer-facing teams

**Customer-facing teams**
- Support briefed, with known issues and workarounds
- Sales briefed: what it is, who it's for, what not to promise
- Customer success knows which accounts to tell first

**Marketing and comms**
- Positioning and core message approved
- Website, in-app, and email changes scheduled
- Social, press, or analyst plans (Tier 1 only)

**Commercial and legal**
- Pricing and packaging decided and reflected in billing
- Legal, security, or privacy review done if data handling changed

**Measurement**
- Success metric and target written down
- Date set to review results

## Step 3: Write the readout

```
# Launch readiness: [Feature] — [Target date]
Tier: [1/2/3]
Recommendation: GO / GO WITH RISKS / NO-GO

## Blockers (must fix before launch)
- [Item] — Owner: [name] — Due: [date]

## Risks (can launch, but watch)
- [Item] — Owner: [name] — Mitigation: [one line]

## Ready
- [Short list, grouped by team]

## Not needed for this tier
- [Rows skipped]
```

Rules:
- Every open item has exactly one owner. "Marketing" is not an owner; a person is.
- If anything in the source is undecided, list it as a blocker or risk. Do not mark it Ready.
- Recommend NO-GO when any customer-facing team would learn about the change from a customer.
