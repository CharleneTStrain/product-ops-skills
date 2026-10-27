---
name: deprecation-plan
description: Plan the retirement of a feature, plan, integration, or API version — who's affected, the timeline, what customers move to, the messages they'll get, and how to handle the ones who won't move. Use when someone is sunsetting, deprecating, retiring, or end-of-lifing anything customers use, or needs deprecation emails, a sunset timeline, or a migration plan.
metadata:
  version: 1.0.0
---

# Deprecation plan

Removing something customers use is a launch in reverse, and it needs the same care. The goal is that no customer is surprised, everyone knows what to do instead, and support isn't flooded on the last day.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Size the impact

From the source, establish:

| Question | Answer |
|---|---|
| What's being retired | [Feature, plan, version] |
| Why | [Reason as given] |
| Who uses it | [Count of accounts or users, segments, any named key accounts] |
| How heavily | [Usage data, if available] |
| What replaces it | [Alternative, or "nothing"] |
| What customers must do | [Migrate, change settings, nothing] |
| Contract or pricing impact | [Any customers paying for it? Contractual commitments?] |

If usage data or contract impact is unknown, flag it as the first thing to find out. Don't estimate.

## Step 2: Set the timeline

A typical shape, adjusted to what the person sets:

1. **Internal prep:** support, sales, and CS briefed; help article and migration guide ready
2. **Announcement:** customers told what, why, when, and what to do
3. **Reminders:** at set intervals before the end date
4. **Read-only or soft stop** (if applicable): still visible, can't be changed
5. **End date:** removed
6. **After:** data retention, handling late requests

Give real dates only if the person provides them or the end date. Otherwise, use relative timing ("announcement minus 2 weeks") and flag that dates are needed.

## Step 3: Plan the messages

For each step, list the audience, channel, and message. Draft the customer announcement:

- Lead with what's changing and the date, in the first sentence
- Say what to do instead and link the guide
- Give the reason honestly, in one or two sentences
- Say who to contact
- No euphemisms ("evolving our offering") for removing something

## Step 4: Plan for stragglers

- Who reaches out to heavy users or key accounts directly, and when
- What happens to customers who haven't moved by the end date
- Who can approve an exception, and the limit on exceptions

## Output

```
# Deprecation plan: [Thing] — End date [date]
**Owner:** [person]

## Impact
[Table from Step 1]

## Timeline
| Date | Step | Audience | Channel | Owner |

## Customer announcement (draft)
[Message]

## Straggler plan
- [Steps]

## Open questions
- [Unknowns that block the plan]
```

## Related skills

- **internal-enablement-brief** — brief the teams who'll get the questions
- **pricing-packaging-change-log** — when plans or prices change with it
- **feature-flag-tracking** — stage the turn-off by customer group
- **decision-log** — record why it's being retired
