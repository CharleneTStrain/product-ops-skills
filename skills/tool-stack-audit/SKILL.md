---
name: tool-stack-audit
description: Inventory every tool a product or go-to-market team uses — what it's for, who uses it, what it costs, where it overlaps with others, and who owns it — and recommend what to keep, consolidate, or cut. Use when someone asks for a tool audit, software or SaaS inventory, tech stack review, wants to cut tool spend, find overlapping tools, or figure out who owns which system.
metadata:
  version: 1.0.0
---

# Tool stack audit

Teams add tools one at a time and almost never remove them. An audit shows the whole stack at once, so overlap, unused seats, and ownerless tools become visible.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Inventory

List every tool in scope. Capture what the source shows and mark the rest "Unknown":

| Tool | What it's used for | Team(s) | Owner | Seats paid | Seats active | Annual cost | Renewal date | Contract type | Connects to |
|---|---|---|---|---|---|---|---|---|---|

"What it's used for" is the job, in plain words ("collect in-app feedback"), not the vendor's category name.

Compute totals with real arithmetic.

## Step 2: Find the problems

Flag each tool with any that apply:

- **Overlap:** two or more tools doing the same job. Group them by job.
- **Low use:** many seats paid, few active
- **No owner:** nobody responsible for the contract, setup, or renewal
- **Unknown cost:** nobody knows what it costs
- **Shadow tool:** used by a team but not on any official list
- **Renewal soon:** renewing within the next couple of months, so now is the time to decide
- **Single point of failure:** one person knows how it's set up
- **Data island:** holds important data that doesn't connect to anything else

## Step 3: Recommend

For each tool, one recommendation:

- **Keep:** clear job, used, owned
- **Right-size:** keep, but reduce seats or tier
- **Consolidate into [tool]:** overlap; name which one stays and why
- **Cut:** not used or fully replaced
- **Investigate:** missing information; say what to find out

When recommending consolidation, note what would be lost (features, integrations, data, habits) and what migration would take. A cheaper stack that breaks a workflow isn't a saving.

## Output

```
# Tool stack audit — [Team or scope] — [Date]

**Summary:** [N] tools · [total annual cost] · [N] overlapping jobs · [potential savings, if computable]

## Decide before renewal
| Tool | Renews | Cost | Recommendation | Owner |

## Overlap
- **[Job]:** [Tool A], [Tool B] → Keep [A] because [reason]. Losing: [what]

## All tools
[Inventory table with a Recommendation column]

## Missing information
- [Tool]: [what's unknown] — ask [name]
```

Recommend only. Never cancel, downgrade, or change any tool or contract.

## Related skills

- **vendor-evaluation-scorecard** — compare replacements for tools you cut
- **information-debt-audit** — find docs stranded in retired tools
- **raci-builder** — name an owner for each tool
