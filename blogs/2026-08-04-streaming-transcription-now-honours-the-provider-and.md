---
title: "Streaming transcription now honours the provider and language a request asks for"
url: "https://speko.ai/changelog#2026-08-03-streaming-transcription-honours-routing"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. GET /v1/transcribe/stream ignored X-Speko-Allow, X-Speko-Deny, X-Speko-Language, the objective, the price cap and the key's own provider order. Every request was served by whichever stream-capable provider ranked first, so four of the five provider families that implement streaming transcription were unreachable.
