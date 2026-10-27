---
name: feedback-tagging
description: Classify raw customer feedback from calls, tickets, surveys, reviews, or interviews into a consistent set of tags (theme, sentiment, type, product area, customer segment) so it can be counted and compared. Use when someone pastes a pile of feedback, a survey export, call notes, or support tickets and wants it organized, coded, or turned into something countable.
metadata:
  version: 1.0.0
---

# Feedback tagging

Tagging turns opinions into data. It only works if the tags are consistent: the same kind of comment gets the same tag every time, no matter who tags it or when.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Set the tag list before tagging

If the person has an existing tag list, use it exactly. Don't invent new tags without flagging them.

If there's no list, build one from a first read of the feedback, then confirm it before tagging everything. Keep it small:

- **Type:** problem, request, praise, question, churn signal
- **Product area:** 5 to 10 areas, named the way the team names them
- **Theme:** 8 to 15 themes, each a specific job or pain ("exporting reports," "permissions setup"), not a vague category ("usability")
- **Sentiment:** positive, neutral, negative, mixed
- **Segment:** whatever the source provides (plan, company size, role, industry)

Write a one-line definition for every theme so the boundaries are clear. Two themes that keep overlapping should be merged.

## Step 2: Tag each piece of feedback

| ID | Source | Customer / segment | Verbatim (short excerpt) | Type | Area | Theme(s) | Sentiment |
|---|---|---|---|---|---|---|---|

Rules:
- One comment can have more than one theme if it truly raises two separate issues. Most should have one.
- Tag what the customer said, not what you think they meant. "It's slow" is a performance comment, not a request for caching.
- Keep the verbatim excerpt short and exact. Never paraphrase inside the verbatim column.
- If a comment doesn't fit any theme, tag it "Other" and list it separately. If several land in Other, that's a new theme.
- Strip personal details (emails, phone numbers) from excerpts.

## Step 3: Summarize the counts

```
# Feedback tagging — [Source] — [Date range] — [N] items

## Top themes
| Theme | Count | % | Sentiment mix | Segments most affected |

## New or emerging
- [Theme from "Other," with count]

## Tag definitions used
- **[Theme]:** [one-line definition]
```

Counts describe what was said in this batch, not the whole customer base. Say so if the sample is small or comes from one channel.

## Related skills

- **voice-of-customer-digest** — summarize the tagged feedback for leadership
- **support-escalation-patterns** — go deeper on ticket themes
- **duplicate-request-merging** — merge requests that show up in the feedback
