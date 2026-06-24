# Proposal Flow vs Current Working Flow

## Summary

The accepted proposal and the current working flow are aligned on the big idea: the workshop is about repeatable AI-assisted dataviz systems, not one-off charts.

The current working flow is more participant-centred and practical. It adds a stronger “teach the LLM visual taste” layer using positive/negative chart examples and explicit classic dataviz craft/the facilitator-style critique loops.

## What remains the same

### 1. Repeatable system, not one chart

Proposal:

- Build systems, not charts.
- Find the story, teach the agent, run it again.
- Participants leave with reusable workflow assets.

Current flow:

- Participants produce a reusable instruction/skill block.
- Final chart matters less than reusable taste + story + review loop.

Status: **strongly aligned**.

### 2. The chart comes late

Proposal:

- Purpose → data checks → context → story-finding → chart generation → critique → reproducibility.

Current flow:

- Taste/context → story candidates → chosen claim → first chart → critique → reusable system.

Status: **aligned**. Current version makes “do not chart yet” more explicit.

### 3. Human judgement stays in loop

Proposal:

- LLMs scaffold process but do not remove judgement.
- Review and reproducibility are central.

Current flow:

- Rendered chart must be critiqued.
- Participants compare visual output against principles and examples.

Status: **aligned**.

## What changes or gets sharpened

### 1. Stronger focus on visual taste

Proposal version:

- Mentions visual taste/context layer.
- Includes visual critique.

Current flow:

- Makes taste capture a full workshop phase.
- Participants bring admired and disliked charts.
- Positive and negative examples become the agent’s “visual constitution”.

Implication:

This is a useful sharpening. It directly addresses the practical problem: default LLM charts look bad.

### 2. More explicit classic dataviz craft/the facilitator principles

Proposal version:

- General emphasis on good-looking/reproducible visualisations.
- Existing the facilitator dataviz style is implicit in background.

Current flow:

- classic dataviz craft-style rules become operational constraints:
  - maximise data-ink;
  - remove chartjunk;
  - direct labels over legends;
  - comparison baseline;
  - graphical integrity;
  - words/numbers near evidence.

Implication:

This should be added to actual teaching content. It is the bridge from “AI workflow” to “good visual output”.

### 3. BYO dataset becomes primary

Proposal version:

- Could use fallback dataset or participant dataset.
- Participant setup not fully settled.

Current flow:

- Participants bring their own dataset, chart need, audience, admired chart, disliked chart.
- Fallback dataset remains safety net.

Implication:

This makes the workshop more useful but increases risk. Need robust fallback material and tool buffer.

### 4. Positive/negative examples become core input

Proposal version:

- Mentions examples/work samples.

Current flow:

- Every participant brings one positive and one negative visual example.
- These are used to define taste by contrast.

Implication:

This is probably the biggest practical improvement over proposal. It makes “teach the agent taste” concrete.

### 5. Less formal production/reproducibility, more hands-on skill creation

Proposal version:

- Strong production-grade language: data checks, reproducibility, review loops, run-again workflow.

Current flow:

- Still includes reproducibility, but in a lighter form: reusable instruction block/skill.
- Less emphasis on production data pipelines and more on personal/team visual agent setup.

Implication:

For a 3-hour BYO laptop workshop, current version is likely better. But keep enough reproducibility language to satisfy accepted programme promise.

## Risks in current flow

### 1. BYO datasets can be messy

Risk:

- Participants bring unsuitable data: too large, too private, too malformed, no clear story.

Mitigation:

- Ask for CSV/Excel under reasonable size.
- Ask for one concrete chart need.
- Provide fallback CSV.
- Use first half to narrow to one story, not solve entire dataset.

### 2. Tool fragmentation

Risk:

- Different participants use Claude, ChatGPT, Gemini, Cursor, R, Python, Excel.

Mitigation:

- Workshop teaches workflow, not one tool.
- Prompt skeletons should be tool-neutral.
- Fallback examples can be Python/R, but participant output can vary.

### 3. Too much time spent on code execution

Risk:

- People debug Python environments instead of learning visual thinking.

Mitigation:

- Allow LLM-generated chart image directly if tool supports it.
- Recommend Google Colab / browser tools.
- Have static fallback outputs.
- Do not require perfect local setup.

### 4. Taste discussion can become subjective and vague

Risk:

- “I like this” / “I hate this” without transferable rules.

Mitigation:

- Force extraction into rules:
  - label placement;
  - colour usage;
  - comparison baseline;
  - clutter;
  - title/subtitle;
  - chart type;
  - evidence/claim relationship.

## Recommended merged workshop flow

Keep proposal’s backbone but implement current flow:

1. **Opening problem:** default LLM chart slop.
2. **Taste capture:** admired/disliked visuals → rules.
3. **Context and audience:** what is this chart for?
4. **Story before chart:** candidate stories and evidence.
5. **Generate:** first chart with explicit taste rules.
6. **Critique:** classic dataviz craft/the facilitator review loop.
7. **Reuse:** convert into skill/instruction block.
8. **Show-and-tell:** before/after and strongest rule.

## Bottom line

The proposal promised: repeatable AI-assisted dataviz systems.

The current working flow delivers that promise through a concrete participant experience:

> Bring your data, bring one good chart, bring one bad chart, and teach the LLM enough taste and judgement to produce a better chart than default slop - then save the process so it can run again.
