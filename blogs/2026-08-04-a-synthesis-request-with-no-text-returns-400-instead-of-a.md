---
title: "A synthesis request with no text returns 400 instead of a provider error"
url: "https://speko.ai/changelog#2026-08-03-missing-tts-text-is-a-400"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. A TTS request whose text field was absent or empty was sent to a provider, rejected, and retried across every candidate before returning 502 all_upstreams_failed. A malformed request now returns 400 and names the field it is missing.
