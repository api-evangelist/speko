---
title: "voice \"auto\" and OpenAI preset names now follow the key's voice settings"
url: "https://speko.ai/changelog#2026-08-06-voice-auto-follows-the-key"
date: "2026-08-07"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. A request that named any voice - including "auto" or an OpenAI preset like "alloy" - silently switched off the key's pinned voice and gender settings, and a preset then landed on each vendor's house default, so the voice could change identity or gender when routing failed over. "auto" now always defers to the key, and a preset defers to the key whenever the key has voice settings.
