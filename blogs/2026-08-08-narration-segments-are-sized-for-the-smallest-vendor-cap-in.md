---
title: "Narration segments are sized for the smallest vendor cap in the catalog"
url: "https://speko.ai/changelog#2026-08-08-narration-segments-clear-every-vendor-cap"
date: "2026-08-08"
feed_url: "https://speko.ai/changelog.xml"
---
Status: scheduled. A narration segment was sized at 4000 characters on the assumption that OpenAI's 4096 was the binding limit. Two vendors refuse past 2000, and the vendor is chosen after the first segment is already sent, so a segment sized for one vendor could be refused by whichever one actually answered.
