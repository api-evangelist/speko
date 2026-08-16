---
title: "transcription: words, speakers, segments and the detected language"
url: "https://speko.ai/changelog#2026-08-06-transcripts-carry-words-speakers-and-language"
date: "2026-08-06"
feed_url: "https://speko.ai/changelog.xml"
---
Status: scheduled. Transcription responses and streaming transcript frames now carry the word timings, speaker labels, utterance segments, duration, confidence and detected language the serving provider already sent and the router used to discard. text is byte for byte what it always was, and every added field is omitted when the provider that answered cannot supply it.
