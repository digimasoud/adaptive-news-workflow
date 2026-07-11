# Adaptive News AI

Public workflow documentation for Adaptive News AI.

The private codebase is not published here. This public package explains the product workflow, goals, architecture, and developer integration model.

Public page:

```text
https://digimasoud.github.io/adaptive-news-workflow/
```

## What It Does

- Ask AI questions about crawled news.
- Discover news URLs from robots and sitemaps.
- Track HTTP status codes and crawl health.
- Store a local news dataset.
- Let developers sign up, choose a plan, create API keys, and define crawl plans.
- Show public screenshots for the homepage, developer portal, and technical crawler panel.
- Publish SEO metadata, Open Graph tags, `robots.txt`, `sitemap.xml`, and JSON-LD structured data.

## Screenshots

- `assets/homepage.png`: AI news question homepage.
- `assets/developer.png`: Developer portal for API keys, plans, and crawl planning.
- `assets/panel.png`: Technical crawler panel for reports, targets, and AI status.

## Workflow

```text
Target sites -> robots/sitemaps -> adaptive crawler -> local dataset -> AI news answers -> developer API
```

## Goals

- `done`: Public news AI homepage.
- `active`: Developer API self-service.
- `next`: Scheduled crawl plans.
- `active`: 100+ Persian and international news sources.
- `planned`: AI extraction, entities, tags, and multilingual summaries.
- `done`: Public workflow with private source code.
- `planned`: Usage metering, rate limits, and billing readiness.

## Private Boundary

This public repo intentionally excludes source code, credentials, private config, local SQLite databases, and raw crawl data.
