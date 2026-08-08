---
title: "A regional language tag no longer silences WebSocket TTS providers"
url: "https://speko.ai/changelog#2026-08-03-regional-language-tags-on-websocket-tts"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. Requesting a regional tag such as es-CO or es-MX forwarded the full tag to providers that accept only a base language. They rejected the request as invalid input, and because the streaming transports commit a 200 before the provider answers, the caller received a successful response carrying no audio.
