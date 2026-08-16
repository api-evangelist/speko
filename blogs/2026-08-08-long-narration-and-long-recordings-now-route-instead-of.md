---
title: "Long narration and long recordings now route instead of hitting a limit"
url: "https://speko.ai/changelog#2026-08-08-long-audio-narration-and-transcription"
date: "2026-08-08"
feed_url: "https://speko.ai/changelog.xml"
---
Status: scheduled. Synthesis past a vendor's character cap answered with the vendor's own refusal, and a recording past 8 MiB answered 413 on the route the OpenAI SDK reaches. Long text is now split at sentence boundaries and narrated on one voice, and a transcription upload is allowed the 25 MiB OpenAI documents plus the first-byte budget the bytes actually need.
