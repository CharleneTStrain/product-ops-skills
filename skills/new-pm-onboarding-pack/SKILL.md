---
name: new-pm-onboarding-pack
description: Build an onboarding pack for a new product manager or product team member — the systems, recurring meetings, key docs, people to meet, and a first 30/60/90 days plan — so they're useful in weeks instead of months. Use when someone is onboarding a new PM, product ops hire, or product team member, wants an onboarding doc, a first-90-days plan, a "start here" page, or a list of who to meet.
metadata:
  version: 1.0.0
---

# New PM onboarding pack

A new PM's first month is mostly spent figuring out where things live and who to ask. An onboarding pack hands them the map on day one.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Gather what exists

From the source, collect:

- **Product:** what it does, who buys it, who uses it, main competitors
- **Area they'll own:** scope, current state, open problems, recent decisions
- **Systems:** every tool they'll need, what it's for, how to get access
- **Rituals:** recurring meetings, with purpose and their role in each
- **Docs:** the handful that matter most (strategy, roadmap, metrics glossary, decision log, process docs)
- **People:** who they'll work with, and why each matters

Don't invent people, meetings, or docs. Where something should exist but doesn't (no metrics glossary, no decision log), list it as a gap. That's useful for the manager to see too.

## Step 2: Write the pack

```
# Welcome, [Name] — [Role], [Team]
**Manager:** [name] · **Onboarding buddy:** [name] · **Start date:** [date]

## Start here (read in week one)
1. [Doc] — [why it matters, one line]
2. ...
(Five to seven docs, maximum.)

## The product in one page
- What it does: [plain words]
- Who buys it / who uses it: [roles]
- Main alternatives customers consider: [names]

## Your area
- Scope: [what you own]
- Where it stands: [current state]
- Open questions waiting for you: [list]

## Tools and access
| Tool | What for | How to get access | Ask |

## Recurring meetings
| Meeting | When | Purpose | Your role |

## People to meet in your first two weeks
| Person | Role | Why meet them | What to ask |

## Glossary
- [Internal term]: [plain meaning]
```

## Step 3: The 30 / 60 / 90 plan

```
## First 30 days: learn
- [Specific: sit in on 5 customer calls, read the last 3 retros, shadow support for half a day]

## Days 31–60: contribute
- [Specific: own the next release notes, run one discovery round]

## Days 61–90: lead
- [Specific: present a plan for your area at the next planning cycle]

## How we'll know it's going well
- [Checkable outcomes for each stage]
```

Rules:
- Every "people to meet" row says why, not just who.
- Each 30/60/90 item is something you could check off, not "build relationships."
- Link docs instead of copying them in.
- If the manager hasn't set 30/60/90 goals, draft them and mark them as a draft for the manager to edit.

## Related skills

- **process-documentation** — the SOPs a new hire needs
- **ritual-calendar** — the meetings they'll join
- **information-debt-audit** — check the docs you're handing them are current
