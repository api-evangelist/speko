---
title: "Streaming TTS reaches every provider that can stream, including the regional-accent voices"
url: "https://speko.ai/changelog#2026-08-03-streaming-reaches-every-progressive-provider"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. POST /v1/audio/speech/stream and POST /v1/synthesize/stream could only be served by the four providers with a WebSocket TTS surface. Seven more already answer with progressive raw PCM over HTTP, and two of them carry the validated regional Spanish voices, so an accent tag could never reach its own voice on a streaming route.
