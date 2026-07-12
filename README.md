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

Adaptive News AI is a lean news platform core with four connected surfaces:

| Surface | Purpose |
| --- | --- |
| AI News Homepage | Public users ask AI questions about the crawled news dataset. |
| Developer Portal | Developers sign up, choose a plan, create API keys, and define crawl plans. |
| Technical Panel | Operators manage targets, AI providers, HTTP status, reports, logs, and dataset access. |
| Public Workflow | Search engines and collaborators see an SEO-safe explanation while source remains private. |

## What It Does

- Ask AI questions about crawled news.
- Discover news URLs from robots and sitemaps.
- Track HTTP status codes and crawl health.
- Rotate and monitor crawl proxies/IPs with quarantine, blacklist detection, and capacity guidance.
- Extract resilient titles, publisher categories, and source tags from metadata and JSON-LD.
- Enrich records with optional AI summaries, entities, and topical tags.
- Store a local news dataset.
- Let developers sign up, choose a plan, create API keys, and define crawl plans.
- Run hourly, daily, and weekly plans with persistent history, quotas, and restart recovery.
- Serve a scoped, rate-limited Developer API with dataset filters and usage reporting.
- Switch every product surface between Persian RTL and English LTR.
- Collect component-level bug reports for operator triage.
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
Target sites -> robots/sitemaps -> crawl IP pool -> adaptive crawler -> metadata/AI enrichment -> local dataset -> AI answers and Developer API
```

Detailed flow:

1. Discover target websites through `robots.txt`, sitemap indexes, and news sitemap paths.
2. Score URLs with deterministic heuristics and optional AI classification.
3. Fetch pages through the proxy/direct-IP pool while recording status, retries, and block health.
4. Extract titles, categories, tags, canonical URLs, and optional AI enrichment.
5. Store private records locally and expose only public-safe fields through the API.
6. Answer news questions from the crawled dataset.
7. Let developers create scoped API keys and persistent crawl plans.
8. Enforce per-minute and monthly plan usage limits.
9. Let operators manage targets, AI providers, crawl IPs, reports, logs, and feedback.

## Goals

- `done`: Public news AI homepage.
- `active`: Developer API self-service.
- `active`: Scheduled hourly/daily/weekly crawl plans.
- `active`: 100+ Persian and international news sources.
- `active`: AI extraction, entities, tags, and multilingual summaries.
- `done`: Public workflow with private source code.
- `active`: Usage metering, rate limits, and billing readiness.
- `active`: Crawl IP rotation, health, blacklist, and capacity management.

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
