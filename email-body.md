# Paste-Ready Email Body

**Status:** historical submission copy, updated to match the accepted public title/subtitle.


Hi,

Thanks, this framing makes sense to me. I agree that the more useful workshop is not "how to make a pretty AI-generated chart once", but how to build a repeatable AI-assisted dataviz workflow that can survive contact with new data, changing stories, and human review.

The workshop will use my Babbage experience as the starting point: what worked about automatically monitoring metrics and surfacing stories, what failed when we expected the system to infer too much context cold, and what has changed now with stronger LLMs, coding agents, reusable skills, and better context workflows. The broader craft lesson is that visualisation still follows a hypothesis-driven data process: question, data, iteration, communication.

For the programme page

Title
Agentic DataViz: Build Systems, Not Charts

Subtitle
Find the Story. Teach the Agent. Run It Again.

Short description
It is now easy to ask an LLM to make a good-looking chart once. The harder problem is getting it to find the right hypotheses / story, use the right data, match your taste, and do it again tomorrow without everything becoming a fresh act of faith. This hands-on workshop teaches a practical workflow for building repeatable AI-assisted dataviz systems: purpose, data checks, context packs, story-finding prompts, visual critique, and review loops. Participants will leave with a small reusable system they can adapt for their own datasets and teams.

Long description
LLMs can now produce surprisingly good charts, dashboards, and data stories. The awkward bit is that most of this work still has a demo problem: it works once, on one dataset, with one lucky prompt. The moment the data changes, the story changes, or another person has to run it, the whole thing becomes fragile.

A useful correction is to remember that visualisation follows the same basic process as data science. You start with a question or hypothesis. You inspect whether the data can actually answer it. You iterate when the first answer is not quite right. The chart comes at the end, as the communication layer. AI does not remove this process. If anything, it makes the process more important, because the first generated chart can look plausible even when the underlying story is weak.

This workshop is about turning that old craft process into a repeatable AI-assisted workflow. We will define the job, inspect the data, create a context pack, ask the model to find candidate stories before charting, generate a visual, critique it, and add simple reproducibility checks. The examples draw on my work at Babbage Insight, where we tried to monitor business metrics and surface stories automatically, and on my more recent AI-generated weather visualisations and narrative posts.

Participants will not just watch a tool produce a chart. They will leave with a small reusable system: input data, context, story-finding prompt, visual-generation prompt, generated output, review checklist, and next-run instructions.

About You
the facilitator is a data and AI practitioner based in Bangalore. He spent five years as SVP at Delhivery building the data and analytics function, and more recently founded Babbage Insight, an AI analytics startup focused on proactive business insights from data. He now works independently with companies on AI-for-data adoption, analytics workflows, and turning AI tools from demos into trusted working systems. He writes about data, analytics, and AI on The Art of Data Science, has written a column for Mint, is the author of Between the Buyer and the Seller, and studied at IIT Madras and IIM Bangalore.

For editorial review

What is the overall objective of the workshop?

The objective is to teach participants how to build repeatable AI-assisted dataviz workflows, not one-off AI-generated charts.

The central idea is simple: the chart is the last step. A good AI dataviz system needs to know the purpose, inspect the data, understand the intended story, respect visual taste, and only then draw. The workshop turns that into a practical workflow participants can reuse.

By the end of the workshop, participants should understand how to turn a vague "make a visualisation" prompt into a structured production workflow; give an LLM enough context to match a desired analytical, narrative, and visual style; make the agent identify candidate stories before it starts drawing; separate exploration, generation, review, and production; preserve reproducibility through files, prompts, examples, and acceptance criteria; and know where human judgement must remain in the loop.

The practical output is a small but complete starter system: a dataset, a context pack, a story-finding prompt, a visual-generation prompt, a review checklist, and a reproducible output.

What is the session-wise agenda?

0:00-0:15 - The Chart Is The Last Step
Quick framing: the difference between a generated chart and a repeatable system. Visualisation as a hypothesis-driven data-science process: question, data, iteration, communication. Babbage story: trying to monitor metrics and surface stories automatically, and learning that the system cannot infer all context cold. What has changed since: stronger LLMs, coding agents, reusable skills, and easier end-to-end generation. What has not changed: purpose, data quality, taste, trust, and review.

0:15-0:35 - The Workflow We Will Build
Introduce the repeatable workflow participants will build: purpose and audience; input data; data checks and caveats; domain and metric context; visual taste and narrative preferences; story-finding step; chart-generation step; critique and revision step; reproducibility and review checklist. The core distinction: the agent should first understand what changed, why it matters, whether the data supports the claim, and what kind of visual story is appropriate.

0:35-1:05 - Purpose And Context Pack
Hands-on exercise: create a small context file for the dataset and audience; define what the output is trying to make the reader see; add metric definitions and caveats; add visual preferences; add anti-patterns; add one or two work samples or style references. Output: every participant has a first context pack that encodes purpose, data meaning, and taste.

1:05-1:25 - Find The Story Before Drawing
Hands-on exercise: ask the LLM to profile the data; identify movements, outliers, inflection points, segment differences, missing context, and possible derived concepts; force it to propose multiple story candidates; ask it to rank them by importance, confidence, and visual suitability; choose one story candidate and write down why it is worth visualising. Output: a short story-candidate memo, with caveats.

1:25-1:35 - Break

1:35-2:05 - Generate, Critique, Revise
Hands-on exercise: generate a chart or small visual story from the chosen candidate; ask the LLM to critique the output against the context pack; revise for clarity, annotation, hierarchy, colour, and narrative restraint; inspect the generated code/spec enough to know what changed. Output: first visual output plus one revision.

2:05-2:35 - Review The Visual Like An Analyst
Hands-on exercise: review the visual through six questions: purpose, hypothesis, data support, tool choice, visual hierarchy, annotation; test whether the reader can get the first-order takeaway in 5-10 seconds; check whether the data supports the claim; identify what the AI guessed, what it knew, and what a human still has to decide; revise the context pack based on the failure modes. Output: a reviewed visual and an improved context/review checklist.

2:35-2:55 - Make It Reproducible
Hands-on exercise and discussion: save the prompt/context structure; define required input columns and expected output; run the same workflow again on a modified or second dataset; compare whether the agent's choices remain consistent. Then zoom out to what changes when this has to run daily, weekly, or for many users; what should be automated and what should stay human-reviewed; how to create an event library; how to maintain a visual-style corpus; how to evaluate hallucinated narratives; and when a dashboard, notebook, static chart, or narrative post is the right output. Output: a reusable mini-workflow that can be rerun.

2:55-3:00 - Wrap
Participants write down one workflow they can apply this to, one context artifact they need to create, and one risk they must guard against.

What are the key takeaways for participants?

- A practical workflow for moving from "LLM, make me a chart" to a repeatable AI-assisted dataviz system.
- A context-pack template that captures purpose, audience, data caveats, visual taste, narrative rules, and examples.
- A story-finding prompt pattern that makes the agent inspect the data before it draws anything.
- A review checklist built around purpose, data quality, tool choice, visual hierarchy, annotation, and narrative fit.
- A simple reproducibility pattern: version the data, context, prompt, output, and acceptance criteria.
- A clearer sense of what LLMs are good at, what still fails, and where human judgement remains non-negotiable.

What are the prerequisites to attend?

Participants should be comfortable working with data in at least one familiar form: spreadsheets, notebooks, BI tools, Datawrapper/Flourish, R/Python, JavaScript, or similar. They do not need to be expert programmers.

They should have some prior experience making or reviewing charts. The workshop is most useful for people who already care about visual clarity and want to use AI without giving up judgement.

Basic familiarity with ChatGPT, Claude, Gemini, Cursor, Codex, or another LLM/coding assistant will help, but the workflow will be explained from first principles.

What prior preparation and setup is needed by participants?

Before the workshop, participants should bring a laptop; access to at least one LLM tool they can use during the session, such as Claude, ChatGPT, Gemini, Cursor, Codex, or equivalent; a small dataset they care about, preferably CSV or spreadsheet format; and 2-3 examples of visualisations they like, or one previous chart/report they have made.

For participants who do not bring data, a fallback dataset will be provided. The workshop can be run with browser-based tools, so deep local setup should not be required.

Room requirements: projector, stable internet, power points for participants, whiteboard or wall space for workflow mapping, and ideally tables that allow participants to work individually or in pairs.

Who is the audience for this workshop?

This is for people who sit between data, design, storytelling, and tools: data journalists, dataviz designers, analytics and BI practitioners, product/data analysts, researchers who communicate with data, civic-tech and public-data practitioners, designers experimenting with AI coding tools, and data leaders trying to make narrative reporting more repeatable.

The ideal participant has made enough charts to know that taste matters, and has used enough AI to know that a plausible answer is not the same as a good one.

Why are you the right person to teach it?

I have worked on this problem from both sides: as a data practitioner trying to communicate messy business data, and as a founder trying to make AI systems do some of that work repeatedly.

At Delhivery, I built and led a data function inside a high-volume operational business, where dashboards, metrics, and investigations had to support real decisions. At Babbage Insight, I tried to build an AI system that could monitor metrics, find interesting movements, and communicate them proactively. That experience exposed the hard parts: data context, metric meaning, user trust, narrative judgement, and the cold-start problem that makes AI-for-data systems look good in demos but weak in production.

Since Babbage, I have continued working on AI-for-data workflows as a consultant and builder. My recent experiments include AI-generated narrative weather visualisations, reusable LLM skills, agentic analysis workflows, and practical systems for getting ChatGPT, Claude, and Codex to produce outputs that match a specific analytical and aesthetic standard.

This workshop is not a generic AI-tools session. It comes from trying to make these systems useful when they have to run repeatedly, explain themselves, and meet a practitioner's taste bar.

Cheers,
the facilitator

