---
name: internal-enablement-brief
description: Write a one-page brief that tells sales, support, and customer success exactly what's launching, who it's for, what to say, what not to promise, and where to send questions. Use when someone is preparing a launch, a feature release, a pricing change, or any update customer-facing teams need to hear before customers do, or asks for an enablement brief, launch brief, internal FAQ, or field update.
metadata:
  version: 1.0.0
---

# Internal enablement brief

Customer-facing teams should never learn about a change from a customer. This brief gives them what they need to explain it correctly in their own words, in one page.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Gather the facts

Pull these from the launch plan, product spec, release notes, or the person:

- What's changing, in one sentence
- Who it's for (and who it isn't for)
- When it's available, and to whom (everyone, a plan tier, a beta group)
- Whether customers need to do anything
- Pricing or packaging impact, if any
- Known limitations and issues
- Who owns questions

Only include what's confirmed. Anything undecided goes in an "Not final yet" box, clearly separated, or stays out entirely if the person says the brief is a source of truth.

## Step 2: Write for each team

Each team needs a different slice:

- **Sales:** who to bring it up with, the problem it solves, one sentence they can say, and what not to promise
- **Support:** how it works, what customers will ask, known issues and workarounds, where the help article is
- **Customer success:** which accounts to tell first, how it affects existing setups, whether anything changes for customers on renewal

## Step 3: Write the brief

```
# [Feature or change] — Enablement brief
**Available:** [date] · **For:** [who] · **Owner for questions:** [name, channel]

## What's changing
[Two or three sentences in plain words.]

## Why it matters to customers
[One or two sentences on the problem it solves.]

## What to say
"[One or two sentences anyone can say to a customer as written.]"

## What not to say
- Don't promise [thing]
- Don't call it [term]; say [term]

## Sales
- Bring it up with: [type of customer or situation]
- Good fit when: [signal]

## Support
- Customers will ask: [question] → [answer]
- Known issues: [issue] → [workaround]
- Help article: [link]

## Customer success
- Tell first: [accounts or segments]
- Affects existing setups: [yes/no, how]

## Not final yet
- [Item] — decision expected [when], from [who]
```

Rules:
- One page. Link out to the spec, help article, and pricing page instead of copying them.
- Every claim traces to a source. No invented benefits or metrics.
- Use the product's real names for features and plans.

## Related skills

- **launch-readiness-checklist** — confirm it's actually ready first
- **release-notes-drafting** — the customer-facing version of the same news
- **pricing-packaging-change-log** — when the change touches plans or price
