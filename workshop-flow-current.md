# Workshop Flow - Current Working Version

**Purpose of this file:** older implementation flow. The current single source of truth is `workshop-overall-framework.md`, which frames the workshop as hands-on, interactive, and participant-dataset-led.

## Workshop premise

Participants should not leave with one nice AI-generated chart. They should leave with a repeatable way to teach an LLM their visual taste, make it find a defensible story, generate a chart, critique the rendered output, and improve it.

The working teaching line:

> You do not teach an LLM dataviz by saying “make it beautiful”. You teach it by showing what you reward, what you punish, and how you review.

## What participants should bring

### Required

1. **A dataset**
   - CSV/Excel preferred.
   - Should be something they understand.
   - Should have one possible communication use, not just random exploration.

2. **One chart they admire**
   - Could be from FT, NYT, classic dataviz craft, Datawrapper, Observable, a public report, or their own work.
   - Used to teach positive taste: “do more like this”.

3. **One chart they dislike**
   - Could be default Excel/matplotlib, a bad dashboard, a misleading chart, or their own old chart.
   - Used to teach negative taste: “never do this”.

4. **One concrete chart need**
   - Example: “I need to show this trend to my boss”, “I need a chart for a blog post”, “I need to explain this metric in a client deck”.
   - This prevents vague “explore my data” behaviour.

5. **Audience/use-case description**
   - Who is this chart for?
   - What should the reader understand or decide?

6. **LLM/tool access**
   - ChatGPT, Claude, Gemini, Cursor, Codex, or similar.
   - Ideally ability to upload files or run generated code locally.

### Optional

- Existing brand/style constraints.
- Existing chart code.
- A company/publication style guide.
- A prior chart they want to improve.

## Why positive and negative chart examples matter

LLMs respond better when taste is defined by contrast:

- “Do more like this.”
- “Never do this.”

Negative examples are especially useful because default LLM charts have predictable failure modes:

- default matplotlib colours;
- yellow/white unreadable palettes;
- legends that force eye ping-pong;
- rainbow palettes;
- unnecessary gridlines;
- titles that name the chart type instead of the insight;
- no comparison baseline;
- misleading axes;
- spaghetti charts;
- chart type chosen before question;
- too much annotation;
- polished visuals with weak evidence.

The workshop should turn these into a participant-specific visual constitution.

## Current content direction

The current overall framework now lives in `workshop-overall-framework.md`. Use that as the source of truth for the hands-on, interactive workshop design. `workshop-content-focus.md` remains useful for teaching substance.
