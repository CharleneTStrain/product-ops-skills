---
name: data-request-router
description: Turn a vague "can I get a number for X?" into a clear data request — the exact question, the metric and definition, the source, and the right person or dashboard to answer it — and check whether the answer already exists before anyone pulls new data. Use when someone asks for data, a metric, a report, a quick number, or an analysis and it's unclear where it lives or who owns it, or when someone is managing a queue of incoming data requests.
metadata:
  version: 1.0.0
---

# Data request router

Most data requests are slow not because the data is hard to get, but because the question is unclear, the answer already exists somewhere, or it went to the wrong person. Routing fixes all three before any query is written.

## Before you start

If `.agents/product-ops-context.md` exists (or `.claude/product-ops-context.md`), read it first. Use the team, owners, tools, meetings, and metric definitions it already has, and only ask for what's missing or specific to this task. If it doesn't exist, go ahead with what you're given, and suggest running **product-ops-context** once so the next skill doesn't have to ask.

## Step 1: Sharpen the question

Turn the ask into a request someone could answer without a follow-up:

| Field | What to capture |
|---|---|
| Asked as | The request in the requester's words |
| Decision it supports | What they'll do with the answer; if unknown, ask |
| Exact question | One question, in plain words |
| Metric | Which metric, using the agreed definition (see product-metrics-definitions) |
| Filters | Time period, segments, plans, regions |
| Comparison | Versus what: last period, target, another segment |
| Precision needed | Ballpark is fine, or must be exact |
| Needed by | Date, and why |

"How's adoption?" becomes "What share of accounts on the Business plan used reporting at least once in September, compared with August?"

If the decision behind the ask is unclear, ask about it first. It often changes what data is actually needed.

## Step 2: Check if it already exists

Before routing, look for:
- An existing dashboard or report that answers it
- A recent analysis, readout, or digest that covered it
- A metric already defined in the glossary

If something exists, point to it and say how current it is. That's the fastest answer.

## Step 3: Route it

| Question type | Usually goes to |
|---|---|
| A number from an existing dashboard | Self-serve: link the dashboard |
| Product usage or behavior | Product analytics owner |
| Revenue, billing, pricing | Finance or RevOps |
| Pipeline or deals | Sales ops or RevOps |
| Support volume or tickets | Support ops |
| Survey or feedback | Research or product ops |
| A new metric that doesn't exist yet | Metric owner to define first, then analytics |

Use the team's actual owners if known. Otherwise, name the type of owner and flag it.

## Output

```
# Data request: [short title]
- **Requester:** [name] · **Needed by:** [date]
- **Decision it supports:** [one line]
- **Question:** [exact question]
- **Metric and definition:** [metric] — [definition or link]
- **Filters:** [period, segments]
- **Compare to:** [baseline]
- **Precision:** [ballpark / exact]

**Already answered?** [Yes: link, last updated] / [No]
**Route to:** [person or team] — [why]
**Questions back to requester:** [if any]
```

Don't run the analysis or estimate the number unless asked. The job here is to get the question to the right place, clearly.

## Related skills

- **product-metrics-definitions** — check whether a definition already exists
- **kpi-health-check** — when the question is really 'is this number off?'
