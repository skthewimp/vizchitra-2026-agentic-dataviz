# Skill build TODO

Use this to start new sessions quickly.

## Source doc

Read first:

- `workshop-skill-gap-analysis.md`

## Build order

1. `karthik-analysis-planner` ✅
2. `karthik-hypothesis-generator`
3. `karthik-evidence-builder`
4. `karthik-claim-validator`
5. `weather-blog-system`
6. `computed-facts-to-post`
7. `chart-critique-skill`

## New session prompt

```text
We are building skills for the VizChitra 2026 agentic dataviz workshop.
Read `workshop-skill-gap-analysis.md` and `skill-build-todo.md`.
Build the next unchecked skill from the TODO list as a Codex skill.
Use the existing skill style in `/Users/Karthik/.codex/skills`.
Keep the skill practical and test it on the 4pm Bangalore rain question.
```

## Skill checklist

### 1. `karthik-analysis-planner`

Status: DONE — built at `/Users/Karthik/.codex/skills/karthik-analysis-planner/` and validated on 2026-06-30

Purpose: turn natural-language question into analysis contract.

Must output:

- operational definition
- unit of analysis
- denominator
- comparison
- metric
- caveats
- falsification condition

Test question:

```text
Does Bangalore rain around 4pm?
```

### 2. `karthik-hypothesis-generator`

Status: TODO

Purpose: generate testable candidate stories from question + data profile.

Must output for each hypothesis:

- claim
- metric
- denominator
- comparison
- test / calculation
- likely chart
- possible confound
- what would falsify this

### 3. `karthik-evidence-builder`

Status: TODO

Purpose: force analysis from data, not priors.

Must output:

- data profile
- row grain
- missingness
- computed facts table
- sanity checks
- candidate claims

### 4. `karthik-claim-validator`

Status: TODO

Purpose: decide which claims survive evidence.

Must check:

- claim/metric match
- denominator explicit
- comparison fair
- sample size adequate
- seasonality handled
- no unsupported causal language
- likely misreadings

### 5. `weather-blog-system`

Status: TODO

Purpose: domain-specific workflow for `weather.karthiks.co`.

Must cover:

- data location/schema
- source caveats
- seasonal definitions
- chart style
- post structure
- publish pipeline
- computed facts before prose

### 6. `computed-facts-to-post`

Status: TODO

Purpose: write blogpost draft only from supplied computed facts.

Must enforce:

- no invented causes
- no unsupported claims
- strongest supported claim leads
- caveat visible
- title is specific claim, not vague topic

### 7. `chart-critique-skill`

Status: TODO

Purpose: participant-facing chart review skill.

Must ask:

- what is the chart claiming?
- what is the evidence?
- what is the denominator?
- what is the comparison?
- what is easiest to misread?
- what would you change first?

## Definition of done for each skill

Each skill should have:

- folder in `/Users/Karthik/.codex/skills/<skill-name>/`
- `SKILL.md`
- clear trigger description
- workflow
- output template
- 4pm Bangalore rain mini-example
- no dependency on model pretraining for factual claims

## After each skill

1. Test briefly on 4pm rain question.
2. Update this TODO status.
3. Commit and push.
