# Analytical Methodology and Guardrails

## Investigation stance

PawMarket is fictional. The task is to investigate weakening operating efficiency, not confirm a predetermined narrative. The current scenario shows revenue growth with margin compression, not revenue contraction or a collapse in absolute operating profit.

The delivery-model decision, advertising efficiency and alternative explanations such as seasonality, customer/product mix and courier workload are investigation paths, not established root causes.

## Evidence hierarchy

1. Validated event-level source records.
2. Reconciled aggregates derived from those records.
3. Clearly labeled synthetic scenario inputs used for prototyping.
4. Assumptions and hypotheses, explicitly labeled.

A dashboard based on starter inputs is a prototype, not evidence of an actual business outcome.

## Grain and joins

Every source table must define its row grain, primary key, foreign keys, expected cardinality, event timestamp and reporting period. Aggregate separate one-to-many fact tables to the intended analysis grain before joining to prevent fan-out and inflated totals.

## Revenue and profitability

Keep gross merchandise sales, net merchandise revenue, net shipping revenue, total net revenue, COGS, gross profit, contribution and operating profit distinct. State denominator choices beside every margin or rate.

Compare top-line growth with profit growth and margin movement. Do not describe a growing business as having falling revenue when modeled evidence shows margin compression.

## Acquisition and retention

Keep all-source `total_new_customers` distinct from paid `paid_first_touch_new_customers`. Paid CAC uses the paid first-touch denominator. ROAS uses order-attributed revenue under the documented attribution model. CRM is a separate retention stream and excluded from paid CAC.

Campaign-month paid-new-customer allocations are synthetic and need customer-level uniqueness checks. Compare retention cohorts at equal ages and exclude immature follow-up windows.

## Fulfillment and customer recovery

Track delivery model, third-party fees, courier payroll, active couriers, paid hours, delivery outcomes, promised and actual timestamps, failed attempts and on-time status. Keep refunds, physical returns and incremental compensation separate.

Deliveries per 100 paid courier hours is a throughput proxy, not service quality. Interpret it alongside on-time delivery, delivery success, average/P90 delivery time, cost per delivered order and customer recovery.

Current P&L delivery cost is a percentage-of-revenue placeholder, not payroll. Reconstruct costs from mutually exclusive delivery events and courier-monthly payroll before evaluating hourly rates or delivery-model effects.

## Data-quality checks

Validate primary-key uniqueness, foreign-key integrity, missing identifiers/timestamps, event ordering, status/value consistency, duplicate business events, order-to-line reconciliation, refunds/returns, campaign spend, unique first-touch attribution, courier payroll/hours and monthly financial reconciliation.

## Causal limitations

A simple before/after comparison does not prove causation. Account for seasonality, volume, campaign mix, courier hours, product/customer mix and concurrent changes. State what the synthetic design can and cannot identify.

## Target schedule

Provisional target: approximately Month 3 from kickoff.
- Month 1: source design, synthetic record generation and data QA.
- Month 2: commercial, marketing, retention and delivery analysis.
- Month 3: evidence synthesis, recommendations and portfolio presentation.

## Public/private boundary

Do not publish the exact hidden intervention date, planted data-generation switches, intended answer or effect sizes reserved for private ground truth. Public files may describe the management decision without disclosing the hidden answer used to validate the investigation.
