# Product Ops Skills for AI Agents

31 open-source skills for the work that keeps product teams running: launches, customer feedback, metrics, planning, decisions, and docs. Built for product ops, product managers, and anyone who ends up owning "how we work." Works with Claude Code, the Claude app, OpenAI Codex, Cursor, and any agent that supports the [Agent Skills spec](https://agentskills.io).

**Browse every skill at [charlenetstrain.github.io/product-ops-skills](https://charlenetstrain.github.io/product-ops-skills/).**

Built by [Charlene Strain](https://www.linkedin.com/in/charlene-strain). Sibling library: [Product Marketing Ops Skills](https://github.com/CharleneTStrain/product-marketing-ops-skills).

**Contributions welcome.** Have a better way to run one of these, or a skill to add? [Open a PR](#contributing) or [request a skill](https://github.com/CharleneTStrain/product-ops-skills/issues/new?template=skill-request.yml).

## Contents

- [What are skills?](#what-are-skills)
- [How the skills work together](#how-the-skills-work-together)
- [The rules every skill follows](#the-rules-every-skill-follows)
- [All skills](#all-skills)
- [Install](#install)
- [Use](#use)
- [Contributing](#contributing)

## What are skills?

A skill is a markdown file of instructions an AI agent follows for one specific job. Add these to your setup, and when you paste in meeting notes, a ticket export, or a roadmap, the agent recognizes the job and does it the same way every time.

## How the skills work together

Everything starts with **product-ops-context**. Run it once and it writes `.agents/product-ops-context.md`: your product, your teams and who decides what, your meeting rhythm, where things live, and what each metric means. Every other skill reads that file first, so it only asks you for what's specific to the task.

```
                       ┌──────────────────────────────────────┐
                       │          product-ops-context         │
                       │    (read by every other skill first) │
                       └───────────────────┬──────────────────┘
                                           │
     ┌─────────────┬─────────────┬─────────┴───┬─────────────┬─────────────┐
     ▼             ▼             ▼             ▼             ▼             ▼
┌───────────┐┌───────────┐┌───────────┐┌───────────┐┌───────────┐┌───────────┐
│ Launches  ││ Feedback  ││ Metrics   ││ Planning  ││ Decisions ││ Knowledge │
│ & releases││ & requests││ & data    ││ & roadmap ││ & owners  ││ & tools   │
├───────────┤├───────────┤├───────────┤├───────────┤├───────────┤├───────────┤
│readiness  ││intake     ││definitions││quarterly  ││decision   ││SOPs       │
│enablement ││duplicates ││kpi-health ││roadmap    ││  log      ││info debt  │
│release    ││tagging    ││experiments││  hygiene  ││meeting →  ││onboarding │
│  notes    ││VoC digest ││data       ││dependency ││  actions  ││tool audit │
│sprint     ││escalations││  requests ││  map      ││RACI       ││vendor     │
│  review   ││CAB prep   ││           ││pricing log││retros     ││  scorecard│
│beta       ││           ││           ││           ││ritual     ││           │
│flags      ││           ││           ││           ││  calendar ││           │
│deprecation││           ││           ││           ││           ││           │
└───────────┘└───────────┘└───────────┘└───────────┘└───────────┘└───────────┘
```

Skills hand off to each other. A few chains that come up most:

- **Feedback tagging → Voice of customer digest:** tag raw feedback, then summarize it for leadership
- **Request intake triage → Duplicate request merging:** sort new asks, then merge them into the backlog with accurate counts
- **Product metrics definitions → KPI health check:** agree on what each number means, then check how it's moving
- **Launch readiness checklist → Internal enablement brief → Release notes drafting:** confirm it's ready, brief the field, tell customers
- **Meeting to action converter → Decision log:** capture actions from a meeting, and log the decisions in full

Each skill ends with a **Related skills** section naming what it hands off to and why.

## The rules every skill follows

- **Every open item gets one named owner.** "Marketing" isn't an owner.
- **"We discussed it" and "we decided it" stay separate.**
- **Nothing gets invented.** If the notes don't say why, the output says "Not recorded."
- **Skills recommend. People decide.**

## All skills

### Start here

| Skill | What it does |
|---|---|
| [Product ops context](skills/product-ops-context/) | Writes down your product, teams, owners, meetings, tools, and metrics once, so every other skill can read it |

### Launches and releases

Getting changes out the door, and making sure every team knows before customers do.

| Skill | What it does |
|---|---|
| [Launch readiness checklist](skills/launch-readiness-checklist/) | Runs a cross-functional go / no-go check with an owner on every gap |
| [Internal enablement brief](skills/internal-enablement-brief/) | One page for sales, support, and success before customers hear about a change |
| [Release notes drafting](skills/release-notes-drafting/) | Turns tickets and changelogs into customer-facing release notes |
| [Sprint review summary](skills/sprint-review-summary/) | Translates what engineering shipped into what it means for everyone else |
| [Beta program manager](skills/beta-program-manager/) | Beta plans with exit criteria set up front, tracking, and a go-live readout |
| [Feature flag tracking](skills/feature-flag-tracking/) | A plain-words register of what's on, for whom, and when it comes out |
| [Deprecation plan](skills/deprecation-plan/) | Retires a feature with a timeline, customer messages, and a plan for stragglers |

### Customer feedback and requests

Turning what customers say and ask for into something the team can count and act on.

| Skill | What it does |
|---|---|
| [Request intake triage](skills/request-intake-triage/) | Sorts incoming requests by need, urgency, and next step, with an owner on each |
| [Duplicate request merging](skills/duplicate-request-merging/) | Merges the same need filed many ways, keeping every requester |
| [Feedback tagging](skills/feedback-tagging/) | Classifies raw customer feedback into consistent, countable tags |
| [Voice of customer digest](skills/voice-of-customer-digest/) | A one-screen recurring summary of what customers said and what changed |
| [Support escalation patterns](skills/support-escalation-patterns/) | Finds the root causes behind tickets and what would fix each |
| [Customer advisory board prep](skills/customer-advisory-board-prep/) | Goals, agenda, questions, and follow-through for CAB sessions |

### Metrics and data

One meaning per number, and a clear path from question to answer.

| Skill | What it does |
|---|---|
| [Product metrics definitions](skills/product-metrics-definitions/) | One agreed definition per metric, so every dashboard means the same thing |
| [KPI health check](skills/kpi-health-check/) | Flags which numbers are actually off and what to check next |
| [Experiment log](skills/experiment-log/) | Briefs before a test, results and decisions after, all searchable |
| [Data request router](skills/data-request-router/) | Turns "can I get a number?" into a clear, routed request |

### Planning and roadmap

Deciding what's next with the right inputs, and keeping the plan trustworthy.

| Skill | What it does |
|---|---|
| [Quarterly planning prep](skills/quarterly-planning-prep/) | A pre-read with results, inputs, capacity, and the decisions planning must make |
| [Roadmap hygiene](skills/roadmap-hygiene/) | Finds stale, ownerless, vague, and overpromised roadmap items |
| [Cross-team dependency map](skills/cross-team-dependency-map/) | Shows who's waiting on whom, by when, and what's at risk |
| [Pricing and packaging change log](skills/pricing-packaging-change-log/) | Records every pricing change and tracks it into every system |

### Decisions and ownership

Who decided, who owns it, and how the team gets better each cycle.

| Skill | What it does |
|---|---|
| [Decision log](skills/decision-log/) | Pulls real decisions out of notes and threads, separated from what was only discussed |
| [Meeting to action converter](skills/meeting-to-action-converter/) | Turns meeting notes into action items with one owner and a due date each |
| [RACI builder](skills/raci-builder/) | Builds a who-does / who-decides chart and flags ownership gaps |
| [Retro facilitation](skills/retro-facilitation/) | Runs a retro that ends with two or three owned changes |
| [Ritual calendar](skills/ritual-calendar/) | Designs or audits a team's meeting rhythm so each one has a purpose and output |

### Knowledge and tools

Docs people can trust, tools that earn their cost, and new hires who get up to speed fast.

| Skill | What it does |
|---|---|
| [Process documentation](skills/process-documentation/) | Turns tribal knowledge into an SOP anyone can follow |
| [Information debt audit](skills/information-debt-audit/) | Finds stale, duplicate, conflicting, and ownerless docs and prioritizes the cleanup |
| [New PM onboarding pack](skills/new-pm-onboarding-pack/) | A day-one pack and 30/60/90 plan for new product hires |
| [Tool stack audit](skills/tool-stack-audit/) | Inventories tools, cost, overlap, and owners, with keep / cut recommendations |
| [Vendor evaluation scorecard](skills/vendor-evaluation-scorecard/) | Weighted, evidence-based comparison of vendors and a defensible pick |

## Install

### Option 1: CLI (recommended)

Use [`npx skills`](https://github.com/vercel-labs/skills) to install into whichever agents you have:

```bash
# Install all skills
npx skills add CharleneTStrain/product-ops-skills

# Install specific skills
npx skills add CharleneTStrain/product-ops-skills --skill decision-log launch-readiness-checklist

# See what's available
npx skills add CharleneTStrain/product-ops-skills --list
```

If you run it from inside a Claude Code session, name the agent so the skills land where Claude Code reads them:

```bash
npx skills add CharleneTStrain/product-ops-skills -a claude-code
```

### Option 2: Claude Code plugin

```
/plugin marketplace add CharleneTStrain/product-ops-skills
/plugin install product-ops-skills
```

Outside an interactive session, use the CLI version:

```bash
claude plugin marketplace add CharleneTStrain/product-ops-skills
claude plugin install product-ops-skills@product-ops-skills
```

### Option 3: Clone and copy

```bash
git clone https://github.com/CharleneTStrain/product-ops-skills.git
cp -r product-ops-skills/skills/* ~/.claude/skills/
```

Use `~/.claude/skills/` for every project, or `.claude/skills/` inside one project.

### Option 4: Claude app

Zip any skill folder from `skills/` and upload it under **Customize → Skills → Upload a skill**. Upload **product-ops-context** too, so the others have something to read.

### Option 5: Fork it

Fork the repo, change the skills to match how your team works, and install from your fork.

## Use

Once installed, ask for the job in plain words:

```
"Set up our product ops context from this onboarding doc"
→ product-ops-context

"Are we ready to launch the new billing page Thursday?"
→ launch-readiness-checklist

"Pull the decisions out of these meeting notes"
→ decision-log

"Here's last month's feedback export — what are customers telling us?"
→ feedback-tagging, then voice-of-customer-digest
```

Or call one directly:

```
/decision-log
/roadmap-hygiene
/kpi-health-check
```

## Contributing

Found a better way to run one of these, or have a skill to add? PRs and issues are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md), and run `./validate-skills.sh` before you open a PR.

## License

[MIT](LICENSE). Use these however you want.
