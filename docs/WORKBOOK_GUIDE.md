# Workbook Guide — PawMarket v0.4.2

Start with Project Brief, Decision Log and Analysis Plan. Review Data Model, Data Dictionary and Metrics Dictionary before interpreting financial and dashboard sheets. Dashboards are prototypes based on synthetic scenario inputs.

| Sheet | Purpose | Guardrail |
|---|---|---|
| Project Brief | Objective, scope and scenario | Quality-of-growth deterioration, not revenue contraction |
| Decision Log | Agreed decisions and open items | Treat only Confirmed entries as approved rules |
| Analysis Plan | Investigation workstreams | Planned sequence, not completed analysis |
| Data Dictionary | Field-level source definitions | Use for source design and QA |
| Data Model | Grains, keys and relationships | Aggregate one-to-many tables before joining |
| Metrics Dictionary | Metric formulas and caveats | Keep numerator, denominator and exclusions consistent |
| Task Tracker | Work status | Scenario model is done; source generation and validation remain open |
| Data Template | Monthly operating snapshot | `total_new_customers` is all-source; paid first-touch customers and CAC are separate |
| Model Assumptions | Editable scenario drivers | Synthetic anchors, not observed business parameters |
| Financial Model | Monthly P&L and checks | Includes revenue/profit growth and margin trend checks |
| Marketing Inputs | Campaign-month starter data | Paid first-touch customers are not total new customers |
| Delivery Inputs | Monthly delivery operations | No intervention date or delivery-model split is disclosed |
| Executive Dashboard | High-level business view | Scenario prototype |
| Marketing Dashboard | Paid acquisition scorecard | CRM/retention is separate |
| Delivery Dashboard | Delivery quality and productivity | Throughput per paid hour is not service quality |

## Key interpretation notes

### Financial scenario
- Net revenue grows approximately 16.5% from M01 to M12.
- Operating profit grows approximately 3.2%.
- Operating margin contracts approximately 0.67 percentage points.
- M03 is slightly above the 3%–6% reference; the other 11 months are within it.
- These are synthetic scenario values, not actual business results.

### Paid CAC
- `total_new_customers`: all acquisition sources.
- `paid_first_touch_new_customers`: new customers attributed to paid first touch.
- Paid CAC = paid media spend / paid first-touch new customers.
- Do not divide paid spend by all-source new customers.
- Campaign-level paid customer allocations still require customer-ID uniqueness validation.

### Delivery
- Financial Model delivery cost is a percentage-of-revenue placeholder, not courier payroll.
- Do not divide it by courier hours to infer an hourly wage.
- Pair deliveries per 100 paid hours with on-time rate, success rate, delivery time and cost per delivered order.

## Missing from this version

Complete transaction-level customers, orders, order items, deliveries, courier payroll, refunds, returns, compensations, CRM activities and order-attribution records are not yet generated. Their intended schema is documented in Data Model.

## Version note

v0.4.2 clarifies the scenario interpretation, separates paid first-touch customers from all-source new customers, adds formula-driven monthly paid CAC and adds P&L trend checks. Dashboard layouts and starter scenario inputs are retained.
