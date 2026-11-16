# PawMarket — Project Brief (v0.1)

## Objective

Investigate why a fictional US pet-supplies e-commerce business is experiencing deteriorating performance over 12 months. Produce a transparent, reproducible analysis and practical management recommendations.

## Role and audience

- **Analyst:** Junior Product / Data Analyst
- **Audience:** Business owner and functional managers
- **Currency:** USD
- **Data:** Entirely synthetic

## Business model

Online retail of cat and dog products across food, litter, treats, toys and accessories. The case may include repeat purchases and scheduled/subscription-style orders, but their importance must be supported by the modeled data rather than assumed.

## Working storyline

The business initially uses a mixed fulfillment model: third-party delivery partners alongside its own couriers. Management later decides to terminate third-party contracts and move to fully in-house delivery. The working narrative also includes changes to existing courier compensation and hiring plans.

Before analysis, the project must define:
- Effective date(s) of the transition.
- Third-party fees versus in-house courier payroll and other direct costs.
- Treatment of existing and newly hired couriers.
- Delivery capacity, failed attempts, delivery time and customer experience.
- Whether any simultaneous changes confound a before/after comparison.

This is a hypothesis-rich business event, not proof that the transition caused the decline.

## Analytical questions

1. When did performance begin to deteriorate, and which metrics moved first?
2. Is the change driven by acquisition volume/efficiency, order frequency, basket size, pricing, product mix, refunds or costs?
3. Which marketing channels and campaigns create incremental value?
4. Are repeat purchase and cohort economics weakening?
5. Did fulfillment costs or service levels change after the delivery-model transition?
6. Which actions have the strongest evidence and most attractive expected impact?

## Methodology rules

- State each metric's numerator, denominator, time window and exclusions.
- Distinguish revenue, gross profit and contribution.
- Define CAC consistently and distinguish new-customer CAC from blended acquisition cost.
- Define ROAS and ROMI explicitly; do not use them interchangeably.
- Keep first-touch channel and campaign/order attribution separate.
- Reconcile order-level and finance-level totals.
- Mark assumptions, limitations and causal uncertainty.

## Scope

**In scope:** sales, marketing, customer behavior, unit economics, financial performance and delivery operations.

**Out of scope for the first iteration:** live integrations, real customer data, production forecasting and causal claims unsupported by the synthetic design.

## Deliverables

1. Synthetic source tables with documented generation logic.
2. Data-quality checks and a data dictionary.
3. Excel workbook with analysis sheets and a concise executive dashboard.
4. Written findings, recommendations and limitations.
5. GitHub documentation sufficient for a reviewer to understand and reproduce the case.

## Status

Version 0.1 is a kickoff scaffold. No analytical results or recommendations have been validated.
