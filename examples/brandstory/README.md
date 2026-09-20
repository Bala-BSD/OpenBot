# BrandStory OpenBot tenant package

White-label tenant for [CopilotKit/OpenBot](https://github.com/CopilotKit/OpenBot), adapted from `examples/fintech`.

**Product name:** BrandStory OpenBot  
**Goal:** Self-hosted AI coworkers for SEO/GEO, Reels, Presentation Guardrails, ops handoff, and OSS research — built in Cursor, deployed on Git.

## Install into a fork

```sh
# from OpenBot repo root
cp -R /path/to/openbot-brandstory-tenant examples/brandstory
# .env (path relative to server/)
echo 'TENANT_PACKAGE_DIR=../examples/brandstory' >> .env
bash scripts/stop.sh
bash scripts/start.sh
```

Open http://localhost:3010 — you should see Studio Desk, Brand Knowledge, SEO & GEO, Reels & Content, Decks & Handoff, Open Source Scout.

## Channels to coworkers

| Channel | Agents |
| --- | --- |
| Studio Desk | general-assistant |
| Brand Knowledge | knowledge |
| SEO & GEO | seo-strategist, content-seo |
| Reels & Content | reels-director |
| Decks & Handoff | deck-guard, ops-handoff |
| Open Source Scout | oss-scout, research-desk |

## After first boot

1. Connect Google Drive / Notion in admin plugins.
2. Grant document tools to Knowledge, Research Desk, SEO, Reels, Deck Guard.
3. Replace Drive root names in `knowledge.yaml` with real folders.
4. Set `model.yaml` `default_model` to what your provider actually supports.
5. For production: real OAuth, drop `OPENBOT_SINGLE_USER`, TLS, own `KEY_ENCRYPTION_KEY`.

## License note

OpenBot template is MIT © CopilotKit. Keep LICENSE attribution in your fork. CopilotKit Intelligence + model APIs are separate services with their own terms.
