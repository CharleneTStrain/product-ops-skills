---
name: product-metrics-definitions
description: Write one clear, agreed definition for each product metric — what it measures, the exact formula, the data source, what counts and what doesn't, and who owns it — so every dashboard and meeting means the same thing by the same word. Use when someone asks to define a metric, build a metrics glossary or dictionary, settle a "which number is right" argument, or document KPIs.
---

# Product metrics definitions

Most metric fights aren't about the number. They're about two people using the same word for different things. A definition settles it once.

## Step 1: Collect every version

For each metric in scope, gather every way it's currently being defined or calculated: dashboards, decks, spreadsheets, what people said. If versions differ, list them side by side before writing anything.

| Metric | Where it's used | How it's calculated there | Gives a different number? |
|---|---|---|---|

Don't pick a winner yourself. If versions conflict, show the conflict and name who should decide.

## Step 2: Write the definition

```
### [Metric name]
- **Plain-language meaning:** [one sentence a new hire would understand]
- **Formula:** [exact calculation, e.g. accounts with 1+ active session in 28 days ÷ total paying accounts]
- **Counts:** [what's included]
- **Doesn't count:** [exclusions: test accounts, internal users, free trials, refunds]
- **Time window:** [daily, 7-day rolling, calendar month]
- **Data source:** [system and table or report name]
- **Refreshes:** [how often]
- **Owner:** [person who answers questions and approves changes]
- **Good direction:** [up / down / within a range]
- **Often confused with:** [similar metrics and how they differ]
- **Last changed:** [date and what changed]
```

Rules:
- The plain-language meaning must not use the metric's own name to define it.
- "Active," "engaged," "retained," and "user" always need a precise meaning. Spell it out every time.
- If a field isn't known from the source, write "Unknown — confirm with [likely owner]."
- One metric per entry. If one name covers two calculations, split it into two metrics with different names.

## Step 3: Build the glossary

```
# Product metrics glossary — Last updated [date]

| Metric | Meaning | Owner |
|---|---|---|

[Full definitions below, alphabetical]

## Conflicts to resolve
- [Metric]: [version A] vs [version B] — Decide: [name]
```

When a definition changes, keep the old one under "Last changed" so past reports still make sense.
