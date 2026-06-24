---
marp: true
title: Agentic DataViz
subtitle: Build Systems, Not Charts
author: the facilitator
url: https://vizchitra.com/2026/sessions/agentic-dataviz
theme: marpessa
paginate: true
style: |
  section { font-size: 25px; }
  h1 { font-size: 44px; }
  h2 { font-size: 34px; }
  code { font-size: 0.72em; }
  pre { font-size: 0.48em; line-height: 1.12; }
  .small { font-size: 0.72em; }
  .big { font-size: 1.15em; }
  section { padding: 52px 60px; }
  li { margin: 0.18em 0; }
---

<!-- _class: title -->

# Agentic DataViz

## Build Systems, Not Charts

Find the story. Teach the agent. Run it again.

VizChitra 2026 · 3-hour workshop  
the facilitator

---

# The basic problem

Most LLMs can now get you to **a graph**.

That is not usually where the work ends.

The annoying bit is the long tail:

- fix the title
- fix the colours
- remove the legend
- add the right annotation
- make it look like something you would actually send

Today is about shortening that tail.

---

# What we are trying to build

Not a magic prompt.

A small system that gets you from:

# “make a chart”

... to something closer to:

# “this is the kind of chart I make”

reliably, and with less fiddling.

---

# First, fill the sheet

Add:

1. name
2. tool you are using
3. dataset topic
4. chart question
5. one chart you like
6. one chart you dislike
7. current blocker
8. output link / screenshot
9. one rule you want your agent to remember

This is partly logistics, partly peer learning.

---

# What you should leave with

A folder, not just a picture.

- `context.md`
- `taste.md`
- `story-candidates.md`
- `visual-brief.md`
- `chart-review.md`
- `next-run.md`

The chart is one run of the system.

The reusable thing is the context, taste, story, and review loop.

---

# What you need today

Ideally:

1. a dataset you understand
2. one chart you like
3. one chart you dislike
4. one chart you need to make
5. some sense of who it is for
6. access to one LLM/tool

If your data misbehaves, use the fallback data. This always happens.

---

# Why default AI charts are irritating

The model often gives you something plausible.

But plausible is not the same as useful.

Common failure modes:

- chart type chosen before the story
- generic title
- default colours
- legend gymnastics
- no baseline
- no caveat
- causal language from non-causal data
- pretty chart, weak claim

---

# A good chart is not “beautiful”

At least not only beautiful.

For this workshop, good means:

# truthful
# readable
# purposeful
# repeatable

A chart can be ugly and honest. It can also be gorgeous and useless.

We are trying to avoid both extremes.

---

# Exercise 1: your good and bad charts

Take the chart you like and the chart you dislike.

Ask yourself:

- What does the good chart make easy?
- What is the bad chart hiding or confusing?
- Which parts are taste?
- Which parts are basic integrity?
- Would this still work for a different audience?

Taste is fine. Vague taste is not useful.

---

# Prompt: extract my taste

```text
Look at my admired chart and disliked chart.
Turn my reactions into chart-agent rules.

Return:
1. Do-more-like-this rules.
2. Never-do-this rules.
3. Rules on colour, labels, annotation, clutter, title, chart form.
4. Which rules are personal taste vs general hygiene.

Make rules concrete enough for an LLM to apply later.
```

---

# The “small edits” are the system

Think of the things you keep fixing manually.

- “Why is this title so useless?”
- “Why is there a legend?”
- “Why are the labels overlapping?”
- “Why is yellow on white a thing?”
- “Why has it made this dramatic claim?”
- “Why is the source missing?”

Those irritations are useful. They are your style guide trying to exist.

---

# Exercise 2: context before chart

Before the agent draws, tell it what the data means.

Capture:

- source
- grain
- time period
- audience
- decision or conversation
- metric definitions
- caveats
- claims it must not make

A dataframe does not know what matters. You do.

---

# Prompt: context pack

```text
Help me create a context pack for this dataset.
Ask only essential clarifying questions.

Capture:
- source, grain, time period
- audience and use case
- key metrics and definitions
- caveats, missingness, denominators
- communication question
- claims the agent must not make
- preferred output format
```

---

# One rule for the next hour

# Do not chart yet.

This is the part where AI often makes us lazy.

Visualization is closer to data science than decoration:

question → evidence → comparison → chart → review

The chart comes late.

---

# Exercise 3: find stories first

Ask the model to inspect the data and propose stories.

Not charts. Stories.

For each candidate, ask for:

- claim
- evidence
- comparison
- chart form
- confidence
- risk of misleading people

If the evidence is weak, drop the story. Even if the chart would look nice.

---

# Prompt: story before chart

```text
Read my context pack and inspect the data.
Do not make a chart yet.

Return:
1. Data profile and caveats.
2. 5 candidate presentation stories.
3. For each: claim, evidence, comparison, likely chart form,
   confidence, misleading risk.
4. Rank by importance, evidence strength, visual clarity.
5. Recommend one story to visualise first.
6. Say what evidence is too weak to visualise.
```

---

# Quick chart-choice cheat sheet

Start with the comparison.

- trend → line + points
- ranking → sorted horizontal bars
- distribution → histogram / ECDF / box / violin
- relationship → scatter
- mix/share → 100% stacked, only if mix is the story
- geography → map only if location matters
- root cause → waterfall only if components reconcile
- many lines → small multiples, not spaghetti

Do not use cleverness as a substitute for clarity.

---

# Exercise 4: visual brief

Now turn one story into a brief.

The brief should say:

- what claim the chart supports
- why the audience should care
- what data is used
- what comparison matters
- what chart form fits
- what labels/annotations are needed
- what caveats must stay visible

This is where a lot of the manual fiddling can be prevented.

---

# Prompt: visual brief

```text
Turn the chosen story into a visual brief.

Include:
- claim and audience
- evidence columns, filters, and aggregations
- comparison baseline
- chart form
- x/y/colour/facet/label encodings
- annotations and source/caveat notes
- acceptance criteria

Do not generate the chart yet.
```

---

# Exercise 5: make the first chart

Use whatever tool works.

- chatbot image
- Python/R
- Datawrapper/Flourish
- spreadsheet chart
- SVG/HTML

I care less about the tool and more about the workflow.

For today, a static presentation chart is enough.

---

# Prompt: generate the chart

```text
Using my context pack, taste rules, chosen story, and visual brief,
generate one static presentation visual.

Rules:
- support exactly one main claim
- show the relevant comparison
- use direct labels where possible
- avoid default chart slop
- avoid unsupported causal language
- include source/caveat notes

Return output/code plus short rationale.
```

---

# Exercise 6: review like an analyst

Ask boring but important questions:

- What is the claim?
- Compared to what?
- Is the evidence visible?
- Are units and denominators clear?
- Is colour doing work?
- Can the legend disappear?
- Does the title say the point?
- What did the AI guess?
- Would someone misread this in 10 seconds?

This is where trust enters the system.

---

# Prompt: critique and revise

```text
Critique the rendered chart using my review checklist.

Identify:
- analytical problems
- visual problems
- misleading risks
- taste-rule violations

Then revise once for clarity, hierarchy, labels, colour,
annotation, and graphical integrity.
Keep only claims supported by the data shown.
```

---

# If the chat becomes cursed

This will happen to some of you.

If two fixes make things worse, stop repairing the thread.

1. Ask for a clean summary.
2. Start a new chat/tool run.
3. Paste context + taste + story + brief.
4. Generate again.

Sometimes restart is cheaper than therapy.

---

# If you have time: run parallel

One model can find stories.

Another can critique them.

A third can render.

A fourth can act like an annoying reviewer.

You do not need this for every chart. But parallel runs give you options, and options improve taste.

---

# Final artifact: your chart agent rules

At the end, save this:

```text
When making charts for me:
1. Read context and taste rules first.
2. Find story candidates before drawing.
3. Create a visual brief before code/image.
4. Generate a static presentation visual.
5. Critique rendered output.
6. Revise once.
7. Save next-run notes.
```

---

# Modify one part

Pick one thing and change it.

- add a personal taste rule
- ban one chart pattern
- add a domain caveat
- add a review question
- add an output preference
- add a source/caption rule

You are not learning one prompt.

You are learning the shape of a chart-making agent.

---

# Show-and-tell

A few people share:

1. the first output or visual brief
2. what the review caught
3. one reusable rule

Good examples:

- “Always direct-label line charts.”
- “Show the baseline before showing the trend.”
- “Do not infer cause from segment differences.”

---

# Closing thought

AI can make charts cheap.

That is useful, but also dangerous.

The trick is to make judgement explicit:

# taste + story + review

That is the part worth carrying back.
