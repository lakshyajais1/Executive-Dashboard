
# Executive Analytics Platform — NYX.Today

> A product case study + metric documentation for a 5-module analytics platform unifying Google Ads, Meta, GA4, and Shopify into a single source of truth for leadership.

**Role:** Product Development Associate at NYX.Today
**Ownership:** End-to-end — user research, metric definition, dashboard design, logic specification, rollout

---

## What's in this Repo

This is a **product documentation repo**, not a code repo. It contains:

- 📊 **Dashboard prototypes** — interactive HTML mockups of all 5 modules
- 📐 **Metric definitions** — 50+ KPI formulas, data sources, and edge cases
- 🧠 **Product logic** — fallback-state logic for partially-integrated brands
- 📝 **Design rationale** — why each module exists and what decision it enables

The production system is internal to NYX.Today; this repo documents the product thinking behind it.

---

## The Problem

Marketing and leadership at NYX were stitching together performance data across 4+ platforms (Google Ads, Meta, GA4, Shopify) — switching tabs, exporting CSVs, and arguing over which numbers were "right." Spend decisions on millions in ad budget were slow and often based on incomplete or inconsistent data.

## The Product

A unified analytics platform with **5 dedicated modules**, each answering one core business question:

| Module | Question it answers |
|---|---|
| **Executive Summary** | How is the business performing this period vs target? |
| **Marketing** | Which channels and funnel stages are driving ROAS? |
| **Revenue & Sales** | What's converting, at what value, and how often? |
| **Customer** | Who are we acquiring, retaining, and losing? |
| **Engagement** | How are users interacting with the product? |

[See dashboard prototypes →](./dashboards/)

---

## Key Product Decisions

### 1. Metric Reconciliation Across 4 Platforms
Each platform defines "conversion," "click," and "revenue" differently. I worked with the marketing team to define 50+ KPIs end-to-end — locking the formula, source platform, and edge cases for every metric — so leadership stops debating "which number is right."

[See full metric definitions →](./metric-definitions/)

### 2. Fallback Logic for Partial Integrations
Not every client brand connects every platform. Instead of showing broken cards or zero values, I designed a fallback system: cards render meaningful states (e.g., "Not connected" with setup CTA) based on which sources are available. This was a key reliability decision that made the dashboard trustworthy across clients with different integration setups.

[See fallback logic spec →](./logic/fallback-system.md)

### 3. Full-Funnel View Across Channels
Designed the Impression → Click → Landing → Engaged → Conversion flow, with multi-channel breakdowns across Google Ads, Meta, TikTok, LinkedIn, and Snapchat. Lets teams pinpoint drop-off stages and realloca
