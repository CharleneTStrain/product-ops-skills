---
name: vendor-evaluation-scorecard
description: Compare two or more vendors or tools against the same weighted criteria, using evidence from demos, trials, docs, and pricing, and produce a scorecard and recommendation the team can defend. Use when someone is choosing between tools, running a software selection or RFP, comparing vendors, needs evaluation criteria, or wants to turn demo notes into a decision.
---

# Vendor evaluation scorecard

Tool decisions often get made on the best demo or the loudest opinion. A scorecard forces every vendor through the same questions, weighted by what actually matters to this team.

## Step 1: Set criteria before looking at vendors

Agree on criteria and weights first, so they aren't bent to favor a vendor someone already likes. Start from the job the tool must do:

- **Must-haves:** pass/fail. A vendor that fails one is out, regardless of score.
- **Weighted criteria:** typically 5 to 8, weights adding to 100

Common criteria, to adapt:

| Criterion | What to check |
|---|---|
| Core job fit | Does it do the main job well, with our real workflow? |
| Ease of use | Can the people who'll use it daily work it without training? |
| Integrations | Connects to the tools we already depend on |
| Admin and security | Permissions, SSO, data handling, compliance needs |
| Total cost | License, seats, add-ons, implementation, renewal increases |
| Implementation effort | Time and people to set up and migrate |
| Vendor strength | Support quality, roadmap, stability |
| Reporting | Can we get our data out and see what we need? |

Let the person set the weights. Suggest them only if asked, and say they're suggestions.

## Step 2: Gather evidence per vendor

For every criterion, record the evidence and its source: a demo note, trial result, doc page, quote, reference call. "Sales said so" is weaker evidence than "we tested it in the trial." Note which.

Look up current pricing and features rather than relying on memory, since both change often. Cite where each fact came from.

## Step 3: Score

Score each criterion 1 to 5:

| Score | Meaning |
|---|---|
| 5 | Clearly exceeds what we need, with strong evidence |
| 4 | Fully meets it |
| 3 | Meets it with workarounds |
| 2 | Partly meets it |
| 1 | Doesn't meet it, or no evidence |

No evidence scores 1, not 3. Compute weighted totals with real arithmetic.

## Output

```
# Vendor evaluation: [Job] — [Date]

## Must-haves
| Must-have | [Vendor A] | [Vendor B] | [Vendor C] |
Eliminated: [vendor] — failed [must-have]

## Scorecard
| Criterion | Weight | [A] | [B] | [C] |
| **Weighted total** | 100 | | | |

## Evidence
### [Vendor A]
- [Criterion]: [score] — [evidence, source]

## Recommendation
[Vendor], because [reasons tied to the highest-weighted criteria].
Risks: [what could go wrong]. Runner-up: [vendor], if [condition].

## Gaps in evidence
- [What we still don't know and how to find out]
```

If the scores are close, say so. A two-point gap isn't a clear winner; the recommendation should name what would break the tie.
