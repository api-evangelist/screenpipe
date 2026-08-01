---
name: Summarize activity and save a memory
description: >-
  Pull a lightweight activity summary for a time range from screenpipe and
  persist a durable AI memory the agent can recall later.
api: openapi/screenpipe-openapi-original.yml
operations:
  - routes_activity_summary_get_activity_summary
  - routes_memories_create_memory_handler
  - routes_memories_list_memories_handler
---

# Summarize activity and save a memory

Use this for "what did I work on today" and to give an agent a persistent second brain. Requires the recorder at `http://localhost:3030`.

## Steps
1. **Get an activity summary** — `GET /activity-summary` (`routes_activity_summary_get_activity_summary`) with `start_time`/`end_time`. Returns a compact overview (~200-500 tokens): app usage, recent accessibility texts, and an audio summary. Prefer this over raw `/search` when you only need the shape of the period.
2. **Draft the summary** for the user from that overview; if they want detail, drill in with `GET /search` (see the search-screen-history skill).
3. **Persist a memory** — `POST /memories` (`routes_memories_create_memory_handler`) with the distilled insight; attach the originating `frame_id` when the memory came from a specific screen moment.
4. **Recall later** — `GET /memories` (`routes_memories_list_memories_handler`) to list saved memories; update/delete with the `{id}` operations when superseded.

## Rules
- Store insight, not raw dumps — memories are durable, so keep them concise and privacy-safe.
- Writes are not idempotency-keyed (`conventions/screenpipe-conventions.yml`); avoid retrying `POST /memories` blindly to prevent duplicates — list first if unsure.
