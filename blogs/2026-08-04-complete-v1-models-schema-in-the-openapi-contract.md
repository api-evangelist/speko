---
title: "Complete /v1/models schema in the OpenAPI contract"
url: "https://speko.ai/changelog#2026-08-04-openapi-models-contract"
date: "2026-08-04"
feed_url: "https://speko.ai/changelog.xml"
---
Status: available. The published Model schema now declares every field GET /v1/models actually serves, not just the OpenAI-compatible core. The Model schema previously declared only id, aliases, object, provider, model, api, and routable; the endpoint has served more for some time.
