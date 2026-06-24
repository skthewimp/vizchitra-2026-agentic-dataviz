# Literature Survey Synthesis - Agentic DataViz Workshop

Source: pasted Claude literature survey from the facilitator, 2026-06-22. Treat as a design input, not a fully verified bibliography. Core claims below are workshop-useful; citations still need final source check before public slides.

## 1. Main design takeaway

The survey strongly supports the current workshop thesis:

> This is an architecture problem, not a prompting trick.

The mature pattern is not “find the magic chart prompt.” It is:

1. define the job;
2. inspect and transform data;
3. externalize context/taste;
4. generate candidate stories;
5. create chart/spec;
6. inspect transformed data + rendered chart;
7. revise;
8. preserve state for next run.

This maps almost exactly to the existing workshop spine: context pack → story finding → visual brief → chart generation → critique → next-run instructions.

## 2. Three workshop pillars from the survey

### Pillar A - Separate transformation from visualization

Do not ask the model to jump straight from raw data to final chart. Separate:

- data profiling;
- reshaping / aggregation / calculated fields;
- chart specification;
- visual styling.

Workshop use:

- Add this as a named principle before chart generation.
- In prompts, ask for transformed table / aggregation logic before asking for the visual.
- For Tableau/Power BI participants, map this to calculated fields, measures, model grain, and visual spec.

Useful line:

> Most AI chart failures are not drawing failures. They are data transformation failures wearing a nice outfit.

### Pillar B - First chart is a draft

LLM chart output can be plausible, pretty, and wrong. The workflow must force:

- multiple candidates;
- explicit evidence;
- alternative explanations;
- inspection of generated code/spec;
- inspection of transformed data;
- rendered-chart critique.

Workshop use:

- Keep “generate first chart” explicitly labelled as draft.
- Add a rendered-output review loop, not only prompt review.
- Add a question: “What transformed data is this chart actually plotting?”

Useful line:

> Trust the workflow, not the first chart.

### Pillar C - Reproducibility is structural

Repeatability comes from system design, not model magic:

- persistent context packs;
- threads/history;
- parameterised workflows;
- saved transformed data;
- saved chart specs/code;
- review logs;
- refresh rules.

Workshop use:

- Make `next_run.md` more important.
- Add optional production architecture slide: free-form chat vs reusable endpoint/spec.
- For repeated analyses, recommend wrapping known-good transformations and letting the model fill parameters, not rewrite SQL/code from scratch.

Useful line:

> Doing it again tomorrow is an engineering choice, not a model capability.

## 3. Evidence-backed slide ideas

### Slide: Field arc

Frame dataviz waves:

1. clarity: make charts readable;
2. systems: grammar of graphics, reusable chart descriptions;
3. convergence: notebooks, BI, publishing tools blur;
4. democratization: prompt-to-chart makes output cheap.

Point:

> When charts become cheap, value moves from producing charts to using them well.

Use carefully unless source verified.

### Slide: Data Formulator as reference architecture

Design decisions to cite:

- separates high-level visual intent from low-level data transformation;
- exposes transformed table and generated program for inspection;
- generates multiple visualization options because intent is ambiguous;
- 0.7 enterprise version stresses persistent data/workflow/visualization context, not isolated chat.

Workshop mapping:

- concept shelf/context pack;
- data view/transformed data inspection;
- visualization options/story candidates;
- shared workspace/next-run notes.

### Slide: D3 generation cautionary tale

Use Scott Logic + Observable comparison:

- Scott Logic: even with one-shot prompting, no tested model exceeded 80% correct; common failures included wrong data handling and D3 version/API mismatch.
- Observable: Claude generated useful D3, but made assumptions about sample size, old-ish library version, generated synthetic extra data when asked to assume more data existed, and made aesthetic choices needing review.

Point:

> The same “AI can make D3” claim is true and dangerous. It works when surrounded by context and verification.

### Slide: Academic convergence

Use as optional speaker note, not heavy slide:

- LIDA decomposes visualization into summarizer, goal explorer, chart generator, stylizer.
- VisEval evaluates charts on multiple dimensions, including validity, legality, readability; single “looks good” judgement is insufficient.
- A2P-Vis style pipelines show analyzer → presenter architecture: profiling, candidate visual directions, code execution, quality checks, narrative assembly.

Point:

> Research systems independently converge on the same workflow: inspect → propose → generate → check → narrate.

## 4. Workshop structure changes implied

### Add concept block: “architecture of a chart-making agent”

Show these modules:

1. Context layer: audience, metric definitions, style, caveats.
2. Data layer: source, grain, cleaning, transformations.
3. Insight layer: candidates, evidence strength, null result.
4. Spec layer: chart grammar/brief/tool instructions.
5. Render layer: code/image/dashboard visual.
6. Review layer: analytical + visual + production QA.
7. Memory layer: next-run instructions, endpoint parameters, versioning.

### Add prompt output requirements

For story finding:

- transformed-data plan;
- candidate stories;
- no-insight option;
- confidence / risk;
- “what would be overclaiming.”

For chart generation:

- show aggregation/transformation before chart;
- return chart spec/code separately from transformed data;
- list assumptions;
- state what to inspect.

For review:

- verify the plotted data;
- verify chart answers the intended question;
- check readability/taste;
- check unsupported claims;
- decide revise / reject / no chart.

## 5. Vega-Lite / grammar-of-graphics note

The survey strongly recommends declarative specs like Vega-Lite where possible.

Workshop stance:

- Do not make Vega-Lite mandatory. Audience may use Python, R, Tableau, Power BI, Datawrapper, or generated images.
- Teach the principle: prefer explicit chart specs over opaque one-shot image output.
- Show that a visual brief is a human-readable grammar even when tool output differs.

Useful line:

> If the tool cannot emit Vega-Lite, make it emit a visual brief. Same discipline, lower tooling burden.

## 6. Production pattern for repeated work

For recurring analysis, avoid free-generation every run.

Better pattern:

1. Human/analyst designs trusted transformation once.
2. Workflow exposes parameters: date range, segment, metric, comparison, threshold.
3. LLM fills parameters and writes narrative/brief.
4. System runs fixed query/chart code.
5. Human reviews exceptions and publication-risk items.

Enterprise mapping:

- SQL/dbt view or BI semantic model = trusted transformation;
- Tableau/Power BI measure = parameterized calculation;
- prompt/agent = request router + explainer + QA assistant;
- dashboard QA checklist = publication gate.

## 7. References to verify before final public use

### Strong anchors already worth keeping

- Microsoft Data Formulator / Data Formulator 0.7.
- LIDA.
- Scott Logic D3 experiment.
- Observable D3 experiment.
- VisEval benchmark.
- Vega-Lite.

### Needs verification / caution

- Exact “Fourth Wave” framing and authorship.
- Exact “Agentic Visualization” claims and term origin.
- Newer 2025/2026 arXiv papers may be useful but should not dominate slides.
- Any numeric claim beyond what source directly says.
