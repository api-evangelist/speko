---
title: "Streaming TTS works without a provider pin, and the WebSocket text lifecycle has one owner"
url: "https://speko.ai/changelog#2026-08-02-streaming-tts-unpinned-and-text-lifecycle"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. Unpinned streaming TTS requests no longer return 503, the documented WebSocket frame sequence now produces audio on every streaming provider, bare provider names work in X-Speko-Allow, and interimResults finally controls whether partial transcripts are sent. POST /v1/audio/speech/stream and POST /v1/synthesize/stream previously returned 503 no_streaming_tts_provider for any request that set no X-Speko-Allow header, whenever the API key's routing chain pinned a provider that cannot stream.
