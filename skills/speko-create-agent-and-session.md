---
name: Create a voice agent and start a browser session
description: Persist a reusable Speko voice agent, then mint a real-time browser session seeded from it and read back the transcript.
api: openapi/speko-openapi-original.json
operations: [createAgent, createSession, postSessionTurns, getSessionTranscript]
---

# Create an agent and run a browser session

## Auth
`Authorization: Bearer sk_live_...` on every request. Agents are org-scoped; ids from another org return 404.

## Steps
1. **Create agent** — `createAgent` (`POST /v1/agents`). Supply `systemPrompt`, optional `voice`, routing `intent`, and optional `llmOptions`, keyed by `name`. Returns the agent `id`.
2. **Create session** — `createSession` (`POST /v1/sessions`) passing `agentId` = the id from step 1. Returns `transportToken` + `transportUrl` (LiveKit) — hand these to `@spekoai/client` to join from the browser.
3. **Post turns** (server-side transcript) — `postSessionTurns` (`POST /v1/sessions/{id}/turns`). Idempotent on `(session_id, index)`: re-posting the same index replaces that turn. Only finalized turns persist.
4. **Read transcript** — `getSessionTranscript` (`GET /v1/sessions/{id}/transcript`).

## Conventions
Idempotency and pagination are documented in `conventions/speko-conventions.yml`. Deleting an org's only remaining agent returns `409`.
