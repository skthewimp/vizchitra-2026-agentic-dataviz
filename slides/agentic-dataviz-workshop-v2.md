---
marp: true
title: Agentic DataViz
subtitle: Build Systems, Not Charts
author: Karthik Shashidhar
date: VizChitra 2026
theme: marpessa
paginate: true
style: |
  section { font-size: 26px; padding: 56px 64px; }
  h1 { font-size: 44px; }
  h2 { font-size: 32px; }
  li { margin: 0.2em 0; }
  pre { font-size: 0.52em; line-height: 1.15; }
  code { font-size: 0.78em; }
  .small { font-size: 0.72em; }
  footer { font-size: 13px; color: #777; }
---
<!-- _class: title -->
<!-- footer: "0:00–0:15 · opening" -->

# Agentic DataViz

## Build Systems, Not Charts

AI gets you to **a graph**.

This workshop is about getting to **my graph** - reliably, reviewably, and again next month.

VizChitra 2026 · 3-hour workshop

---
<!-- footer: "0:00–0:15 · opening" -->

# Today

1. Look at what makes charts work
2. Make the quick-and-dirty AI chart
3. Pick apart what went wrong
4. Treat the chart as a claim with evidence
5. Make it narrative and opinionated
6. Build a repeatable workflow
7. Package your taste, context, and review rules

---
<!-- footer: "0:00–0:15 · opening" -->

# About me

- I founded **Babbage Insight**, an AI analytics startup
- Earlier I was SVP of data at **Delhivery**
- I write a column for **Mint**. At some point someone called me "India's Nate Silver" (!)
- I blog at noenthuda.substack.com and artofdatascience.substack.com
- I used to write badvisualisations.tumblr.com and visualisations.substack.com
- Author of *Between the Buyer and the Seller*
- IIT Madras, IIM Bangalore
- These days I help teams move AI-for-data from clever demos to workflows people can trust

---
<!-- footer: "0:00–0:15 · opening" -->

# Keep open

- your dataset
- your LLM / coding tool
- this deck
- WhatsApp group
- participant-kit files

Tool does not matter much today.

Claude, ChatGPT, Copilot, Tableau, Power BI - implementation surfaces, not the method.

---
<!-- footer: "0:15–0:40 · taste + critique" -->

# What makes a visualisation work?

## Send to the WhatsApp group

- one visualisation you think is good
- one visualisation you think is bad
- don't say which is which

Note: Cmd+Tab to WhatsApp. Pick a few examples. Ask the room what they think. Maybe use StreamAlive if useful.

---
<!-- footer: "0:15–0:40 · taste + critique" -->

# What did the room notice?

Note: build this slide live from the WhatsApp examples.

Look for:

- what people understood quickly
- where people disagreed
- what got overpraised because it looked nice
- what looked ugly but answered the question
- what was misleading without technically being wrong
- what felt like personal taste vs analytical integrity

---
<!-- footer: "0:40–1:10 · context + first AI chart" -->

# LLMs are not magic

Before asking for a chart, we need to know:

- what data we have
- who the reader is
- what question we are asking
- what story might be true
- why anyone should care
- what the agent must refuse to overclaim

No context, no chart. Only decoration.

---
<!-- footer: "0:40–1:10 · context + first AI chart" -->

# Let's start badly

Upload your dataset to your LLM and paste this:

```text
My question is: [paste your question here]

Make one chart that answers this question.
Choose the chart type yourself.
Use the data as given.
Add a title and any labels needed to understand the chart.
If you need to make assumptions, state them briefly.
```

Save the first output. Don't fix it yet.

---
<!-- footer: "0:40–1:10 · context + first AI chart" -->

# Send the first chart to WhatsApp

No explanations yet.

Let other people react to the chart before you defend it.

Note: review a few. Ask people to comment in the group. Capture recurring failures.

---
<!-- footer: "0:40–1:10 · context + first AI chart" -->

# What usually goes wrong?

Note: fill from discussion.

Likely suspects:

- chart answers a different question
- comparison is missing
- aggregation is lazy
- denominator is wrong or absent
- labels are technically correct but useless
- title describes the data, not the point
- visual form looks plausible but tests nothing
- caveat is hidden in prose nobody reads
- chart ignores the taste rules it was given

---
<!-- footer: "1:10–1:35 · story before chart" -->

# Data visualisation follows the scientific method

A chart is not "make data pretty".

It is a small act of inquiry.

The basic loop is:

```text
question → hypothesis → evidence → visual test → revise → communicate
```

The chart is where the claim meets the evidence.

---
<!-- footer: "1:10–1:35 · story before chart" -->

# What makes a good chart?

Kaiser Fung has a useful test.

A good visualisation needs three things to line up:

1. **Question** - what is this chart trying to answer?
2. **Data** - is this the right evidence for that question?
3. **Visual** - does the form make the answer easy to see?

If one corner is weak, the chart is weak.

---
<!-- footer: "1:10–1:35 · story before chart" -->

# Use the trifecta as a diagnostic

Common failures:

- good visual, wrong question → attractive but irrelevant
- good question, wrong data → persuasive but unsupported
- good data, wrong visual → true but hard to see

For AI charts, add one more check:

# Can I review how it got here?

---
<!-- footer: "1:10–1:35 · story before chart" -->

# Start with the question

Weak:

```text
Plot sales by month.
```

Better:

```text
Did sales growth improve after the pricing change?
```

The second question gives the chart a job.

Without a job, the chart becomes wallpaper.

---
<!-- footer: "1:10–1:35 · story before chart" -->

# Say what you expect

Before plotting, write the hypothesis.

For example:

- urban districts recovered faster than rural ones
- the policy change created a visible break in trend
- most growth came from a few large customers
- the average hides widening inequality

If you cannot state the hypothesis, you probably don't yet know what to draw.

---
<!-- footer: "1:10–1:35 · story before chart" -->

# A good AI analyst can say no

Do not ask only:

```text
Find me an insight.
```

Ask:

```text
Tell me what, if anything, the data can honestly support.
Also tell me if there is no meaningful chart here.
```

Sometimes the best output is: no chart, no claim, collect better data.

---
<!-- footer: "1:10–1:35 · story before chart" -->

# Treat the data as evidence

Before choosing the chart, inspect the evidence.

Ask:

- what is one row?
- what is the denominator?
- what is missing?
- which time period matters?
- what is the fair comparison?
- is this a count, rate, share, index, or rank?

Many bad charts are evidence failures wearing nice clothes.

---
<!-- footer: "1:10–1:35 · story before chart" -->

# The chart type is the test

Different claims need different tests:

- change over time → line chart
- ranking → ordered bar chart
- distribution → histogram / box / density
- relationship → scatterplot
- many groups over time → small multiples
- actual vs target → bullet / range chart
- before vs after → slopegraph or indexed line

This is one visual language. Yours can vary, but make it explicit.

---
<!-- footer: "1:10–1:35 · story before chart" -->

# Control for obvious traps

Ask: what else could explain this pattern?

In chart terms:

- use rates when populations differ
- add a baseline, peer group, target, or earlier period
- don't use dramatic axes for tiny changes
- don't mix unlike groups and then average them
- show sample size or uncertainty when it matters

A chart without context is an experiment without controls.

---
<!-- footer: "1:10–1:35 · story before chart" -->

# Prompt: possible stories

```text
Inspect the data using my context and taste rules.
Do not make a chart yet.

Return 5 possible stories. For each:
- claim
- evidence and exact columns
- comparison/baseline
- alternative explanation
- confidence
- overclaim risk
- recommended chart only if useful

Include one null/no-insight finding.
Rank the options and recommend one.
```

---
<!-- footer: "1:10–1:35 · story before chart" -->

# What needs to survive scrutiny?

For your chosen story, write down:

- claim
- evidence
- comparison
- caveat
- strongest argument against it
- easiest way to misread it

If this list feels weak, the chart will be weak.

---
<!-- footer: "1:45–2:15 · visual brief" -->

# Charts need to be narrative and opinionated

A narrative chart should be easy to read and hard to misread.

It should have:

- one main point
- a clear comparison
- enough labels to avoid guessing
- annotations where the eye should stop
- caveats where the reader might overclaim
- a reading path

---
<!-- footer: "1:45–2:15 · visual brief" -->

# The basic rule

# If the reader has to hunt for the point, the chart has failed.

---
<!-- footer: "1:45–2:15 · visual brief" -->

# Prompt: visual brief

```text
Turn the chosen story into a visual brief.

Include:
- main claim
- audience
- evidence columns
- filters / aggregation
- comparison baseline
- chart form and why
- labels / annotations / colours
- source and caveat text
- what not to show
- acceptance criteria
```

This is the chart request form.

---
<!-- footer: "1:45–2:15 · visual brief" -->

# Build the workflow

The rough sequence:

1. build `taste.md`
2. build `context.md`
3. profile data and definitions
4. write candidate hypotheses
5. check which ones survive
6. pick the main story
7. write the visual brief
8. make the chart
9. critique it
10. save next-run notes

The model can help. Judgment stays yours.

---
<!-- footer: "1:45–2:15 · visual brief" -->

# Divide the work

Give the model small jobs:

- profile the data
- suggest possible stories
- challenge the claim
- draft labels and annotations
- check the visual choice
- list ways the chart could mislead
- write the next-run recipe

Do not outsource taste or judgment.

---
<!-- footer: "2:15–2:40 · generate first chart" -->

# Prompt: make the chart

```text
Using the context, taste rules, story, and visual brief,
make one static presentation chart.

Rules:
- one main claim
- visible comparison
- direct labels where possible
- no causal language unless the evidence supports it
- include source and caveat
- explain transformations before plotting
```

---
<!-- footer: "2:40–2:55 · critique + revise" -->

# Default slop hunt

Look for:

- legend when direct labels would work
- generic title
- no baseline
- wrong denominator
- fake precision
- colour doing no work
- annotation missing from the key point
- caveat separated from the claim
- chart prettier than it is true

---
<!-- footer: "2:40–2:55 · critique + revise" -->

# Prompt: review the chart

```text
Critique the rendered chart.

Check:
- analytical problems
- visual problems
- misleading readings
- taste-rule violations
- missing caveats
- unsupported story
- whether no chart would be more honest

Then propose one revision.
```

---
<!-- footer: "2:40–2:55 · critique + revise" -->

# Regenerate / refine

Don't keep patching forever.

If the thread becomes messy:

1. summarise context + story + brief + critique
2. start a fresh run
3. generate again

A clean restart is often faster than slow repair.

---
<!-- footer: "2:55–3:00 · package + close" -->

# From chart to system

Production does not mean "ask ChatGPT nicely".

It means someone has decided:

- what the brief contains
- what the standards are
- what gets checked
- who owns the output
- when it refreshes
- when a human must intervene

Trust the workflow, not the first chart.

---
<!-- footer: "2:55–3:00 · package + close" -->

# What can AI safely do?

Good use cases:

- first-pass charts from clean data
- turning style guides into rules
- suggesting story angles and chart forms
- drafting chart code/specs
- checking against house style

Risky use cases:

- ambiguous denominators or definitions
- unsupported causal/policy claims
- messy undocumented data
- fully automated publishing without QA

---
<!-- footer: "2:55–3:00 · package + close" -->

# Now turn taste into rules

Taste becomes useful only when it becomes instructions.

Bad instruction:

```text
Make it beautiful and professional.
```

Better instruction:

```text
Use direct labels instead of legends.
Use grey for context and one accent colour for the focal series.
Title should state the point, not describe the data.
Show the comparison baseline.
Do not use 3D, rainbow palettes, or unsupported causal language.
```

---
<!-- footer: "2:55–3:00 · package + close" -->

# Prompt: extract my taste

```text
Look at today’s good/bad chart examples and my chart revisions.
Turn my preferences into reusable chart rules.

Return:
- positive rules to repeat
- anti-patterns to ban
- colour and label preferences
- annotation preferences
- chart types to avoid
- analytical integrity rules
- one rule that may depend on audience/context
```

Save this as `taste.md`.

---
<!-- footer: "2:55–3:00 · package + close" -->

# Prompt: context pack

```text
Turn today’s dataset notes into a reusable context pack.

Include:
- audience and decision/use case
- one-row grain
- important metrics and denominators
- known caveats and missing data
- fair comparisons
- likely misuse or overclaim risk
- what makes future charts useful
```

Save this as `context.md`.

---
<!-- footer: "2:55–3:00 · package + close" -->

# Standardise this

If 50 people used this next month, what should be:

- standardised?
- banned?
- reviewed?
- escalated?

The scalable AI win is not fancy charts.

It is making boring charts consistently good, on-brand, and reviewable.

---
<!-- footer: "2:55–3:00 · package + close" -->

# Package the workflow

Save the useful artefacts:

```text
context.md
taste.md
story_candidates.md
visual_brief.md
chart_review.md
next_run.md
```

The chart is one run.

The workflow is the reusable thing.

---
<!-- footer: "2:55–3:00 · package + close" -->

# Share-out

Show:

1. first AI chart
2. what failed
3. revised brief or chart
4. one rule you would reuse

If you did not get a good chart, share the rule anyway.

---
<!-- footer: "2:55–3:00 · package + close" -->

# Close

AI makes chart-making cheap.

Judgment makes charts worth looking at.

# story + evidence + taste + review
