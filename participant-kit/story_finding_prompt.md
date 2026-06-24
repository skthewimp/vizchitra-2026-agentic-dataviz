# Story-Finding Prompt

Use before asking for a chart.

```text
You are helping me find visual stories in a dataset.

Read the context pack and inspect the data. Do not make a chart yet.

Return:
1. Data profile: rows, columns, units, time range, missingness, obvious caveats.
2. 5 candidate stories, each with:
   - claim
   - evidence needed
   - chart type likely to work
   - comparison baseline
   - confidence: high/medium/low
   - risk of misleading reader
3. Rank candidates by:
   - importance
   - evidence strength
   - visual clarity
4. Recommend one story to visualise first.
5. Say what not to visualise yet because evidence is weak.
```
