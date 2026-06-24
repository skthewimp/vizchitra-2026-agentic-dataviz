# Learnings from the workshop designer's LLM-first lecture/workshop format

**Purpose:** Extract practical lessons from the workshop designer's public talk/workshop materials and adapt them for the VizChitra 2026 Agentic DataViz workshop.

Sources inspected:

- the workshop designer's project index: `public project index`
- Talks repo/listing: `public talks repository`
- `LLM Data Visualization` talk: `public LLM dataviz talk deck`
- `Prompt to Plot` VizChitra 2025 workshop: `public prompt-to-plot workshop deck`
- Marpessa theme: `public Marp theme page`
- Slidegen/Slideforge repo: `public slide-generation repository`

## 1. His decks are not conventional slide decks

the workshop designer's decks are closer to **live workshop control surfaces** than presentation slides.

They contain:

- setup instructions;
- links and QR codes;
- live prompts;
- tool lists;
- screenshots/outputs;
- transcript notes embedded in the markdown;
- activity logs after the fact.

For our workshop, the deck should not be a polished keynote. It should be the thing that keeps the room moving.

Implication:

- Use slides as navigation and copy-paste surfaces.
- Each exercise slide should answer: what to do, where to paste, what output to expect, when to stop.

## 2. Marp markdown is a good format

the workshop designer's recent talks use Marp markdown. The `LLM Data Visualization` deck frontmatter shows:

- `marp: true`
- title/author/url metadata;
- `theme: marpessa`;
- pagination;
- build command using Marp CLI.

This is useful because:

- Markdown is LLM-editable.
- Slides are version-controllable.
- HTML output is easy to publish.
- Speaker notes/transcripts can live alongside slides.
- QR codes and links are easy.

Recommendation for our workshop:

- Build `slides.md` in Marp.
- Use a clean theme, possibly Marpessa or a derivative with the facilitator dataviz styling.
- Export HTML and PDF/PPT only as needed.
- Keep source markdown as the canonical deck.

## 3. Every slide should do one of four jobs

From the workshop designer's workshop decks, slides usually do one of these:

1. **Orient** - where are we, what are we doing?
2. **Prompt** - copy-paste this into an LLM.
3. **Demonstrate** - here is what happened when the LLM did it.
4. **Debrief** - what did we learn from the output?

For our workshop, avoid conceptual-only slides unless they set up an activity.

Good slide archetypes:

- Bad chart → what is wrong?
- Good chart → what rules can we extract?
- Prompt block → extract visual taste.
- Prompt block → find stories, do not chart yet.
- Output screenshot → critique.
- Revised chart → what improved?
- Reusable skill/instruction block.

## 4. Prompts belong inside the slides

`Prompt to Plot` embeds full prompts for:

- finding datasets;
- ideating data stories;
- analyzing/visualizing;
- writing a meta-prompt for code;
- improving a visual into a fuller story.

This is a big practical lesson. Participants should not hunt for prompts in a separate document while watching slides.

Recommendation:

- Put the active prompt on the slide.
- Keep it short enough to be readable, but complete enough to copy.
- Also publish a companion prompt page/repo for copying.
- Use QR code to open the slide/prompt page.

For this workshop, core prompt slides:

1. extract taste from good/bad examples;
2. profile dataset and find stories;
3. generate visual brief;
4. create first chart;
5. critique rendered chart;
6. compress workflow into reusable skill/instruction.

## 5. The deck can model the thing being taught

the workshop designer often explicitly says the deck/workshop itself was made using LLMs. This is powerful because the artifact demonstrates the method.

For us:

- The slide deck should itself be LLM-generated/LLM-edited from markdown.
- The deck can include one slide: “This deck was built the way we will build charts today: context → draft → critique → revise.”
- Show the prompt/skill used to make the deck if useful.

This makes the workshop more credible and meta-consistent.

## 6. Use multiple models/agents in parallel

In `LLM Data Visualization`, the workshop designer's core move is: don't wait on one model/path; run multiple prompts/models in parallel. In `Prompt to Plot`, he used Jules and Codex in parallel, then moved to Claude Code when useful.

Workshop lesson:

- LLM work is sampling.
- Parallelism gives more candidate ideas and reduces dead time.
- The teacher should show options, not one sacred tool.

For our workshop:

- Participants can use ChatGPT/Claude/Gemini/Cursor/Codex.
- We can suggest: ask one model for stories, another for chart critique.
- If time permits: compare two generated chart directions and pick the better one.

Caveat:

- Do not overcomplicate for a 3-hour workshop. Parallelism should be optional, not required.

## 7. De-risk the data problem

the workshop designer de-risks by both searching for datasets and generating synthetic ones. He asks models to create classroom-sized datasets with enough richness and reproducibility.

For our BYO-data workshop:

- Ask participants to bring data, but keep a synthetic fallback dataset ready.
- The fallback should be “designed for teaching”: small, varied, with obvious and subtle stories.
- The fallback should have precomputed bad/good chart examples.

This prevents the room from getting stuck on broken CSVs or privacy concerns.

## 8. Make live failure part of the pedagogy

the workshop designer's format embraces live uncertainty: model outputs, errors, workarounds, asking the model to explain itself, debugging in public.

For us:

- Show a bad first chart deliberately.
- Treat bad output as material.
- Ask: what did the model optimise for? What did it miss? Which instruction was absent?
- Then fix using taste rules and critique loop.

This is better than pretending the LLM creates perfect charts.

## 9. Ask models to explain their own outputs

In `LLM Data Visualization`, the workshop designer asks models to explain unfamiliar charts and interpret their generated visualisations.

For our workshop:

After chart generation, ask:

- What does this chart claim?
- What data supports the claim?
- What might be misleading?
- What visual choices did you make and why?
- What would classic dataviz craft object to?
- What would the facilitator's dataviz skill object to?

This converts LLM output into reviewable reasoning.

## 10. Build activities as first-class artifacts

the workshop designer's talk folders include `activities.md`, summarising what happened in the session.

For our workshop, this suggests:

- Before workshop: define intended activities.
- After workshop: capture actual activities, participant outputs, failures, and good prompts.
- This becomes reusable teaching material and public follow-up.

We do not need participants to read documentation. But LLMs and future prep will benefit from a session activity log.

## 11. QR codes and public URLs matter

the workshop designer's slides commonly include QR codes to the public deck/repo. This helps in a room: participants can open slides/prompts without typing URLs.

For our workshop:

- Publish one workshop page/repo.
- QR code on title slide and exercise slides.
- The page should include:
  - slides;
  - prompts;
  - fallback dataset;
  - public dataviz skill link;
  - examples;
  - post-workshop outputs if appropriate.

## 12. Use transcript/speaker notes, but keep them hidden

The `LLM Data Visualization` deck has transcript content embedded but hidden with CSS. This is useful because the deck can serve both live presentation and post-event archive.

For us:

- Add brief speaker notes under slides in Markdown.
- Hide them in presentation view if needed.
- After event, notes can become a public recap or facilitator guide.

## 13. the workshop designer's format is high-agency, not hand-holding

The audience is expected to use tools, make choices, debug, and publish. The facilitator is not solving every participant's problem.

For our workshop:

- Let participants choose their LLM/tool.
- Give them a workflow, not a single guaranteed path.
- Use fallback data only when needed.
- Encourage quick iterations over perfect outputs.

## 14. Adaptation for our workshop deck

Recommended deck shape: 18-22 Marp slides.

### Section 1 - Frame the problem

1. Title + QR to workshop page.
2. What you will leave with: reusable AI dataviz workflow.
3. Default LLM chart slop: show bad chart.
4. Good chart = truthful + readable + purposeful + repeatable.

### Section 2 - Teach taste

5. Bring out your admired chart and disliked chart.
6. Prompt: extract visual taste from examples.
7. classic dataviz craft principles as agent rules.
8. the facilitator dataviz skill: house style and anti-patterns.

### Section 3 - Story before chart

9. Do not make a chart yet.
10. Prompt: profile data and propose candidate stories.
11. Choose one story: claim, evidence, comparison.

### Section 4 - Generate and critique

12. Prompt: generate first chart from visual brief.
13. First output will be flawed. Good.
14. Prompt: critique rendered chart.
15. Before/after example.

### Section 5 - Reuse

16. Convert conversation into reusable instruction/skill.
17. Optional: run second pass / compare another model.
18. Show-and-tell instructions.
19. Close: chart is one output; taste system is asset.
20. Links/resources.

## 15. Slide style recommendations

Borrow from the workshop designer, but adapt to the facilitator/classic dataviz craft style:

- Use Markdown-first slides.
- Big headings, few bullets.
- Lots of prompt blocks and screenshots.
- Use QR codes.
- Keep live links visible.
- Avoid decorative theme clutter.
- Use white background, charcoal text.
- Use accent colour sparingly.
- Make prompts copyable from public HTML.
- Keep deck useful after the workshop.

## 16. What not to copy blindly

the workshop designer's sessions often thrive on chaotic live exploration. That works because he is comfortable performing the tool chaos.

For this workshop, reduce chaos because:

- BYO datasets already add uncertainty;
- visual taste discussion needs reflection;
- 3 hours can disappear into setup/debugging.

So copy:

- LLM-first production;
- prompt slides;
- QR/public repo;
- live failure as pedagogy;
- parallel model optionality;
- activity log.

Do not over-copy:

- too many tools;
- publishing to GitHub as required outcome;
- open-ended “let's see what happens” for every step.

## 17. Practical next step

Build a Marp `slides.md` with:

- 20 slides max;
- 6 copy-paste prompts;
- one bad/good chart demo;
- one fallback dataset link;
- QR code to workshop repo/page;
- speaker notes hidden in HTML.

The deck should be usable as both:

1. live facilitator spine;
2. participant prompt sheet;
3. public archive after VizChitra.
