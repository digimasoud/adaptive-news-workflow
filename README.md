# Adaptive News AI Public Workflow

Public, SEO-friendly workflow documentation for **Adaptive News AI**.

This repository does **not** publish the private crawler codebase. It explains the product workflow, goals, architecture, screenshots, and developer integration model so the project can be shared publicly without exposing source code, secrets, local databases, or raw crawl data.

Public page:

```text
https://digimasoud.github.io/adaptive-news-workflow/
```

Private implementation repo:

```text
https://github.com/digimasoud/adaptive-news-crawler
```

The implementation repository is private. This public repository is the shareable product/workflow layer.

## Product Summary

Adaptive News AI is a lean news platform core with three surfaces:

| Surface | Purpose |
| --- | --- |
| AI News Homepage | Public users ask AI questions about the crawled news dataset. |
| Developer Portal | Developers sign up, choose a plan, create API keys, and define crawl plans. |
| Technical Panel | Operators manage targets, AI providers, HTTP status, reports, logs, and dataset access. |

## What It Does

- Ask AI questions about crawled news.
- Discover news URLs from robots and sitemaps.
- Track HTTP status codes and crawl health.
- Store a local news dataset.
- Let developers sign up, choose a plan, create API keys, and define crawl plans.
- Show public screenshots for the homepage, developer portal, and technical crawler panel.
- Publish SEO metadata, Open Graph tags, `robots.txt`, `sitemap.xml`, and JSON-LD structured data.

## What Stays Private

- Source code.
- `.env` files and API keys.
- Crawler keys and ingestion credentials.
- Local SQLite databases.
- Raw HTML datasets when licensing/source terms are unclear.
- Internal implementation details that are not needed for public product discovery.

## Screenshots

- `assets/homepage.png`: AI news question homepage.
- `assets/developer.png`: Developer portal for API keys, plans, and crawl planning.
- `assets/panel.png`: Technical crawler panel for reports, targets, and AI status.

## Workflow

```text
Target sites -> robots/sitemaps -> adaptive crawler -> local dataset -> AI news answers -> developer API
```

Detailed flow:

1. Discover target websites through `robots.txt`, sitemap indexes, and news sitemap paths.
2. Score URLs with deterministic heuristics and optional AI classification.
3. Fetch raw HTML while recording HTTP status and redirect history.
4. Store public-safe metadata in a local dataset.
5. Answer news questions from the crawled dataset.
6. Let developers create API keys and crawl plans.
7. Let operators manage targets, reports, logs, and AI providers.

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

## SEO Assets

- `index.html`: public project page.
- `robots.txt`: crawler access rules.
- `sitemap.xml`: sitemap for GitHub Pages.
- `assets/homepage.png`: social preview and homepage screenshot.
- `assets/developer.png`: developer portal screenshot.
- `assets/panel.png`: technical panel screenshot.
- `assets/workflow.svg`: architecture/workflow diagram.
