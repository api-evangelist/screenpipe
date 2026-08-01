---
name: Retrieve and clean up meeting transcripts
description: >-
  List detected meetings in screenpipe, pull a meeting's transcript, and tidy up
  speaker identities (name the unnamed speakers).
api: openapi/screenpipe-openapi-original.yml
operations:
  - routes_meetings_list_meetings_handler
  - routes_meetings_get_meeting_handler
  - routes_speakers_get_unnamed_speakers_handler
  - routes_speakers_update_speaker_handler
---

# Retrieve and clean up meeting transcripts

Use this to answer "summarize my last meeting" or "who was on that call." Requires the recorder running at `http://localhost:3030`.

## Steps
1. **List meetings** — `GET /meetings` (`routes_meetings_list_meetings_handler`) returns detected and manually started meetings with transcriptions. Filter/paginate with `limit`/`offset` and a time range.
2. **Open a meeting** — `GET /meetings/{id}` (`routes_meetings_get_meeting_handler`) for the full transcript, speaker segments, and timing.
3. **Find unnamed speakers** — `GET /speakers/unnamed` (`routes_speakers_get_unnamed_speakers_handler`) to see which diarized speakers still need a name.
4. **Name a speaker** — `POST /speakers/update` (`routes_speakers_update_speaker_handler`) with the `speaker_id` and the resolved `name`. Only do this when you can confidently attribute the voice (calendar context, prior naming, or explicit user confirmation).
5. **Summarize** the transcript grouped by speaker; cite meeting id and time range.

## Rules
- Never invent a speaker name — confirm with the user before writing via `POST /speakers/update`.
- Speaker merge/reassign are separate operations (`routes_speakers_merge_speakers_handler`, `routes_speakers_reassign_speaker_handler`); prefer naming over merging unless clearly the same identity.
- Errors surface as HTTP status codes (`errors/screenpipe-problem-types.yml`).
