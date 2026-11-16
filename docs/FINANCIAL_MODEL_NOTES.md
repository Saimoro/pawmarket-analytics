# Financial Model Notes — PawMarket v0.4.2

## Purpose

The Financial Model is an illustrative 12-month scenario P&L for testing metric definitions, financial bridges and dashboard logic. Every input is synthetic. It is not a real company's financial statement, forecast or finding.

## Scenario interpretation

From M01 to M12:
- Net revenue rises from approximately $336.8k to $392.5k (**+16.5%**).
- Operating profit rises from approximately $19.7k to $20.3k (**+3.2%**).
- Operating margin moves from approximately 5.85% to 5.18% (**−0.67 percentage points**).

This is weakening **quality of growth**: profit growth trails revenue growth and margin compresses. Revenue and absolute operating profit do not decline in this scenario.

The operating-margin reference is 3%–6%. M03 is approximately 6.02%, slightly above the upper reference; the remaining 11 months are inside it. This is a diagnostic reference, not a constraint.

## Revenue definitions

- **Gross merchandise sales:** merchandise value before discounts and merchandise refunds.
- **Net merchandise revenue:** gross merchandise sales less merchandise discounts and merchandise refunds. Excludes shipping revenue and sales tax.
- **Net shipping revenue:** shipping fees charged less shipping refunds.
- **Net revenue:** net merchandise revenue plus net shipping revenue; excludes sales tax.

## Profit bridge

1. Net merchandise revenue less COGS = gross profit.
2. Gross profit less payment processing, packaging, picking, delivery operating costs and incremental compensation = contribution before paid marketing.
3. Contribution before paid marketing less paid acquisition spend = contribution after paid marketing.
4. Contribution after paid marketing less CRM direct costs and fixed operating costs = operating profit under this case definition.
5. Operating margin = operating profit / total net revenue.

COGS is modeled using a varying monthly rate around a 48% calibration anchor. In the event-level model, reconstruct COGS from order-item quantities and historical unit-cost snapshots.

## Delivery cost

Delivery operating cost in the current scenario is a **percentage-of-revenue placeholder**. It is not courier payroll, an hourly-rate proxy or a source-level sum of delivery events. Do not divide it by paid courier hours to infer an hourly wage.

The future source model must distinguish:
- Third-party fees from deliveries assigned to external partners.
- In-house courier payroll from courier-monthly records.
- Other direct delivery costs, where supported.

Do not charge both third-party fees and in-house payroll to the same delivery. Do not duplicate courier payroll in fixed costs.

## Refunds, returns and compensation

- Refunds reduce the appropriate merchandise or shipping revenue component.
- Returns are physical returned items and affect COGS only when restockable under the defined policy.
- Incremental compensation is a separate customer-recovery cost.
- Avoid double counting discounts, refunds or replacement COGS.

## Paid acquisition and CRM

- `total_new_customers`: distinct new customers from all acquisition sources.
- `paid_first_touch_new_customers`: distinct new customers assigned to paid first touch.
- Paid new-customer CAC = paid media spend / paid first-touch new customers.
- CRM and organic acquisition are excluded from paid CAC.

Campaign-month paid customer counts are synthetic allocations, not yet validated against customer-level IDs. Validate unique first-touch assignment when source events are generated.

**ROAS** is order-attributed net revenue / campaign spend. It measures revenue efficiency, not profit.

**Contribution-based ROMI** requires contribution allocated to orders credited to a campaign under the selected attribution model. Do not use total company contribution as a shortcut.

## Calibration anchors

- COGS: 48% of net merchandise revenue.
- Delivery operating costs: 9% of net revenue.
- Paid acquisition: 5% of net revenue.
- Operating-margin reference: 3%–6% of net revenue.

Percentage assumptions are stored as decimal fractions and displayed as percentages (for example, 0.48 displays as 48%). These are design anchors, not hard constraints.

## Reconciliation and limitations

Monthly campaign spend reconciles to paid media in the scenario P&L. Paid CAC uses a separate paid first-touch denominator. Delivery inputs are illustrative aggregates and do not expose the exact delivery-model split or intervention date. The final model must reconcile generated orders, order items, refunds, returns, deliveries, payroll, paid media, CRM and fixed costs to monthly financial totals.
