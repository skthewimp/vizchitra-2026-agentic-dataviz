# Learnings from a data-visualization critic for Evaluating Good Visualisations

Purpose: distil a data-visualization critic / Junk Charts-style thinking into a practical framework for the workshop **Creating good visualisations consistently with LLMs**.

Source orientation: a data-visualization critic's *Junk Charts* writing is useful less as a fixed rulebook and more as a diagnostic habit: every chart should be judged by whether its **question**, **data**, and **visual form** work together. This is often described as the chart-making/checking trifecta.

## 1. A chart is not good because it looks good

A polished chart can still be bad if it answers no useful question, uses the wrong data, or hides the comparison the reader needs.

Workshop implication:

> Do not ask an LLM only to make a chart prettier. Ask it what question the chart answers, whether the data supports that question, and whether the visual form reveals the answer.

## 2. The core trifecta: Question, Data, Visual

A good visualisation aligns three things:

1. **Question** — what is the chart trying to answer?
2. **Data** — what evidence is available, and is it appropriate?
3. **Visual** — what form best reveals the answer?

If one corner is weak, the whole chart is weak.

Examples:

- Clear visual, wrong question: attractive but irrelevant.
- Clear question, wrong data: persuasive but unsupported.
- Good data, wrong visual form: true but hard to see.

## 3. Start with the question, not the chart type

A common failure is beginning with “make a bar chart” or “make this look nicer.” the critic-style critique starts earlier:

- What should the reader learn?
- What decision or understanding should this support?
- What comparison matters?
- What would count as evidence?

Better LLM prompt:

> Before making a chart, identify the main question this data can answer. Suggest candidate claims, the evidence needed for each, and the chart form that would best reveal the comparison.

## 4. Titles should expose the intended claim

A weak title names the topic. A stronger title states the finding or question.

Weak:

> Sales by region

Better:

> West and South drove most of the post-2022 sales growth

For review, ask:

- Is the title just a label?
- Does it tell the reader what to look for?
- Does the chart actually support the title?

## 5. Data choice is part of chart design

Chart critique is not only about colors, fonts, or axes. It includes whether the right metric was chosen.

Check:

- absolute count vs rate;
- total vs per-capita;
- nominal vs inflation-adjusted;
- cumulative vs period change;
- average vs distribution;
- current value vs change from baseline;
- cherry-picked time period vs full relevant window.

LLM review instruction:

> Identify whether a different denominator, transformation, baseline, or comparison group would better answer the stated question.

## 6. Comparison is the heart of explanation

A chart should make comparison easy. If the reader has to work hard to compare, the visual form is failing.

Ask:

- Compared to what?
- Compared to when?
- Compared to whom?
- Compared on what scale?
- Is the comparison encoded by position/length, or by something harder to decode?

Workshop line:

> A chart without a comparison is usually a picture of numbers, not an explanation.

## 7. Visual form should match analytical task

Choose chart form based on the job:

- trend over time → line chart;
- ranking → sorted bar/dot plot;
- relationship → scatterplot;
- distribution → histogram/box/violin/ridgeline;
- composition → stacked/area only if part-to-whole is truly the task;
- many categories → small multiples or table-plus-sparklines;
- before/after or current/range → slope/range plot.

Review question:

> What visual operation must the reader perform, and is this chart making that operation easy?

## 8. Remove decoration that competes with evidence

The issue is not minimalism for its own sake. The issue is whether non-data elements make the message harder to see or easier to misunderstand.

Check:

- 3D effects;
- shadows and gradients;
- heavy gridlines;
- unnecessary icons;
- loud backgrounds;
- legends that force eye-ping-pong;
- too many colors without meaning.

LLM review instruction:

> List every visual element that does not carry data, context, label, or useful emphasis. Recommend removals.

## 9. But context and annotation are not chartjunk

Useful annotation is not decoration. Labels, notes, baselines, benchmarks, and caveats can make a chart more honest.

Good additions:

- source;
- timeframe;
- denominator;
- definition note;
- benchmark line;
- event marker;
- caveat about missing data;
- direct labels near important marks.

Key distinction:

> Remove ornament, not explanation.

## 10. Self-sufficiency matters

A strong chart should not rely entirely on surrounding prose. The reader should be able to understand the basic claim from the chart, title, labels, and notes.

Self-sufficiency checks:

- If the chart is separated from the article/deck, does it still make sense?
- Are units and timeframe visible?
- Are labels clear?
- Is the main comparison visible without narration?
- Does the title/subtitle orient the reader?

## 11. Honesty beats drama

Charts can mislead by exaggerating or hiding effects.

Check:

- truncated axes;
- inconsistent intervals;
- dual axes;
- selective start/end dates;
- area/volume used for linear quantities;
- missing uncertainty;
- percentages without base counts;
- rankings without meaningful differences.

LLM review instruction:

> Identify every way this chart could mislead a reasonable reader, even if the underlying data is correct.

## 12. A good critique produces a better alternative

the critic-style critique is constructive. The point is not to dunk on a bad chart but to diagnose why it fails and propose a stronger version.

For every critique, produce:

1. what the chart appears to claim;
2. what is hard or misleading;
3. what data/metric would better fit;
4. what visual form would better reveal it;
5. what title/annotation would make it clearer.

## 13. LLM-era extension: make charts reviewable

With LLMs, the new failure mode is plausible polish without evidence. So the trifecta needs a fourth operating layer: **reviewability**.

For every AI-generated chart, require:

- inferred question;
- stated claim;
- data fields used;
- calculation/transformation;
- chart choice rationale;
- caveats;
- verification checklist;
- claim-to-evidence table.

Workshop line:

> The AI chart is not finished when it renders. It is finished when its claim can be checked.

## 14. Practical review rubric

Score each 0–2.

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| Question | unclear topic | implied question | clear useful question |
| Data | wrong/unknown | partly suitable | directly supports claim |
| Visual form | obscures/misleads | understandable with effort | makes comparison obvious |
| Integrity | likely distortion | minor caveats | honest scales/context |
| Clarity | cluttered/confusing | readable | fast and self-sufficient |
| Reviewability | unverifiable | partly checkable | evidence trail is explicit |

Verdict:

- **10–12:** strong; polish and verify.
- **7–9:** promising; revise.
- **4–6:** weak; rethink question/data/form.
- **0–3:** rebuild; do not publish.

## 15. Prompt pattern for an LLM visualisation reviewer

```md
Act as a data visualisation editor using a data-visualization critic's Question-Data-Visual trifecta.

Review this chart for whether it is good, not merely attractive.

Inputs:
- Chart/image/code/spec:
- Intended question, if known:
- Intended claim, if known:
- Audience:
- Dataset/source/fields, if known:
- Metric definitions/time period, if known:

Return:
1. Inferred question.
2. Inferred claim.
3. Question review.
4. Data review.
5. Visual-form review.
6. Integrity risks.
7. Self-sufficiency check.
8. Claim-evidence-caveat table.
9. 3 concrete fixes.
10. Better chart recommendation, if needed.

Be explicit about what you cannot judge without more context.
Do not invent data validity.
```

## 16. What this means for the workshop

The workshop should teach participants to build a system with two agents:

1. **Chart maker** — generates chart drafts from context, data, question, and style rules.
2. **Chart reviewer** — checks the draft against the trifecta before publication.

The reviewer is not optional. It is what makes LLM-generated visualisation reliable.

Final framing:

> Creating good visualisations consistently with LLMs means turning taste and judgment into a repeatable review system: Question, Data, Visual, Integrity, Clarity, Reviewability.
