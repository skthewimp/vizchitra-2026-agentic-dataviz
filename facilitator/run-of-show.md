# 3-Hour Run-of-Show

Design note: concept-led, tool-agnostic. Hands-on files are optional follow-along, not mandatory live debugging.

## 0:00-0:10 - Setup and promise

- Show ugly default LLM chart.
- State working promise: we will build a repeatable, tool-agnostic chart-making system, not one lucky chart.
- Use FAQ line: one good chart is easy; making it work again tomorrow, for new data or another teammate, is hard.
- Files participants will produce: context, taste, story candidates, visual brief, chart, review checklist, next-run note.

## 0:10-0:25 - Why default LLM charts are bad

Explain failure modes:

- matplotlib defaults;
- unreadable yellow/white palettes;
- legends instead of direct labels;
- too many gridlines;
- weak titles;
- no comparison baseline;
- chart type chosen before story;
- visually plausible but analytically unsupported claim.

## 0:25-0:45 - classic dataviz craft principles as agent instructions

Translate principles into agent constraints:

- maximise data-ink;
- remove chartjunk;
- direct-label instead of legends;
- make comparison explicit;
- keep graphical integrity;
- use words/numbers near evidence;
- let complexity come from data, not decoration.

Show how these become `taste.md` and review checklist.

## 0:45-1:10 - Demo 1: deslop a chart

Flow:

1. Ask LLM for chart from CSV.
2. Show bad chart.
3. Add the facilitator/classic dataviz craft taste rules.
4. Regenerate.
5. Render and critique.
6. Revise labels, colour, hierarchy.

Teaching point: visual skill must be explicit and reusable.

## 1:10-1:30 - Participant exercise 1: create context + taste

Participants choose one path. Follow-along participants fill:

- `context.md`
- `taste.md`

Concept-path participants instead sketch how these map to their team style guide, data dictionary, Tableau/Power BI dashboard process, or enterprise AI tool.

They choose fixed dataset or own dataset.

## 1:30-1:40 - Break

## 1:40-2:05 - Story before chart

Demo:

1. profile data;
2. propose candidate stories;
3. rank by confidence, importance, visual suitability;
4. choose one;
5. create visual brief.

Teaching point: chart choice follows claim/evidence.

## 2:05-2:35 - Participant exercise 2: generate visual brief + chart

Participants run:

- `story_finding_prompt.md`
- `visual_brief_template.md`
- chart-generation prompt using `taste.md`

Output: first chart, chart spec, or dashboard implementation brief.

## 2:35-2:55 - Critique loop

Participants review rendered chart:

- Is claim supported?
- Compared to what?
- Any default slop?
- Are labels direct?
- Is colour doing semantic work?
- Would it survive a 10-second glance?

Revise once.

## 2:55-3:00 - Package and close

Participants save:

- final chart;
- prompts;
- review notes;
- next-run instructions.

Close line: a good chart agent is a reusable taste + context + review system.
