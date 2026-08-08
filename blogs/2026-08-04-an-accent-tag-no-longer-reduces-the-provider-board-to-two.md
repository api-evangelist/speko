---
title: "An accent tag no longer reduces the provider board to two candidates"
url: "https://speko.ai/changelog#2026-08-02-accent-tags-keep-the-full-provider-board"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. Requesting a regional accent such as es-CO or es-MX left only the two providers named in that accent's table, so an explicit X-Speko-Allow for any other healthy provider returned 503 no_candidate and an accent request had almost no failover depth. An accent now orders the board instead of replacing it.
