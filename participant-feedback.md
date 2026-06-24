# Participant Feedback - What People Want

Purpose: growing notes from registered/interested participants. Use this to tune workshop promise, exercises, and artifacts.

## Feedback 1 - Reduce tail-end chart fiddling

> I’m hoping to reduce time to “the type of graphs I like” drastically. Ideally, automate my data vis altogether.
>
> Currently, ai helps me get to “a graph” and then I spend a lot of time fiddling manually to get it just right. Cutting that tail of small but crucial edits.. reliably, across a wide variety of data viz tasks would be masssive.
>
> Plus, a chance to learn best practices.. it’s a system so it can encode taste that I have not refined myself.. like LaTeX for typesetting.

### What this means

They want AI to move from **“a graph”** to **“my graph”** faster.

Main pain: final-mile edits:

- labels;
- spacing;
- colours;
- annotations;
- axis formatting;
- clutter removal;
- title/subtitle;
- legend removal/placement;
- source/caption;
- consistency across chart types.

### Workshop implication

Frame part of workshop as building a **visual typesetting system** or **dataviz style compiler**.

Useful line:

> AI gets you to “a graph”. The workshop is about getting from “a graph” to “my graph” reliably.

### Exercise implication

Ask participants:

> What are your recurring chart fiddles?

Convert answers into reusable rules in `taste.md` / visual constitution.

### Teaching implication

Balance three taste layers:

1. personal taste — graphs I like;
2. craft principles — workshop visual principles and dataviz best practices;
3. audience context — appropriate for this reader and decision.

Formula:

> Personal taste + craft principles + audience context = reusable visual constitution.

---

## Feedback 2 - Modular skill system, not one monolithic workflow

> I think i would most want a system of skills that I can use for either parts or the whole process. And learn why the system is that way, and how I can modify or extend it

### What this means

They want reusable building blocks, not only a single end-to-end recipe.

They want to understand:

- what each skill does;
- when to use it alone;
- when to chain skills together;
- why workflow order matters;
- how to edit the skills for their own taste, tools, and data contexts.

### Workshop implication

Position output as a **skill stack**:

1. context skill — explain dataset, audience, constraints;
2. taste skill — encode visual preferences and anti-patterns;
3. story skill — find candidate claims before charting;
4. brief skill — convert claim into visual spec;
5. generation skill — produce chart/code;
6. review skill — critique and revise;
7. reproducibility skill — save next-run notes.

Participants can use:

- one skill for a small task;
- a subset for an existing workflow;
- full chain for new presentation visual.

### Teaching implication

Do not present workflow as magic pipeline. Explain design logic:

- context before story because columns alone do not imply importance;
- story before chart because chart form depends on claim/comparison;
- brief before generation because output needs acceptance criteria;
- review after rendering because first outputs are plausible, not trustworthy;
- next-run notes because system quality compounds over repeated use.

### Exercise implication

Add a short “modify the system” moment near the end:

Ask participants to choose one skill and edit it:

- add one personal taste rule;
- add one banned chart pattern;
- add one domain caveat;
- add one review question;
- add one output-format preference.

### Useful line

> You are not learning one prompt. You are learning the architecture of a chart-making agent, so you can swap parts in and out.

---

## Feedback 3 - Production workflow for a large research organization

> Climate policy think tank; data visualization specialist inside communications team. Personal need is not basic chart-making help. Wider 200-300 person research organization is curious about AI for simple charts: bar, line, area, etc. Wants to explore production workflow where style guidelines, knowledge, and preferences can be uploaded, then prompts generate charts that meet expected standards. Also wants scalable guidance: what AI can/cannot do, when to use it, when not to, and how to explain this to a wider team. More interested in assembly-line workflows than bespoke one-off custom charts.

### What this means

This participant is already a dataviz practitioner. Main need is organizational enablement:

- turn expert judgement into reusable style/context instructions;
- support non-specialists making basic charts without breaking standards;
- create repeatable production workflows, not artisanal one-off prompts;
- define quality gates and refusal conditions;
- help a large team understand realistic AI use cases and limits.

### Workshop implication

Lean harder into **Build Systems, Not Charts**. The workshop should speak to two audiences at once:

1. individual participants making one better chart;
2. dataviz/communications leads designing a team workflow.

Add explicit language around:

- style-guide-as-system-prompt;
- chart factory / assembly-line workflow;
- reusable chart QA checklist;
- simple chart types as production target, not only fancy custom visuals;
- governance: when AI is appropriate, when human expert review is mandatory.

### Exercise implication

Add optional “team workflow” framing to artifacts:

- `taste.md` can become organization style guide excerpt;
- `context.md` can become project/data brief template;
- `visual_brief_template.md` can become request form before chart production;
- `chart_review_checklist.md` can become QA gate before publication;
- `next_run.md` can become reusable SOP/change log.

Prompt participants to ask:

> If 50 colleagues used this workflow next month, what would you want standardized, banned, reviewed, or escalated?

### Teaching implication

Include a clear AI suitability matrix:

Good use cases:

- first-pass basic charts from clean data;
- converting style guides into chart rules;
- generating alternatives for claim/comparison/chart type;
- checking chart against house style;
- drafting chart code/specs;
- documenting repeatable workflows.

Risky use cases:

- messy or undocumented data;
- unsupported causal claims;
- high-stakes policy claims without analyst review;
- charts where denominators/definitions are ambiguous;
- fully automated publishing with no human QA;
- visualizations requiring deep domain judgement or bespoke interaction design.

### Useful line

> The scalable AI win is not fancy charts. It is making the boring charts consistently good, on-brand, and reviewable.

---

## Feedback 4 - Reliable AI analysis, honest insight, repeated market/economic datasets

> Works with market and economic data. Currently shares data with Claude and asks it to analyse. Sometimes gets strong insights and visuals, e.g. India's forex reserves: gold share rose mainly due to gold price increase, not large extra gold purchases. But AI also sometimes tries too hard to find an insight because asked, builds a weak chart/story, then admits the insight is not meaningful when challenged. Wants a process where AI can say “there is no meaningful insight here.” Also wants fewer prompts due to Claude Pro limits, repeated agents for changing datasets, simpler chart choice, and guidance on choosing tools/models by task, accuracy, and cost.

### What this means

This participant wants to move from lucky insight discovery to a reliable analytical system.

Main needs:

- repeatable AI-assisted analysis workflow;
- honest null result: AI should be allowed to say “nothing meaningful here”;
- less back-and-forth because usage limits matter;
- recurring agents for datasets that update over time;
- simple chart choices that explain, not impress;
- model/tool routing based on task complexity, risk, and cost.

### Workshop implication

Strengthen the “story before chart” section into **evidence before story**.

The agent must not only generate candidate stories. It must also:

- rank evidence strength;
- separate signal from noise;
- identify mechanical/decomposition explanations;
- list alternative explanations;
- say when a chart is not warranted;
- flag when a finding is too weak, obvious, or misleading.

Add a norm:

> A good AI analyst is allowed to come back with no story.

### Exercise implication

In `story_finding_prompt.md`, add explicit output fields:

- strongest supported insight;
- “boring but important” finding;
- null/no-insight finding;
- what would be overclaiming;
- alternative explanations;
- confidence level;
- checks needed before publication;
- recommended chart only if chart improves understanding.

Add a short participant check:

> Ask the model: “What is the strongest argument against this insight?”

### Teaching implication

Introduce a lightweight AI analysis process:

1. Human frames question, audience, known caveats.
2. AI profiles data and checks definitions/grain.
3. AI proposes candidate findings with evidence strength.
4. AI explicitly searches for null/boring explanations.
5. Human chooses only supported claim.
6. AI creates visual brief and simple chart.
7. AI reviews for overclaiming, complexity, and missing context.
8. Workflow saves next-run instructions for updated data.

### Cost / model-routing implication

Add a small “use cheap/fast vs expensive/smart model” guide:

Use cheaper/faster model for:

- cleaning column names;
- summarising schema;
- drafting chart code from a clear brief;
- applying known style rules;
- mechanical refresh of existing chart.

Use stronger model for:

- ambiguous analytical questions;
- detecting weak/unsupported insights;
- choosing among competing stories;
- causal language and policy/economic interpretation;
- designing reusable workflow/agent instructions.

### Useful lines

> The goal is not “find me an insight.” The goal is “tell me what, if anything, the data can honestly support.”

> Sometimes the most valuable output is: no chart, no claim, collect better data.

---

## Feedback 5 - More conceptual, LLM-agnostic, enterprise production tools

> Wants less hands-on and more conceptual framework/understanding. Finds zooming into hands-on and back out to concepts mentally exhausting. Prefers hands-on files shared separately at end. Also wants workshop to be LLM-agnostic, not Claude-heavy, because enterprises often use ChatGPT Enterprise or GitHub Copilot; Claude is more startup/personal. Wants examples of applying the ideas to enterprise dashboard tools like Tableau or Power BI, and wants something production-ready.

### What this means

This participant values reusable mental models over live tool choreography.

Main needs:

- clear conceptual architecture;
- fewer live hands-on interruptions;
- tool-neutral language;
- enterprise compatibility: ChatGPT Enterprise, Copilot, Tableau, Power BI;
- production path, not toy prompt demo.

### Workshop implication

Avoid a session that constantly alternates between lecture and fiddly execution. Structure as:

1. concept block;
2. short demo to make concept concrete;
3. optional participant reflection;
4. leave detailed hands-on templates/files for after.

Use neutral terms:

- “LLM/agent” instead of Claude;
- “workspace/tool” instead of one product;
- “chart code/spec/dashboard instruction” instead of only Python output.

### Enterprise/dashboard implication

Show that the same workflow can produce:

- Python/R chart code;
- Datawrapper/Flourish instructions;
- Tableau calculated fields + chart spec;
- Power BI DAX/measures + visual setup checklist;
- dashboard QA checklist;
- refresh notes for recurring reports.

Do not promise full dashboard automation inside 3 hours. Promise a production grammar:

> context → data definitions → insight test → visual brief → tool-specific implementation → QA gate → refresh notes.

### Exercise implication

Offer two paths:

- **Follow-along path:** use files during session and generate one chart.
- **Concept path:** annotate the workflow and decide how it maps to their enterprise stack.

For concept-path participants, outputs can be:

- team workflow sketch;
- dashboard QA checklist;
- style/instruction pack;
- Power BI/Tableau implementation brief.

### Useful lines

> The workflow is tool-agnostic. Claude, ChatGPT, Copilot, Tableau, Power BI are implementation surfaces, not the method.

> Production does not mean the model publishes the dashboard. Production means the workflow has roles, specs, QA gates, and refresh rules.

---

## Feedback 6 - Non-technical AI primer for rigorous data storytelling

> I don't have a background in AI, but my workplace is very AI friendly. I've recently been exposed to some workflows where AI is being used to assist with data storytelling, from identifying potential datasets that could be stories to generating visual outputs. Seeing this has made me curious about how these systems actually work beyond the final result.
>
> Some things I'd particularly like to understand are:
> - Basic introduction for someone without a technical AI background about how these tools function.
> - How AI can be used not just to generate charts, but also to identify potential stories or insights from datasets.
> - How much of the workflow can realistically be automated, and where human judgment remains essential.
> - How prompts, context, and review processes influence the quality of the final output.
> - Even when AI surfaces a potential story, it still needs to be verified, fact-checked, and assessed for relevance. I'd be interested in learning if this review process can be easier or automated.
>
> Overall, I'm hoping to leave with a better understanding of how AI can support the end-to-end process of data storytelling while maintaining editorial rigor and reliability.

### What this means

This participant wants the workshop to explain the machinery, not only show the output.

Main needs:

- non-technical explanation of how LLMs/AI agents work;
- how AI can support story discovery before chart generation;
- realistic boundary between automation and human editorial judgment;
- why prompts, context, examples, and review loops change output quality;
- how verification and fact-checking can be systematized without surrendering editorial responsibility.

### Workshop implication

Add a clear **AI-assisted data storytelling pipeline** framing:

1. identify possible datasets;
2. profile data and definitions;
3. suggest candidate story angles;
4. test evidence and caveats;
5. draft visual briefs;
6. generate rough charts or dashboard specs;
7. review claims against data;
8. refine narrative, labels, and design;
9. publish only after human editorial sign-off.

The session should explicitly say:

> AI can propose stories; humans must commission, verify, and publish them.

### Teaching implication

Include a plain-language AI primer:

- LLMs predict plausible next text/code from context;
- they are good at pattern matching, summarising, drafting, translating between formats, and generating alternatives;
- they can sound confident even when wrong;
- they do not automatically know whether a claim is true in the dataset unless forced to show evidence;
- agents are workflows around models: prompts, tools, files, checks, and review loops.

Use this to demystify why the same model gives better output when given:

- clear role;
- dataset context;
- audience;
- editorial standard;
- examples of good/bad output;
- required evidence format;
- explicit review checklist.

### Automation realism implication

Add a traffic-light model.

**Green: often safe to automate**

- schema summaries;
- data profiling;
- first-pass chart code;
- alt text;
- chart variants;
- style-rule checks;
- anomaly candidates;
- draft captions.

**Yellow: automate drafts, require review**

- insight selection;
- headline wording;
- chart type choice;
- narrative framing;
- relevance to audience;
- caveat wording;
- dashboard recommendations.

**Red: human owns**

- final truth claims;
- causal claims;
- editorial relevance;
- ethical/fairness implications;
- high-stakes policy/business interpretation;
- publish/no-publish decision.

### Exercise implication

Add a demo where AI receives a dataset summary/schema and is asked to find stories before making charts:

> Act as a data editor. Given this dataset summary, suggest 5 possible story angles. For each, include the exact metric, likely chart, strongest caveat, verification step, and reason this would matter to the audience.

Then show how quality improves when the prompt adds:

- audience;
- editorial bar;
- “do not force an insight” instruction;
- required evidence rows/calculations;
- reviewer critique pass.

### Review and verification implication

Make review a first-class artifact, not an afterthought.

AI can help by generating:

- claim-to-evidence tables;
- verification checklists;
- reproducible calculation/code snippets;
- skeptical editor questions;
- alternative explanations;
- source/definition checks;
- “what would make this claim false?” tests.

But final verification should rely on deterministic checks where possible:

- code over vibes;
- exact rows/calculations over summaries;
- source links and definitions over memory;
- separate critique pass over same-pass self-approval.

### Useful lines

> The goal is not to trust AI more. The goal is to make AI outputs easier to inspect, challenge, and verify.

> AI is useful not because it removes judgment, but because it can make judgment better structured and faster.

> A reliable AI workflow has prompts, context, tools, evidence, review gates, and humans who know when to say no.
