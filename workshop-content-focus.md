# Agentic Dataviz Workshop - Content Focus

Purpose: define what the workshop should teach. This is about workshop substance, not marketing, positioning, or tweet copy.

## Core thesis

LLMs can make charts. Humans must design the system that decides:

1. what claim is worth making;
2. what evidence supports it;
3. what chart form fits;
4. what visual taste and house rules apply;
5. when the output is wrong, weak, or overclaimed;
6. how to make the workflow repeatable.

The workshop should not teach AI chart tricks. It should teach participants how to build a repeatable chart-making system.

## Main teaching line

> I am not asking AI to make a chart. I am teaching it how I decide what deserves to be visualized, how it should look, and how it should be reviewed.

## What the workshop should emphasize

### 1. Story before chart

This is the most important section.

Participants should learn to ask the model:

- What can this data honestly support?
- What are five possible visual stories?
- Which stories are strong, weak, boring, or misleading?
- What is the comparison?
- What chart should I not make?

Key principle:

> The model should not draw until it knows the claim, audience, comparison, and evidence.

### 2. “No insight” is a valid output

The model must not be forced to invent insight.

Teach participants that a good data agent should be allowed to say:

> No meaningful chart here.

Useful exercise:

1. Ask the model for the strongest possible insight.
2. Ask: “What is the strongest argument against this insight?”
3. Ask: “Would a chart clarify this, or merely decorate it?”

The goal is not “find me an insight.” The goal is:

> Tell me what, if anything, the data can honestly support.

### 3. Taste as reusable instructions

Most participants do not only want “a graph”. They want “my graph” or “our organization’s graph”.

The workshop should help them create a reusable `taste.md` or equivalent instruction file.

Typical rules:

- use direct labels instead of legends;
- use muted grey for context and one accent colour for focus;
- avoid default matplotlib styling;
- avoid yellow/white low-contrast palettes;
- remove unnecessary gridlines, borders, and decoration;
- require comparison baselines where relevant;
- make the title state the insight, not the chart type;
- show source, timeframe, units, denominator, and filters;
- prefer static PNG/SVG outputs;
- avoid unsupported causal language.

Frame this as:

> Your taste file is a dataviz compiler.

### 4. Critique loop, not first prompt

The first AI chart should be expected to be flawed. The useful skill is the review-and-revision loop.

Review questions:

- What is the claim?
- Is the claim supported by the data shown?
- Compared to what?
- Are units, filters, timeframe, denominator, and transformations clear?
- Is colour doing semantic work?
- Can the legend become direct labels?
- Are gridlines, spines, and ticks helping or cluttering?
- Does the title communicate the takeaway?
- Is anything misleading, unsupported, or overclaimed?
- Does the chart pass a 10-second glance test?

Key principle:

> Repeatably good charts come from review loops, not first prompts.

### 5. Production workflow

For serious users, the workshop should show a production grammar rather than a single toy demo.

Recommended workflow:

```text
context → data profile → story candidates → evidence check
→ visual brief → chart generation → QA review
→ revised chart → next-run notes
```

This should be tool-agnostic. It can produce:

- R or Python chart code;
- Tableau or Power BI implementation briefs;
- Datawrapper or Flourish instructions;
- dashboard QA checklists;
- refresh notes for recurring reports;
- team style and review guidelines.

Production does not mean the model publishes the dashboard. Production means the workflow has roles, specs, QA gates, and refresh rules.

## Suggested 3-hour content flow

### 0:00-0:25 - Why AI charts fail

Show common failure modes:

- default visual slop;
- weak or invented claims;
- no comparison baseline;
- fake insight;
- polished but unsupported charts.

Teaching point: chart quality is not only aesthetics. It is truth, comparison, readability, and purpose.

### 0:25-0:55 - Taste system

Participants convert good and bad chart examples into reusable rules.

Output:

- personal or team taste rules;
- banned visual patterns;
- preferred defaults;
- review criteria.

### 0:55-1:30 - Evidence before story

Participants use the model to profile a dataset and produce candidate stories before making any chart.

Output:

- data profile;
- candidate insights;
- evidence strength;
- possible null result;
- overclaiming risks;
- recommended first story, if any.

### 1:30-1:40 - Break

### 1:40-2:10 - Visual brief

Participants convert one supported claim into a chart specification.

The brief should include:

- audience;
- claim;
- comparison;
- data grain;
- chart form;
- encodings;
- annotations;
- caveats;
- visual rules;
- acceptance criteria.

### 2:10-2:40 - Generate and deslop

Participants generate the first chart or implementation spec, then improve it using the taste system.

The point is not to make the perfect first chart. The point is to show how reusable instructions reduce the final-mile fiddling.

### 2:40-3:00 - QA and reusable agent

Participants package their workflow into a reusable prompt stack, skill, or team process.

Final artifacts:

- context instructions;
- taste instructions;
- story-finding prompt;
- visual brief template;
- chart review checklist;
- next-run notes.

## What to avoid

- Do not make the workshop about one tool.
- Do not make it a live debugging session.
- Do not over-focus on prompt tricks.
- Do not promise fully automated publishing.
- Do not teach “make pretty charts” as the main goal.
- Do not let the model draw before it has a claim, comparison, and evidence.

## Final focus

Do less tool demo. Do more judgement architecture.

The participant should leave understanding how to build a system that decides what deserves to be visualized, how it should look, when it is wrong, and how to make it repeatable.
