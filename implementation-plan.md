# VizChitra 2026 Workshop Implementation Plan

**Workshop:** Agentic DataViz: Build Systems, Not Charts  
**Date/time:** 2026-07-03, 14:30-17:30  
**Goal now:** build the actual 3-hour workshop: demos, participant kit, public skills, and run-of-show.

## Core implementation objective

Participants should leave with a working mini-system for repeatably producing better LLM-assisted charts — and a way to explain/adapt it as a production workflow for teams:

1. data goes in;
2. context/taste rules guide the agent;
3. agent tests whether meaningful insight exists, including null/no-insight possibility;
4. agent finds candidate stories before drawing;
5. agent generates chart code only when a chart is warranted;
6. rendered chart is critiqued against classic dataviz craft/the facilitator principles and overclaim risk;
7. revised chart is saved with reproducible prompts and review notes;
8. workflow can be reused as a team SOP: style guide, request brief, generation step, QA gate, escalation rules.

## What we are not doing

- Not changing title/public positioning.
- Not making a generic “AI makes charts” talk.
- Not doing only live vibe-coding.
- Not relying on one lucky prompt.
- Not making the workshop Claude-specific.

## Build tracks

### Track A - Facilitator deck

Need 25-35 slides, light and concept-led. Structure:

1. Opening: default LLM chart slop problem.
2. Why this happens: model optimises for plausible chart code, not visual judgement.
3. classic dataviz craft principles as machine-readable constraints.
4. the facilitator dataviz skill as reusable taste layer.
5. Demo 1: ugly default chart → deslop loop.
6. Demo 2: evidence-before-story using market/economic or weather data, including “no insight” / overclaim check.
7. Participant build-along.
8. Review and reproducibility.
9. Close: skill pack + next-run workflow + team production lens + enterprise tool mapping.

### Track B - Participant kit

Files to prepare:

- `participant-kit/README.md`
- `participant-kit/context.md`
- `participant-kit/taste.md`
- `participant-kit/story_finding_prompt.md`
- `participant-kit/visual_brief_template.md`
- `participant-kit/chart_review_checklist.md`
- `participant-kit/next_run.md`
- `participant-kit/enterprise_dashboard_mapping.md`

### Track C - Public skills

Publishable skills to prepare:

1. `dataviz-style-rules` - existing public skill.
2. `story-before-chart` - force story candidates before visual generation.
3. `classic-dataviz-review` - review against classic dataviz craft-ish principles.
4. `matplotlib-deslopper` - fix default Python chart aesthetics.
5. `visual-brief-generator` - turn data story into structured chart brief.

### Track D - Demos

Need at least two robust demos:

1. **Default slop demo**
   - input: simple CSV.
   - first prompt: “make chart”.
   - expected bad output: default matplotlib, legend, ugly colours, weak labels.
   - then apply skill/review loop.

2. **Evidence-before-story demo**
   - input: weather, market, or economic dataset.
   - show: facts are not enough; model must test evidence strength, alternative explanations, and whether any chart is warranted.

Optional third:

3. **Babbage metric monitoring demo**
   - synthetic metric time series.
   - output: candidate stories, selected brief, chart.

## Build order

1. Finalise run-of-show.
2. Build participant kit templates.
3. Build demo datasets and expected outputs.
4. Draft skill specs.
5. Create facilitator deck outline.
6. Dry run once end-to-end.
7. Package public repo/zip.

## Open decisions

- Python-first, R-first, or both? Recommended: Python-first for participants, R examples for your own weather case.
- Bring-your-own-data or fixed dataset? Recommended: fixed fallback dataset, optional BYO only after core exercise.
- Live internet needed? Recommended: no. Use local files and any LLM UI/API participants already have.


### Track E - Literature/evidence spine

Use `facilitator/literature-survey-synthesis.md` to add 3-4 evidence-backed slides:

1. Architecture, not prompting trick.
2. Separate transformation from visualization.
3. First chart is a draft: plausible-but-wrong risk.
4. Reproducibility is structural: persistent context, specs, endpoints, review logs.

Before public slides, verify exact citations and avoid overloading the workshop with academic references.
