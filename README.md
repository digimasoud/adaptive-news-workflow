# Adaptive News AI

Public workflow documentation for Adaptive News AI.

The private codebase is not published here. This public package explains the product workflow, goals, architecture, and developer integration model.

## What It Does

- Ask AI questions about crawled news.
- Discover news URLs from robots and sitemaps.
- Track HTTP status codes and crawl health.
- Store a local news dataset.
- Let developers sign up, choose a plan, create API keys, and define crawl plans.

## Workflow

```text
Target sites -> robots/sitemaps -> adaptive crawler -> local dataset -> AI news answers -> developer API
```

## Goals

- Public news AI homepage.
- Private production crawler core.
- Public workflow and SEO-friendly project page.
- Developer API self-service.
- Scheduled crawl plans.
- Multilingual news summaries.

## Private Boundary

This public repo intentionally excludes source code, credentials, private config, local SQLite databases, and raw crawl data.

