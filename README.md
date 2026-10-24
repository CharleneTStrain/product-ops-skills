# Product Ops Skills

A library of Claude skills for product operations work: the launches, decisions, docs, and processes that keep product teams running.

Each skill lives in its own folder with two files:
- `SKILL.md` — the instructions Claude follows
- `README.md` — the problem it solves and what you get

## Skills

| Skill | What it does |
|---|---|
| [Release notes drafting](release-notes-drafting/) | Turns tickets and changelogs into customer-facing release notes |
| [Launch readiness checklist](launch-readiness-checklist/) | Runs a cross-functional go / no-go check with an owner on every gap |
| [Decision log](decision-log/) | Pulls real decisions out of notes and threads, separated from what was only discussed |
| [Process documentation](process-documentation/) | Turns tribal knowledge into an SOP anyone can follow |
| [Information debt audit](information-debt-audit/) | Finds stale, duplicate, conflicting, and ownerless docs and prioritizes the cleanup |
| [Request intake triage](request-intake-triage/) | Sorts incoming requests by need, urgency, and next step, with an owner on each |
| [Feedback tagging](feedback-tagging/) | Classifies raw customer feedback into consistent, countable tags |
| [Voice of customer digest](voice-of-customer-digest/) | A one-screen recurring summary of what customers said and what changed |
| [Meeting to action converter](meeting-to-action-converter/) | Turns meeting notes into action items with one owner and a due date each |
| [RACI builder](raci-builder/) | Builds a who-does / who-decides chart and flags ownership gaps |
| [Product metrics definitions](product-metrics-definitions/) | One agreed definition per metric, so every dashboard means the same thing |
| [KPI health check](kpi-health-check/) | Flags which numbers are actually off and what to check next |
| [Experiment log](experiment-log/) | Briefs before a test, results and decisions after, all searchable |
| [Roadmap hygiene](roadmap-hygiene/) | Finds stale, ownerless, vague, and overpromised roadmap items |
| [Cross-team dependency map](cross-team-dependency-map/) | Shows who's waiting on whom, by when, and what's at risk |
| [Sprint review summary](sprint-review-summary/) | Translates what engineering shipped into what it means for everyone else |
| [Internal enablement brief](internal-enablement-brief/) | One page for sales, support, and success before customers hear about a change |
| [Beta program manager](beta-program-manager/) | Beta plans with exit criteria set up front, tracking, and a go-live readout |
| [Deprecation plan](deprecation-plan/) | Retires a feature with a timeline, customer messages, and a plan for stragglers |
| [Retro facilitation](retro-facilitation/) | Runs a retro that ends with two or three owned changes |
| [Quarterly planning prep](quarterly-planning-prep/) | A pre-read with results, inputs, capacity, and the decisions planning must make |
| [Support escalation patterns](support-escalation-patterns/) | Finds the root causes behind tickets and what would fix each |
| [Tool stack audit](tool-stack-audit/) | Inventories tools, cost, overlap, and owners, with keep / cut recommendations |
| [Vendor evaluation scorecard](vendor-evaluation-scorecard/) | Weighted, evidence-based comparison of vendors and a defensible pick |
| [New PM onboarding pack](new-pm-onboarding-pack/) | A day-one pack and 30/60/90 plan for new product hires |
| [Feature flag tracking](feature-flag-tracking/) | A plain-words register of what's on, for whom, and when it comes out |
| [Duplicate request merging](duplicate-request-merging/) | Merges the same need filed many ways, keeping every requester |
| [Ritual calendar](ritual-calendar/) | Designs or audits a team's meeting rhythm so each one has a purpose and output |
| [Customer advisory board prep](customer-advisory-board-prep/) | Goals, agenda, questions, and follow-through for CAB sessions |
| [Pricing and packaging change log](pricing-packaging-change-log/) | Records every pricing change and tracks it into every system |
| [Data request router](data-request-router/) | Turns "can I get a number?" into a clear, routed request |

## Using these skills

**Claude Code:** copy a skill folder into `~/.claude/skills/` (for all projects) or `.claude/skills/` inside a project.

**Claude app:** zip the skill folder and upload it under your skills settings.

## Author

Charlene Strain — [LinkedIn](https://www.linkedin.com/in/charlene-strain)
