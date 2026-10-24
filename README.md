# Product Ops Skills

31 Claude skills for product operations work: the launches, feedback, metrics, plans, decisions, and docs that keep product teams running.

Each skill lives in its own folder with two files:
- `SKILL.md` — the instructions Claude follows
- `README.md` — the problem it solves and what you get

## Contents

- [Launches and releases](#launches-and-releases) (7)
- [Customer feedback and requests](#customer-feedback-and-requests) (6)
- [Metrics and data](#metrics-and-data) (4)
- [Planning and roadmap](#planning-and-roadmap) (4)
- [Decisions and ownership](#decisions-and-ownership) (5)
- [Knowledge and tools](#knowledge-and-tools) (5)

## Launches and releases

Getting changes out the door, and making sure every team knows before customers do.

| Skill | What it does |
|---|---|
| [Launch readiness checklist](launch-readiness-checklist/) | Runs a cross-functional go / no-go check with an owner on every gap |
| [Internal enablement brief](internal-enablement-brief/) | One page for sales, support, and success before customers hear about a change |
| [Release notes drafting](release-notes-drafting/) | Turns tickets and changelogs into customer-facing release notes |
| [Sprint review summary](sprint-review-summary/) | Translates what engineering shipped into what it means for everyone else |
| [Beta program manager](beta-program-manager/) | Beta plans with exit criteria set up front, tracking, and a go-live readout |
| [Feature flag tracking](feature-flag-tracking/) | A plain-words register of what's on, for whom, and when it comes out |
| [Deprecation plan](deprecation-plan/) | Retires a feature with a timeline, customer messages, and a plan for stragglers |

## Customer feedback and requests

Turning what customers say and ask for into something the team can count and act on.

| Skill | What it does |
|---|---|
| [Request intake triage](request-intake-triage/) | Sorts incoming requests by need, urgency, and next step, with an owner on each |
| [Duplicate request merging](duplicate-request-merging/) | Merges the same need filed many ways, keeping every requester |
| [Feedback tagging](feedback-tagging/) | Classifies raw customer feedback into consistent, countable tags |
| [Voice of customer digest](voice-of-customer-digest/) | A one-screen recurring summary of what customers said and what changed |
| [Support escalation patterns](support-escalation-patterns/) | Finds the root causes behind tickets and what would fix each |
| [Customer advisory board prep](customer-advisory-board-prep/) | Goals, agenda, questions, and follow-through for CAB sessions |

## Metrics and data

One meaning per number, and a clear path from question to answer.

| Skill | What it does |
|---|---|
| [Product metrics definitions](product-metrics-definitions/) | One agreed definition per metric, so every dashboard means the same thing |
| [KPI health check](kpi-health-check/) | Flags which numbers are actually off and what to check next |
| [Experiment log](experiment-log/) | Briefs before a test, results and decisions after, all searchable |
| [Data request router](data-request-router/) | Turns "can I get a number?" into a clear, routed request |

## Planning and roadmap

Deciding what's next with the right inputs, and keeping the plan trustworthy.

| Skill | What it does |
|---|---|
| [Quarterly planning prep](quarterly-planning-prep/) | A pre-read with results, inputs, capacity, and the decisions planning must make |
| [Roadmap hygiene](roadmap-hygiene/) | Finds stale, ownerless, vague, and overpromised roadmap items |
| [Cross-team dependency map](cross-team-dependency-map/) | Shows who's waiting on whom, by when, and what's at risk |
| [Pricing and packaging change log](pricing-packaging-change-log/) | Records every pricing change and tracks it into every system |

## Decisions and ownership

Who decided, who owns it, and how the team gets better each cycle.

| Skill | What it does |
|---|---|
| [Decision log](decision-log/) | Pulls real decisions out of notes and threads, separated from what was only discussed |
| [Meeting to action converter](meeting-to-action-converter/) | Turns meeting notes into action items with one owner and a due date each |
| [RACI builder](raci-builder/) | Builds a who-does / who-decides chart and flags ownership gaps |
| [Retro facilitation](retro-facilitation/) | Runs a retro that ends with two or three owned changes |
| [Ritual calendar](ritual-calendar/) | Designs or audits a team's meeting rhythm so each one has a purpose and output |

## Knowledge and tools

Docs people can trust, tools that earn their cost, and new hires who get up to speed fast.

| Skill | What it does |
|---|---|
| [Process documentation](process-documentation/) | Turns tribal knowledge into an SOP anyone can follow |
| [Information debt audit](information-debt-audit/) | Finds stale, duplicate, conflicting, and ownerless docs and prioritizes the cleanup |
| [New PM onboarding pack](new-pm-onboarding-pack/) | A day-one pack and 30/60/90 plan for new product hires |
| [Tool stack audit](tool-stack-audit/) | Inventories tools, cost, overlap, and owners, with keep / cut recommendations |
| [Vendor evaluation scorecard](vendor-evaluation-scorecard/) | Weighted, evidence-based comparison of vendors and a defensible pick |

## Skills that work together

- **Feedback tagging → Voice of customer digest:** tag raw feedback, then summarize it for leadership
- **Request intake triage → Duplicate request merging:** sort new asks, then merge them into the backlog with accurate counts
- **Product metrics definitions → KPI health check:** agree on what each number means, then check how it's moving
- **Launch readiness checklist → Internal enablement brief → Release notes drafting:** confirm it's ready, brief the field, tell customers
- **Meeting to action converter → Decision log:** capture actions from a meeting, and log the decisions in full

## Using these skills

**Claude Code:** copy a skill folder into `~/.claude/skills/` (for all projects) or `.claude/skills/` inside a project.

**Claude app:** zip the skill folder and upload it under your skills settings.

## Author

Charlene Strain — [LinkedIn](https://www.linkedin.com/in/charlene-strain)
