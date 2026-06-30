# Skill gap analysis for weather-blog demo

Question: if Karthik gives the agent a question like “does Bangalore rain around 4pm?”, what skills are needed so the analysis is Karthik's analysis, not generic LLM priors?

## Existing useful skills

### 1. `r-analysis-rules`

Covers R coding style and pipeline hygiene:

- tidyverse-first
- small composable transformations
- keep acquisition separate from analysis/charting
- prefer documented canonical datasets
- avoid destructive git ops

Useful, but mostly about coding style, not analytical judgment.

### 2. `karthik-r-exploration-style`

Covers exploratory notebook shape:

- short RMarkdown chunks
- inspect raw data early
- practical, iterative exploration
- quick tables/plots
- tidytable/tidyverse defaults
- rough analyst-thinking style

Very useful for live exploration. Missing stronger rules for causal/denominator/estimand discipline.

### 3. `dataviz-selector`

Covers chart-form choice:

- one claim per chart
- identify comparison
- choose visual form
- avoid misleading decorative forms

Useful after we know the claim and computed facts.

### 4. `karthik-data-visualization`

Covers Karthik chart taste:

- comparison-first
- low chartjunk
- direct labels
- annotations
- graphical integrity
- source/caveat notes

Useful for final chart and chart critique.

### 5. `karthik-writing-style`

Useful for blogpost prose once analysis is done.

Should not be used to invent analysis. It should only phrase computed facts.

## Main gap

Existing skills mostly cover:

```text
code style → exploration style → chart selection → chart styling → prose style
```

Missing middle:

```text
question → operational definition → denominator → analytical plan → validation → computed facts → defensible claim
```

That is exactly where “Karthik's analysis” lives.

## Skills we need to build

### A. `karthik-analysis-planner`

Purpose: turn a natural-language question into a defensible analysis plan.

For “does it rain at 4pm?”, it should force:

- what does “rain at 4pm” mean?
  - any measurable rain in 4-5pm hour?
  - rainfall amount during 4pm hour?
  - rain event starting at 4pm?
- what is the unit of analysis?
  - hour, day, rain event, month?
- what is the denominator?
  - all observed 4pm hours?
  - all days?
  - only rainy days?
- what comparison matters?
  - 4pm vs other hours
  - monsoon vs non-monsoon
  - recent years vs historical
- what would falsify the claim?
- what caveats must survive to the final post?

Output should be an analysis contract, not prose.

### B. `karthik-hypothesis-generator`

Purpose: generate testable hypotheses from the question plus data profile.

Not generic brainstorming. Each hypothesis must be analyzable.

For each hypothesis, require:

- claim
- metric
- denominator
- comparison
- test / calculation
- likely chart
- possible confound
- what would falsify this

Example for 4pm rain:

1. Rain probability peaks in late afternoon.
2. The 4pm peak is stronger in monsoon months.
3. Pre-monsoon rain is more evening-skewed than monsoon rain.
4. Total rainfall and rain probability tell different stories.
5. Recent years have shifted the hourly rain profile.

This should run after data profiling, before evidence building.

### C. `karthik-evidence-builder`

Purpose: execute the analysis only from data, producing computed facts.

Rules:

- never answer from pretraining
- inspect schema first
- print row grain and missingness
- compute denominators explicitly
- produce small facts tables
- compare alternative definitions where plausible
- save reproducible code
- flag when data cannot answer the question

Output:

```text
data_profile.md
analysis_plan.md
computed_facts.csv
sanity_checks.md
candidate_claims.md
```

### D. `karthik-claim-validator`

Purpose: decide which candidate claims are actually supported.

Checks:

- claim matches metric
- denominator visible
- comparison fair
- outliers not driving story
- seasonality handled
- sample size adequate
- no causal language without evidence
- likely misreadings listed

For weather posts, it should reject vague claims like “Bangalore gets most rain at 4pm” if the metric is actually “probability of measurable rain by hour”.

### E. `weather-blog-system`

Purpose: domain-specific skill for `weather.karthiks.co`.

Should know:

- where weather data lives
- schema / column meanings
- source caveats
- usual seasonal definitions
- house chart style
- blogpost structure
- publish pipeline
- how to create computed facts before prose

This is the strongest way to make the demo feel real and yours.

### F. `computed-facts-to-post`

Purpose: let LLM write only after facts exist.

Rules:

- use only supplied computed facts
- do not invent causes
- lead with strongest supported claim
- include caveat visibly
- separate finding from speculation
- keep title claim-specific

This can combine with `karthik-writing-style`.

### G. `chart-critique-skill`

Some of this exists in `karthik-data-visualization`, but workshop needs a participant-facing review skill.

It should ask:

- what is the chart claiming?
- what is the evidence?
- what is the denominator?
- what is the comparison?
- what is easiest to misread?
- what would I change first?

This is also the skill participants can adapt using WhatsApp critique comments.

## Recommended build order

1. `karthik-analysis-planner`
2. `karthik-hypothesis-generator`
3. `karthik-evidence-builder`
4. `karthik-claim-validator`
5. `weather-blog-system`
6. `computed-facts-to-post`
7. `chart-critique-skill`

Do not start with writing/chart skills. Existing skills already cover that reasonably well.

## How the 4pm workflow should run

```text
User question
→ analysis planner creates estimand + denominator + comparison
→ evidence builder profiles data
→ hypothesis generator creates testable candidate stories
→ evidence builder computes facts
→ claim validator ranks supported claims
→ dataviz selector chooses chart form
→ karthik-data-visualization styles chart
→ chart-critique-skill reviews chart
→ computed-facts-to-post writes draft
→ human reviews/publishes
```

## One-line workshop message

The agent is not “smart” because it knows weather.

It is useful because it is forced to think in Karthik's analytical sequence:

```text
question → denominator → comparison → evidence → claim → chart → caveat → prose
```
