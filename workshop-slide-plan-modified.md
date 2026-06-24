# Workshop Slide Plan - Agentic DataViz

**Created:** 2026-06-24
**Purpose:** planning document for the workshop deck. This is not the final PPT; it is the content spine, source-selection memo, and slide-by-slide markdown plan.

## About me section

Add this near the top of the deck, immediately after the title / room setup, before the workshop arc. It should establish why this workshop is grounded in real data and dataviz work, not only AI enthusiasm.

### Suggested slide: About me

**the facilitator**
Fractional Data & AI Consultant · Bangalore

Relevant anchors:

- Built and led the data and analytics function at **Delhivery** as SVP, working with high-volume operational data, dashboards, metrics, and decision workflows.
- Founded **Babbage Insight**, an AI analytics startup that tried to monitor business metrics and surface proactive stories from data.
- Writes and thinks publicly about data, analytics, AI, markets, and decision-making through *The Art of Data Science* / No Enthuda; has also written for *Mint*.
- Built public data/storytelling experiments including **Bangalore weather visualisations** at `public weather-demo site`, combining data pipelines, charts, and AI-assisted narrative commentary.
- Author of *Between the Buyer and the Seller*; studied at IIT Madras and IIM Bangalore.
- Current work: helping teams turn AI-for-data from demos into trusted workflows — context, metric definitions, review loops, reproducibility, and production judgement.

Speaker framing:

> I come at this from three directions: running data teams, building an AI analytics product, and making my own data stories. The common lesson is that charts fail less because tools cannot draw them, and more because the system has not been taught the question, the data caveats, the taste, or the review standard.

### Optional shorter slide copy

```text
I have spent most of my career around data products and data stories:

• built data/analytics at Delhivery
• founded Babbage Insight, an AI analytics startup
• write about data, analytics, markets, and AI
• build public dataviz experiments like Bangalore weather
• now help teams make AI-for-data workflows trustworthy and repeatable

This workshop is based on what breaks when charts, dashboards,
and AI analytics systems meet real data and real users.
```

### Why this matters for the workshop

Use this section to connect biography to the workshop thesis:

- **Delhivery** → dashboards and metrics must support real decisions, not just look good.
- **Babbage Insight** → AI can propose stories, but it struggles without context, metric meaning, examples, and review.
- **Weather visualisations** → recurring public dataviz needs pipelines, editorial judgement, visual taste, and reproducible updates.
- **Consulting work** → teams do not need one impressive chart; they need workflows that can survive new data, new users, and publication risk.

Transition line:

> So today we are not learning how to make one AI chart. We are building the judgement system around the chart.

## Source hierarchy

### Canonical

1. `workshop_outline.md`
   Use as the primary arc: failure → framework → improved chart → production system.

2. `scientific-process-data-visualization.md`
   Must be included as the conceptual heart. The workshop should explicitly teach: chart = visual experiment.

### Must also go in

1. `workshop-overall-framework.md`
   Best current version of the hands-on, participant-led 3-hour flow.

2. `workshop-content-focus.md`
   Best concise teaching thesis: story before chart, no-insight option, taste as reusable instructions, critique loop, production workflow.

3. `participant-kit/*.md`
   These become activity slides and copy-paste artifacts:
   - `context.md`
   - `taste.md`
   - `story_finding_prompt.md`
   - `visual_brief_template.md`
   - `chart_review_checklist.md`
   - `next_run.md`

4. `ai-first-slide-format-learnings.md` and `facilitator/ai-first-workshop-learnings.md`
   Use for deck format, not content doctrine: slides as operating system, prompts in slides, QR/shared sheet, live failure, high-agency room.

5. `dataviz-critique-learnings.md`
   Include Question–Data–Visual trifecta as the simplest review frame. This sits nicely beside scientific-process thinking.

6. `facilitator/literature-survey-synthesis.md`
   Include lightly: architecture problem, not prompt trick; separate transformation from visualization; first chart is draft; reproducibility is structural.

7. `demos/demo-build-list.md` and `talk-prep-source-inventory.md`
   Use for demo choices: default chart slop, weather judgement example, optional Babbage-style metric monitor.

8. `facilitator-visual-style.md`
   Use for personal philosophy lines: clarity, intentional design, data literacy, narrative, systems thinking.

### Existing draft to mine, not treat as canonical

- `slides/agentic-dataviz-workshop.md`
  Already has a useful Marp-style sequence and prompt blocks. Reuse many prompt slides, but add the scientific-process section more explicitly.

## What should not dominate

- Heavy literature review or citation tour.
- Tool-specific demos that turn into environment debugging.
- “Prompt tricks.”
- Fully autonomous dashboard/publishing claims.
- Too many abstract slides before participant work begins.

## Core deck promise

Participants should leave with a folder, not just a chart:

```text
context.md
taste.md
story_candidates.md
visual_brief.md
chart_review.md
next_run.md
```

The chart is one run of the system. The reusable thing is the context, taste, evidence, and review loop.

## Main thesis

> I am not asking AI to make a chart. I am teaching it how I decide what deserves to be visualized, how it should look, and how it should be reviewed.

## Key conceptual line from scientific-process doc

> An effective data visualization is a visual experiment: it begins with a question, tests a hypothesis against evidence, controls for misleading explanations, and communicates what survived scrutiny.

This should be a major slide, not a throwaway quote.

---

# Proposed deck structure

Target: 28–34 content slides for a 3-hour workshop. Many slides are activity/prompt slides, not lecture slides.

## Section 0 - Room operating system

### Slide 1 - Title

**Agentic DataViz**
**Build Systems, Not Charts**
Find the story. Teach the agent. Run it again.

Needs:
- QR / URL to workshop page or repo.
- Shared sheet link.
- Date/venue.

Source: `README.md`, `talk-prep-source-inventory.md`.

### Slide 2 - This is a working session

Message:
- Open laptop.
- Open dataset or fallback dataset.
- Open LLM/tool.
- Fill shared sheet.

Activity:
- Name, tool, dataset topic, chart question, good chart, bad chart, blocker.

Source: `workshop-overall-framework.md`, `facilitator/ai-first-workshop-learnings.md`.

### Slide 3 - What you will leave with

A folder:
- context
- taste
- story candidates
- visual brief
- chart/spec/code
- review checklist
- next-run notes

Teaching line:
> The chart is one artifact. The workflow is the product.

Source: `workshop-overall-framework.md`, `participant-kit/README.md`.

### Slide 4 - The basic problem

Most LLMs can make **a graph**. That is not enough.

Failure modes:
- chart type before story
- generic title
- default colours
- legend gymnastics
- no baseline
- no caveat
- causal language from non-causal data
- polished chart, weak claim

Source: `workshop_outline.md`, `workshop-content-focus.md`.

### Slide 5 - Today’s arc

```text
bad first chart → taste rules → context/data profile → candidate stories
→ scientific process → visual brief → generate → critique → rerun system
```

Source: `workshop_outline.md`.

---

## Section 1 - Taste and standards

### Slide 6 - A good chart is not “beautiful”

Good means:
- truthful
- readable
- purposeful
- repeatable

Teaching line:
> A chart can be ugly and honest. It can also be gorgeous and useless.

Source: `slides/agentic-dataviz-workshop.md`, `facilitator-visual-style.md`.

### Slide 7 - Question, Data, Visual

Introduce a data-visualization critic-style trifecta:

1. What question is the chart trying to answer?
2. What data supports that answer?
3. What visual form reveals the answer?

Add workshop extension:
4. Is the output reviewable?

Source: `dataviz-critique-learnings.md`.

### Slide 8 - Exercise: good chart / bad chart

Participants inspect admired and disliked chart.

Questions:
- What does the good chart make easy?
- What is the bad chart hiding or confusing?
- Which parts are taste?
- Which parts are integrity?
- What should the agent remember?

Source: `workshop-overall-framework.md`, `workshop-flow-current.md`.

### Slide 9 - Prompt: extract my taste

Copy-paste prompt adapted from existing slide:

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

Source: `slides/agentic-dataviz-workshop.md`, `participant-kit/taste.md`.

### Slide 10 - Taste rules are not decoration

Core rules:
- direct labels over legends
- grey for context, one accent for focus
- title states insight, not chart type
- source/timeframe/unit/denominator visible
- remove chartjunk
- no unsupported causal language

Teaching line:
> Your taste file is a dataviz compiler.

Source: `workshop-content-focus.md`, the facilitator dataviz style guide.

---

## Section 2 - Context and data before chart

### Slide 11 - Context before chart

A dataframe does not know what matters.

Capture:
- audience
- decision/conversation
- source
- grain
- metrics
- caveats
- claims the agent must not make

Source: `participant-kit/context.md`.

### Slide 12 - Prompt: context pack

Use/shorten `participant-kit/context.md` as copy-paste template.

Output target: `context.md`.

### Slide 13 - Most AI chart failures are upstream

Teaching line from literature synthesis:

> Most AI chart failures are not drawing failures. They are data transformation failures wearing a nice outfit.

Explain:
- profile data
- inspect grain
- identify denominators
- plan transformations
- check missingness/outliers
- only then visualize

Source: `facilitator/literature-survey-synthesis.md`.

---

## Section 3 - Visualization as scientific process

This is the new section that must be added strongly.

### Slide 14 - A chart is a visual experiment

Big line:

> A chart is a claim with evidence arranged visually.

Scientific loop:

```text
question → hypothesis → evidence → experiment/chart form
→ controls/context → visual test → revise → communicate conclusion
```

Source: `workshop_outline.md`, `scientific-process-data-visualization.md`.

### Slide 15 - Start with a question

Not:
> Let’s plot sales by month.

Better:
> Did sales growth actually improve after the pricing change?

Activity:
Participants rewrite their chart need as a question.

Source: `scientific-process-data-visualization.md`.

### Slide 16 - Form a hypothesis

Examples:
- Urban districts recovered faster than rural ones.
- The policy change created a visible break in trend.
- Most growth came from a few large customers.
- The average hides widening inequality.

Activity:
Write one expected claim and one possible null result.

Source: `scientific-process-data-visualization.md`.

### Slide 17 - Gather evidence like evidence

Ask:
- What is the unit?
- What is the denominator?
- What is missing?
- What period matters?
- What comparison group is fair?
- Is this count, rate, share, index, or rank?

Source: `scientific-process-data-visualization.md`, `workshop-overall-framework.md`.

### Slide 18 - Chart type = experiment design

Mapping:
- change over time → line
- ranking → ordered bar/dot
- distribution → histogram/box/density
- relationship → scatter
- many groups over time → small multiples
- actual vs target → bullet/range
- before/after → slopegraph/indexed line

Teaching line:
> The form should follow the hypothesis.

Source: `scientific-process-data-visualization.md`.

### Slide 19 - Control for confounders

Visualization controls:
- rates not raw counts when population differs
- baseline / prior period / peer group / target / normal range
- avoid misleading axes
- separate unlike groups
- show uncertainty/sample size where relevant

Teaching line:
> A chart without context is like an experiment without controls.

Source: `scientific-process-data-visualization.md`.

### Slide 20 - Revise after observing

First chart is rarely final.

Look for:
- wrong grouping
- missing per-capita denominator
- outlier dominance
- too many categories
- better small multiples
- missing annotation
- decoration to remove

Source: `scientific-process-data-visualization.md`, `facilitator/literature-survey-synthesis.md`.

---

## Section 4 - Story before chart

### Slide 21 - Do not chart yet

Big slide:

> Do not chart yet.

The model should not draw until it knows:
- claim
- audience
- comparison
- evidence
- caveat

Source: `workshop_outline.md`, `workshop-content-focus.md`.

### Slide 22 - Prompt: story candidates

Use `participant-kit/story_finding_prompt.md`.

Require:
- 5 candidate stories
- evidence needed
- chart type likely to work
- comparison baseline
- confidence
- risk of misleading reader
- no-insight option

Output target: `story_candidates.md`.

Source: `participant-kit/story_finding_prompt.md`.

### Slide 23 - No insight is valid

Teaching line:
> Would a chart clarify this, or merely decorate it?

Prompt add-on:
```text
What should I not visualize yet because the evidence is weak?
```

Source: `workshop-content-focus.md`.

### Slide 24 - Peer critique: supported / boring / misleading / useful

Participants explain their chosen claim to a neighbor.

Neighbor asks:
- Compared to what?
- What would make this wrong?
- Is this useful for the audience?
- Is the chart form obvious?

Source: `workshop-overall-framework.md`.

---

## Section 5 - Visual brief before drawing

### Slide 25 - The visual brief

A visual brief is the bridge between analysis and rendering.

Include:
- audience
- claim
- comparison
- data grain
- chart form
- encodings
- annotations
- caveats
- title direction
- source/unit/denominator/timeframe notes
- acceptance criteria

Source: `participant-kit/visual_brief_template.md`, `workshop_outline.md`.

### Slide 26 - Prompt: make visual brief

Use shortened `visual_brief_template.md`.

Add instruction:
```text
Do not write plotting code yet. First produce the brief and list assumptions to inspect.
```

### Slide 27 - Chart-choice cheat sheet

Use chart form by analytical task:
- trend → line
- ranking → sorted bar/dot
- distribution → histogram/box/ridgeline
- relationship → scatter
- many groups → small multiples
- current vs historical/target → range/bullet
- dense repeated metrics → table + sparklines

Source: `scientific-process-data-visualization.md`, the facilitator dataviz style guide, `dataviz-critique-learnings.md`.

---

## Section 6 - Generate, deslop, review

### Slide 28 - Generate the first chart

Set expectation:
> The first output is material for critique, not the answer.

Allow output forms:
- R/Python code
- generated chart image
- Tableau/Power BI spec
- Datawrapper/Flourish instructions
- dashboard implementation brief

Source: `workshop-overall-framework.md`, `facilitator/ai-first-workshop-learnings.md`.

### Slide 29 - Prompt: generate chart/spec

```text
Using my context.md, taste.md, story_candidates.md, and visual_brief.md:

1. Show the aggregation/transformation you will use.
2. Generate the chart/code/spec.
3. State assumptions.
4. List what I should inspect in the rendered output.

Follow the taste rules. Prefer static PNG/SVG. Do not invent data.
```

Source: `facilitator/literature-survey-synthesis.md`, `participant-kit/taste.md`.

### Slide 30 - Default slop hunt

Mark the chart:
- useless title
- legend that could be direct labels
- default colour cycle
- missing denominator/source/timeframe
- chart type mismatch
- unsupported causal language
- bad baseline
- overlapping labels
- grid/spine clutter

Source: `workshop-flow-current.md`, `participant-kit/chart_review_checklist.md`.

### Slide 31 - Review like an analyst

Use checklist headings:
- analytical review
- visual review
- classic dataviz craft review
- reviewability

Key questions:
- What is the claim?
- Is it visibly supported?
- Compared to what?
- Are units/time/denominator clear?
- Is colour doing semantic work?
- Can it stand alone?

Source: `participant-kit/chart_review_checklist.md`, `dataviz-critique-learnings.md`.

### Slide 32 - Prompt: critique and revise

Use `participant-kit/chart_review_checklist.md` revision prompt.

Add:
```text
First infer the chart's claim and the plotted data. Then critique. Then revise.
```

Source: `participant-kit/chart_review_checklist.md`.

---

## Section 7 - Agentic / production layer

### Slide 33 - What makes this agentic?

Not a clever prompt. A system with layers:

1. context
2. taste
3. data profile
4. story candidates
5. visual brief
6. chart generation
7. review
8. memory for next run

Teaching line:
> A good chart agent is a judgment system: it knows what to reward, what to punish, what to verify, and when to refuse to draw.

Source: `workshop-overall-framework.md`, `facilitator/literature-survey-synthesis.md`.

### Slide 34 - Production means decisions, not magic

If 50 people used this next month, what gets:
- standardized
- banned
- reviewed
- escalated
- saved for next run

Production artifacts:
- style guide as system input
- chart request brief
- visual QA gate
- tool-specific handoff
- refresh notes
- escalation rules

Source: `workshop_outline.md`.

### Slide 35 - Next-run notes

Use `participant-kit/next_run.md`.

Human review required when:
- schema changed
- story is low-confidence
- chart implies causality
- missingness/outliers matter
- public/high-stakes output

Source: `participant-kit/next_run.md`.

### Slide 36 - Show-and-tell

Each participant shares:
- original question
- one taste rule
- chosen claim
- first chart flaw
- one revision
- next-run rule

Source: `workshop-overall-framework.md`, `facilitator/ai-first-workshop-learnings.md`.

### Slide 37 - Closing

Big line:

> A good chart agent is not one prompt. It is reusable context, taste, evidence checks, and critique loops.

Final formula:

```text
taste + story + review = charts you can trust more than default AI slop
```

Source: `workshop-overall-framework.md`, `slides/agentic-dataviz-workshop.md`.

---

# Demo material to prepare

## Demo A - Default chart slop → taste-guided chart

Use early to show stakes.

Needs:
- small synthetic monthly metrics dataset
- naive first chart
- improved chart after taste + review
- side-by-side screenshot

Source: `demos/demo-build-list.md`.

## Demo B - Scientific-process chart story

Use in Section 3.

Needs:
- one example question
- hypothesis
- evidence table
- confounder/control
- first chart revision

Could use synthetic pricing-change sales data or Bangalore weather.

Source: `scientific-process-data-visualization.md`.

## Demo C - Weather judgement example

Use if time permits or as credibility anchor.

Point:
- LLM can summarize technically true things but miss editorial judgement.
- Few-shot examples teach judgement, not wording.
- Context pack must include facts, caveats, and examples.

Source: `talk-prep-source-inventory.md`, `demos/demo-build-list.md`.

## Demo D - Babbage-style metric monitor

Optional production-layer demo.

Point:
- recurring analysis should use fixed transformations/metrics and parameterized reruns.
- LLM helps with candidate stories and narrative, not unchecked truth.

Source: `talk-prep-source-inventory.md`, `demos/demo-build-list.md`.

---

# Time map

## 0:00-0:15 - Setup and stakes

Slides 1-5.

Participant output:
- shared sheet row
- one-sentence chart need

## 0:15-0:40 - Taste system

Slides 6-10.

Participant output:
- draft `taste.md`

## 0:40-1:05 - Context and data profile

Slides 11-13.

Participant output:
- draft `context.md`
- basic data cautions

## 1:05-1:35 - Scientific process + story candidates

Slides 14-24.

Participant output:
- rewritten question
- hypothesis
- `story_candidates.md`
- chosen claim or no-chart decision

## 1:35-1:45 - Break

## 1:45-2:10 - Visual brief

Slides 25-27.

Participant output:
- `visual_brief.md`

## 2:10-2:40 - Generate and deslop

Slides 28-32.

Participant output:
- first chart/spec/code
- critique notes
- revised chart/spec/code if possible

## 2:40-2:55 - Package reusable agent

Slides 33-35.

Participant output:
- `next_run.md`
- review thresholds

## 2:55-3:00 - Show-and-tell / close

Slides 36-37.

Participant output:
- one shareable rule or screenshot

---

# Open decisions

1. Should the final deck be 25 tighter slides or 37 operational slides?
   Recommendation: keep 30+ because many are prompt/activity slides, not lecture slides.

2. What fallback dataset?
   Recommendation: synthetic monthly metric data with segment break + denominator trap + outlier.

3. How much weather example?
   Recommendation: one compact demo or backup example, not a long detour.

4. Should we use Marp first?
   Recommendation: yes. Use markdown as canonical; PPT can come later.

5. Need citations?
   Recommendation: cite only stable anchors if final public deck mentions external research. Internal teaching lines can stand without citation.

---

# Timing strategy

The public slot is 3 hours, but actual usable workshop time will be closer to **150-165 minutes** after settling, breaks, tool friction, and share-outs. Design for **165 minutes of core content**, with optional pieces that can be dropped.

## Recommended 3-hour allocation

| Section | Time | Purpose | Must happen? |
|---|---:|---|---|
| 0. Setup + stakes | 15 min | room logistics, shared sheet, why AI charts fail | yes |
| 1. About me + credibility | 5 min | establish data/dataviz/AI background | yes, short |
| 2. Taste + standards | 25 min | good/bad chart → `taste.md` | yes |
| 3. Context + data profile | 25 min | `context.md`, grain, caveats, denominator | yes |
| 4. Scientific process + story | 35 min | question, hypothesis, evidence, candidate stories | yes, core |
| Break | 10 min | reset | yes |
| 5. Visual brief | 20 min | claim → chart spec before drawing | yes |
| 6. Generate first chart/spec | 25 min | first output, expected to be flawed | yes |
| 7. Critique + revise | 25 min | review checklist, deslop, improve | yes |
| 8. Package next run | 10 min | `next_run.md`, review thresholds | yes |
| 9. Show-and-tell + close | 10 min | share one rule/output | yes if possible |
| **Total** | **205 min** | too long | cut needed |

That is too much. The real 3-hour version needs sharper cuts.

## Practical 3-hour run-of-show

Target: **180 minutes total**, including break.

| Time | Section | What happens | Output |
|---:|---|---|---|
| 0:00-0:10 | Setup | shared sheet, tools, dataset/fallback | row in sheet |
| 0:10-0:15 | About me | why this comes from real data work | credibility |
| 0:15-0:25 | Stakes | default AI chart slop, workshop promise | mental frame |
| 0:25-0:50 | Taste system | good/bad chart exercise + prompt | `taste.md` |
| 0:50-1:15 | Context/data | audience, grain, metrics, caveats | `context.md` |
| 1:15-1:40 | Scientific story | question → hypothesis → evidence → candidate stories | chosen claim |
| 1:40-1:50 | Break | hard stop | — |
| 1:50-2:10 | Visual brief | claim, comparison, chart form, annotations | `visual_brief.md` |
| 2:10-2:35 | Generate | chart/code/spec from brief | first chart/spec |
| 2:35-2:55 | Critique/revise | review checklist, peer critique, model revision | fix list / revised output |
| 2:55-3:00 | Close | save workflow, one takeaway | next step |

This is the recommended default.

## What to protect

The workshop must not lose these four work blocks:

1. **Taste capture** - without this, agentic dataviz becomes generic prompting.
2. **Context/data profile** - without this, charts become plausible but ungrounded.
3. **Scientific story selection** - this is the conceptual heart.
4. **Critique/revision** - without this, participants leave with first-draft slop.

If time is tight, cut demos and theory before cutting work time.

## What to compress

### About me

Keep to **5 minutes max**. One slide. No biography tour.

### Literature / research

Use only as speaker framing. Do not spend more than **2 minutes** on external research unless asked.

### Production workflows

Compress into the closing / `next_run.md`. Do not run a full enterprise-production section unless the room is advanced and moving fast.

### Weather / Babbage examples

Use only one compact example. These are credibility anchors, not the main workshop.

Recommended:
- Mention Babbage in about-me.
- Use weather only if participant data/tooling stalls.

## Slide count by time

For 3 hours, aim for:

| Section | Slides | Time |
|---|---:|---:|
| Setup/title/about | 3-4 | 15 min |
| Stakes/problem | 3 | 10 min |
| Taste | 5 | 25 min |
| Context/data | 4 | 25 min |
| Scientific process/story | 7 | 25 min |
| Visual brief | 3 | 20 min |
| Generate/review | 5 | 45 min |
| Package/close | 2 | 5 min |
| **Total** | **32-33** | **180 min** |

Slides are not lecture slides. Many are prompt/activity screens.

## 45-minute compressed version

If this becomes a short talk/workshop, make it a demo-led walkthrough, not a full BYO-data session.

| Time | Section | Output |
|---:|---|---|
| 0:00-0:04 | About me + thesis | trust |
| 0:04-0:09 | Default AI chart failure | stakes |
| 0:09-0:16 | Taste rules | mini `taste.md` |
| 0:16-0:24 | Scientific process | question → hypothesis → evidence |
| 0:24-0:31 | Visual brief | chart spec before drawing |
| 0:31-0:39 | Generate + critique demo | before/after |
| 0:39-0:45 | Reusable system | context/taste/story/review/next-run |

No participant dataset work. Use fallback demo only.

## 75-minute compressed workshop

| Time | Section | Output |
|---:|---|---|
| 0:00-0:08 | Setup/about/stakes | frame |
| 0:08-0:23 | Taste exercise | `taste.md` rough |
| 0:23-0:38 | Context + data profile | `context.md` rough |
| 0:38-0:53 | Story/scientific process | chosen claim |
| 0:53-1:05 | Visual brief | brief |
| 1:05-1:15 | Critique checklist | review habit |

No live chart generation unless tools are already ready.

## 120-minute workshop

| Time | Section | Output |
|---:|---|---|
| 0:00-0:10 | Setup/about/stakes | sheet row |
| 0:10-0:30 | Taste | `taste.md` |
| 0:30-0:50 | Context/data profile | `context.md` |
| 0:50-1:15 | Scientific story | `story_candidates.md` |
| 1:15-1:30 | Visual brief | `visual_brief.md` |
| 1:30-1:50 | Generate first chart/spec | first output |
| 1:50-2:00 | Critique + next-run | review notes |

Skip break or make it 5 minutes.

## Facilitation rule

Use this live rule:

> If we are behind, we stop trying to make the chart prettier and preserve the workflow artifacts.

The minimum successful workshop is not “everyone made a final chart.” It is:

```text
context.md + taste.md + chosen claim + visual_brief.md + review checklist
```
