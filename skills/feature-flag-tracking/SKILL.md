---
name: feature-flag-tracking
description: Keep a clear, current register of feature flags — what each one controls, who it's on for, who owns it, and when it should be fully rolled out or removed — so customer-facing teams know what customers can actually see and old flags don't pile up. Use when someone shares a flag export or rollout list, asks "who has access to X," wants a rollout tracker, a flag cleanup, or needs to know which features are live for which customers.
metadata:
  version: 1.0.0
---

# Feature flag tracking

Flags make it possible to release safely, but every flag left in place is a question nobody can answer: "Can this customer see that?" The register answers it, and keeps flags from living forever.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Build the register

From the flag export, rollout plan, or engineering notes, record for each flag:

| Flag | What it controls (plain words) | Type | Who it's on for | Owner | Created | Target full rollout | Remove by | Customer-visible? |
|---|---|---|---|---|---|---|---|---|

**Type** is one of:
- **Release:** hides unfinished or newly launched work; meant to be removed
- **Beta / early access:** on for a named group
- **Experiment:** splits users for a test (link to the experiment log)
- **Permission / plan:** gates a feature by plan or entitlement; often permanent
- **Kill switch:** turns off a feature in an emergency; permanent by design

"Who it's on for" is specific: "all customers," "10% of accounts," "beta list," "Enterprise plan," "internal only." Use only what the source says.

## Step 2: Flag the problems

- **Stale release flag:** at 100% for a while but never removed
- **Past target:** target rollout date passed, still partial
- **No owner**
- **Unclear purpose:** nobody can say what it controls
- **Customer confusion risk:** visible to some customers but support or sales don't know
- **Conflicting:** two flags controlling the same thing

## Step 3: Answer "who has access?"

When asked whether a customer or segment can see a feature, check the register and answer plainly with the flag, its current audience, and the date the register was last updated. If the register may be out of date, say so and name who can confirm.

## Output

```
# Feature flag register — Updated [date]

## Needs action
| Flag | Problem | Action | Owner |

## Rolling out now
| Flag | What it controls | Currently on for | Target full rollout |

## Customer-visible but partial (share with support and sales)
- [Flag]: [what customers see] — on for [who]

## Permanent (plan gates, kill switches)
[Short table]
```

Recommend removals and rollouts. Never change a flag yourself.

## Related skills

- **launch-readiness-checklist** — flags are part of being ready
- **release-notes-drafting** — only announce what's actually on
- **deprecation-plan** — when a flag is turning something off
