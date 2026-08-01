---
name: Search screen and audio history
description: >-
  Search a user's captured screen text, audio transcriptions, and UI elements in
  screenpipe, then pull a specific frame and its context to ground an answer.
api: openapi/screenpipe-openapi-original.yml
operations:
  - routes_search_search
  - routes_search_keyword_search_handler
  - routes_frames_get_frame_data
  - routes_frames_get_frame_context
---

# Search screen and audio history

Use this when the user asks "what was I looking at / who said what / find that thing on my screen." The screenpipe recorder must be running and serving `http://localhost:3030`.

## Preconditions
- Base URL: `http://localhost:3030`. No auth by default (loopback). If the server requires a token, get it with `screenpipe auth token` and send it as a bearer header.
- Times are ISO 8601 (`start_time` / `end_time`).

## Steps
1. **Search** — `GET /search` (`routes_search_search`). Set `q` to the search text, `content_type` to one of `all | ocr | audio | input | accessibility | memory`, and narrow with `app_name`, `window_name`, `browser_url`, `speaker_name`, `start_time`, `end_time`. Page with `limit` and `offset` (see `conventions/screenpipe-conventions.yml`). For a fast, keyword-only lookup use `GET /search/keyword` (`routes_search_keyword_search_handler`) instead.
2. **Pick the best match** — each result carries a `frame_id` and timestamp. Choose the frame that best answers the question.
3. **Read the frame** — `GET /frames/{frame_id}` (`routes_frames_get_frame_data`) for the screenshot/metadata; add `include_frames`/base64 only when you actually need the image.
4. **Get surrounding context** — `GET /frames/{frame_id}/context` (`routes_frames_get_frame_context`) for accessibility text, tree nodes, and extracted URLs (falls back to OCR for legacy frames).
5. **Answer** with a citation to the timestamp/app; offer `screenpipe://frame/{frame_id}` as a deep link.

## Rules
- Respect the user's privacy: only surface what the query needs; do not dump full history.
- Errors are plain HTTP status codes (see `errors/screenpipe-problem-types.yml`); a `503` from `/health` means the recorder is not ready.
