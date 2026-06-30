# Work needed before updating the workshop slides

This is the prep work to do before rewriting `slides/agentic-dataviz-workshop.md` around the new structure.

## 1. Build the end-to-end demo

Need one small but rigorous demo that shows the full agentic dataviz workflow.

Candidate: Bangalore weather / rain timing example.

Demo should include:

- raw data source
- precise question
- data profile
- candidate hypotheses
- validation steps
- chosen claim
- visual brief
- first chart
- critique
- revised chart
- reusable rules saved at the end

Important: avoid YOLO analysis. The demo needs clear denominators, time period, aggregation logic, caveats, and source notes.

## 2. Prepare fallback datasets

Need at least two simple datasets for participants who do not bring their own.

Each dataset should have:

- CSV file
- 3 possible questions
- one obvious trap
- one decent narrative chart possibility
- one misleading chart possibility

Good fallback data properties:

- small enough to understand fast
- real enough to be interesting
- messy enough to require judgment
- no private/sensitive data

## 3. Prepare seeded good/bad charts

Need charts to start the WhatsApp critique even if participants are quiet.

Prepare:

- 2 good charts
- 2 bad charts
- 1 visually attractive but analytically weak chart
- 1 ugly but useful chart

For each chart, write private facilitator notes:

- what works
- what fails
- likely participant reactions
- what principle it illustrates

## 4. Create a reusable chart critique skill

Need one prompt/skill that can review charts consistently.

It should check:

- question-data-visual alignment
- claim support
- denominator / aggregation
- missing context
- misleading encodings
- accessibility
- title / labels / annotations
- caveats
- dashboard extension if relevant

Also create a shorter participant-friendly version they can adapt.

## 5. Design the human vs LLM critique exercise

Need clear flow:

1. participant posts first AI chart
2. peers critique in WhatsApp / StreamAlive
3. LLM critiques same chart
4. compare differences
5. extract reusable rules

Need decide:

- how many charts to review live
- how to select charts
- whether people work alone or pairs
- where captured rules are saved

## 6. Write participant prep email

Email should ask participants to bring:

- laptop + charger
- LLM/coding tool access
- one dataset, preferably CSV
- one question they want to answer with the data
- one good visualisation example
- one bad visualisation example

Also say fallback datasets will be available, so nobody is stuck.

## 7. Confirm workshop logistics

Check:

- projector
- HDMI / USB-C connector
- reliable internet
- Zoom or Meet availability
- StreamAlive works with chosen platform
- WhatsApp projection works
- power sockets
- whether a helper/TA is available

## 8. Decide dashboard / BI handling

Keep this lightweight.

Prepare one slide / note on how the same critique system extends to dashboards:

- consistent colours
- metric definitions
- filter clarity
- reading path
- each view has a job
- cross-chart consistency
- human review before production

Do not get dragged into Tableau-specific implementation unless asked.

## 9. Create final artefact template

Participants should leave with a reusable mini-system, not just a chart.

Template folder/files:

```text
context.md
data_profile.md
story_candidates.md
visual_brief.md
chart_review.md
taste_rules.md
next_run.md
```

Need decide whether this is shown as files, a prompt bundle, or a single markdown worksheet.

## 10. Only then rewrite the deck

Once above artefacts exist, update slides to follow this arc:

1. show end-to-end system
2. run bad first chart
3. critique with humans + LLM
4. convert critique to rules
5. build story/evidence/brief
6. generate/revise chart
7. package reusable workflow
