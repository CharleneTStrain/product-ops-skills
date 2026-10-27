---
name: voice-of-customer-digest
description: Write a short, recurring digest of what customers said this week or month, what changed since last time, and what the product team should look at. Use when someone asks for a voice of customer (VoC) report, a weekly or monthly customer feedback summary, a "what are customers saying" update, or wants to share feedback themes with leadership or the product team.
metadata:
  version: 1.0.0
---

# Voice of customer digest

A VoC digest is read in two minutes by busy people. It succeeds if a reader knows the one or two things customers care about most right now, and whether that's new.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Inputs

Work from tagged feedback (see the feedback-tagging skill), or tag it first if it's raw. Also use the previous digest if one exists, so you can show what changed.

## What goes in

1. **The headline.** The single most important thing customers said this period, in one sentence.
2. **Top themes.** Three to five, ranked by a mix of volume and stakes (a theme from three enterprise renewals can outrank one from thirty free users). Say which you used.
3. **What changed.** New themes, themes growing or shrinking, and anything resolved since last time.
4. **Customer voice.** One or two short, real quotes per top theme. Exact words, no edits beyond trimming. Attribute by segment or account type, not by personal name unless the person asks.
5. **Worth a look.** Specific things the product team could act on or investigate, each tied to a theme.

## What stays out

- Every single comment. Link to the full tagged set instead.
- Your own product recommendations presented as customer requests.
- Counts without context: "12 mentions" means little without the total and the channel.

## Format

```
# Voice of customer — [Period]
**Sources:** [channels] · **Items:** [N] · **Compared to:** [last period]

**Headline:** [One sentence.]

## Top themes
1. **[Theme]** — [count / share], [trend: new / up / steady / down]
   [One sentence on what customers are saying.]
   > "[Short quote]" — [segment]

## What changed
- New: [theme]
- Growing: [theme] ([from] → [to])
- Resolved: [theme] — [what fixed it]

## Worth a look
- [Theme] → [what to investigate or who should see it]

[Link to full tagged feedback]
```

Keep the whole digest under one screen. If it runs long, cut themes, not the headline.

## Related skills

- **feedback-tagging** — tag the raw feedback first
- **support-escalation-patterns** — the ticket side of the same story
- **quarterly-planning-prep** — feed the digest into planning
