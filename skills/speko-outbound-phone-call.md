---
name: Place an outbound phone call and pull the call report
description: Start an outbound PSTN call backed by a Speko voice session, follow the call events, and retrieve the post-call report.
api: openapi/speko-openapi-original.json
operations: [createPhoneSession, getCall, listCallEvents, getCallReport]
---

# Outbound phone call + report

## Auth
`Authorization: Bearer sk_live_...`. A provisioned phone number (see `listPhoneNumbers` / `createPhoneNumber`) or SIP trunk is required to place calls.

## Steps
1. **Place the call** — `createPhoneSession` (`POST /v1/sessions/phone`) — places an outbound PSTN call backed by a Speko voice session.
2. **Inspect the call** — `getCall` (`GET /v1/calls/{id}`) for status/detail.
3. **Follow events** — `listCallEvents` (`GET /v1/calls/{id}/events`) for the live lifecycle event stream (also delivered as webhooks; see `asyncapi/speko-webhooks.yml`).
4. **Get the report** — `getCallReport` (`GET /v1/calls/{id}/report`) for summary, outcome, structured data, transcript, and cost breakdown. Finalize with `finalizeCallReport` if needed.

## Errors
`404` = call id unknown to your org. All errors are `{ error, code }` — see `errors/speko-problem-types.yml`.
