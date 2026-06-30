# VizChitra 2026 Talk Prep: Local Work Inventory

**Purpose:** Source-grounded material from the facilitator's own work that can feed the accepted VizChitra workshop/talk prep.  
**Prepared:** 2026-06-12  
**Scope:** Local files under `~/Documents/work`, with emphasis on prior talks, Babbage, weather/dataviz experiments, AI-for-data consulting notes, and reusable teaching frames. External literature in `proposal-and-prep.md` is intentionally not expanded here.

---

## 1. Core public framing

Public page now frames the workshop as:

> **Agentic DataViz: Build Systems, Not Charts**  
> Find the Story. Teach the Agent. Run It Again.

Public page: https://vizchitra.com/2026/sessions/agentic-dataviz  
Date/time: **2026-07-03, 14:30-17:30**  
Venue: **Underline Center**

Internal hook to keep using in the talk: **the chart is the last step.**

Useful accepted frame:

1. define purpose and audience;
2. inspect whether data can support the story;
3. give the agent context, taste, and examples;
4. ask it to find candidate stories before drawing;
5. generate and critique the visual;
6. save workflow so it can run again.

Primary local source:

- `WORK/consulting/workshops/vizchitra-2026-agentic-dataviz/proposal-and-prep.md`
- `WORK/consulting/workshops/vizchitra-2026-agentic-dataviz/README.md`
- `WORK/consulting/workshops/vizchitra-2026-agentic-dataviz/session-notes.md`

This document adds the “only from my work” source bank beneath that spine.

---

## 2. Best raw material to reuse

### A. Babbage Insight: dashboards, stories, and why LLMs need structure

**Why it matters for VizChitra:** This is the talk’s credibility anchor. It shows you already tried to build proactive AI analytics/storytelling, learned what failed, and now have a better workflow.

Local sources:

- `WORK/BabbageInsight/PitchDeck1.pptx`
- `WORK/BabbageInsight/PitchDeck1.pdf`
- `WORK/BabbageInsight/SalesPitch.pptx`
- `WORK/BabbageInsight/mockup.Rmd`
- `WORK/vibes/blog-embeddings/noenthuda-substack-html/184040183.my-learnings-for-myself-from-babbage.html`
- `WORK/vibes/blog-embeddings/noenthuda-substack-html/183324919.have-we-been-disrupting-bi-the-wrong.html`
- `WORK/vibes/blog-embeddings/noenthuda-substack-html/183034858.how-llms-will-change-business-intelligence.html`

Reusable ideas:

- Dashboards are self-service; the business still has to interpret the data.
- When data changes, the information/story changes; representation should change too.
- Business leaders do not only want “what happened”; they want “why did this happen?”
- Numbers without context make people miss the forest for the trees.
- LLMs can help with candidate stories, annotations, ordering, and narrative media choice.
- But LLMs are weak validators. Use them as hypothesis/story generators, then validate with deterministic/statistical systems.
- “LLMs cannot analyse data except by writing code to analyse it” is a useful provocative line from the sales deck.
- Babbage’s cold-start mistake: expecting the product to infer too much from generic data access instead of giving it live customer context, examples, and workflow-specific priors.
- Babbage’s product lesson: build with a specific customer/use case in mind; generic product becomes “for no one”.
- Dashboard correction: dashboards are not dead; they are reporting surfaces. Problems start when people expect them to be analytics tools.
- Future BI direction: personalised dashboards/visuals built cheaply with LLMs, grounded in shared metric definitions/semantic layers.

Possible talk section:

> “At Babbage we started from the right dissatisfaction — dashboards leave interpretation to the user — but we underestimated how much context, examples, and review the system needs before it can tell useful stories. That is why this workshop starts before the chart.”

Concrete demo idea from `mockup.Rmd`:

- Show a metric-monitoring pipeline:
  - one dataset;
  - several metrics;
  - known time column;
  - hardcoded segmentation axes;
  - compare current period vs past periods/forecast;
  - calculate “interestingness”;
  - choose whether the story is period-on-period change, deviation from expectation, trend, seasonality, or segment change;
  - then decide how to display it.
- This maps cleanly to “find story before drawing”.

---

### B. Old teaching frame: data analysis is iterative and hypothesis-driven

**Why it matters:** This gives the talk its non-AI backbone. AI does not replace the old data process; it scaffolds it.

Local sources:

- `WORK/IIMB/The Art of Data Analysis.pptx`
- `WORK/BabbageInsight/SalesPitch.pptx` (slide citing the Fifth Elephant 2012 loop)
- `WORK/takshashila/Data Presentation.pptx`

Reusable frame from `The Art of Data Analysis`:

1. Frame a clear problem statement.
2. Break problem into smaller problems.
3. Use those to generate hypotheses.
4. Gather, clean, and prepare data.
5. Test hypotheses.
6. Generate additional hypotheses during testing.
7. Consolidate results.
8. Make the data tell a story.

This is almost exactly the accepted workshop sequence. Use it to show continuity: the AI workflow is not new magic; it is your old analysis loop with agents inserted into specific steps.

Pitfalls from old slides that fit the review checklist:

- Outliers distort inference.
- Correlation does not imply causality.
- Start by getting a feel for the data; do not throw everything into the model.
- Do not overfit.
- A simple model should be explainable in English.
- Look at the data before fitting models.
- Axis/scale choices alter the story.
- Graphics can deceive.
- Models are not reality.
- Do not overcomplicate graphics.

Workshop use:

- Turn these into the “review visual like an analyst” checklist.
- Ask participants: “What would my old 2012/teaching self object to in this AI-generated chart?”

---

### C. Weather project: strongest public dataviz case study

**Why it matters:** This is the cleanest public, non-confidential, visual example. It shows code, taste, automation, LLM commentary, and few-shot editorial judgement.

Local sources:

- `WORK/bangalore-weather/bangalore_weather_update.R`
- `WORK/bangalore-weather/bangalore_weather_historical.R`
- `WORK/bangalore-weather/charts/bangalore_weather_2021.png` through `2025.png`
- `WORK/data_work/bangalore/weather/blog-post.md`
- `WORK/data_work/bangalore/weather/blog-post-fewshot-weather.md`
- `WORK/data_work/bangalore/weather/blog-post-wind.md`
- `WORK/data_work/bangalore/weather/weather_chart_common.R`

Reusable ideas:

- Data pipeline: hourly Oikolab/ERA5 weather data, current year vs 40+ years of historical norms and records.
- Visual grammar: temperature panel = current range layered against historical normal and record range; rainfall panel = cumulative monthly precipitation vs normal monthly total.
- LLM role deliberately bounded: R computes stats; LLM rephrases or chooses a lead; model does not do core analysis.
- Local model/Claude commentary can fail by flattening real events into aggregate summaries.
- Few-shot examples were not about teaching prose style; they taught **editorial judgement** — what to emphasise.
- Review cards are a powerful teaching object: compact chart + facts + human-written lead line.
- Production now samples reviewed examples instead of stuffing all examples into every call — avoids prompt rot and surface mimicry.
- The agent needs structured input matching production reality, not toy examples.

Strong lines from the local blog material:

- “Prompt engineering is often a data curation problem in disguise.”
- “The useful signal was not the wording. It was what I chose to emphasise.”
- “Few-shot examples were not there to teach style. They were there to teach editorial judgment.”

Workshop demo:

1. Show naive recent-weather AI summary that says something technically true but editorially wrong.
2. Show review-card workflow.
3. Show the same chart/commentary after example curation.
4. Extract general rule: context pack must include facts, caveats, and examples of judgement.

This should probably be the main live/public example.

---

### D. AI-for-data consulting notes: production-grade trust/adoption frame

**Why it matters:** This is the “beyond demo” layer organisers asked for. Translate enterprise AI adoption into dataviz systems.

Local sources:

- `WORK/consulting/consulting-positioning.md`
- `WORK/consulting/ai-product-adoption-playbook.md`
- `WORK/consulting/conversation_insights.md`
- `WORK/consulting/blog_material_for_ai_data_copilot_pitch.md`
- `WORK/consulting/fifthelephant-2026-submission.md`
- `WORK/consulting/workshop-business-plan.md`
- `WORK/consulting/conversations/nutanix.md`, `snowflake.md`, `wisdomai.md`, `impactanalytics.md`, `meesho.md`, `kapiva.md`

Reusable thesis:

- The problem is not just “missing context”; it is the **cold-start / plug-and-play mistake**.
- AI-on-data systems need guided warm starts: live analysis, exemplars, iterative context-building.
- Context is not only schema/semantic metadata. It includes SQL, notebooks, dashboards, metric debates, caveats, business review decks, recurring investigations, and historical decisions.
- Adoption is not training. Pair-drive real users on real questions, diagnose failures live, and convert failures into context/evals/workflow changes.
- Trust requires repeated-run consistency, refusal behavior, evidence, and thresholds for human review.
- Mature buyers may already have “what happened?” working. Harder layer is “why did it happen?” — RCA, forecasting, experiment readouts, business reviews.
- The interface may be chat, dashboard, headless agent, command centre, or recurring report. Do not over-anchor on chatbot.
- Raw query volume/logins are weak adoption metrics. Better signs: query sophistication rising; ad hoc analyst request volume falling; decisions made faster/better.

Translation to dataviz:

| AI-for-data adoption | Dataviz workshop translation |
|---|---|
| business-context layer | taste/context layer |
| exemplar analyses | prior charts/reports/reviewed examples |
| semantic layer | metric definitions + data caveats |
| evals | visual/story review checklist |
| pair-driving | participant works through own data with agent |
| adoption cadence | saved workflow for next run |
| refusal behavior | “do not make unsupported claims” rules |

Possible talk line:

> “A reusable dataviz system has the same cold-start problem as an AI analytics agent. If you only give it a dataset, it has no idea what you care about, what you consider elegant, what counts as evidence, or when it should refuse to tell a story.”

---

### E. Kshipra / maritime visual brief: structured extraction before infographic rendering

**Why it matters:** This is a production-like example of forcing an agent to produce structured visual/story data, with strict anti-hallucination rules.

Local sources:

- `WORK/kshipra/ais-explorer/server/src/agent/visualBrief.ts`
- `WORK/kshipra/UDAL/datafusion/server/src/agent/visualBrief.ts`
- `WORK/kshipra/DAILY-SOURCE-COLLECTION-RUNBOOK.md`
- `WORK/kshipra/analysis/scripts/run_daily_analysis_refresh.sh`

Reusable ideas:

- Visual brief is pipeline step 2, after executive summary and scratchpad findings.
- Agent output is JSON, not prose: situation summary, risk score, vessel cards, event breakdown, anomaly strip, key insights, network graph, source contributions, timeline, recommendations, stats ribbon.
- Prompt rules: every fact must come from provided data; do not fabricate; use definitive vessel list; keep labels short; empty graph if no network data exists.
- This is a good example of converting messy findings into a visual-brief schema before rendering.

Workshop use:

- Show a simplified schema for participant outputs:
  - story summary;
  - claim;
  - evidence rows;
  - chart type;
  - annotations;
  - caveats;
  - “do not show” / refusal conditions.
- Emphasise: production-grade systems ask for structured intermediate artifacts, not only final charts.

---

### F. Blog embeddings / triangle: personal corpus as navigable data

**Why it matters:** Secondary example. Shows a personal corpus becoming a visualization and story surface.

Local sources:

- `WORK/vibes/blog-embeddings/blogmap.py`
- `WORK/vibes/blog-embeddings/triangle.py`
- `WORK/vibes/blog-embeddings/blog-post.md`
- `WORK/vibes/blog-embeddings/blogmap/blogmap.json`
- `WORK/vibes/blog-embeddings/charts/blog_triangle_final.png`
- `WORK/vibes/blog-embeddings/charts/blog_triangle.gif`

Reusable ideas:

- Embeddings make a messy archive navigable.
- Categories like “Data science & AI”, “Work & careers”, etc. can become map coordinates/story axes.
- Good side demo if you want a “my own corpus as context” example.

Do not overuse. It is less central than weather/Babbage.

---

### G. Data presentation / public communication teaching

**Why it matters:** Useful for participant exercises and the “review” phase.

Local sources:

- `WORK/takshashila/Data Presentation.pptx`
- `WORK/takshashila/Smelling Bullshit.pptx`
- `WORK/takshashila/Smelling Bullshit.pdf`
- `WORK/IIMB/The Art of Data Analysis.pptx`
- Mint/Data journalism files under `WORK/Mint/` if examples needed later.

Reusable lessons:

- Put big numbers in relevant context.
- Separate stocks and flows.
- Beware survey framing and sampling bias.
- Judge process, not only outcome.
- Compare appropriate conditional probabilities.
- Numbers can be framed to fit narratives.
- Narrative bias can dominate base rates.
- Averages always lose information.
- When someone says “50% of all X”, ask for absolute numbers.
- Anecdata is sample size 1.
- Selection bias: information providers are not randomly picked.
- Confirmation bias: cherry-picking data that fits priors.
- Social desirability bias: people answer to look good.
- Normalise before comparing large groups.
- Separate stocks from flows.
- Compare large numbers with relevant, well-understood numbers.

Workshop use:

- Good source for “what can go wrong when the visual/story is plausible”.
- Convert into a one-page “AI chart scepticism” checklist.

### H. Economic reasoning: scarcity, incentives, costs, and coordination

**Why it matters:** This is the sharpest “the facilitator” layer to add. Most AI/dataviz talks will stop at prompts, tools, and visual taste. Your old economics teaching material gives a stronger way to ask whether a visual system is worth building, what incentives it creates, and how it changes coordination.

Local sources:

- `WORK/takshashila/Principles of Economics.pptx`
- `WORK/takshashila/gcpp7 cp102/CP 102_Economic Reasoning and Public Policy .pdf`
- `WORK/takshashila/gcpp7 cp102/Assignment 1. CP 102 - Economic Reasoning and Public Policy.pdf`
- `WORK/Book/Sequoia Talk.pptx`
- `WORK/Book/The Other Side.scriv/QuickLook/Preview.html`

Reusable concepts:

- **Scarcity:** if everything is abundant, no economic decision exists. For dataviz, scarce resources are attention, analyst time, trust, review bandwidth, and meeting time.
- **Opportunity cost:** a chart/workflow is not free even if AI generates it cheaply. The real cost is the time spent reviewing it, acting on it, and maintaining its context.
- **Marginal cost:** LLMs collapse the marginal cost of producing another chart/report, but not the marginal cost of judgment or trust.
- **Transaction costs:** dashboards/agents exist to reduce search, interpretation, coordination, and verification costs. Bad AI output increases transaction costs by forcing analysts to check everything.
- **Liquidity / market thickness:** self-service BI fails when users cannot easily find the right insight. Good workflows create “liquidity” between questions, data, and answers.
- **Prices as signals:** in organisations, repeated requests, Slack threads, dashboard refreshes, and meeting questions are signals. Use them to decide what workflows to automate.
- **Incentives:** users will not adopt an AI visual system because it exists. They adopt it when it reduces their cost of getting trusted answers or improves their decision payoff.
- **Coordination:** shared metric definitions and context packs are coordination devices. They let many people/agents produce consistent outputs without renegotiating meaning each time.
- **Comparative advantage:** let LLMs generate candidate views, wording, and code; let deterministic systems compute/validate; let humans judge taste, claim strength, and actionability.
- **Public good vs private good:** shared context, metric definitions, and reviewed examples are internal public goods. Underinvesting in them hurts every downstream chart/agent.
- **Natural monopoly / semantic layer:** one canonical metric/context layer may be better than every team inventing definitions independently.

Workshop use:

- Add a short “economics of AI dataviz” segment near the reproducibility section:
  - What scarce resource is this workflow saving?
  - Whose cost does it reduce?
  - What new verification costs does it create?
  - What shared context/public good must be maintained?
  - What should humans, code, and LLMs each specialise in?

Possible talk line:

> “AI makes charts cheap. It does not make attention, trust, or judgement cheap.”

Possible exercise addition:

Ask participants to add an `economics.md` note to their mini-system:

```md
## Economics of this workflow
- Scarce resource saved:
- User whose cost falls:
- New cost/risk created:
- Shared context needed:
- Human review threshold:
- When this workflow is not worth running:
```

---

## 3. Suggested talk/workshop structure using only local work

### Opening: “I have been trying to do this for 15 years”

Use `The Art of Data Analysis` loop.

- Data work has always been iterative: problem → hypotheses → data → test → more hypotheses → story.
- LLMs do not remove this loop.
- They make it easier to externalise parts of the loop into files, prompts, examples, and agents.

### Case 1: Babbage and the trap of assuming the story is in the data

Use Babbage pitch deck + sales pitch + reflection.

- Dashboards make users self-serve interpretation.
- Babbage tried to automate insight/storytelling.
- Correct insight: stories should adapt when data changes.
- Wrong assumption: product can infer too much cold.
- Lesson: agent needs context, metrics, examples, business logic, and validation.

### Case 2: Weather chart and teaching editorial judgement

Use public weather repo/blog.

- Chart updates repeatably.
- R computes facts; LLM chooses/rephrases commentary.
- Bad summary exposed the problem: technically true is not editorially right.
- Few-shot review cards teach judgement, not prose.
- This is the best concrete “taste/context pack” story.

### Hands-on workflow: build the repeatable system

Participants produce:

1. `context.md`
2. `data_profile.md`
3. `story_candidates.md`
4. `visual_brief.json` or markdown equivalent
5. chart/output
6. `review_checklist.md`
7. `next_run.md`

### Close: production-grade does not mean no human

Use consulting notes + kshipra visual brief.

- Production-grade means clear boundaries: what agent generates, what code validates, what human reviews, what system refuses.
- Reproducibility includes data, code, prompts, examples, acceptance criteria, and review notes.

---

## 4. Assets to prepare next

### Must-have

- Weather example folder:
  - one chart PNG;
  - old weak commentary;
  - review-card screenshot or recreated card;
  - improved commentary;
  - notes on what changed.
- Babbage anonymised metric-monitoring example:
  - metric time series;
  - interestingness scores;
  - candidate story list;
  - chart choice.
- One slide with the old `The Art of Data Analysis` loop.
- One slide/table translating AI-for-data context into dataviz context.
- Templates:
  - `context.md`
  - `story_finding_prompt.md`
  - `visual_brief.md/json`
  - `review_checklist.md`
  - `next_run.md`

### Nice-to-have

- Kshipra visual-brief schema as advanced example.
- Blog-map / personal corpus example if audience asks about examples/style corpora.
- Takshashila/IIMB “pitfalls” mini deck for review section.

---

## 5. Strong lines from your own work

- The chart is the last step.
- Data analysis is an iterative hypothesis-driven process.
- LLMs generate ideas; deterministic systems bless ideas.
- The data has contours of the story, but the model needs context to read those contours.
- Context is taste, caveats, prior work, and judgement in a form the agent can use.
- Few-shot examples teach editorial judgement, not just writing style.
- Prompt engineering is often data curation in disguise.
- Dashboards are not analytics tools; they are reporting surfaces.
- Chat is only one form factor; the durable thing is a trusted workflow.
- Production-grade does not mean fully automated. It means knowing what is automated, what is reviewed, and what happens when the system is uncertain.

---

## 6. Source map scanned / used

High-value files actually inspected:

- `WORK/consulting/workshops/vizchitra-2026-agentic-dataviz/proposal-and-prep.md`
- `WORK/consulting/workshops/vizchitra-2026-agentic-dataviz/README.md`
- `WORK/consulting/workshops/vizchitra-2026-agentic-dataviz/session-notes.md`
- `WORK/BabbageInsight/PitchDeck1.pptx`
- `WORK/BabbageInsight/PitchDeck1.pdf`
- `WORK/BabbageInsight/SalesPitch.pptx`
- `WORK/BabbageInsight/mockup.Rmd`
- `WORK/BabbageInsight/weight_exploration.Rmd`
- `WORK/IIMB/The Art of Data Analysis.pptx`
- `WORK/takshashila/Data Presentation.pptx`
- `WORK/data_work/bangalore/weather/blog-post.md`
- `WORK/data_work/bangalore/weather/blog-post-fewshot-weather.md`
- `WORK/data_work/bangalore/weather/blog-post-wind.md`
- `WORK/data_work/bangalore/weather/weather_chart_common.R`
- `WORK/bangalore-weather/bangalore_weather_update.R`
- `WORK/consulting/README.md`
- `WORK/consulting/consulting-positioning.md`
- `WORK/consulting/ai-product-adoption-playbook.md`
- `WORK/consulting/conversation_insights.md`
- `WORK/consulting/fifthelephant-2026-submission.md`
- `WORK/consulting/workshop-business-plan.md`
- `WORK/kshipra/ais-explorer/server/src/agent/visualBrief.ts`
- `WORK/vibes/blog-embeddings/noenthuda-substack-html/184040183.my-learnings-for-myself-from-babbage.html`
- `WORK/vibes/blog-embeddings/noenthuda-substack-html/183324919.have-we-been-disrupting-bi-the-wrong.html`
- `WORK/vibes/blog-embeddings/noenthuda-substack-html/183034858.how-llms-will-change-business-intelligence.html`
- `WORK/vibes/blog-embeddings/noenthuda-substack-html/186508764.why-analytics-is-useful-and-selection.html`
- `WORK/vibes/blog-embeddings/noenthuda-substack-html/165563513.on-llms-reasoning.html`

Broader scan also found many older talks/decks (`Book/Sequoia Talk.pptx`, `data_work/consulting/pitchdeck_v2.pptx`, `IIMB/IIMB Presentation.pdf`, `Mint/`, sports projects, etc.). Most are less directly relevant unless you want extra anecdotes about markets, public data, or data storytelling traps.
