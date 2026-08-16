---
title: "transcription: guide OpenAI's transcribe models with a prompt"
url: "https://speko.ai/changelog#2026-08-08-openai-transcription-prompt"
date: "2026-08-08"
feed_url: "https://speko.ai/changelog.xml"
---
Status: scheduled. The provider-options document now forwards openai.prompt, so a caller can seed OpenAI's prompt-guided transcription models with vocabulary and style -- product names, speaker names, spelling conventions -- on every transcription route. The prompt travels in OpenAI's own spelling on each transport and reaches OpenAI only; providers that never read it never receive it.
