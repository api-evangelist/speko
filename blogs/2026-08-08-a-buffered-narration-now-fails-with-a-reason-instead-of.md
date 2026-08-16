---
title: "A buffered narration now fails with a reason instead of outrunning the response deadline"
url: "https://speko.ai/changelog#2026-08-08-buffered-narration-gives-up-before-the-platform-does"
date: "2026-08-08"
feed_url: "https://speko.ai/changelog.xml"
---
Status: scheduled. A long narration on the buffered route could run past the platform's request deadline and come back 500 with no routing headers, giving the caller nothing to act on. It now stops at four minutes with a named cause and points at the streaming route.
