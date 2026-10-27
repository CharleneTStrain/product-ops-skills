---
name: decision-log
description: Capture product and cross-functional decisions as clean, searchable log entries — what was decided, by whom, why, what was ruled out, and when to revisit. Use when someone pastes meeting notes, a Slack thread, or an email chain and wants the decisions pulled out, asks to "log this decision," or wants to check whether something was actually decided.
metadata:
  version: 1.0.0
---

# Decision log

A decision log answers "why did we do it this way?" six months from now, when nobody remembers the meeting. Its value depends on separating what was truly decided from what was only discussed.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Find the decisions

Read the source and sort every candidate into one of three groups:

- **Decided:** someone with the authority to decide said yes, and the source shows it.
- **Leaning:** the group agreed in principle, but nobody confirmed it or a condition is still open.
- **Discussed only:** raised, debated, or suggested, with no conclusion.

Only **Decided** items become log entries. List the other two under "Not yet decided" so they don't get lost or mistaken for decisions.

When in doubt, it is not decided. Agreement in a meeting is not a decision unless the source shows who made the call.

## Step 2: Write each entry

```
### [Short decision title, written as the decision itself]
- **Date:** [when it was decided]
- **Decided by:** [person, not team]
- **Decision:** [one or two sentences, specific enough to act on]
- **Why:** [the reasons given in the source]
- **Ruled out:** [alternatives considered and why they lost]
- **Affects:** [teams, products, or documents that need to change]
- **Revisit:** [date or trigger, e.g. "if churn rises above X," or "none set"]
- **Source:** [link or where it came from]
```

Rules:
- The title is the decision: "Launch to all customers on Nov 4," not "Launch timing discussion."
- Use the source's reasons. Never add your own rationale.
- If "Ruled out" or "Why" isn't in the source, write "Not recorded" rather than filling it in.

## Step 3: Close with open items

```
## Not yet decided
- [Topic] — Status: Leaning / Discussed only — Needs: [who has to decide, and what's missing]
```

## Checking an existing log

If asked whether something was decided, search the log and the source. Answer with the entry if one exists, or say plainly that no decision is recorded and who would need to make it.

## Related skills

- **meeting-to-action-converter** — capture the actions from the same meeting
- **raci-builder** — check the decider had the authority
- **retro-facilitation** — review past decisions in a retro
