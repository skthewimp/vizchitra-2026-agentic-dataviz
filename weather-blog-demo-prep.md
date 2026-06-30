# Weather blog demo prep

Goal: show workshop participants how posts at `weather.karthiks.co` are produced, as an example of agentic dataviz: stable data pipeline + human question + computed facts + LLM-assisted writing + reviewed chart/story.

## Demo thesis

Do not present this as “AI writes weather posts”.

Present it as:

```text
question → data → computed signals → candidate claims → chart → LLM phrasing → human review → published post
```

The important point: R does the analysis. The LLM mostly helps choose/phrase from facts already computed.

## 1. Pick one blogpost to reverse-engineer live

Best candidates:

- `Bangalore rain has a 4pm habit`
- `Pre-monsoon rain is an evening creature`
- `Bangalore is dry. That does not make early May a monsoon oracle.`

Pick one that has:

- simple human question
- clear denominator
- one strong chart
- one analytical trap
- easy before/after narrative

Recommended first demo: **4pm rain habit**.

Why:

- memorable question
- simple hourly aggregation
- clear monsoon vs non-monsoon comparison
- shows why denominator matters
- can make a bad AI chart first, then better chart

## 2. Create the “before AI” question

Need a plain-English question that starts the workflow.

Example:

```text
Does Bangalore rain at particular hours of the day, or is that just something we remember because evening rain is annoying?
```

Then sharpen it:

```text
How does the probability of rain vary by hour of day, and is the 4pm pattern stronger during monsoon months?
```

## 3. Prepare data explanation

Need one simple slide / note explaining the data.

Include:

- hourly Bangalore weather data from 1981 onward
- fields used: timestamp, rain, temperature, maybe month/season/hour
- caveat: Bangalore rain is local; exact mm should be treated cautiously
- unit of analysis: one hour
- denominator: number of observed hours in each hour-of-day × season bucket

## 4. Prepare the bad first chart

Generate an intentionally naive chart from the prompt:

```text
Using this Bangalore hourly weather data, make a chart showing when it rains most often.
```

Likely bad outputs to preserve:

- total rainfall by hour, without denominator
- average mm by hour, distorted by outliers
- no monsoon/non-monsoon split
- title says “rainfall pattern” but claim is vague
- no caveat on local rain

Save this as workshop material.

## 5. Prepare computed-facts table

Before asking LLM to write anything, compute a small table like:

```text
season | hour | observed_hours | rainy_hours | rainy_share | total_rain_mm
monsoon | 16 | ... | ... | 0.55 | ...
non_monsoon | 16 | ... | ... | 0.21 | ...
```

Also compute:

- top rainy hours by season
- 4pm rank in monsoon
- 4pm rank outside monsoon
- afternoon vs morning contrast
- caveats / missingness

This is the key proof that analysis precedes prose.

## 6. Prepare candidate claims

Make 4-5 possible claims from the computed facts.

Example:

1. Bangalore has a late-afternoon rain clock.
2. The 4pm pattern exists all year but is much stronger in monsoon.
3. Pre-monsoon rain is more evening-skewed than monsoon rain.
4. Morning rain is rare compared to afternoon rain.
5. The average rainfall amount is less useful than rain probability for this question.

Rank them live or show how the agent ranks them.

## 7. Prepare visual brief

For the chosen claim, prepare a visual brief:

```text
Main claim: Bangalore rain has a 4pm habit, especially in monsoon.
Audience: general Bangalore readers.
Data: hourly rainfall, 1981-present.
Metric: share of hours with measurable rain.
Comparison: monsoon vs non-monsoon by hour of day.
Chart form: line chart or grouped hourly profile.
Annotation: mark 4pm; label monsoon and non-monsoon values.
Caveat: local rainfall; public station rain is noisy; read broad pattern, not exact mm.
Acceptance: reader should see the afternoon bump in <5 seconds.
```

## 8. Prepare final chart and post excerpt

Need final artefacts:

- final chart image
- post title
- subtitle / dek
- 2-3 paragraph post excerpt
- source/caveat note

Also prepare the “what changed from first chart” explanation.

## 9. Prepare LLM role demo

Show two prompts:

### Bad prompt

```text
Write a blogpost about Bangalore rainfall patterns from this data.
```

### Better prompt

```text
You are not doing analysis. Use only the computed facts below.
Write a short weather blogpost for Bangalore readers.
Lead with the strongest claim. Mention the caveat. Do not invent causes.
```

This demonstrates controlled generation.

## 10. Prepare review checklist

Before publishing, check:

- Is the claim supported by computed facts?
- Is the denominator explicit?
- Is the comparison fair?
- Is the chart readable in 5 seconds?
- Is the title a claim, not a description?
- Are caveats visible?
- Did the LLM invent any causal story?
- Can this run again on new data?

## 11. Package as reusable system

End the demo with files/artifacts:

```text
question.md
weather_data_profile.md
computed_facts.csv
candidate_claims.md
visual_brief.md
chart.png
post_draft.md
review_checklist.md
publish_notes.md
```

This maps directly to the workshop message: build systems, not one-off charts.

## 12. Things to build now

Immediate next tasks:

1. Clone / inspect the `bangalore-weather` repo locally.
2. Pick exact blogpost for live demo.
3. Extract or recreate the data slice behind that post.
4. Script the computed-facts table.
5. Generate bad first chart.
6. Generate final/revised chart.
7. Write the facilitator notes.
8. Add 4-6 demo slides into the deck.
