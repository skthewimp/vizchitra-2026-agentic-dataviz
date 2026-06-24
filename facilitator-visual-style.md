# My Philosophy on Data Visualisation

**the facilitator**  
*Expert in stirring the pile of data • Author • Columnist*

This document distils my thinking and writing on data visualisation, drawn from years of tweets, observations, and practice. It captures the consistent principles that run through my work — from foundational critiques to my current focus on agentic approaches with LLMs.

---

## Core Belief: Clarity and Intentionality Above All

Data visualisation is not decoration or a technical exercise. It is communication. Every element must earn its place by making the underlying data **clearer and more meaningful** to the viewer.

I am consistently critical of anything that introduces unnecessary friction or ambiguity:
- Charts whose type is unclear (line vs area, with confusing shading).
- Missing or poorly labelled axes.
- Default colours or visual choices that do not serve meaning.
- Visuals that look impressive but fail basic interpretability tests.

**Example from my posts**:  
“How is one even supposed to interpret this? Is this a line chart or an area chart? If it’s an area chart, it makes absolutely no sense. If it’s a line chart, I have no clue why it’s been shaded! And like a good CEO post, the Y axis is conveniently not labelled.”

Even as tools become more powerful (including LLMs), the standard remains the same: the visualisation must stand on its own without requiring the creator to explain what it means.

---

## Design Choices Must Be Deliberate

Colour, shading, layout, and encoding are not neutral. They carry meaning (or create confusion).

- Colours should reflect real categories or data properties, not arbitrary defaults or aesthetic preferences.
- In the age of LLMs, there is still no excuse for poor colour choices (e.g., using slightly different shades of blue for different countries without justification).
- Automated or “smart” systems often fail here because they lack contextual understanding of what the colours *should* represent.

Good visualisation respects the data and the audience. It does not force the viewer to do extra mental work.

---

## Historical and Philosophical Context Matters

Modern dashboards and many visualisation conventions did not emerge in a vacuum. Understanding their origins helps us use them appropriately rather than over-hyping them.

- The dashboard as we know it has roots in attempts at central planning (notably in mid-20th century contexts). It was designed to present consistent, static overviews — not to magically deliver “actionable insights” on demand.
- Many contemporary claims about dashboards over-promise. They were never primarily tools for dynamic decision-making in the way they are often sold today.

This perspective keeps expectations realistic and prevents us from treating visualisation tools as silver bullets.

---

## Data Literacy and Fundamentals Remain Essential

Visualisation sits on top of solid data thinking. Weak foundations lead to flawed visuals and misleading conclusions.

Key areas I repeatedly highlight:
- Dimensional analysis and unit consistency (e.g., avoiding nonsensical comparisons such as market capitalisation versus GDP).
- Statistical thinking and understanding of uncertainty or error rates.
- Proper use of analytical tools (e.g., the power of pivot tables in Excel versus limited alternatives in some cloud spreadsheets).

People often reach for advanced visualisation tools before mastering these basics. The result is attractive but misleading output.

---

## Narrative and Storytelling Elevate Visualisation

Beyond accurate representation, the best visualisations tell a story or surface insights in a memorable way.

- Sankey diagrams and other flow visualisations can be powerful when used thoughtfully (they were underrated outside specialist circles before becoming trendy).
- Real-world, organic examples of data visualisation (such as patterns formed by wear on a tennis court over decades) demonstrate how visualisation can reveal evolution and behaviour without deliberate charting.
- The goal is often **narrative visualisation** — charts that communicate a point of view or insight, not just display numbers.

---

## Tools Are Means, Not Ends

I have practical experience across several environments and remain pragmatic:

- Strong familiarity with **ggplot2** in R and the challenges of producing clean, maintainable code.
- Interest in conversions to interactive formats (e.g., Plotly) and BI platforms such as Tableau.
- Preference for tools that support serious analytical work rather than convenience alone.

The tool should serve the clarity and narrative goals — not dictate them through limitations or flashy defaults.

---

## The Evolution: From Critique to Agentic Systems

My thinking has evolved while remaining consistent in its foundations.

**Earlier phase** (roughly up to ~2024): Strong emphasis on identifying and correcting common failures in traditional and automated visualisation. Focus on clarity, avoiding pitfalls, and respecting data fundamentals.

**Current phase** (2025–2026 onward): Active exploration and teaching of **agentic data visualisation** using LLMs. 

Key shifts in my view:
- LLMs can now generate surprisingly good individual charts and narratives.
- The real challenge is moving beyond fragile, one-off “demo” visualisations to **repeatable, robust systems**.
- Agentic approaches involve workflows that include data inspection, context building, story discovery, generation, critique, and reproducibility checks.
- Important nuance: Distinguish between systems that merely *do* things (agentic) and those that *think* before acting (proactive). Many current AI agents are closer to automated workflows than true proactive systems.
- LLMs have clear limitations — for example, they struggle to surface true “unknown unknowns” without strong human-guided context and iteration.
- There remains value in real data, real feedback loops, and human oversight. Pure simulation or one-prompt magic is rarely sufficient for production use.

This evolution does not abandon earlier principles. On the contrary, the agentic approach is a way to **scale and systematise** clarity, intentionality, narrative quality, and robustness — using modern tools while preserving the standards I have always advocated.

---

## Summary of My Philosophy

1. **Clarity first** — Ambiguity is the enemy.
2. **Intentional design** — Every visual choice must justify itself.
3. **Respect for fundamentals** — Data literacy and context are non-negotiable.
4. **Purpose and narrative** — Visualisation should communicate insight, not just display data.
5. **Realistic expectations** — Understand the history and limitations of tools and methods.
6. **Systems thinking in the AI era** — Move from impressive one-offs to repeatable, critiqueable, reproducible workflows powered by LLMs.

My work on agentic data visualisation is the natural extension of these principles into the current technological landscape. The goal remains the same: help people see and communicate truth in data more effectively.

---

*This philosophy is drawn directly from patterns across my tweets and writing over the years. It continues to evolve as tools and practices change, but the core commitment to clarity, intentionality, and meaningful communication remains constant.*
