# PawMarket Analytics

**Portfolio case study | Junior Product / Data Analyst | Synthetic US e-commerce business**

PawMarket is a fictional online retailer of cat and dog supplies. This project investigates a deterioration in business performance over a 12-month period and develops evidence-based recommendations for management.

> **Data disclaimer:** PawMarket, its customers, transactions, campaigns and operating results are fictional. All data created for this case study will be synthetic. This is a learning/portfolio project, not commercial work.

## Project status

**Phase 0 — Kick-off and analytical design**

The initial workbook captures the project brief, working assumptions, analysis plan, starter data dictionary and task backlog. No performance findings have been produced yet.

## Business context

The working case includes a major fulfillment strategy change: the company moves from a mixed model (third-party delivery plus its own couriers) to fully in-house delivery. The timing, cost mechanics and operational consequences still need to be formalized before analysis.

The analyst's task is not to prove a predetermined explanation. It is to establish what changed, quantify the drivers, test data quality and distinguish supported findings from hypotheses.

## Planned analysis

- Business performance: orders, revenue, average order value and profitability
- Marketing: channel and campaign spend, CAC, ROAS and ROMI
- Customers: acquisition, repeat purchase, retention and cohorts
- Unit economics: contribution after variable and fulfillment costs
- Delivery operations: cost, capacity, speed and service quality before/after the model change
- Executive synthesis: prioritized actions, trade-offs and limitations

## Repository structure

- `PawMarket_Project_Kickoff_v0.1.xlsx` — initial project workbook and planning scaffold
- `docs/PROJECT_BRIEF.md` — scope, methodology principles and project roadmap

## Important modeling principles

1. Define the grain of every table before generating records.
2. Keep gross, net and contribution measures distinct.
3. Separate first-touch acquisition from order-level marketing attribution.
4. Document the treatment of cancellations, discounts, refunds, taxes and shipping.
5. Validate joins, duplicates, missing values and time consistency.
6. Do not treat early scenario figures as observed results or targets until their meaning is confirmed.

## Current assumptions requiring validation

- 12-month analysis horizon.
- Four marketing channels and approximately 10–12 campaigns as an initial design assumption.
- Product categories: food, litter, treats, toys and accessories.
- Earlier draft figures (including $55,000 revenue and ROMI near 0%) are **unvalidated scenario notes**, not findings.

## Roadmap

1. Confirm business timeline and metric definitions.
2. Design and generate synthetic source tables.
3. Run data-quality and reconciliation checks.
4. Build Excel analysis and dashboard.
5. Develop findings and recommendations.
6. Publish the final case study and methodology.

