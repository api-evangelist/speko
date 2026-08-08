---
title: "Routing preview reflects the per-language transcription preference"
url: "https://speko.ai/changelog#2026-08-03-routing-preview-reflects-language-preference"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. The Spanish transcription preference applied to requests but not to GET /v1/routing/preview, so the console key wizard listed and pinned the global ranking instead. A key created that way was pinned to an order that then outranked the preference on every request it made.
