# Public Skill Pack Plan

Purpose: share workshop-ready skills participants can install/reuse.

## 1. dataviz-style-rules

Status: existing public skill.
Use as base visual style and review guide.

## 2. story-before-chart

Trigger: user asks to visualise data or make chart.
Behavior:

- refuse to chart immediately unless story/claim is obvious;
- profile data first;
- propose candidate stories;
- rank by evidence, importance, visual clarity;
- ask/generate visual brief before chart code.

## 3. classic-dataviz-review

Trigger: user asks to review/improve chart.
Behavior:

- apply data-ink, chartjunk, integrity, comparison, label proximity;
- produce concise critique;
- suggest concrete edits;
- if code available, patch code.

## 4. matplotlib-deslopper

Trigger: Python/matplotlib chart looks default/ugly.
Behavior:

- remove top/right spines;
- set white background;
- use charcoal text;
- remove legend where direct labels possible;
- replace default colours;
- simplify grids;
- improve title/subtitle/caption;
- save static PNG/SVG.

## 5. visual-brief-generator

Trigger: data story selected, before chart generation.
Behavior:

- output structured brief;
- separate claim, evidence, encodings, annotations, caveats;
- include refusal conditions.

## Packaging

Each skill should include:

- `SKILL.md`
- one before/after example
- one compact checklist
- optional code template for Python/R
