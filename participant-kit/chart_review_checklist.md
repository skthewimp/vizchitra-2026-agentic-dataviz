# Chart Review Checklist

## Analytical review

- What is the claim?
- Is the claim supported by the data shown?
- Compared to what?
- Are units, time period, denominator clear?
- Any missing caveat that changes interpretation?
- Any causal language without causal evidence?

## Visual review

- Does chart look like default matplotlib/Excel slop?
- Is background clean?
- Are colours legible and purposeful?
- Are series directly labelled where possible?
- Can gridlines/spines/ticks be removed?
- Are labels readable at final size?
- Any overlap?
- Does title say the takeaway, not the chart type?

## classic dataviz craft review

- Is useful data-ink high?
- Is chartjunk removed?
- Is comparison easy?
- Is visual effect proportional to data effect?
- Are words/numbers close to evidence?

## Revision instruction

Ask the LLM:

```text
Critique the rendered chart using this checklist. Then revise the code. Preserve the analytical claim, but improve visual clarity, hierarchy, labels, colour, and graphical integrity.
```
