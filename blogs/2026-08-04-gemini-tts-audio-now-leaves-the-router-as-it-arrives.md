---
title: "Gemini TTS audio now leaves the router as it arrives"
url: "https://speko.ai/changelog#2026-08-03-gemini-tts-streams-incrementally"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. Gemini answers in server-sent events with base64 audio per frame, and the router was decoding the whole body before sending any of it. On a streaming route each frame is now decoded and forwarded as it arrives, which moved first-byte latency from 3695 ms to 786 ms on the same request, and gives the Dominican Spanish accent a streaming voice for the first time.
