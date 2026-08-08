---
title: "Voice policy controls for router keys"
url: "https://speko.ai/changelog#2026-08-03-voice-policy-keys"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. Router key policies can now select a TTS gender, pin a model voice, and set per-model voice overrides through the API and console. POST and PATCH /api/keys accept TTS policy fields gender, pinnedVoice with model and voice members, and overrides keyed by TTS catalog model id.
