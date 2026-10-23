---
title: "Auto routing supports languages that have no benchmark ranking"
url: "https://speko.ai/changelog#router-unranked-languages"
date: "2026-10-09"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. For a language the benchmark does not rank, such as Swahili or Indonesian, auto routing picks models that support the language. Before this change, a Swahili STT request could go to an English-only model and return English text.
