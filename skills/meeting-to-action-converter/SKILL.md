---
name: meeting-to-action-converter
description: Turn meeting notes, transcripts, or recordings summaries into a short recap of action items with one owner and a due date each, plus decisions and open questions. Use when someone pastes meeting notes or a transcript and wants next steps, action items, a recap email, a follow-up message, or asks "what did we agree to?"
metadata:
  version: 1.0.0
---

# Meeting to action converter

Most meetings end with everyone agreeing and nobody owning anything. This skill finds the commitments hidden in the conversation and makes each one specific enough to check off.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Find the commitments

Read the whole source and pull out three kinds of things:

- **Action items:** someone said they would do something, or was asked and agreed
- **Decisions:** a call was made (hand these to the decision-log skill if a full entry is needed)
- **Open questions:** raised but not answered, or parked for later

Only count something as an action item if the source shows someone taking it on. "We should look into X" with no taker is an open question, not an action.

## Step 2: Make each action specific

Every action item needs:

| Field | Rule |
|---|---|
| Action | Starts with a verb; says what "done" looks like |
| Owner | One person, by name. Never a team, never "we," never two names |
| Due | Date from the source. If none was set, write "No date set" |
| Depends on | Another action or person, if the source says |

Rewrite vague actions into checkable ones only using what the source says: "follow up on pricing" becomes "Send Dana the updated pricing sheet" if the notes say that's what was meant. If the source doesn't say, keep it vague and flag it.

If two people both said they'd handle something, list it once with both names and flag "Owner unclear."

## Step 3: Write the recap

```
# [Meeting name] — [Date]
**Attendees:** [names]

## Action items
- [ ] **[Owner]:** [Action] — Due [date]

## Decisions
- [Decision, one line each]

## Open questions
- [Question] — Who can answer: [name, if known]

## Flags
- [Actions with no owner, no date, or an unclear owner]
```

Keep it short enough to paste into chat or email as is. No meeting narrative, no "great discussion," no summary of who said what unless asked.

If the person wants a follow-up message, write it as the recap with one opening line, ready to send.

## Related skills

- **decision-log** — log the decisions in full
- **ritual-calendar** — check the meeting has a clear purpose
- **cross-team-dependency-map** — track actions that block other teams
