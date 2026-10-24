# Awesome-User-Engagement-Analytics

# Top User Engagement Analytics Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Self-Hosted Product Analytics, Session Replay & Feature Flag Integration*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **User Engagement Analytics**. These tools help product teams understand how users actually behave inside their applications — tracking events, funnels, retention, and feature adoption — with a spectrum running from polished commercial suites to self-hosted platforms that keep your behavioral data on your own infrastructure.

**Examples** include PostHog, OpenPanel, Matomo, Countly, and the commercial platforms (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, transparent data ownership, and integrated analytics-plus-replay workflows — ideal for engineering-led teams who want product intelligence without per-event pricing that scales with growth.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Mixpanel** — **The polished product analytics standard.** Event tracking, funnels, retention, and cohort analysis with a clean UI. **Free tier** with limited events; paid plans scale with volume. **Best for product teams** wanting the most approachable analytics interface without infrastructure management. **Trade-offs**: cloud-only, and add-ons like Group Analytics and Data Pipelines can significantly increase costs .

- **Amplitude** — **The deepest behavioral analytics platform.** Advanced cohort analysis, growth modeling, and retention curves. **Free tier** available; paid plans per-event. **Best for dedicated product analysts** needing mature analysis surface for complex behavioral questions . **Trade-offs**: steeper learning curve than Mixpanel, and no self-hosting option.

- **Pendo** — **In-app guides plus analytics in one platform.** Combines product analytics with user onboarding, tooltips, and feedback collection. **Subscription-based**. **Best for product teams** wanting analytics tightly coupled with in-app guidance workflows .

- **Google Analytics 4** — **The ubiquitous web analytics standard.** Free with Google Ads integration, but **product analytics depth is closer to web analytics** than Mixpanel or Amplitude . **Best for marketing teams** needing traffic analysis with Google ecosystem integration. **Trade-offs**: GDPR concerns in some EU jurisdictions due to US data transfers , and raw data access often requires BigQuery.

## Open-Source GitHub Projects

- **PostHog** — **The leading open-source product analytics platform.** MIT licensed (except `ee` directory), with a **self-hostable core** and a generous hosted free tier . **Bundles analytics, session replay, feature flags, experiments, surveys, and error tracking** on one event database — the same user can be counted in a funnel, watched in a replay, targeted by a flag, and enrolled in an experiment with no data export between tools . **Engineering-led design**: built for teams where the engineer makes product decisions, with published pricing that has been reduced multiple times . **The honest trade-off**: **Amplitude's analysis surface for cohorts and growth modeling is more mature and polished** for dedicated product analysts . **Best for engineering-led startups** wanting an all-in-one stack with self-hosting and no per-tool data fragmentation.

- **OpenPanel** — **The open-source Mixpanel alternative with built-in session replay.** **Funnels, cohorts, user profiles, session history, real-time dashboards, A/B testing, and revenue tracking** . **Cookieless tracking by default** for GDPR compliance . **MCP Server with 38 tools** for querying user data from Claude, Cursor, or any MCP client . **Stack**: Next.js dashboard, Fastify event API, PostgreSQL for metadata, ClickHouse for events, Redis for cache/queue . **Self-hosting supported** with Docker . **Trade-off**: **no usage limits on session replay** unlike Mixpanel's 5k/month free tier . **Best for teams wanting Mixpanel-like depth with session replay** and transparent self-hosting.

- **Matomo** — **The leading open-source web analytics platform with full data ownership.** GPL v3 licensed, used on **1.4M+ websites** . **Self-hosted PHP/MySQL** — data stays in your own database, you set retention policies, and no third party can access or monetize it . **HIPAA, GDPR, and CCPA-friendly by design**; plugin ecosystem for extended functionality . **Trade-offs**: **product analytics depth is closer to GA4 than Mixpanel** — covers web analytics, some funnel analysis, and campaign tracking, but **lacks behavioral cohort depth** and **auto-capture requires manual event instrumentation** . **Best for regulated industries and EU organizations** where data residency is non-negotiable.

- **Countly** — **The open-source product analytics platform with enterprise features.** **Feature flags, push notifications, crash reporting, and user profiles** alongside analytics . **Recent releases (25.03.x) focus heavily on security hardening** — fixing cross-tenant data exfiltration vectors, path traversal, XSS, and SSRF issues . **Best for teams needing analytics plus engagement tooling** in one self-hosted stack, with the caveat that recent security fixes suggest past vulnerabilities worth reviewing.

- **OpenMetrics Analytics** — **The lightweight self-hosted analytics platform with ClickHouse backend.** **Go + ClickHouse + PostgreSQL + Redis** stack. **Collector → Redis Stream → Worker → ClickHouse** pipeline for high-throughput ingestion with **<200ms dashboard query latency** . **Docker Compose deployment** for quick setup . **Best for teams wanting a minimal, modern analytics stack** without the breadth of PostHog or Matomo.

- **smolanalytics** — **The single-binary analytics toolkit with MCP integration.** **One Go binary, one data file, no external database** . **Web analytics (visitors, referrers, UTM, devices) and product analytics (funnels, retention, paths, cohorts)** from the same events, plus **feature flags, A/B testing, click heatmaps, in-product surveys, and session inspector** . **Cookieless mode** means no consent banner. **MCP server** so your coding agent queries real analytics from your editor — **79 tools and 14 built-in prompts** . **MIT licensed, free forever, data never leaves your box** . **Best for developers** wanting analytics they can query from their IDE without a separate dashboard login.

### Additional Strong Open-Source Options

- **Plausible** — Lightweight, privacy-focused web analytics. **Cookieless by default**, simple dashboard, no consent banner required . Best for teams wanting privacy-first traffic analytics without product analytics depth.
- **OpenAnalytics** — Lightweight self-hosted analytics API with **PostgreSQL storage** and **tracker.js** for custom dashboards . Best for developers wanting to build their own analytics UI on a simple API.
- **Kissmetrics** — Person-centric behavioral analytics tying user actions to revenue. **Commercial only, no self-hosted option** . Best for e-commerce teams needing revenue attribution depth.

**Frameworks for building custom systems**: Combine **PostHog** for the most complete open-source analytics-plus-replay-plus-flags stack, **OpenPanel** for Mixpanel-like depth with self-hosted session replay, **Matomo** for regulated-industry web analytics with full data sovereignty, **Countly** for analytics plus engagement tooling, and **smolanalytics** for single-binary simplicity with MCP integration — to build a user engagement analytics stack tailored to your need for product depth versus web analytics, self-hosting versus managed, and integrated tooling versus focused simplicity.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- User engagement analytics tools differ significantly in product analytics depth, data ownership model, and operational complexity. **PostHog is the most complete open-source option** with analytics, replay, flags, and experiments on one event database, but **Amplitude's cohort and growth modeling analysis is more mature** for dedicated product analysts . **Matomo excels at data sovereignty** for regulated industries, but its **product analytics depth is closer to GA4** and it requires manual event instrumentation with no auto-capture . **OpenPanel provides Mixpanel-like depth with self-hosted session replay** and no replay limits . **Countly's recent releases include extensive security fixes** — review the changelog if you're evaluating it for production . **smolanalytics is a single-binary toolkit** — simpler than PostHog or Matomo, but with less ecosystem depth.
- Self-hosted open-source solutions require proper database configuration (ClickHouse for PostHog and OpenPanel, PostgreSQL for OpenMetrics and OpenAnalytics), Redis for event streaming, and awareness that "free" self-hosted still has infrastructure and maintenance costs.

---

**Made for product engineers, data analysts, and teams choosing engagement analytics that match their data-ownership requirements and workflow needs.**
Let's make user engagement analytics more open, self-hostable, and product-focused.
