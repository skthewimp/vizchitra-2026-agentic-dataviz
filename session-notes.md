# Session Notes

## User Context

the facilitator had made an ad hoc / post-deadline pitch to VizChitra for a 20-minute talk or workshop titled roughly "Building aesthetic and narrative agentic visualisations."

The organisers replied that they were interested in including it as an invited workshop, but wanted the angle sharpened from "aesthetic narrative visualisations" to **production-grade, reproducible dataviz systems using LLMs and agents**. They requested:

- title;
- subtitle;
- short description;
- long description;
- third-person bio;
- overall objective;
- session-wise agenda;
- key takeaways;
- prerequisites;
- participant preparation/setup;
- audience;
- why the facilitator is the right person to teach it.

## Main Decisions

- Public title: **Agentic DataViz: Build Systems, Not Charts**.
- Public subtitle: **Find the Story. Teach the Agent. Run It Again.**.
- Public page: https://vizchitra.com/2026/sessions/agentic-dataviz
- Date/time: **2026-07-03, 14:30-17:30**.
- Venue: **Underline Center**.
- Internal opening hook retained: **The chart is the last step.**
- The proposal should not compete with the existing VizChitra AI-coding workshop. The differentiator is repeatability, context, taste, review, and reproducibility.
- The final conceptual spine is:
  1. visualisation follows a hypothesis-driven data-science process;
  2. AI can help automate/scaffold parts of that process;
  3. the system needs context, examples, and review before the chart is generated;
  4. the final output should be reproducible, not a lucky one-off prompt.

## Source Material Used

- VizChitra 2026 sessions and workshop list.
- a public workshop designer's blog post on submitting an AI-assisted VizChitra proposal.
- the facilitator's Babbage / AI-for-data consulting positioning in this repo.
- the facilitator's weather site and AI-generated weather blog.
- Data Chatter S1E12 with a geospatial data practitioner, used only for the small point that mapmaking/visualisation follows the same hypothesis/process logic as data science.
- Literature scan on narrative visualisation, automated insight discovery, LLM-based visualisation generation, agent workflows, and chart evaluation.

## Transcript / Tooling Notes

The Data Chatter RSS feed was found through Apple's podcast lookup API. The a geospatial data practitioner episode audio was downloaded from the podcast RSS enclosure to `/private/tmp`.

Temporary local files:

- `/private/tmp/datachatter.rss`
- `/private/tmp/example-audio.mp3`
- `/private/tmp/datachatter-transcript/example-transcript.txt`

Whisper setup:

- Existing `~/.local/bin/whisper` was stale and pointed at a removed Anaconda Python.
- A temporary venv was created at `/private/tmp/whisper-venv`.
- `openai-whisper` was installed into that venv.
- Whisper `base` model was downloaded into `/private/tmp/whisper-models`.
- Homebrew `ffmpeg` was broken due to a missing `x265` dylib; `brew reinstall x265` repaired it and upgraded `ffmpeg`.

None of the audio/transcript/model files were copied into the repo.

## Files Created / Moved

- `workshops/README.md`
- `workshops/vizchitra-2026-agentic-dataviz/README.md`
- `workshops/vizchitra-2026-agentic-dataviz/proposal-and-prep.md`
- `workshops/vizchitra-2026-agentic-dataviz/proposal-and-prep.html`
- `workshops/vizchitra-2026-agentic-dataviz/email-body.md`
- `workshops/vizchitra-2026-agentic-dataviz/session-notes.md`

Root `README.md` was updated to include `workshops/`.

