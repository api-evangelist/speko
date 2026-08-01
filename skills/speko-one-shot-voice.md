---
name: Transcribe, complete, and synthesize with automatic provider routing
description: Use Speko's one-shot voice endpoints to run speech-to-text, an LLM completion, and text-to-speech, each routed to the best provider with automatic failover.
api: openapi/speko-openapi-original.json
operations: [transcribe, complete, synthesize, listVoices]
---

# One-shot voice pipeline on Speko

Speko routes each call to the highest-scoring provider for your intent and fails over server-side. No provider keys required (or bring your own).

## Auth
Every request sends `Authorization: Bearer sk_live_...`. Keys are minted at https://platform.speko.dev.

## Routing intent
One-shot endpoints take routing intent as a JSON `x-speko-intent` header: `(language, region, optimizeFor)`.

## Steps
1. **Transcribe** — `transcribe` (`POST /v1/transcribe`). Body is binary audio; put routing intent in `x-speko-intent`. Returns transcript text.
2. **Complete** — `complete` (`POST /v1/complete`). Send the transcript (plus any system prompt) as messages; returns assistant text + token usage.
3. **List voices** (optional) — `listVoices` (`GET /v1/voices`) to pick a TTS voice; catalog is grouped by provider.
4. **Synthesize** — `synthesize` (`POST /v1/synthesize`). Returns binary audio; the `Content-Type` / `X-Speko-Audio-Format` header tells you the format.

## Errors
All errors return `{ error, code }` (not RFC 9457). `401` = bad/missing key; `400` = validation failure. See `errors/speko-problem-types.yml`.
