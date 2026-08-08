---
title: "An omitted speed no longer breaks synthesis on Hume and Smallest AI"
url: "https://speko.ai/changelog#2026-08-02-wav-output-and-optional-speed"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. A synthesis request that did not set speed serialized it as JSON null, which Hume and Smallest AI reject. On the streaming transports the 200 status line is sent before the provider replies, so the caller received a successful response carrying zero bytes.
