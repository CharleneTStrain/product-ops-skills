---
name: experiment-log
description: Record product experiments and A/B tests in a consistent log — hypothesis, setup, success metric, result, and the decision made — so the team stops rerunning old tests and can see what it has learned. Use when someone is planning a test, has results to write up, asks to log an experiment, wants an experiment brief, or asks "have we tested this before?"
---

# Experiment log

An experiment is only useful if someone can find it later and trust what it says. The log is the team's memory of what worked, what didn't, and why.

## Before the test: the brief

Write this before the experiment starts. Writing the success metric after seeing results is how tests get misread.

```
### [Experiment name]
- **Status:** Planned
- **Owner:** [person]
- **Hypothesis:** If we [change], then [audience] will [behavior], because [reason].
- **Primary metric:** [one metric, with its definition]
- **Guardrail metrics:** [what must not get worse]
- **Audience:** [who sees it, how they're split]
- **Variants:** Control: [what]. Test: [what].
- **Success looks like:** [the specific result that would make us ship]
- **Planned run time / sample:** [as set by the owner or analyst]
- **Start date:** [date]
```

Rules:
- One primary metric. If there are three, ask which one decides.
- The hypothesis names a reason. "Let's see what happens" is not a hypothesis.
- Don't set sample size or run time yourself unless asked; record what the owner or analyst set.

## After the test: the result

```
- **Status:** Complete
- **End date:** [date]
- **Result:** [primary metric: control vs test, with the numbers and confidence as reported]
- **Guardrails:** [held / broke, with numbers]
- **What we learned:** [one to three sentences]
- **Decision:** Ship / Don't ship / Iterate / Inconclusive
- **Decided by:** [person]
- **Follow-up:** [next test or action, if any]
```

Rules:
- Report results as given by the analysis. Never round a flat result into a win or call a result significant if the source doesn't say it is.
- "Inconclusive" is a real outcome. Record it as one.
- Negative results stay in the log. They're the most valuable entries for avoiding repeat tests.

## The log

```
# Experiment log

| Name | Area | Hypothesis (short) | Result | Decision | Date | Owner |
|---|---|---|---|---|---|---|
```

When asked whether something has been tested, search the log by area and hypothesis, and answer with matching entries or say plainly that nothing similar is logged.
