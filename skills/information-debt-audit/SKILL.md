---
name: information-debt-audit
description: Audit a set of docs, wikis, dashboards, decks, or folders for information debt — what's outdated, duplicated, conflicting, missing, or ownerless — and produce a prioritized cleanup list. Use when someone says "nobody can find anything," asks to clean up a wiki, Confluence space, Notion workspace, Google Drive, or shared folder, wants a content inventory, or is onboarding and finds conflicting answers.
---

# Information debt audit

Information debt builds up every time something changes and the docs don't. The cost shows up later as wrong answers, repeated questions, and people trusting the wrong page.

This audit uses Abby Covert's three types of information problems (from *How to Make Sense of Any Mess*): **too much** information, **not enough** information, and **not the right** information.

## Step 1: Inventory

List every item in scope. For each, record what's knowable from the source:

| Item | Type | Owner | Last updated | Audience | Links to / from |
|---|---|---|---|---|---|

If owner or last-updated date is missing, record "None" or "Unknown." That is itself a finding.

## Step 2: Diagnose

Tag each item with every problem that applies.

**Too much information**
- Duplicate: two or more items cover the same thing
- Bloated: the answer is buried under history, notes, or tangents
- Orphaned: nothing links to it and nobody would find it

**Not enough information**
- Gap: a question people ask that no item answers
- Stub: started, never finished
- No owner: nobody is responsible for keeping it current

**Not the right information**
- Stale: describes something that has since changed
- Conflicting: says something different from another item on the same topic
- Wrong audience: written for one group, used by another

Only flag "Stale" or "Conflicting" with evidence: a date, a newer source, or two items that disagree. Quote the conflicting lines side by side.

## Step 3: Prioritize

Score each finding on two things:
- **Risk:** what happens if someone trusts it (wrong customer answer = high, minor confusion = low)
- **Reach:** how often it's used or found

High risk + high reach goes first.

## Step 4: Write the readout

```
# Information debt audit: [Scope] — [Date]

## Summary
- [N] items reviewed
- Too much: [N] · Not enough: [N] · Not the right: [N]
- Biggest risk: [one sentence]

## Fix first
| Item | Problem | Evidence | Action | Owner |
|---|---|---|---|---|

## Fix next
[Same table]

## Archive or delete
- [Item] — [reason]

## Gaps to fill
- [Question nobody can answer] — [who should own the answer]
```

Actions are one of: **Update**, **Merge into [item]**, **Archive**, **Assign owner**, **Create**. Every action has a person, not a team.

Never delete or archive anything yourself. Recommend; the owner decides.
