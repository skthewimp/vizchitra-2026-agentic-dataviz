# Learnings from a public workshop designer's Workshop Format

Purpose: extract reusable patterns from a public workshop designer's public talks/workshops and adapt them for the VizChitra Agentic DataViz workshop.

Main sources scanned:

- a public workshop designer GitHub profile: public workshop-designer profile
- Talks repo: public talks repository
- Prompt to Plot: public talks repository/tree/main/2025-06-28-prompt-to-plot
- Data Design by Dialogue: public talks repository/tree/main/2025-06-27-data-design-by-dialogue
- LLM Data Visualization: public talks repository/tree/main/2025-10-29-llm-data-visualization
- Vibe Analysis: public talks repository/tree/main/2025-10-16-vibe-analysis
- Vibe Coding: public talks repository/tree/main/2025-10-23-vibe-coding
- AI Coding Guide: public talks repository/tree/main/2025-08-21-ai-coding-guide
- Applied Vibe Coding: public talks repository/tree/main/2025-11-15-applied-vibe-coding
- Tools in Data Science course repo: public tools-in-data-science repository

## 1. the workshop designer's workshop formula

the workshop designer's popular workshops are not lecture-first. They are **public, live, messy, artifact-producing sessions**.

Common pattern:

1. Give participants a live URL / QR code.
2. Set up minimal tools.
3. Use a shared sheet/chat for coordination.
4. Start with participant-relevant tasks or data.
5. Use LLMs live, including failures.
6. Work in parallel across tools/models.
7. Publish or save outputs before the session ends.
8. Capture activities/transcript/artifacts afterwards.

The appeal is high-agency: participants feel they are making something real, not watching a polished demo.

## 2. Slides are an operating system, not a lecture deck

His decks are usually Marp markdown with:

- public URL;
- QR code on title / many slides;
- direct tool links;
- copy-paste prompts;
- transcript or speaker notes hidden in HTML;
- build command in frontmatter;
- links to generated outputs.

Implication for our workshop:

- Build `slides.md` as a working control surface.
- Every activity slide should answer: what to paste, where to paste, what output to expect, when to stop.
- Keep slides few, but make each slide operational.
- Put prompt blocks inside deck, not only in participant kit.

## 3. Public artifacts create urgency and pride

In Prompt to Plot and vibe-coding sessions, participants are pushed toward public repos, GitHub Pages links, shared sheets, and visible outputs.

This changes energy:

- people make concrete choices;
- outputs become shareable;
- peer examples create momentum;
- the room can see progress.

Adaptation:

For our workshop, public publishing may be optional, but we need visible artifacts:

- shared sheet with participant name, dataset, chart goal, status, final rule, output link/screenshot;
- optional GitHub repo / folder;
- final show-and-tell of before/after chart or visual brief;
- post-workshop gallery if participants consent.

## 4. Use shared sheet/chat as room control

Repeated pattern:

- participants put GitHub profiles, setup status, tasks, blockers, links in a sheet;
- chat is used for questions and peer help;
- facilitator triages visible blockers without derailing whole room.

Adaptation:

Create a simple sheet with columns:

- name;
- tool used;
- dataset topic;
- chart question;
- good visual example;
- bad visual example;
- current stage: taste/context/story/brief/chart/review;
- blocker;
- output link/screenshot;
- one reusable rule learned.

This lets us run a 20-person BYO-data workshop without losing the room.

## 5. Start from participant tasks, not generic demos

the workshop designer often crowdsources tasks/data first, then chooses live demos from the room. This makes the workshop feel relevant.

Adaptation:

Ask participants to add their chart need to the sheet early:

> What graph are you trying to make? Who is it for? What is the decision/story?

Then pick 2-3 participant cases for live mini-critiques.

Fallback demo still exists, but should not dominate unless BYO data fails.

## 6. De-risk with fallback and synthetic data

the workshop designer often searches for real datasets and generates synthetic classroom data in parallel. This prevents data availability from killing the session.

Adaptation:

Prepare:

- one clean fallback dataset;
- one deliberately messy fallback dataset;
- one bad default chart;
- one improved chart;
- good/bad visual examples;
- a second data snapshot for rerun/reproducibility.

Use synthetic data when:

- participant data is sensitive;
- upload fails;
- data has no useful story;
- code environment breaks.

## 7. Work in parallel to reduce dead time

Strong recurring lesson: do not wait on one agent/model/path.

the workshop designer uses:

- ChatGPT for voice ideation;
- Claude/ChatGPT/Gemini for alternate answers;
- Jules/Codex/Claude Code in parallel;
- one model for generation, another for review.

Adaptation:

For our workshop:

- ask one model for story candidates;
- ask another to critique the proposed visual brief;
- ask a coding agent/tool to render;
- ask a second model to review the rendered chart.

Keep optional, not required. Main line:

> Parallelism gives more samples and keeps momentum.

## 8. Live failure is part of pedagogy

the workshop designer's sessions openly include broken uploads, bad cluster names, failed code, context drift, environment issues, and restarts.

This works because failure is reframed as method:

- ask the model to fix error messages;
- rerun when output is poor;
- start fresh when context rots;
- split planning from execution;
- switch tools when stuck.

Adaptation:

Our workshop should deliberately show:

- default AI chart slop;
- polished but analytically weak chart;
- unsupported claim;
- chart improved after review loop.

Teaching line:

> The first output is material for critique, not the answer.

## 9. Outcome-first, code-secondary

the workshop designer's vibe-analysis/coding frame: ignore the code first; judge whether the useful outcome exists. Then extract reusable scripts/specs after success.

Adaptation:

For our audience, do not make local Python/R debugging central.

Allow multiple output paths:

- image generated by chatbot;
- Python/R code;
- Datawrapper/Flourish instructions;
- spreadsheet chart;
- SVG/HTML.

Judge the process artifact:

- claim;
- comparison;
- visual brief;
- critique;
- reusable rules.

Not just final chart polish.

## 10. Separate planning from execution

In Vibe Analysis, the workshop designer explicitly separates:

1. What interesting/useful analyses can we run?
2. Now execute selected analyses.

Planning + execution in one prompt creates shallow plans.

Adaptation:

This maps perfectly to our workshop:

1. context pack;
2. story candidates;
3. visual brief;
4. chart generation;
5. review.

Hard rule:

> Do not make a chart yet.

This should be repeated and visible on slides.

## 11. Prompts/specs are the product

Recurring the workshop designer line: specs/tests are the product; code is a build artifact. Prompts should be committed, reused, and improved.

Adaptation:

Our equivalent:

> Visual constitution is the product. Chart is a build artifact.

Participants should leave with:

- `context.md`;
- `taste.md`;
- `story_finding_prompt.md`;
- `visual_brief.md`;
- `review_checklist.md`;
- `next_run.md`.

This aligns with participant feedback wanting modular skills.

## 12. Make the repo/folder LLM-friendly

the workshop designer recommends `AGENTS.md`, small files, examples, fast tests, standing instructions, and reusable skills.

Adaptation:

Workshop kit should have simple folder structure:

```text
my-dataviz-agent/
  data/
  examples/
    good-chart.png
    bad-chart.png
  context.md
  taste.md
  story-candidates.md
  visual-brief.md
  chart-review.md
  next-run.md
  outputs/
```

Optional `AGENTS.md`:

```text
Before making charts, read context.md and taste.md.
Do not chart before producing story candidates and a visual brief.
Prefer static presentation visuals.
Critique rendered output before finalizing.
```

## 13. Skills/standing instructions are central

the workshop designer's newer workshops explicitly teach `AGENTS.md` and skills to steer agent behaviour across tasks/folders.

Adaptation:

Frame our workshop as building a **skill stack**:

1. context skill;
2. taste skill;
3. story-before-chart skill;
4. visual-brief skill;
5. chart-generation skill;
6. review/deslop skill;
7. next-run/reproducibility skill.

Participants should understand not only how to use the chain, but how to modify one part.

## 14. Use voice prompting for live ideation

the workshop designer uses voice because it is faster, richer, and keeps flow playful.

Adaptation:

Suggest voice for:

- describing good/bad chart preferences;
- explaining dataset context;
- brainstorming story candidates;
- narrating critique of first chart.

This matters because chart judgement is easier to say than to type.

## 15. Playfulness lowers fear

Vibe Analysis explicitly uses playful experiments, odd ideas, and failure as learning. This reduces pressure and encourages participants to try.

Adaptation:

Our workshop should avoid sounding like a design exam.

Use questions like:

- “What does this chart want you to believe?”
- “Where is the chart lying with a straight face?”
- “What is the fiddly edit you always make?”
- “What would make this feel like your graph?”

## 16. Review beats generation

the workshop designer repeatedly says AI shifts effort from coding to verification. His AI Coding Guide emphasises validation loops, tests, evals, and review.

Adaptation:

For dataviz:

- review the claim;
- review data support;
- review visual hierarchy;
- review misleading risk;
- review taste-rule violations;
- review caveats and source notes.

Teaching line:

> AI makes drawing cheaper. That makes review more important, not less.

## 17. Restart when context rots

the workshop designer advises starting fresh when long threads accumulate mistakes. Summarize and reseed new runs.

Adaptation:

Add a participant tactic:

If chart generation gets messy after 2 failed revisions:

1. ask model to summarize current context, chosen story, taste rules, and chart brief;
2. start a new chat/tool run;
3. paste only clean summary + data + brief;
4. regenerate.

This is especially useful for chart polish loops.

## 18. Extract reusable scripts after success

In vibe-coding/analysis, after a good run, the workshop designer asks for self-contained scripts and commits prompts.

Adaptation:

After a good chart:

- ask for a reusable chart-generation prompt;
- ask for reusable code if applicable;
- save style constants/theme;
- save next-run requirements;
- capture before/after and critique notes as examples.

## 19. Use multiple reviewers

Vibe Analysis recommends independent reviewers/models to catch numerical/statistical errors.

Adaptation:

For charts, ask separate reviews:

1. data analyst review: is claim supported?
2. dataviz review: is visual form appropriate?
3. audience review: does takeaway land in 10 seconds?
4. adversarial review: how could this mislead?

Can be done by different models or peers.

## 20. Publish logs/activities for compounding learning

the workshop designer's talks repo often includes:

- `README.md` slide deck;
- `activities.md` summary;
- `transcript.md`;
- generated artifacts;
- prompts;
- screenshots/sketchnotes.

This makes each workshop reusable and discoverable.

Adaptation:

After VizChitra, create:

- `activities.md` — what participants actually did;
- `participant-output-gallery.md` — links/screenshots with permission;
- `prompt-improvements.md` — what failed and what changed;
- `facilitator-retro.md` — timing, blockers, next version.

## 21. the workshop designer-style structure for our 3-hour workshop

Recommended structure using the workshop designer patterns:

### 0:00-0:10 - Live URL, sheet, promise

- QR to slides/kit.
- Fill shared sheet.
- Promise: “AI gets you to a graph. Today we build system to get to your graph.”

### 0:10-0:25 - Show failure fast

- Default AI chart.
- Polished but wrong chart.
- Quick critique.

### 0:25-0:45 - Participant taste extraction

- Good/bad visuals.
- Prompt extracts rules.
- Sheet captures one personal rule.

### 0:45-1:05 - Context and chart need

- Dataset, audience, question.
- Do not chart yet.

### 1:05-1:25 - Story candidates

- LLM proposes 5 candidate claims.
- Rank by evidence/importance/visual clarity/risk.

### 1:25-1:35 - Break / blocker triage

- Use sheet to identify stuck participants.

### 1:35-1:55 - Visual brief

- Convert chosen story into chart spec.
- Peer/model critique of brief.

### 1:55-2:25 - Generate chart

- Use any tool.
- Static presentation visual preferred.
- Parallel option: one model generates, another critiques.

### 2:25-2:45 - Review and revise

- Checklist.
- One revision.
- If stuck: restart with clean summary.

### 2:45-2:55 - Extract skill/instructions

- Save personal/team chart agent instructions.
- Modify one skill/rule.

### 2:55-3:00 - Show-and-tell

- 3-4 people share one before/after or one reusable rule.

## 22. Practical changes to our current plan

Add these to our workshop assets:

1. Shared progress sheet.
2. QR on every exercise slide.
3. Prompt blocks inside slides.
4. Optional GitHub/folder structure.
5. `AGENTS.md` / skill-stack example.
6. Live “restart when context rots” tactic.
7. One slide: “Visual constitution is the product. Chart is a build artifact.”
8. Post-workshop `activities.md` habit.
9. Parallel reviewer prompt.
10. Fallback synthetic dataset with baked-in stories.

## 23. Key lines to reuse

- AI gets you to “a graph”. The system gets you to “my graph”.
- Visual constitution is the product. Chart is a build artifact.
- Do not chart yet.
- Parallelism gives more samples and keeps momentum.
- The first output is material for critique, not the answer.
- AI makes drawing cheaper. That makes review more important, not less.
- You are not learning one prompt. You are learning chart-agent architecture.
- If context rots, restart with a clean brief.
