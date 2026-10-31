# Screenpipe

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Screenpipe is a local-first, source-available desktop application (by Mediar AI, Y Combinator S26) that continuously captures everything you see, say, and hear on your computer, reads on-screen text through OS accessibility APIs with an OCR fallback, transcribes system and microphone audio with local Whisper by default (or, when the user selects one in settings, with a cloud engine such as Deepgram or screenpipe-cloud, or an OpenAI-compatible transcription endpoint; audio leaves the device only when a remote engine is selected), and stores it all in a local SQLite database as a private, searchable memory. It exposes a full local REST API at http://localhost:3030 (71 operations across search, frames, audio, meetings, memories, speakers, tags, vault, cloud sync, cloud archive, and data retention) and ships as an MCP server so agents like Claude, Cursor, Codex, and Cline can query screen history and meeting transcripts. Automations are built as "pipes" — scheduled AI agents written in plain markdown. It is positioned as a local-first alternative to Rewind.ai, Microsoft Recall, and cloud meeting bots.

**Areas:** Company · Screen Recording · Screen Memory · Audio Transcription · Meeting Intelligence · Local-First · Privacy · AI Agents · MCP · Developer Tools · Productivity

## Screenpipe on APIs.io

Everything profiled for Screenpipe is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/screenpipe/](https://apis.io/providers/screenpipe/)** — or go straight to one of the APIs or properties below.

### APIs (18)

- [Screenpipe Activity API](https://apis.io/apis/screenpipe/screenpipe-activity-api/) — Activity summaries and analytics
- [Screenpipe Audio API](https://apis.io/apis/screenpipe/screenpipe-audio-api/) — Manage audio recording devices
- [Screenpipe Cloud Archive API](https://apis.io/apis/screenpipe/screenpipe-cloud-archive-api/) — Archive old data to cloud storage
- [Screenpipe Cloud Sync API](https://apis.io/apis/screenpipe/screenpipe-cloud-sync-api/) — Sync data across devices via cloud
- [Screenpipe Data Management API](https://apis.io/apis/screenpipe/screenpipe-data-management-api/) — Manual data deletion and storage info
- [Screenpipe Data Retention API](https://apis.io/apis/screenpipe/screenpipe-data-retention-api/) — Auto-delete old data locally
- [Screenpipe Database API](https://apis.io/apis/screenpipe/screenpipe-database-api/) — Direct database access
- [Screenpipe Elements API](https://apis.io/apis/screenpipe/screenpipe-elements-api/) — Query captured UI accessibility tree data
- [Screenpipe Experimental API](https://apis.io/apis/screenpipe/screenpipe-experimental-api/) — Experimental/unstable endpoints
- [Screenpipe Frames API](https://apis.io/apis/screenpipe/screenpipe-frames-api/) — Access captured screenshots and their extracted text
- [Screenpipe Meetings API](https://apis.io/apis/screenpipe/screenpipe-meetings-api/) — Detected and manual meeting transcriptions
- [Screenpipe Memories API](https://apis.io/apis/screenpipe/screenpipe-memories-api/) — AI-extracted knowledge from screen activity
- [Screenpipe Search API](https://apis.io/apis/screenpipe/screenpipe-search-api/) — Search through captured screen and audio content
- [Screenpipe Speakers API](https://apis.io/apis/screenpipe/screenpipe-speakers-api/) — Speaker identification and management
- [Screenpipe System API](https://apis.io/apis/screenpipe/screenpipe-system-api/) — Health checks and system status
- [Screenpipe Tags API](https://apis.io/apis/screenpipe/screenpipe-tags-api/) — Tag content items for organization
- [Screenpipe Vault API](https://apis.io/apis/screenpipe/screenpipe-vault-api/) — Encrypt/decrypt all data at rest
- [Screenpipe Vision API](https://apis.io/apis/screenpipe/screenpipe-vision-api/) — Manage screen capture monitors

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [screenpipe](https://apis.io/servers/screenpipe/screenpipe/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Screenpipe Agentic Access](https://apis.io/agentic-access/screenpipe/screenpipe-agentic-access/)

#### JSON Schema (56)

The data models the API reads and writes.

- [ActivitySummaryResponse](https://apis.io/schemas/screenpipe/screenpipe-activity-summary-response/)
- [AddContentRequest](https://apis.io/schemas/screenpipe/screenpipe-add-content-request/)
- [AddContentResponse](https://apis.io/schemas/screenpipe/screenpipe-add-content-response/)
- [AddTagsRequest](https://apis.io/schemas/screenpipe/screenpipe-add-tags-request/)
- [AddTagsResponse](https://apis.io/schemas/screenpipe/screenpipe-add-tags-response/)
- [ArchiveConfigureRequest](https://apis.io/schemas/screenpipe/screenpipe-archive-configure-request/)
- [ArchiveInitRequest](https://apis.io/schemas/screenpipe/screenpipe-archive-init-request/)
- [ArchiveInitResponse](https://apis.io/schemas/screenpipe/screenpipe-archive-init-response/)
- [ArchiveStatusResponse](https://apis.io/schemas/screenpipe/screenpipe-archive-status-response/)
- [AudioDeviceControlRequest](https://apis.io/schemas/screenpipe/screenpipe-audio-device-control-request/)
- [AudioDeviceControlResponse](https://apis.io/schemas/screenpipe/screenpipe-audio-device-control-response/)
- [BulkDeleteMeetingsRequest](https://apis.io/schemas/screenpipe/screenpipe-bulk-delete-meetings-request/)
- [CreateMemoryRequest](https://apis.io/schemas/screenpipe/screenpipe-create-memory-request/)
- [DeleteDeviceDataRequest](https://apis.io/schemas/screenpipe/screenpipe-delete-device-data-request/)
- [DeleteTimeRangeRequest](https://apis.io/schemas/screenpipe/screenpipe-delete-time-range-request/)
- [DeleteTimeRangeResponse](https://apis.io/schemas/screenpipe/screenpipe-delete-time-range-response/)
- [DeviceStorageEntry](https://apis.io/schemas/screenpipe/screenpipe-device-storage-entry/)
- [ElementsListResponse](https://apis.io/schemas/screenpipe/screenpipe-elements-list-response/)
- [FrameContextResponse](https://apis.io/schemas/screenpipe/screenpipe-frame-context-response/)
- [FrameMetadataResponse](https://apis.io/schemas/screenpipe/screenpipe-frame-metadata-response/)
- [FrameTextResponse](https://apis.io/schemas/screenpipe/screenpipe-frame-text-response/)
- [GetTagsBatchRequest](https://apis.io/schemas/screenpipe/screenpipe-get-tags-batch-request/)
- [GetTagsBatchResponse](https://apis.io/schemas/screenpipe/screenpipe-get-tags-batch-response/)
- [HealthCheckResponse](https://apis.io/schemas/screenpipe/screenpipe-health-check-response/)
- [ListDeviceResponse](https://apis.io/schemas/screenpipe/screenpipe-list-device-response/)
- …and 31 more published on APIs.io

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Screenpipe Context](https://apis.io/jsonld/screenpipe/screenpipe-context/)

#### Collections (18)

Postman and Open Collection request collections.

- [Screenpipe Activity API](https://apis.io/collections/screenpipe/open-screenpipe-activity-api/)
- [Screenpipe Activity Audio API](https://apis.io/collections/screenpipe/open-screenpipe-audio-api/)
- [Screenpipe Activity Cloud Archive API](https://apis.io/collections/screenpipe/open-screenpipe-cloud-archive-api/)
- [Screenpipe Activity Cloud Sync API](https://apis.io/collections/screenpipe/open-screenpipe-cloud-sync-api/)
- [Screenpipe Activity Data Management API](https://apis.io/collections/screenpipe/open-screenpipe-data-management-api/)
- [Screenpipe Activity Data Retention API](https://apis.io/collections/screenpipe/open-screenpipe-data-retention-api/)
- [Screenpipe Activity Database API](https://apis.io/collections/screenpipe/open-screenpipe-database-api/)
- [Screenpipe Activity Elements API](https://apis.io/collections/screenpipe/open-screenpipe-elements-api/)
- [Screenpipe Activity Experimental API](https://apis.io/collections/screenpipe/open-screenpipe-experimental-api/)
- [Screenpipe Activity Frames API](https://apis.io/collections/screenpipe/open-screenpipe-frames-api/)
- [Screenpipe Activity Meetings API](https://apis.io/collections/screenpipe/open-screenpipe-meetings-api/)
- [Screenpipe Activity Memories API](https://apis.io/collections/screenpipe/open-screenpipe-memories-api/)
- [Screenpipe Activity Search API](https://apis.io/collections/screenpipe/open-screenpipe-search-api/)
- [Screenpipe Activity Speakers API](https://apis.io/collections/screenpipe/open-screenpipe-speakers-api/)
- [Screenpipe Activity System API](https://apis.io/collections/screenpipe/open-screenpipe-system-api/)
- [Screenpipe Activity Tags API](https://apis.io/collections/screenpipe/open-screenpipe-tags-api/)
- [Screenpipe Activity Vault API](https://apis.io/collections/screenpipe/open-screenpipe-vault-api/)
- [Screenpipe Activity Vision API](https://apis.io/collections/screenpipe/open-screenpipe-vision-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Screenpipe Openapi Overlay](https://apis.io/overlays/screenpipe/screenpipe-openapi-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Screenpipe API Rules](https://apis.io/rules/screenpipe/screenpipe-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Screenpipe Authentication](https://apis.io/security/screenpipe/screenpipe-authentication/)
- [Screenpipe Domain Security](https://apis.io/security/screenpipe/screenpipe-domain-security/)
- [Screenpipe Trust Center](https://apis.io/security/screenpipe/screenpipe-trust-center/)
- [Screenpipe Vulnerability Disclosure](https://apis.io/security/screenpipe/screenpipe-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Screenpipe Plans Pricing](https://apis.io/plans/screenpipe/screenpipe-plans-pricing/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://screenpi.pe)
- [Documentation](https://docs.screenpipe.com)
- [Getting started](https://docs.screenpipe.com/getting-started)
- [API reference](https://docs.screenpipe.com/api-reference)
- [Pricing](https://screenpipe.com/pricing)
- [Support](https://docs.screenpipe.com/troubleshooting)
- [Changelog](https://docs.screenpipe.com/changelog)
- [Blog](https://screenpipe.com/blog)
- [Security](https://screenpipe.com/security)
- [Compliance](https://screenpipe.com/security)
- [Terms of service](https://screenpipe.com/terms)
- [Privacy policy](https://screenpipe.com/privacy)
- [GitHub](https://github.com/screenpipe)

## API Evangelist rating

**Kin Score 60.9** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 50.0 |
| Contract governance | 35.6 |
| Operational transparency | 36.8 |
| Developer ergonomics | 73.2 |
| Access clarity | 78.9 |

**Agent readiness 23.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 35.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/screenpipe/](https://apis.io/providers/screenpipe/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Screenpipe: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/screenpipe/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
