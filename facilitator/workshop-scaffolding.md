# Workshop Scaffolding - Agentic DataViz

**Workshop:** Agentic DataViz: Build Systems, Not Charts  
**Date/time:** 2026-07-03, 14:30-17:30  
**Format:** 3-hour concept-led workshop with optional BYO-data follow-along  
**Core line:** The chart is the last step.

## 1. What this workshop is really about

Participants should leave with a repeatable, tool-agnostic way to use AI for presentation-quality data visualisation — usable by an individual, but also understandable as a small production workflow for a wider team.

Not:

- one lucky LLM chart;
- a tool demo tied to one model;
- a generic “make charts prettier” session;
- exploration-first dashboarding.

Yes:

- start with a hypothesis or communication need;
- check whether data can support the claim;
- teach the agent context, taste, and judgement;
- test whether there is a meaningful insight before forcing a story;
- produce a visual brief before producing a chart;
- generate a static presentation visual only when the chart improves understanding;
- critique, revise, and save the workflow for next time;
- know when this workflow is safe to scale across a team, and when expert review is mandatory.

The durable artifact is not the final PNG. It is the small system around it: context, taste rules, story candidates, visual brief, chart, review notes, and next-run instructions.


## 1.1 Public FAQ framing

Use these answers when participants ask why this is not just prompt engineering or autonomous-agent hype.

**Already vibe-code charts?** One good chart is easy. Repeatability across new data, new questions, and new teammates is the hard part. The workshop teaches the workflow around the chart: hypotheses, data checks, context, visual generation, critique, and rerun rules.

**Autonomous agents?** Not the promise. Agent is the system; agentic is the behaviour. We design workflows where the LLM does analytical and visual heavy lifting while the human keeps control of question, judgement, and story.

**Just another AI demo?** No. The point is what happens after the demo: what breaks, what holds, and what a team can trust in production.

## 2. Participant premise

Each participant may bring:

1. **A dataset** they understand.
2. **One analysis or communication question** they want the chart to support.
3. **One visualisation they admire** — “do more like this”.
4. **One visualisation they dislike** — “never do this”.
5. **An audience/use case** — boss, client, reader, policy audience, public report, blog post, etc.
6. **An LLM/tool** they can use: ChatGPT, Claude, Copilot, local enterprise tool, etc.

Participants who prefer not to work hands-on during the session can instead map the workflow to their team/tool stack.

Fallback dataset and examples remain ready for anyone with unsuitable data, privacy issues, or tool problems.

## 3. Teaching philosophy

### 3.0 Concept first, tool second

Keep the workshop LLM-agnostic. Use “LLM/agent” by default, not Claude-specific language. The same method should map to:

- ChatGPT Enterprise;
- Claude;
- GitHub Copilot;
- Python/R notebooks;
- Tableau or Power BI production workflows;
- Datawrapper/Flourish-style publishing tools.

Avoid constant zooming between abstract concepts and hands-on debugging. Teach concept, show small demo, then give optional files for practice.


## 3.0B Architecture, not prompting trick

Literature/practitioner survey reinforces the workshop thesis: serious AI dataviz systems separate modules instead of relying on one magic prompt. Name the architecture explicitly:

1. context layer — audience, metric definitions, taste, caveats;
2. data layer — source, grain, cleaning, transformations;
3. insight layer — candidates, evidence strength, null/no-insight option;
4. spec layer — visual brief / grammar / dashboard instructions;
5. render layer — chart code, image, BI visual, or dashboard spec;
6. review layer — analytical, visual, and production QA;
7. memory layer — next-run notes, parameters, saved specs, workflow history.

Useful lines:

> Most AI chart failures are not drawing failures. They are data transformation failures wearing a nice outfit.

> Trust the workflow, not the first chart.

> Doing it again tomorrow is an engineering choice, not a model capability.

### 3.1 Taste is real, but must become explicit

Everyone has different visual taste. That is not a bug. The workshop should use this difference as teaching material.

Participants should see that taste becomes useful only when converted from vague preference into operational rules:

- label directly, do not use legends;
- use grey for context and one accent for focus;
- avoid rainbow palettes;
- title should state the insight, not the chart type;
- show baseline or comparison;
- avoid unsupported causality;
- remove decoration that does not help the claim.

Good/bad examples are the fastest way to extract these rules.

### 3.2 Appropriateness beats prettiness

Good visualisation is not one universal style. It depends on:

- audience;
- decision context;
- data grain;
- claim strength;
- chart size and medium;
- what comparison matters;
- whether the chart is for presentation, not exploration.

A chart is good if it is truthful, readable, purposeful, and repeatable for that use case.

### 3.3 Visualisation is hypothesis-driven

Frame visualisation as close to data science:

1. Start with question or hypothesis.
2. Inspect data and caveats.
3. Test whether evidence supports claim.
4. Choose comparison.
5. Choose visual form.
6. Communicate clearly.
7. Review and revise.

Agentic workflow mirrors this. The agent should not draw before it knows the claim and evidence.

### 3.4 The agent needs judgement, not vibes

“You are a world-class designer, make it beautiful” is weak instruction.

Better instruction gives the agent:

- purpose;
- audience;
- metric definitions;
- caveats;
- admired examples;
- disliked examples;
- chart-selection rules;
- review checklist;
- refusal conditions.

This is the “taste/context layer” for dataviz, analogous to business context in AI analytics systems.

## 4. Three-hour structure

Target: ~20 slides, not 110. Slides should mostly do four jobs: orient, prompt, demonstrate, debrief.

| Time | Segment | Mode | Output |
|---|---|---|---|
| 0:00-0:15 | Opening: chart is last step | short talk + critique | shared vocabulary |
| 0:15-0:35 | Good/bad visual critique | group discussion | taste vocabulary |
| 0:35-0:55 | Build personal taste rules | participant work | `taste.md` draft |
| 0:55-1:15 | Dataset context + hypothesis | participant work | `context.md` draft |
| 1:15-1:30 | Break / tool buffer | support | unblock participants |
| 1:30-1:55 | Story before chart | prompt + participant work | story candidates |
| 1:55-2:15 | Visual brief | participant work | selected claim + chart plan |
| 2:15-2:40 | Generate first chart | participant work | first output |
| 2:40-2:55 | Critique and revise | paired/LLM review | improved output |
| 2:55-3:00 | Show-and-tell + close | 3-4 quick shares | one reusable rule |

## 5. Detailed run logic

### 0:00-0:15 - Opening: why default AI charts fail

Show three visuals:

1. ugly default LLM/matplotlib chart;
2. polished but misleading chart;
3. clean, purposeful chart.

Ask:

- Which is good?
- Good for whom?
- What is the chart trying to make us see?
- Is the problem taste, truth, readability, or context?

Teaching line:

> The model optimises for plausible chart output. We must make it optimise for evidence, comparison, and communication.

### 0:15-0:35 - Critique good and bad examples

Participants use their brought good/bad visuals.

Discussion prompts:

- What does the good chart do that you want repeated?
- What does the bad chart do that you want banned?
- Which rules are taste? Which rules are truth/integrity?
- What would be inappropriate in another context?

Output: rough list of positive rules and anti-patterns.

### 0:35-0:55 - Turn taste into agent instructions

Participants fill `participant-kit/taste.md`.

Minimum rules:

- overall style;
- chart rules;
- colour rules;
- annotation rules;
- anti-patterns;
- chart forms to avoid;
- claims the agent must not make.

Facilitator warning: avoid vague rules like “make it elegant”. Translate them into visible behaviours.

### 0:55-1:15 - Dataset context and hypothesis

Participants fill `participant-kit/context.md`.

They define:

- dataset source and grain;
- important columns and metrics;
- caveats;
- intended audience;
- one communication question;
- what the reader should understand or decide.

Teaching line:

> If the agent only sees columns, it will invent importance. Give it the decision context.

### 1:15-1:30 - Break / tool buffer

Use this time to fix:

- CSV upload issues;
- data too large;
- privacy concerns;
- unclear question;
- participants needing fallback data.

### 1:30-1:55 - Story before chart

Participants run `participant-kit/story_finding_prompt.md`.

Hard instruction:

> Do not make a chart yet.

Agent returns:

- data profile;
- caveats;
- 5 candidate stories;
- null/no-insight possibility;
- boring-but-important finding;
- claim, evidence, comparison, likely chart form;
- confidence and misleading-risk;
- alternative explanations and strongest argument against the story;
- recommendation, including “do not chart this yet” if evidence is weak.

Participants choose one story. If none is supported, they narrow the question or switch data.

Teaching lines:

> Chart choice follows claim + comparison + data grain.

> A good AI analyst is allowed to come back with no story.

### 1:55-2:15 - Visual brief

Participants complete `participant-kit/visual_brief_template.md`.

Brief must include:

- chosen claim;
- why it matters;
- evidence columns;
- filters/aggregations;
- comparison baseline;
- chart type;
- encodings;
- annotations;
- caveats;
- acceptance criteria.

This prevents “chart first, story later”.

### 2:15-2:40 - Generate first chart

Participants ask the LLM/tool to produce a static chart using:

- context pack;
- taste rules;
- story candidate;
- visual brief;
- chart-selection constraints;
- output format.

Allowed outputs:

- generated image;
- Python/R code;
- Datawrapper/Flourish spec;
- Tableau calculated fields + visual setup instructions;
- Power BI DAX/measures + visual setup checklist;
- spreadsheet chart instructions;
- SVG/HTML if participant can render it.

Do not over-debug local environments. If code fails, let the agent produce image or use fallback path.

### 2:40-2:55 - Critique and revise

Participants use `participant-kit/chart_review_checklist.md`.

Review questions:

- What is the claim?
- Compared to what?
- Is evidence visible?
- Are units/time/denominator clear?
- Is visual effect proportional to data effect?
- Is colour semantic or decorative?
- Can legend become direct labels?
- Does title say the takeaway?
- What did AI guess?
- What should be refused or caveated?

Revise once. Emphasise: one strong revision is better than endless polishing.

### 2:55-3:00 - Close

Ask 3-4 participants to share:

- first output vs revised output;
- one rule that improved the chart;
- one thing their agent must remember next time.

Closing line:

> The skill is the system. The chart is only one run of it.

### 5.1 Production workflow / team-scaling lens

For participants who already make charts professionally, frame the same artifacts as a lightweight chart production system:

- `taste.md` = house style and expert judgement;
- `context.md` = data/project brief;
- story candidates = analyst/editorial options;
- visual brief = chart request/spec;
- review checklist = QA gate;
- next-run notes = SOP/change log.

Useful prompt:

> If 50 colleagues used this workflow next month, what should be standardized, banned, reviewed, or escalated?

Core message:

> The scalable AI win is not fancy charts. It is making the boring charts consistently good, on-brand, and reviewable.

Enterprise/dashboard mapping:

- context pack = data dictionary + dashboard purpose;
- story candidates = candidate KPIs/views;
- visual brief = Tableau/Power BI visual spec;
- chart review checklist = dashboard QA gate;
- next-run notes = refresh SOP.

Production does not mean the model publishes the dashboard. Production means the workflow has roles, specs, QA gates, and refresh rules.

## 6. Core concepts to repeat throughout

### 6.1 One chart, one job

A visual should make one intended sentence easier to see. If there are two sentences, make two charts or make one secondary.

### 6.2 Data transform → evidence → claim → comparison → chart

Before a chart exists, ask what transformed data/aggregation would be required, and whether that data honestly supports any claim. Then every useful presentation visual needs a comparison:

- over time;
- against target;
- against peer;
- before/after;
- distribution vs threshold;
- actual vs forecast;
- segment vs segment;
- contribution to change.

No comparison usually means weak chart. Weak evidence means no chart yet. Uninspected transformation means do not trust the chart yet.

### 6.3 Fit chart to data grain

Use simple default choices:

- trend: line + points;
- ranking: sorted horizontal bars;
- distribution: histogram/ECDF/box/violin;
- relationship: scatter;
- composition: 100% stacked only when mix is story;
- geography: map only when spatial pattern matters;
- root cause: waterfall only when components reconcile; otherwise ranked drivers/table;
- many series: small multiples, not spaghetti.

Avoid pie/donut, 3D, gauges, radar, decorative infographic forms, and dashboards as substitute for interpreted story.

### 6.4 Use AI where it scales; require humans where judgement matters

AI is strongest for:

- first-pass bar/line/area/scatter charts from clean data;
- translating style guides into concrete visual rules;
- proposing claim/comparison/chart-form options;
- checking against house style and review checklists;
- producing reproducible code/specs and next-run notes.

AI is risky for:

- messy, undocumented, or sensitive data;
- ambiguous denominators/definitions;
- unsupported causal or policy claims;
- publication without human QA;
- bespoke visuals needing deep domain/editorial judgement.

### 6.5 Human judgement remains non-negotiable

The agent can suggest and render. Human must decide:

- what matters;
- whether claim is supported;
- what is misleading;
- what is appropriate for audience;
- what to omit;
- what caveat must be visible.

## 7. Facilitator assets needed

Before workshop, prepare:

1. **Fallback CSV** with obvious and subtle stories.
2. **Bad default chart** from naive prompt.
3. **Improved chart** after taste/review loop.
4. **Good visual example** for critique.
5. **Bad visual example** for critique.
6. **Prompt slides** for each activity.
7. **Participant kit zip/repo** with templates.
8. **QR code** to slides + kit.
9. **One weather/editorial judgement demo** if time allows.
10. **One Babbage-style context/cold-start anecdote** for framing.

## 8. Slide plan

Keep deck around 18-22 slides.

1. Title + QR.
2. Promise: leave with reusable AI dataviz workflow.
3. The chart is the last step.
4. Default LLM chart slop.
5. Polished but wrong/misleading chart.
6. Clean purposeful chart.
7. Good chart = truthful + readable + purposeful + repeatable.
8. Activity: critique your good/bad examples.
9. Prompt: extract taste rules.
10. Debrief: taste as rules, not vibes.
11. Activity: dataset context and hypothesis.
12. Prompt: story-finding, do not chart yet.
13. Chart-selection mini-guide: claim → comparison → grain.
14. Activity: choose one candidate story.
15. Prompt: visual brief.
16. Prompt: generate first chart.
17. Checklist: critique rendered output.
18. Prompt: revise chart.
19. Reuse: convert conversation into instruction/skill.
20. Show-and-tell.
21. Close: run it again.

## 9. Success criteria

Workshop succeeds if hands-on participants leave with:

- a filled context pack;
- a personal visual taste constitution;
- at least 3-5 candidate stories from their data;
- one chosen story with visual brief;
- one first chart or chart plan;
- one critique/revision cycle;
- reusable next-run instructions.

For concept-path participants, it succeeds if they leave with a clear workflow map for their enterprise stack: roles, inputs, outputs, QA gates, and refresh rules.

It also succeeds if participants become more sceptical of AI output, not less. They should trust the workflow more than the first answer.

## 10. Risks and mitigations

| Risk | Mitigation |
|---|---|
| BYO data messy/private/too large | fallback dataset; narrow to one question; allow summaries/sample rows |
| Too much tool debugging | browser-first; generated image allowed; code optional |
| Taste discussion becomes vague | force rule extraction from examples |
| Participants chart too early | repeat “do not chart yet” until visual brief exists |
| AI hallucinates stories | evidence columns + caveats + refusal conditions |
| Final charts uneven | judge process artifacts, not beauty contest |
| Time overrun | one revision only; show-and-tell short |

## 11. What to tell participants before workshop

Bring:

- laptop and charger;
- LLM access;
- small CSV/Excel dataset you understand;
- one chart/visual you admire;
- one chart/visual you dislike;
- one analysis or communication question;
- audience/use case for the chart.

Dataset guidance:

- small enough to upload or inspect;
- no sensitive private data unless anonymised;
- column names understandable;
- ideally includes time, category, geography, segment, or metric comparisons;
- come with one possible presentation need.

## 12. Minimal prompt pack

### Taste extraction

```text
Look at my admired visual and disliked visual. Extract visual rules for a chart-making agent.
Return:
1. Do-more-like-this rules.
2. Never-do-this rules.
3. Rules about colour, labels, annotation, chart type, clutter, comparison, and title.
4. Any subjective preferences that may not apply universally.
Make rules concrete enough to apply to future charts.
```

### Story finding

```text
Read my context pack and inspect the dataset. Do not make a chart yet.
Return data profile, caveats, 5 candidate presentation stories, evidence needed, comparison baseline, likely chart form, confidence, misleading risk, and one recommended story.
Also include: null/no-insight possibility, boring-but-important finding, alternative explanations, strongest argument against each insight, and what not to visualise yet because evidence is weak.
You are allowed to say: no meaningful chart or claim is supported by this data.
```

### Visual brief

```text
Turn the chosen story into a visual brief.
Include claim, audience, evidence columns, filters, aggregations, comparison baseline, chart form, x/y/colour/facet/label encodings, annotations, caveats, and acceptance criteria.
Do not generate the chart yet.
```

### Chart generation

```text
Using the context pack, taste rules, chosen story, and visual brief, generate one static presentation visual.
The chart must support exactly one main claim, show the relevant comparison, use direct labels where possible, avoid chartjunk, avoid unsupported causal language, and include source/caveat notes.
Return chart output or code plus a short rationale.
```

### Critique and revision

```text
Critique the rendered chart using the review checklist.
Identify analytical problems, visual problems, misleading risks, and taste-rule violations.
Then revise once to improve clarity, hierarchy, labels, colour, annotation, and graphical integrity.
Preserve only claims supported by the data shown.
```

## 13. Open build tasks

- Finalise fallback dataset.
- Generate bad/good demo chart pair.
- Build Marp deck from slide plan.
- Add QR/public kit page.
- Package participant kit.
- Dry-run the BYO flow with one real dataset.
- Prepare 2-minute Babbage/weather anecdotes.
