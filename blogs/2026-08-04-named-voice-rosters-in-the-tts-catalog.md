---
title: "Named voice rosters in the TTS catalog"
url: "https://speko.ai/changelog#2026-08-03-tts-voice-rosters"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. /v1/models TTS entries now include a curated voices array and a voicesVerified date. Each TTS entry in GET /v1/models now carries voices[] with { id, name, gender, styles }; roster order is meaningful, and the first entry is the provider default.
