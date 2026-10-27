---
name: duplicate-request-merging
description: Find feature requests, ideas, or tickets that describe the same underlying need in different words, merge them into one clean request, and keep every requester and piece of evidence attached. Use when someone shares a backlog, ideas board, Productboard or Canny export, or request spreadsheet and asks to dedupe, consolidate, clean up, or find duplicates, or wants an accurate count of how many customers asked for something.
metadata:
  version: 1.0.0
---

# Duplicate request merging

The same need gets filed five ways: "CSV export," "download my data," "get reports into Excel," "export button," "send data to finance." Counted separately, each looks minor. Merged, it's one of the top asks. Merging done carelessly, though, hides real differences.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Group by underlying need

Read every request and write the need behind it in plain words. Group requests whose needs match, even if the proposed solutions differ.

Merge when requests share the same:
- **Job:** what the customer is trying to get done
- **Outcome:** what "solved" looks like for them

Don't merge when:
- The same words mean different things ("permissions" for admins vs. for end users)
- One request is a narrow subset of another and needs separate tracking
- They need the same feature but for clearly different reasons that would change how it's built

When unsure, list the pair as "possible duplicate" for a person to decide rather than merging.

## Step 2: Write the merged request

For each group:

```
### [Merged title: the need, in plain words]
- **Need:** [one or two sentences]
- **Variations asked for:** [the different solutions people proposed]
- **Requesters:** [N] — [names or accounts]
- **Segments:** [plan, size, industry, as available]
- **Evidence:** [revenue at stake, quotes, deal or renewal links, as given]
- **Merged from:** [IDs or titles of original requests]
- **Keep as primary:** [ID of the original to keep, usually the oldest or most detailed]
```

Count requesters as unique accounts or people, not original requests. One account filing three times is one requester. Compute counts with real arithmetic.

## Step 3: Output

```
# Request dedupe — [Source] — [Date]

**Summary:** [N] requests reviewed → [N] unique needs · [N] merged groups · [N] possible duplicates

## Merged groups (largest first)
[Entries from Step 2]

## Possible duplicates (need a decision)
| Request A | Request B | Why they might match | Why they might not |

## Unique requests
[Short list]
```

Recommend merges; don't delete or merge records in any tool yourself. Never drop a requester or piece of evidence during a merge.

## Related skills

- **request-intake-triage** — sort new asks first
- **feedback-tagging** — tag the merged requests consistently
- **roadmap-hygiene** — connect merged requests to roadmap items
