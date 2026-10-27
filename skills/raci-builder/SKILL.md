---
name: raci-builder
description: Build a RACI chart that makes clear, for each task or decision in a project, who does the work, who signs off, who gives input, and who just needs to know. Use when someone asks for a RACI, a responsibility matrix, "who owns what," role clarity for a project or launch, or when ownership keeps getting dropped between teams.
metadata:
  version: 1.0.0
---

# RACI builder

A RACI exists to end the question "wait, whose job was that?" It only works if every row has exactly one person accountable.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## The four roles

| Letter | Role | Meaning | How many per row |
|---|---|---|---|
| R | Responsible | Does the work | One or more |
| A | Accountable | Makes the final call and owns the outcome | Exactly one |
| C | Consulted | Gives input before it's done (two-way) | As few as possible |
| I | Informed | Told after it's done (one-way) | As needed |

## Step 1: List the rows

Rows are tasks or decisions, not people or teams. Pull them from the project plan, launch checklist, or the person's description. Each row starts with a verb: "Approve final pricing," "Write help center article," "Decide launch date."

Aim for 8 to 20 rows. Fewer means the rows are too broad to settle anything; more means it's become a task list.

## Step 2: List the columns

Columns are people, by name or by role if names aren't known. Prefer names. A team as a column hides who actually owns it.

## Step 3: Fill it in

Use only what the source says or what the person confirms. Where the source is silent, leave the cell blank and list it as an open question. Don't assign accountability on anyone's behalf.

## Step 4: Check the chart

Flag every one of these:

- **No A:** nobody owns the outcome
- **More than one A:** two people think they make the call
- **No R:** nobody does the work
- **A with no R anywhere near them:** the decider is far from the work; check they have what they need
- **Too many C's:** more than three consulted people on a row slows everything down
- **One person who is A on most rows:** a bottleneck
- **A column with no letters:** that person doesn't need to be on the project

## Output

```
# RACI — [Project] — [Date]

| Task or decision | [Name] | [Name] | [Name] | [Name] |
|---|---|---|---|---|
| [Verb + object] | A | R | C | I |

## Flags
- [Row]: [problem] — Suggested fix: [one line]

## Open questions
- [Row]: who is Accountable? Needs decision from: [name]
```

Suggest fixes, but mark them as suggestions. The people on the chart agree to it, not the person who drew it.

## Related skills

- **decision-log** — record decisions the chart says who makes
- **cross-team-dependency-map** — see where ownership gaps cause waiting
- **process-documentation** — put owners into the SOP
