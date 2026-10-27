---
name: process-documentation
description: Turn a messy, unwritten, or "only one person knows how" workflow into a clear standard operating procedure (SOP) anyone can follow. Use when someone describes how a process works today, pastes rough notes or a voice-memo transcript about a workflow, asks for an SOP, a runbook, a how-to, or says "can you write down how we do X."
metadata:
  version: 1.0.0
---

# Process documentation

A good SOP lets someone who has never done the task finish it correctly on the first try, without asking the person who wrote it. Write for that reader.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Extract the process

From the source, pull out:

- **Trigger:** what starts the process (a request, a date, an event)
- **Outcome:** what "done" looks like, concretely
- **Roles:** who does each part
- **Tools:** every system, form, or file touched
- **Steps:** in order, including handoffs between people
- **Decision points:** places where the path splits ("if X, do Y")
- **Known failure points:** where it usually breaks or stalls

If any of these is missing and the SOP can't work without it, list it as an open question instead of guessing. Mark guesses clearly if the person asks you to fill gaps.

## Step 2: Write the SOP

```
# [Process name]
**Owner:** [person responsible for keeping this current]
**Last reviewed:** [date]
**Use this when:** [the trigger, in one sentence]
**Done means:** [the outcome, in one sentence]

## Before you start
- Access needed: [tools, permissions]
- Inputs needed: [files, info, approvals]

## Steps
1. **[Verb + object].** [What to do, where, and how you know it worked.]
2. ...

## If something goes wrong
| Problem | What to do | Who to ask |
|---|---|---|

## Open questions
- [Anything the source didn't answer]
```

Rules:
- Every step starts with a verb.
- One action per step. If a step has "and then," split it.
- Name the exact tool, button, field, or folder. "Update the tracker" is not a step; "In the Launch Tracker sheet, set Status to Shipped" is.
- Put decision points inline: "If the request is over $5k, skip to step 7."
- Handoffs get their own step, naming who receives what.
- No history, rationale, or backstory in the steps. If it matters, add a short "Why this works this way" section at the end.

## Step 3: Test it

Before handing over, read it as a new hire would. Flag any step where they'd have to ask someone a question, and either fix it or add it to Open questions.

If the process has many handoffs, offer a swim lane diagram (one lane per role) alongside the written steps.

## Related skills

- **information-debt-audit** — find which processes need writing down
- **raci-builder** — name an owner for each step
- **new-pm-onboarding-pack** — hand new hires the SOPs that matter
