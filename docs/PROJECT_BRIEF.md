# PawMarket — Project Brief

**Workbook version:** v0.4.2  
**Stage:** analytical design, scenario P&L and dashboard prototyping  
**Kickoff:** 2026-11-16  
**Target completion:** approximately Month 3 from kickoff *(provisional)*

## Objective

Investigate why a fictional US pet-supplies e-commerce business is experiencing weakening operating efficiency over 12 months. Produce a transparent, reproducible analysis and practical management recommendations.

## Conventions

- Analyst: Junior Product / Data Analyst
- Audience: business owner and functional managers
- Currency: USD
- Period: 12 relative months (M01–M12)
- Data: entirely synthetic
- Exact calendar dates and reporting timezone: open

## Business model

Online retail of cat and dog products across food, litter, treats, toys and accessories. Repeat purchasing is part of the model, but its behavior and economics must be measured rather than assumed.

## Current scenario signal

The synthetic P&L represents **weakening quality of growth, not falling revenue**. From M01 to M12, net revenue rises by approximately 16.5%, operating profit rises by approximately 3.2%, and operating margin contracts by approximately 0.67 percentage points.

The operating-margin reference is 3%–6%. M03 is approximately 6.02%, slightly above the upper reference; the other 11 months are within the band. The range is a diagnostic reference, not a constraint that every month must satisfy.

## Known management decision

The business initially uses mixed fulfillment: third-party delivery partners plus in-house couriers. Management decides to terminate third-party contracts and move to fully in-house delivery. The working storyline also includes a reduction in pay for existing couriers as part of a cost and replacement-hiring decision.

The analyst may know this decision. The exact effective date, staffing sequence, capacity consequences and hidden ground truth are not public. The decision is a candidate explanation, not proof of causation.

Test effects on delivery fees, courier payroll, capacity, paid hours, delivery time, on-time performance, failed attempts, complaints, compensation, cancellations, repeat behavior and contribution per order.

## Core questions

1. When did operating efficiency begin to weaken, and which metrics moved first?
2. Are changes associated with acquisition efficiency, order frequency, basket size, discounts, refunds, product mix or costs?
3. Which paid channels and campaigns deliver customers and attributed revenue at acceptable economics?
4. Are repeat purchase and customer cohorts changing at comparable cohort ages?
5. Did delivery costs, capacity or service levels change around the fulfillment decision?
6. Which actions have the strongest evidence, and what are the limitations?

## Methodology rules

- Define numerator, denominator, grain, window and exclusions for every metric.
- Distinguish ROAS from contribution-based ROMI.
- Separate all-source `total_new_customers` from paid `paid_first_touch_new_customers`.
- Paid CAC uses paid first-touch customers only; CRM and organic customers are excluded.
- Keep third-party fees and in-house payroll separate at source level.
- Keep refunds, physical returns and incremental compensation separate.
- Aggregate one-to-many facts before joining.
- Compare cohorts at equal ages and exclude immature windows.
- Reconcile order-level and finance-level totals.
- Mark assumptions, limitations and causal uncertainty.

## Current workbook scope

The v0.4.2 workbook includes project control sheets, data dictionary/model, metrics dictionary, a 12-month scenario P&L, editable assumptions, monthly/campaign/delivery starter inputs, and executive/marketing/delivery dashboard prototypes. It also separates all-source and paid first-touch new-customer denominators and adds trend checks.

Starter inputs are illustrative, not validated event-level records. Dashboards must be rebuilt from validated sources before final findings are reported.

## Out of scope for this iteration

Live integrations, real customer data, production forecasting, final event-level source data, validated root-cause diagnosis and unsupported causal claims.

## Next stage

1. Approve exact calendar dates and reporting timezone.
2. Generate linked synthetic source records at the documented grains.
3. Validate keys, timestamps, statuses and monetary reconciliation.
4. Rebuild monthly, campaign and delivery aggregates.
5. Analyze findings, recommendations and limitations.

**Status:** analytical design and scenario model only. No root cause or management recommendation has been validated.
