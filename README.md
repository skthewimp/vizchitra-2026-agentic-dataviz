# VizChitra 2026 - Agentic Dataviz Workshop

## Current workshop framework

Use `workshop-overall-framework.md` as the current source of truth. It frames the workshop as hands-on and interactive: participants bring laptops, datasets, chart examples, and a real chart need; the session alternates short demos, work blocks, peer critique, and revision loops.


**Status:** accepted; public programme page live  
**Date prepared:** 2026-06-08  
**Conference:** VizChitra 2026, Bangalore  
**Format:** 3-hour invited workshop, likely 20 participants  
**Public title:** Agentic DataViz: Build Systems, Not Charts  

## Public Programme Page

- URL: https://vizchitra.com/2026/sessions/agentic-dataviz
- Public title: **Agentic DataViz: Build Systems, Not Charts**
- Public subtitle: **Find the Story. Teach the Agent. Run It Again.**
- Date/time: **2026-07-03, 14:30-17:30**
- Venue: **Underline Center**
- Public speaker line: **the facilitator, Fractional Data & AI Consultant**
- Internal hook retained: **The chart is the last step.**

## Core Thesis

It is now easy to get an LLM to produce a good-looking chart once. The harder and more valuable problem is making the process repeatable: purpose, data checks, story finding, context, visual taste, critique, and reproducibility.

The workshop should be positioned around this sentence:

> The chart is the last step.

The useful craft frame is that visualisation follows the same hypothesis-driven process as data science: start with a question, inspect whether the data can support it, iterate, and then communicate the result. LLMs make this process easier to scaffold, but they do not remove the need for it.


## FAQ / Positioning Answers

### I already use Claude/ChatGPT/Gemini to vibe-code charts and dashboards. What do I learn in this workshop?

Making one chart with a good prompt is getting easier by the day. Making it work again tomorrow, for new data, with a different question, or by someone else on your team is the hard part.

Right now, most of us rely on a mix of prompting, cajoling, and hope. This workshop is about moving beyond that: building repeatable workflows that reliably find hypotheses, check data, generate visuals, and critique the results.

### Is this about building autonomous AI agents for dataviz?

Not really. Think of getting a new car in Bengaluru. Buying the car is easy. Driving it well through Bengaluru traffic is the real skill. Similarly, an agent is a system; agentic describes how that system behaves.

This workshop is not about building autonomous agents. It is about designing workflows where LLMs can do the analytical and visual heavy lifting — finding hypotheses, checking data, generating charts, and critiquing their own output — while you stay in control of the questions, judgement, and story.

### Is this just another AI demo?

No. This workshop is about what happens after the demo.

The facilitator has built systems like this in production at Babbage Insight, where they surfaced business stories automatically from live metrics. They know what breaks, what holds, and what it takes to go from a clever prompt to something a team can actually trust.

## Files

- `proposal-and-prep.md` - canonical working document. Includes source notes, programme-page copy, editorial answers, recommended email response, prep backlog, literature map, and participant-handout sketch.
- ``email-body.md` - paste-ready body for the organiser reply.
- `assets/` - placeholder for future workshop assets, datasets, examples, templates, screenshots, and generated outputs.

## Important Source Links

- VizChitra sessions: https://vizchitra.com/2026/sessions
- VizChitra workshops: https://vizchitra.com/2026/workshops
- the workshop designer's proposal-process post: public AI-assisted proposal-process post
- Weather blog example: public weather-demo blog
- Babbage reflection: https://noenthuda.substack.com/p/my-learnings-from-babbage-insight
- Data Chatter / a geospatial data practitioner episode: https://podcasters.spotify.com/pod/show/data-chatter/episodes/12--Carts-and-graphs-Storytelling-through-maps-e18blbr

## Local / Temporary Artifacts

The Data Chatter episode was downloaded and transcribed locally during prep. These were not copied into the repo.

- RSS feed copy: `/private/tmp/datachatter.rss`
- Audio: `/private/tmp/example-audio.mp3`
- Transcript: `/private/tmp/datachatter-transcript/example-transcript.txt`
- Temporary Whisper venv/model: `/private/tmp/whisper-venv`, `/private/tmp/whisper-models`

The only point carried into the proposal from this episode is that visualisation/mapmaking follows the hypothesis/process logic of data science; the proposal should not over-index on the practitioner or the podcast.

## Next Prep Steps

- Decide whether participants should bring their own dataset or whether the fallback dataset should be primary.
- Build fallback dataset and second snapshot for reproducibility demo.
- Create templates:
  - `context.md`
  - `story_finding_prompt.md`
  - `visual_generation_prompt.md`
  - `review_checklist.md`
- Prepare one weather-site example and one anonymised Babbage-style metric-monitoring example.
- Convert the literature map into a short facilitator outline rather than participant reading.
