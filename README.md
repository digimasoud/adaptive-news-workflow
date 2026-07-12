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

## Commercial Requests

The website's `Request customization` action opens a structured public issue for custom deployments, source onboarding, AI-provider routing, API changes, reports, and branded experiences. Do not include credentials, private datasets, or confidential details in a public issue.

A dedicated domain mailbox is the recommended long-term channel for private commercial conversations. No email address is published until a verified business mailbox is configured.

## SEO Assets

- `index.html`: public project page.
- `robots.txt`: crawler access rules.
- `sitemap.xml`: sitemap for GitHub Pages.
- `llms.txt`: concise product and data-boundary context for AI agents.
- `404.html`: index-safe custom not-found page.
- `favicon.svg`: Adaptive News AI browser icon.
- `assets/homepage.png`: social preview and homepage screenshot.
- `assets/og-image.png`: dedicated `1200x630` Open Graph and Twitter share image.
- `assets/developer.png`: developer portal screenshot.
- `assets/panel.png`: technical panel screenshot.
- `assets/workflow.svg`: architecture/workflow diagram.
- `.github/ISSUE_TEMPLATE/customization-request.yml`: structured commercial request form.

## Search Launch Checklist

Implemented in the public site:

- English title, description, canonical URL, robots directives, and semantic heading structure.
- Open Graph and Twitter metadata with a dedicated `1200x630` share image.
- `WebSite`, `WebPage`, `ImageObject`, `SoftwareApplication`, and visible `FAQPage` JSON-LD.
- Discoverable HTML images with dimensions, descriptive alt text, lazy loading, and image sitemap entries.
- Root sitemap, robots declaration, favicon, HTTPS GitHub Pages hosting, custom 404, and `llms.txt`.
- Responsive layouts verified at desktop and mobile widths.

External setup still requires the site owner:

- Add the final custom domain and enforce HTTPS after DNS is configured.
- Verify ownership in Google Search Console and Bing Webmaster Tools.
- Submit `https://digimasoud.github.io/adaptive-news-workflow/sitemap.xml` and request indexing for the canonical page.
- Configure a real domain mailbox before publishing commercial email contact details.
