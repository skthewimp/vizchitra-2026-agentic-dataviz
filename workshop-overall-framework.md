# Workshop Overall Framework - Current

**Last updated:** 2026-06-24  
**Purpose:** single current source for the workshop design. This frames the session as hands-on, interactive, and dataset-led.

## One-line promise

Bring your laptop, bring your data, and leave with a reusable AI-assisted workflow for finding, designing, critiquing, and improving charts.

## Core positioning

This is not a lecture about AI charts. It is a working session.

Participants will use their own datasets, chart needs, and visual taste to build a repeatable dataviz system with an LLM. The room should feel like a studio: short demos, guided work blocks, peer review, facilitator critique, and visible iteration.

## Philosophy from the facilitator's dataviz practice

The workshop should make one idea unavoidable:

> AI does not remove dataviz judgment. It makes judgment more important, because bad taste now scales faster.

The standards remain the old standards: clarity, intentionality, data literacy, narrative discipline, and realistic expectations about tools. LLMs are useful because they can help systematize these standards, not because they can magically discover truth or taste.

Core beliefs to carry through every segment:

- **Clarity first:** a chart should stand on its own without the creator explaining what it means.
- **Ambiguity is the enemy:** unclear chart type, missing axes, unexplained shading, weak labels, or hidden denominators are not minor style issues; they break communication.
- **Design choices must mean something:** colour, layout, annotation, and emphasis should encode meaning, not tool defaults.
- **Data fundamentals precede visuals:** units, denominators, grain, transformations, missingness, uncertainty, and nonsensical comparisons must be checked before drawing.
- **Narrative must be earned:** a chart should make a defensible point, not decorate weak evidence or invent insight.
- **Dashboards are not magic insight machines:** they are useful status displays, but the workshop should not sell dashboard or AI automation hype.
- **Agentic dataviz scales judgment:** the goal is to make clarity, critique, evidence checks, and taste repeatable.

Useful teaching line:

> The question is not “Can AI make a chart?” The question is “Can we teach AI what a good chart is, when no chart is better, and how to know the difference?”

## What makes it hands-on

Participants bring:

1. **Laptop** with access to an LLM or coding/data tool.
2. **A dataset** they understand: CSV, Excel, database extract, dashboard export, or similar.
3. **One real chart need**: a boss/client/blog/report/dashboard question they need to answer.
4. **One chart they admire**: for positive taste rules.
5. **One chart they dislike**: for anti-patterns.
6. **Audience/use-case context**: who the chart is for and what decision or understanding it should support.

They produce during the session:

- `context.md`: audience, purpose, data context, constraints.
- `taste.md`: reusable visual rules and banned patterns, organized into clarity rules, design rules, and integrity rules.
- `story_candidates.md`: possible claims, evidence strength, caveats.
- `visual_brief.md`: chart spec before drawing.
- first chart, chart code, dashboard spec, or implementation brief.
- `review_checklist.md`: QA questions for truth, readability, and taste.
- `next_run_notes.md`: how to reuse the workflow later.

## What makes it interactive

The workshop alternates between:

- **5-10 min concept/demo blocks**: facilitator shows one move.
- **15-25 min work blocks**: participants apply it to their own dataset.
- **pair/peer critique**: explain the claim, chart choice, and risk to another participant.
- **room share-outs**: 2-3 examples projected and critiqued live.
- **revision loops**: every first output is treated as a draft.

The facilitator should ask the room repeatedly:

- What claim is this chart making?
- Compared to what?
- What would make this misleading?
- What should the model be banned from doing next time?
- What taste rule did we just learn?
- Can this chart stand alone without us explaining it?
- Is the model using colour, shading, or layout because it means something, or because it looked nice?

## Core teaching thesis

LLMs can make charts. Humans must design the system that decides:

1. what claim is worth making;
2. what evidence supports it;
3. what chart form fits;
4. what visual taste and house rules apply;
5. when the output is wrong, weak, or overclaimed;
6. how to make the workflow repeatable.

Teaching line:

> I am not asking AI to make a chart. I am teaching it how I decide what deserves to be visualized, how it should look, and how it should be reviewed.

Another framing line:

> A good chart agent is a judgment system: it knows what to reward, what to punish, what to verify, and when to refuse to draw.

## Workshop spine

```text
context → taste rules → data profile → story candidates → evidence check
→ visual brief → chart/spec generation → critique → revision → reusable workflow
```

This is deliberately tool-agnostic. Participants may use ChatGPT, Claude, Gemini, Cursor, Codex, R, Python, Tableau, Power BI, Datawrapper, Flourish, or a notebook. The common output is the workflow and judgment system, not one specific tool artifact.

## Three-hour interactive flow

### 0:00-0:15 - Setup: this is a working session

- Participants open laptops and files.
- State promise: each person will build a reusable chart-making workflow on their own data.
- Quick room poll: tools, datasets, chart needs.
- Show one bad AI chart to set stakes.

Interactive move: ask participants to write one sentence: “My chart needs to help ___ understand/decide ___.”

### 0:15-0:40 - Taste system: good chart / bad chart

- Convert admired and disliked charts into agent instructions.
- Extract positive rules: do more like this.
- Extract negative rules: never do this.
- Build first `taste.md` with three sections:
  - **Clarity rules:** axes, labels, units, title, source, timeframe, denominator, comparison.
  - **Design rules:** colour semantics, direct labels, gridlines, layout, annotation, emphasis, house style.
  - **Integrity rules:** no unsupported causality, no hidden denominators, no fake precision, no fake insight.
- Make every taste rule explain its reason: not just “use muted colours”, but “use grey for context and one accent colour for the claim.”

Interactive move: pair exchange. Each person explains one taste rule and one banned pattern.

### 0:40-1:10 - Context and data profile

- Create `context.md` with audience, purpose, filters, units, denominators, source, caveats.
- Ask LLM to profile the dataset before drawing.
- Identify missingness, grain, comparisons, suspicious fields, possible joins/filters, uncertainty, and transformations.
- Check for dimensional nonsense: wrong denominators, inconsistent units, comparing stocks with flows, totals with rates, or incompatible time periods.

Interactive move: participants ask the model: “What should I be careful not to claim from this data?”

### 1:10-1:35 - Story before chart

- Generate 5-7 candidate stories.
- Rank by evidence strength, audience importance, novelty, and visual suitability.
- Ask for the strongest argument against each candidate story.
- Allow “no meaningful chart here” as valid.
- Pick one supported claim, or explicitly decide not to chart.

Interactive move: peer critique the chosen claim: supported, boring, misleading, or useful?

### 1:35-1:45 - Break

### 1:45-2:10 - Visual brief before drawing

Participants turn the selected claim into `visual_brief.md`:

- audience;
- claim;
- comparison;
- data grain;
- chart form;
- encodings;
- annotations;
- caveats;
- title direction;
- source/unit/denominator/timeframe/filter notes;
- visual rules from `taste.md`;
- acceptance criteria.

Interactive move: facilitator live-critiques 1-2 visual briefs before anyone generates a chart.

### 2:10-2:40 - Generate and deslop

- Participants generate chart/code/spec from the visual brief.
- First output is expected to be flawed.
- Apply `taste.md` and revise.
- Treat LLM defaults as suspicious until they justify themselves: chart type, colours, shading, legends, annotations, and title.
- If tool/coding fails, participant may produce a dashboard implementation brief instead of debugging forever.

Interactive move: “default slop hunt” — participants mark legends, weak titles, bad colours, missing units, unsupported claims.

### 2:40-2:55 - QA review loop

Use review checklist:

- What is the claim?
- Is it supported by visible evidence?
- Compared to what?
- Are units, filters, timeframe, denominator, and transformations clear?
- Is colour doing semantic work?
- Does any shading, area fill, or annotation change the interpretation?
- Can legend become direct labels?
- Does title state insight, not chart type?
- Is anything overclaimed?
- Does it pass the 10-second glance test?
- Can it stand alone without the presenter explaining it?

Interactive move: one peer gives “keep / fix / ban next time” feedback.

### 2:55-3:00 - Package the reusable agent

Participants save:

- `context.md`
- `taste.md`
- `story_candidates.md`
- `visual_brief.md`
- chart/spec
- `review_checklist.md`
- `next_run_notes.md`

Close line:

> A good chart agent is not one prompt. It is reusable context, taste, evidence checks, and critique loops.

## Facilitation principles

- Keep demos short; maximize participant work time.
- Do not let the model draw before claim + comparison + evidence are clear.
- Do not make it about prompt tricks.
- Do not turn the room into a debugging clinic.
- Encourage participants to work with their real constraints.
- Treat failures as teaching material.
- Keep asking: “What rule do we want the agent to remember next time?”
- Keep participants skeptical of polished output: attractive charts can still be unsupported, ambiguous, or wrong.
- Emphasize dashboards and agents as workflows with QA gates, not magic insight machines.

## Required pre-work email language

Bring your laptop and one dataset you know well. Also bring one chart you admire, one chart you dislike, and one real chart need from your work. This is a hands-on workshop: we will use your data to build a repeatable AI-assisted dataviz workflow, not just watch demos.
