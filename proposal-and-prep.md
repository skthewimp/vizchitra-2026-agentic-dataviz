# VizChitra 2026 Invited Workshop Proposal

**Working file:** for editorial submission and later workshop prep  
**Prepared:** 2026-06-08  
**Context:** Ad hoc / post-deadline invited workshop pitch after VizChitra editorial review  

---

## Source Notes

Reference links:

- VizChitra 2026 sessions: https://vizchitra.com/2026/sessions
- VizChitra 2026 workshops: https://vizchitra.com/2026/workshops
- Interactive DataViz using AI Coding: https://vizchitra.com/2026/sessions/interactive-dataviz-using-ai-coding
- a public workshop designer's proposal-process post: public AI-assisted proposal-process post
- Weather blog example: public weather-demo blog
- Babbage reflection: https://noenthuda.substack.com/p/my-learnings-from-babbage-insight
- Data Chatter / a geospatial data practitioner episode: https://podcasters.spotify.com/pod/show/data-chatter/episodes/12--Carts-and-graphs-Storytelling-through-maps-e18blbr


### Public Programme Page

Accepted public listing:

- URL: https://vizchitra.com/2026/sessions/agentic-dataviz
- Title: **Agentic DataViz: Build Systems, Not Charts**
- Subtitle: **Find the Story. Teach the Agent. Run It Again.**
- Date/time: **2026-07-03, 14:30-17:30**
- Venue: **Underline Center**
- Speaker line: **the facilitator, Fractional Data & AI Consultant**

Keep **“the chart is the last step”** as the workshop's internal hook/opening line, not the public title.

### Organiser Brief

The original pitch was about building aesthetic and narrative agentic visualisations: using LLMs, skills, prompting, work samples, event-finding, and examples such as `public weather-demo blog`, where the data visualisations are AI-generated.

The organisers liked the pitch but asked for a workshop rather than a talk. Their editorial correction is important:

- Do not make this only about producing attractive narrative visualisations.
- Make the workshop about the harder problem: **production-grade, reproducible dataviz systems using LLMs and agents**.
- Include Babbage: what worked, what did not, and what has changed since then.
- Give participants a repeatable workflow they can take back and use.
- Format: 3 hours, with a break in the middle.
- Likely room capacity: 20.
- They want copy for the programme page plus internal editorial review answers.

### VizChitra 2026 Programme Fit

The current programme already has strong craft/tool workshops:

- Dataviz fundamentals: chart decisions and frameworks.
- AI coding for interactive dataviz: raw dataset to live interactive web visualisation.
- Mobile-first data stories.
- Datawrapper maps.
- D3 custom dataviz.
- Sketching data stories.
- Sensory data walkshop.

The talks/dialogues also include several adjacent themes:

- dashboards that fail users;
- making and choosing in the AI era;
- design for speed and trust in AI-assisted high-stakes work;
- public-data dashboards as infrastructure;
- chart/story curation and what charts do not say.

So this workshop should not be framed as "come vibe-code a chart with Claude". That is already covered. The whitespace is:

> How do you build an LLM-assisted dataviz workflow that can run repeatedly, preserve taste and judgement, find stories in new data, show its work, and be trusted beyond a demo?

### the workshop designer's Submission Post

a public workshop designer's blog post is useful less for content and more for meta-process. He used multiple AI agents to scan the programme/submissions, identify whitespace, generate proposal angles, critique each other's suggestions, and then rewrote the result in his own voice. The key lesson for this proposal: use AI for structure and coverage, but keep the final voice specific, opinionated, and human.

### Local Consulting / Babbage Material To Reuse

Relevant recurring thesis from the consulting docs:

- AI-for-data systems are not plug-and-play.
- The failure mode is often a cold-start problem: the tool lacks business context, examples, prior analyst work, and decision habits.
- Dashboards and chatbots share an adoption problem: users do not want one more self-service surface; they want opinionated, trusted insight delivery.
- The best context is often not only schema metadata. It is prior analyst work: SQL, notebooks, dashboards, metric debates, recurring investigations, caveats, and business review decks.
- The frontier is moving from "chat with data" to AI data workflows: recurring readouts, RCA agents, command centres, embedded assistants, and scheduled/headless agents.
- Trust requires evals, consistency checks, refusal behaviour, evidence, and human review thresholds.

For this workshop, translate those ideas from enterprise AI adoption into dataviz practice:

- The "semantic layer" equivalent in dataviz is the **taste/context layer**: chart preferences, narrative patterns, annotation style, event libraries, caveats, and review checklists.
- A one-off LLM chart is easy. A reusable dataviz system needs a corpus, prompts, tests, examples, and versioned judgement.
- Babbage is the case study for what goes wrong when you expect the system to infer too much too cold.
- The post-Babbage/weather-site work is the case study for what works better now: explicit skills, tighter prompting, work samples, structured story-finding, and acceptance criteria.

### Reworked Workshop Spine

The proposal should now hang on one sentence:

> The chart is the last step.

This comes from three places that fit together:

- The old data-science process: start with a question or hypothesis, inspect the data, iterate, and only then communicate the result.
- Babbage's failed/partial lesson: AI insight systems need context before they can be trusted.
- The current LLM opportunity: we can now turn parts of this process into reusable workflows, as long as we do not pretend the model's first pretty output is the work.

So the workshop is not "AI makes beautiful charts". It is:

1. define the purpose and audience;
2. inspect whether the data can support the story;
3. give the agent context, taste, and examples;
4. ask it to find candidate stories before drawing;
5. generate and critique the visual;
6. save the workflow so it can run again.

---

# Programme Page Copy

## Title

**Agentic DataViz: Build Systems, Not Charts**

Alternative titles:

- **Data Stories That Ship Again**
- **Repeatable AI Workflows for Data Stories**
- **Agentic Dataviz Beyond The Demo**

## Subtitle

Find the Story. Teach the Agent. Run It Again.

Alternative subtitle:

Purpose, data, taste, repeatability.

## Short Description

It is now easy to ask an LLM to make a good-looking chart once. The harder problem is getting it to find the right hypotheses / story, use the right data, match your taste, and do it again tomorrow without everything becoming a fresh act of faith. This hands-on workshop teaches a practical workflow for building repeatable AI-assisted dataviz systems: purpose, data checks, context packs, story-finding prompts, visual critique, and review loops. Participants will leave with a small reusable system they can adapt for their own datasets and teams.

## Long Description

LLMs can now produce surprisingly good charts, dashboards, and data stories. The awkward bit is that most of this work still has a demo problem: it works once, on one dataset, with one lucky prompt. The moment the data changes, the story changes, or another person has to run it, the whole thing becomes fragile.

A useful correction is to remember that visualisation follows the same basic process as data science. You start with a question or hypothesis. You inspect whether the data can actually answer it. You iterate when the first answer is not quite right. The chart comes at the end, as the communication layer. AI does not remove this process. If anything, it makes the process more important, because the first generated chart can look plausible even when the underlying story is weak.

This workshop is about turning that old craft process into a repeatable AI-assisted workflow. We will define the job, inspect the data, create a context pack, ask the model to find candidate stories before charting, generate a visual, critique it, and add simple reproducibility checks. The examples draw on my work at Babbage Insight, where we tried to monitor business metrics and surface stories automatically, and on my more recent AI-generated weather visualisations and narrative posts.

Participants will not just watch a tool produce a chart. They will leave with a small reusable system: input data, context, story-finding prompt, visual-generation prompt, generated output, review checklist, and next-run instructions.

## About You

the facilitator is a data and AI practitioner based in Bangalore. He spent five years as SVP at Delhivery building the data and analytics function, and more recently founded Babbage Insight, an AI analytics startup focused on proactive business insights from data. He now works independently with companies on AI-for-data adoption, analytics workflows, and turning AI tools from demos into trusted working systems. He writes about data, analytics, and AI on *The Art of Data Science*, has written a column for *Mint*, is the author of *Between the Buyer and the Seller*, and studied at IIT Madras and IIM Bangalore.

---

# Editorial Review Answers

## Overall Objective

The objective is to teach participants how to build **repeatable AI-assisted dataviz workflows**, not one-off AI-generated charts.

The central idea is simple: the chart is the last step. A good AI dataviz system needs to know the purpose, inspect the data, understand the intended story, respect visual taste, and only then draw. The workshop turns that into a practical workflow participants can reuse.

By the end of the workshop, participants should understand how to:

- turn a vague "make a visualisation" prompt into a structured production workflow;
- give an LLM enough context to match a desired analytical, narrative, and visual style;
- make the agent identify candidate stories before it starts drawing;
- separate exploration, generation, review, and production;
- preserve reproducibility through files, prompts, examples, and acceptance criteria;
- know where human judgement must remain in the loop.

The practical output is a small but complete starter system: a dataset, a context pack, a story-finding prompt, a visual-generation prompt, a review checklist, and a reproducible output.

## Session-Wise Agenda

### 0:00-0:15 - The Chart Is The Last Step

- Quick framing: the difference between a generated chart and a repeatable system.
- Visualisation as a hypothesis-driven data-science process: question, data, iteration, communication.
- Babbage story: trying to monitor metrics and surface stories automatically, and learning that the system cannot infer all context cold.
- What has changed since: stronger LLMs, coding agents, reusable skills, and easier end-to-end generation.
- What has not changed: purpose, data quality, taste, trust, and review.

### 0:15-0:35 - The Workflow We Will Build

Introduce the repeatable workflow participants will build:

- purpose and audience;
- input data;
- data checks and caveats;
- domain and metric context;
- visual taste and narrative preferences;
- story-finding step;
- chart-generation step;
- critique and revision step;
- reproducibility and review checklist.

The core distinction: the agent should first understand what changed, why it matters, whether the data supports the claim, and what kind of visual story is appropriate.

### 0:35-1:05 - Purpose And Context Pack

Hands-on exercise:

- create a small `context.md` for the dataset and audience;
- define what the output is trying to make the reader see;
- add metric definitions and caveats;
- add visual preferences: what should pop, what should recede, how annotations should work;
- add anti-patterns: chart types, colours, claims, or narrative moves to avoid;
- add one or two work samples or style references.

Output: every participant has a first context pack that encodes purpose, data meaning, and taste.

### 1:05-1:25 - Find The Story Before Drawing

Hands-on exercise:

- ask the LLM to profile the data;
- identify movements, outliers, inflection points, segment differences, missing context, and possible derived concepts;
- force it to propose multiple story candidates;
- ask it to rank them by importance, confidence, and visual suitability;
- choose one story candidate and write down why it is worth visualising.

Output: a short story-candidate memo, with caveats.

### 1:25-1:35 - Break

### 1:35-2:05 - Generate, Critique, Revise

Hands-on exercise:

- generate a chart or small visual story from the chosen candidate;
- ask the LLM to critique the output against the context pack;
- revise for clarity, annotation, hierarchy, colour, and narrative restraint;
- inspect the generated code/spec enough to know what changed.

Output: first visual output plus one revision.

### 2:05-2:35 - Review The Visual Like An Analyst

Hands-on exercise:

- review the visual through six questions: purpose, hypothesis, data support, tool choice, visual hierarchy, annotation;
- test whether the reader can get the first-order takeaway in 5-10 seconds;
- check whether the data supports the claim;
- identify what the AI guessed, what it knew, and what a human still has to decide;
- revise the context pack based on the failure modes.

Output: a reviewed visual and an improved context/review checklist.

### 2:35-2:55 - Make It Reproducible

Hands-on exercise and discussion:

- save the prompt/context structure;
- define required input columns and expected output;
- run the same workflow again on a modified or second dataset;
- compare whether the agent's choices remain consistent.

Then zoom out:

- what changes when this has to run daily, weekly, or for many users;
- what should be automated and what should stay human-reviewed;
- how to create an event library;
- how to maintain a visual-style corpus;
- how to evaluate hallucinated narratives;
- when a dashboard, notebook, static chart, or narrative post is the right output.

Output: a reusable mini-workflow that can be rerun.

### 2:55-3:00 - Wrap

Participants write down:

- one workflow they can apply this to;
- one context artifact they need to create;
- one risk they must guard against.

## Key Takeaways

- A practical workflow for moving from "LLM, make me a chart" to a repeatable AI-assisted dataviz system.
- A context-pack template that captures purpose, audience, data caveats, visual taste, narrative rules, and examples.
- A story-finding prompt pattern that makes the agent inspect the data before it draws anything.
- A review checklist built around purpose, data quality, tool choice, visual hierarchy, annotation, and narrative fit.
- A simple reproducibility pattern: version the data, context, prompt, output, and acceptance criteria.
- A clearer sense of what LLMs are good at, what still fails, and where human judgement remains non-negotiable.

## Prerequisites To Attend

Participants should be comfortable working with data in at least one familiar form: spreadsheets, notebooks, BI tools, Datawrapper/Flourish, R/Python, JavaScript, or similar. They do not need to be expert programmers.

They should have some prior experience making or reviewing charts. The workshop is most useful for people who already care about visual clarity and want to use AI without giving up judgement.

Basic familiarity with ChatGPT, Claude, Gemini, Cursor, Codex, or another LLM/coding assistant will help, but the workflow will be explained from first principles.

## Participant Preparation And Setup

Before the workshop, participants should bring:

- a laptop;
- access to at least one LLM tool they can use during the session: Claude, ChatGPT, Gemini, Cursor, Codex, or equivalent;
- a small dataset they care about, preferably CSV or spreadsheet format;
- 2-3 examples of visualisations they like, or one previous chart/report they have made;
- optional: a GitHub account or local code editor if they want to save and rerun generated code.

For participants who do not bring data, a fallback dataset will be provided. The workshop can be run with browser-based tools, so deep local setup should not be required.

Room requirements:

- projector;
- stable internet;
- power points for participants;
- whiteboard or wall space for workflow mapping;
- ideally tables that allow participants to work individually or in pairs.

## Audience

This is for people who sit between data, design, storytelling, and tools:

- data journalists;
- dataviz designers;
- analytics and BI practitioners;
- product/data analysts;
- researchers who communicate with data;
- civic-tech and public-data practitioners;
- designers experimenting with AI coding tools;
- data leaders trying to make narrative reporting more repeatable.

The ideal participant has made enough charts to know that taste matters, and has used enough AI to know that a plausible answer is not the same as a good one.

## Why This Workshop Fits

the facilitator has worked on this problem from both sides: as a data practitioner trying to communicate messy business data, and as a founder trying to make AI systems do some of that work repeatedly.

At Delhivery, he built and led a data function inside a high-volume operational business, where dashboards, metrics, and investigations had to support real decisions. At Babbage Insight, he tried to build an AI system that could monitor metrics, find interesting movements, and communicate them proactively. That experience exposed the hard parts: data context, metric meaning, user trust, narrative judgement, and the cold-start problem that makes AI-for-data systems look good in demos but weak in production.

Since Babbage, he has continued working on AI-for-data workflows as a consultant and builder. His recent experiments include AI-generated narrative weather visualisations, reusable LLM skills, agentic analysis workflows, and practical systems for getting ChatGPT, Claude, and Codex to produce outputs that match a specific analytical and aesthetic standard.

This workshop is not a generic AI-tools session. It comes from trying to make these systems useful when they have to run repeatedly, explain themselves, and meet a practitioner's taste bar.

---

# Recommended Email Response

Hi,

Thanks, this framing makes sense to me. I agree that the more useful workshop is not "how to make a pretty AI-generated chart once", but how to build a repeatable AI-assisted dataviz workflow that can survive contact with new data, changing stories, and human review.

I've attached the full structure below. The short version is:

**Title:** Agentic DataViz: Build Systems, Not Charts  
**Subtitle:** Find the Story. Teach the Agent. Run It Again.

The workshop will use my Babbage experience as the starting point: what worked about automatically monitoring metrics and surfacing stories, what failed when we expected the system to infer too much context cold, and what has changed now with stronger LLMs, coding agents, reusable skills, and better context workflows. The broader craft lesson is that visualisation still follows a hypothesis-driven data process: question, data, iteration, communication.

Participants will build a small repeatable system: dataset, context pack, story-finding prompt, visual-generation prompt, critique loop, review checklist, and next-run instructions.

The goal is for them to leave with something they can adapt inside their own newsroom, design team, analytics team, research project, or personal data practice.

[Paste programme copy and editorial answers.]

Cheers,  
the facilitator

---

# Later Workshop Prep Backlog

## Assets To Prepare

- Fallback dataset with obvious but non-trivial story candidates.
- One weather-site example showing generated visual + generated narrative.
- One Babbage-style business-metric example, preferably anonymised.
- `context.md` template.
- `story_finding_prompt.md` template.
- `visual_generation_prompt.md` template.
- `review_checklist.md` template.
- `economics.md` template: scarce resource saved, user cost reduced, new verification cost, shared context needed, human review threshold.
- Before/after example: naive prompt output vs context-pack output.
- One reproducibility demo: run the same workflow on two data snapshots.

## Workshop Files To Build

Suggested folder structure:

```text
vizchitra-agentic-dataviz-workshop/
  README.md
  data/
    fallback_dataset.csv
    fallback_dataset_week2.csv
  examples/
    weather/
    business_metrics/
  templates/
    context.md
    story_finding_prompt.md
    visual_generation_prompt.md
    review_checklist.md
    economics.md
  outputs/
    sample_output.html
    sample_output.png
```

## Possible Fallback Datasets

- Bangalore weather: daily temperature, rainfall, humidity, wind, anomalies, heat/rain spells.
- IPL or football results: familiar event-driven data with obvious narrative hooks.
- Public transport or city data: stronger VizChitra fit but may need cleanup.
- Synthetic business metrics: revenue/orders/conversion/traffic with injected events.

## Risks To Handle In The Workshop

- Participants spend too long fighting tool setup.
- People without coding background get stuck on generated code.
- People with coding background over-focus on implementation and miss the workflow design.
- LLMs produce inconsistent outputs because participants use different tools.
- The "production-grade" promise sounds too enterprise-heavy for a VizChitra audience.

Mitigation:

- Keep the core workflow tool-agnostic.
- Provide browser-friendly fallback paths.
- Make the deliverable a workflow artifact, not a perfect deployed app.
- Pair participants when useful.
- Keep examples concrete and visual throughout.

## Strong Lines To Reuse

- One good AI chart is easy. A system that makes acceptable charts repeatedly is the hard part.
- The agent should not start by drawing. It should first find the story.
- Context is not documentation. Context is taste, caveats, prior work, and judgement in a form the agent can use.
- Reproducibility is not only code. It is also prompts, examples, data assumptions, review rules, and refusal conditions.
- Production-grade does not mean fully automated. It means you know which parts are automated, which parts are reviewed, and what happens when the system is uncertain.
- AI makes charts cheap. It does not make attention, trust, or judgement cheap.

## Open Questions

- Should participants be required to bring their own dataset, or should that be optional?
- Should the workshop use one official tool stack for consistency, or be tool-agnostic?
- Can `public weather-demo site` examples be cleaned into a public teaching case quickly?
- Is there an anonymised Babbage-style metric-monitoring example that can be shared without exposing sensitive data?
- Should the final output be a static chart, an HTML page, or a short narrative post with embedded charts?

---

# Appendix: Literature And Reference Map

This is the source map for building the workshop, not a reading list to hand to participants. The workshop should draw from these ideas lightly: one or two concepts per module, translated into practical templates.

## 1. Narrative Visualization And Data Storytelling

**narrative-visualization researchers, "Narrative Visualization: Telling Stories with Data"**  
https://idl.uw.edu/papers/narrative

Use this as the classic anchor. The paper's useful distinction is between author-driven narrative flow and reader-driven exploration. For the workshop, this becomes a design question for the agent: is it producing an explanatory story, an exploratory surface, or a hybrid? This helps prevent the agent from defaulting to generic dashboards when the real task is a narrated visual.

Workshop use:

- Add a prompt field: `intended narrative mode`.
- Ask the agent to choose between explainer, exploratory chart, annotated trend, comparison, or small multiple.
- Include a review question: "Is the visual trying to guide the reader, or asking the reader to explore?"

**Data storytelling / visual data story generation systems: Calliope, DataNarrative, DataReel**

- Calliope: https://arxiv.org/abs/2010.09975
- DataNarrative: https://arxiv.org/abs/2408.05346
- DataReel: https://arxiv.org/abs/2604.25220

These systems are useful because they separate data storytelling into stages: finding data facts, ranking them, arranging them into a story, and rendering the output. The workshop should borrow this pipeline rather than the exact systems.

Workshop use:

- "Find facts before making charts" as a rule.
- Story candidates should include fact type, confidence, visual suitability, and possible narrative order.
- The generated chart should be downstream of a chosen story, not the first action.

## 2. Automated Insight Discovery Before LLMs

**QuickInsights, Microsoft Research / Power BI**  
https://www.microsoft.com/en-us/research/project/quickinsights/  
https://www.microsoft.com/en-us/research/uploads/prod/2019/05/QuickInsights-camera-ready-final.pdf

QuickInsights is directly relevant to Babbage-like thinking: automatically discover interesting patterns such as anomalies, trends, correlations, and outliers in multidimensional data. The key idea to reuse is not the algorithm, but the idea that "interestingness" can be operationalized.

Workshop use:

- Create a lightweight "story-finding checklist": trend, anomaly, outlier, rank change, segment gap, correlation, concentration, seasonality, missingness.
- Ask the LLM to score story candidates on strength, novelty, confidence, and actionability.

**Foresight: Recommending Visual Insights**  
https://arxiv.org/abs/1707.03877

Foresight frames an insight as a strong statistical property and lets users explore the "space of insights", not just the space of dimensions and encodings. This is a strong conceptual bridge to agentic dataviz: the agent should explore possible insights before choosing visual encodings.

Workshop use:

- Separate `insight search` from `chart generation`.
- Ask participants to inspect the agent's candidate list before accepting a visual direction.

**DataShot: Automatic Generation of Fact Sheets from Tabular Data**  
https://www.microsoft.com/en-us/research/publication/datashot-automatic-generation-of-fact-sheets-from-tabular-data/

DataShot uses a pipeline of fact extraction, fact composition, and presentation synthesis. This maps almost perfectly to the proposed workshop structure.

Workshop use:

- Convert the workshop output from "a chart" to "a small fact sheet / visual note".
- Use a three-stage template: extract facts, compose story, synthesize presentation.

## 3. LLM-Based Visualization Generation

**LIDA: grammar-agnostic visualizations and infographics using LLMs**  
https://arxiv.org/abs/2303.02927  
https://microsoft.github.io/lida/

LIDA is probably the closest direct precedent. Its modules are: summarizer, goal explorer, visualization generator, and infographer. This supports the workshop's core structure: summarize data, propose goals, generate visualizations, then revise.

Workshop use:

- Borrow the four-stage mental model, but simplify it for participants:
  1. data summary;
  2. story goals;
  3. chart generation;
  4. critique and repair.
- Show why the "goal explorer" step matters.

**Data Formulator, Microsoft Research**  
https://www.microsoft.com/en-us/research/publication/data-formulator-ai-powered-concept-driven-visualization-authoring/

Data Formulator's key idea is concept-driven visualization authoring: users define high-level concepts, and the AI helps transform data to surface those concepts. It also exposes transformed data and generated programs for inspection.

Workshop use:

- Teach participants to define derived concepts before charting, e.g. "rain spell", "heatwave", "above-normal day", "weekend effect".
- Add a review instruction: "Show the transformed table / derived fields before drawing."
- This is a good antidote to black-box chart generation.

**CoDA: Agentic Systems for Collaborative Data Visualization**  
https://research.google/pubs/coda-agentic-systems-for-collaborative-data-visualization/

CoDA reframes visualization authoring as a collaborative multi-agent problem with roles for metadata analysis, task planning, code generation, and iterative reflection. This is useful as architecture inspiration, but probably too complex for a 3-hour workshop.

Workshop use:

- Mention as the production version of what participants are building manually.
- Translate into simple roles: analyst, storyteller, designer, critic.

**MatPlotAgent / PlotGen / multi-agent scientific visualization**

- MatPlotAgent: https://huggingface.co/papers/2402.11453
- PlotGen: https://arxiv.org/abs/2502.00988
- Multi-Agent Data Visualization and Narrative Generation: https://arxiv.org/abs/2509.00481

These are useful for the "agent roles" section. PlotGen's split into planning, code generation, and feedback agents is especially relevant.

Workshop use:

- Use agent roles as prompts rather than separate infrastructure:
  - data profiler;
  - story scout;
  - chart builder;
  - visual critic;
  - reproducibility reviewer.

## 4. Evaluation, Trust, And Reproducibility

**Vi(E)va LLM: conceptual stack for evaluating generative AI visualizations**  
https://arxiv.org/abs/2402.02167

Useful for framing evaluation as layered: generated visualization quality is not one thing. There are code, chart, data, image, and interpretation layers.

Workshop use:

- Build the review checklist in layers:
  - Does code run?
  - Does chart use the right data?
  - Is the visual encoding legal and readable?
  - Is the narrative faithful?
  - Are uncertainty and caveats handled?

**Evaluating LLMs' abilities to create charts**  
https://www.sciencedirect.com/science/article/pii/S0097849326000154

This is a useful cautionary source. It finds that even strong LLMs still fail on chart generation in diverse ways. That supports the workshop's insistence on review, not blind generation.

Workshop use:

- Use as evidence for "LLMs can make plausible chart code that is still wrong."
- Add a final check where participants compare visual output against the underlying data.

**VisEval / ChartEval / chart QA evaluation**

- VisEval: https://app.argminai.com/arxiv-dashboard/papers/2407.00981v2
- ChartEval: https://aclanthology.org/2025.ijcnlp-demo.10.pdf
- Charting the Future: https://arxiv.org/abs/2409.18764

These systems evaluate generated charts using validity, legality, readability, scene graphs, or chart question-answering. We do not need to implement them, but they give useful review categories.

Workshop use:

- Convert into a human checklist:
  - validity: did it render?
  - legality: did it answer the stated question?
  - fidelity: are values and labels correct?
  - readability: can the intended reader parse it quickly?
  - narrative: does the takeaway follow from the visual?

**Misleading visualisation detection and LLM chart literacy**

- MisVisFix: https://www.sciencestack.ai/paper/2508.04679
- How good are LLMs at detecting misleading visualizations?: https://researchportal.hkust.edu.hk/en/publications/how-good-or-bad-are-llms-at-detecting-misleading-visualizations
- Adobe: human chart takeaways vs LLM predictions: https://research.adobe.com/publication/how-aligned-are-human-chart-takeaways-and-llm-predictions-a-case-study-on-bar-charts-with-varying-layouts/
- Georgia Tech visualization literacy eval: public visualization-literacy evaluation paper

These sources support a good discussion: LLMs can critique charts, but their takeaways may not match human takeaways. This is especially relevant for narrative visualisation.

Workshop use:

- Use LLM critique, but do not outsource final judgement to it.
- Ask humans to write the intended takeaway before asking the model to critique the chart.
- Compare "what the agent thinks the chart says" with "what the author intended".

## 5. Visualization Recommendation And Design Knowledge

**Draco: formalizing visualization design knowledge as constraints**  
https://dig.cmu.edu/publications/2018-draco.html

Draco is useful because it treats visual design knowledge as constraints and tradeoffs, not vibes. For this workshop, this becomes the reason to write a style/context file: the agent needs explicit preferences and constraints.

Workshop use:

- Add `hard constraints` and `soft preferences` to the context pack.
- Hard constraints: no pie charts, accessible colors, label units, no truncated axes unless justified.
- Soft preferences: prefer small multiples, direct labels, restrained annotation, minimal chartjunk.

**Data Formulator and concept binding**

Also fits here: design intent should be expressed as data concepts and visual channels, not only as a prompt like "make this beautiful".

Workshop use:

- Ask participants to specify "what should be compared" before specifying "what chart should be drawn".

## 6. Agentic Workflow Design

**Anthropic: Building Effective Agents**  
https://www.anthropic.com/engineering/building-effective-agents

The main idea to borrow is the distinction between workflows and agents. For this workshop, the honest framing is that participants are building a workflow with agentic steps, not unleashing an autonomous agent.

Workshop use:

- Keep the architecture simple and inspectable.
- Use evaluator-optimizer as the critique/revision loop.
- Avoid overengineering multi-agent systems during the workshop.

**OpenAI Evals / evaluation as application development**
https://cookbook.openai.com/examples/evaluation/getting_started_with_openai_evals

Useful because it frames evals as part of the development cycle, not an afterthought.

Workshop use:

- Version prompt + context + dataset + output.
- Add 3-5 acceptance tests for each generated visual.
- Rerun on a second data snapshot.

**Reflection / evaluator-optimizer patterns**

- AutoGen reflection: https://microsoft.github.io/autogen/stable/user-guide/core-user-guide/design-patterns/reflection.html
- AWS evaluator-reflect-refine: https://docs.aws.amazon.com/prescriptive-guidance/latest/agentic-ai-patterns/evaluator-reflect-refine-loop-patterns.html

Workshop use:

- Teach a simple generate -> critique -> revise loop.
- Make critique rubric-specific, not "make it better".
- Include a stopping rule: stop after one revision unless a hard error remains.

## 7. Human-Centered AI, Trust, And Control

**Google People + AI Guidebook worksheets**  
https://pair.withgoogle.com/worksheet/People%20%2B%20AI%20Guidebook%20-%20All%20Worksheets.pdf

Useful for the human-control side: when should users verify outputs, when should uncertainty be shown, and what explanation is needed?

Workshop use:

- Ask: "What decision could this visual influence?"
- If the stakes are high, require explicit caveats and human verification.
- Add an uncertainty / confidence field to story candidates.

**Human-centered explainable AI surveys**

- Human-Centered XAI: https://arxiv.org/abs/2110.10790
- Human-centered design of XAI survey: https://arxiv.org/abs/2410.21183

Workshop use:

- Keep explanations user-centered: explain what the audience needs to verify, not how impressive the model is.
- Build the review checklist around the human decision context.

## 8. Natural Language Interfaces For Data And Visualization

**Natural Language Interfaces for Tabular Data Querying and Visualization: A Survey**  
https://arxiv.org/abs/2310.17894

**Chatbot-Based Natural Language Interfaces for Data Visualisation: A Scoping Review**  
https://diposit.ub.edu/dspace/handle/2445/199360?mode=full

These sources are background for the broader lineage: natural language to data query, natural language to visualization, and the limits of chat as an interface.

Workshop use:

- Use this to justify not making the workshop a "prompt better" session.
- The workflow should include structured artifacts, not only chat turns.

## 9. the facilitator's Own Material To Integrate

**Babbage reflection**  
https://noenthuda.substack.com/p/my-learnings-from-babbage-insight

Use as the lived case study: proactive insights are compelling, but the hard parts are context, metric meaning, trust, adoption, and repeatability.

**Weather blog**  
public weather-demo blog

Use as the current working demo: AI-generated narrative visualisations can be aesthetically acceptable if the system has the right context, examples, and review loop.

**AI-for-data consulting docs in this repo**

Use these to adapt enterprise AI adoption ideas into dataviz language:

- cold start -> blank-context chart generation;
- semantic layer -> taste/context pack;
- analyst work corpus -> prior visualisations and narrative examples;
- evals -> chart/story review checklist;
- adoption cadence -> repeated publishing workflow.

**Data Chatter S1E12 with a geospatial data practitioner: "Carts and graphs: Storytelling through maps"**  
https://podcasters.spotify.com/pod/show/data-chatter/episodes/12--Carts-and-graphs-Storytelling-through-maps-e18blbr  
Transcript generated locally on 2026-06-08 from the podcast RSS audio. Temporary transcript path: `/private/tmp/datachatter-transcript/example-transcript.txt`.

This episode is useful mainly for one point: mapmaking, like other visualisation, follows the same basic hypothesis/process logic as data science. The visual is the final communication layer, not the starting point. That is the only idea to carry into the proposal itself.

```text
Hypothesis-To-Visual Review

Before accepting an AI-generated visual, ask:

1. Purpose: What is this trying to make the reader see?
2. Hypothesis: What claim or question is this visual built around?
3. Data: Is the data strong enough for that claim?
4. Visual form: Is this the right way to communicate it?
5. Annotation: What will the reader understand in 5-10 seconds?
6. Reproducibility: What would need to be saved to run this again?
```

## Recommended Workshop Spine After Literature Review

The source map supports this sharper structure:

1. **Do not start with the chart.** Start with data understanding and story candidates. Draw from QuickInsights, Foresight, DataShot, LIDA.
2. **Give the agent a context pack.** Include metric definitions, derived concepts, visual constraints, style preferences, and examples. Draw from Data Formulator, Draco, and the facilitator's consulting thesis.
3. **Generate through roles, not vibes.** Use data profiler, story scout, chart builder, critic, and reproducibility reviewer. Draw from CoDA, PlotGen, Anthropic agent patterns.
4. **Review in layers.** Code validity, data fidelity, visual readability, narrative faithfulness, uncertainty. Draw from Vi(E)va LLM, VisEval, ChartEval, LLM chart-evaluation papers.
5. **Keep the human in control.** AI suggests stories and drafts visuals; humans own taste, claim strength, and publication judgement. Draw from PAIR / human-centered XAI.

## Possible Participant Handout

Keep the handout to one page:

```text
Agentic Dataviz Workflow

1. Define the job
   - audience
   - decision/context
   - narrative mode

2. Build the context pack
   - metric definitions
   - caveats
   - visual constraints
   - style examples

3. Find stories first
   - trend
   - anomaly
   - rank change
   - segment gap
   - correlation
   - missingness

4. Generate the visual
   - chosen story
   - chart type
   - annotations
   - source/caveat

5. Review and rerun
   - code runs
   - numbers match
   - visual is readable
   - takeaway is faithful
   - reruns are consistent
```
