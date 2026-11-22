# PawMarket Analytics

**Portfolio case study | Junior Product / Data Analyst | Fictional US pet-supplies e-commerce business**

PawMarket is a fictional online retailer of cat and dog supplies. This case investigates weakening quality of growth over a 12-month period. All business entities and figures are synthetic.

> **Data disclaimer:** This is a learning/portfolio project, not commercial work. Starter inputs and dashboards are illustrative scenario data, not observed company results.

## Project status

**Phase 0 — analytical design, scenario model and dashboard prototypes**  
**Workbook:** [PawMarket_Project_Kickoff_v0.4.3.xlsx](PawMarket_Project_Kickoff_v0.4.3.xlsx)  
**Target completion:** approximately Month 3 from kickoff *(provisional planning target, not a deadline).*

The v0.4.3 workbook carries forward the scenario P&L, relational data model, metric definitions, monthly/campaign/delivery starter inputs and three dashboard prototypes, with a visual-formatting revision. The next stage is linked event-level synthetic data generation and validation.

## What the current scenario shows

The scenario represents **weakening quality of growth, not revenue contraction**:

- Net revenue increases by approximately **16.5%** from M01 to M12.
- Operating profit increases by approximately **3.2%**.
- Operating margin contracts by approximately **0.67 percentage points**.
- M03 is slightly above the 3%–6% margin reference; the other 11 months are within it.

This is a synthetic scenario pattern, not a root-cause finding. The investigation asks why profit growth trails revenue growth.

## Business context

Management decides to move from mixed fulfillment (third-party delivery partners plus in-house couriers) to fully in-house delivery. The working storyline also includes a reduction in pay for existing couriers as part of a cost and replacement-hiring decision.

The exact effective date, staffing sequence and hidden ground truth are kept out of public files. The decision is an investigation path, not proof of causation.

## Acquisition and delivery guardrails

- `total_new_customers` means new customers from all sources.
- `paid_first_touch_new_customers` is the paid-acquisition denominator. Paid CAC = paid media spend / paid first-touch new customers. Never divide by all-source new customers.
- Campaign-month paid customer counts are synthetic allocations; customer-level uniqueness and attribution need validation.
- Deliveries per 100 paid courier hours is a throughput proxy, not a service-quality metric.
- Delivery cost in the current scenario P&L is a percentage-of-revenue placeholder, not courier payroll.

## Repository structure

- [docs/PROJECT_BRIEF.md](docs/PROJECT_BRIEF.md) — scope, questions and scenario interpretation
- [docs/WORKBOOK_GUIDE.md](docs/WORKBOOK_GUIDE.md) — workbook sheet map and usage notes
- [docs/FINANCIAL_MODEL_NOTES.md](docs/FINANCIAL_MODEL_NOTES.md) — financial definitions and scenario limitations
- [docs/METHODOLOGY.md](docs/METHODOLOGY.md) — grain, joins, QA and causal guardrails
- [data/README.md](data/README.md) — planned synthetic source-data generation
- [CHANGELOG.md](CHANGELOG.md) — version history
- [PawMarket_Project_Kickoff_v0.4.3.xlsx](PawMarket_Project_Kickoff_v0.4.3.xlsx) — current workbook

The v0.4.3 workbook is available in the root of this repository. Event-level CSV/SQL datasets and generation scripts are not published yet.

## Planned roadmap

| Target | Work |
|---|---|
| Month 1 | Finalize source grains and rules; generate linked synthetic tables; validate keys, timestamps and financial reconciliation |
| Month 2 | Analyze commercial performance, paid acquisition, cohorts, unit economics and delivery operations; rebuild dashboards from validated sources |
| Month 3 | Prepare SQL/Excel evidence, recommendations, limitations and portfolio write-up |

The schedule is provisional and will be adjusted as the project develops.

## Analytical principles

1. Define grain, primary keys and foreign keys before generating data.
2. Separate gross sales, net merchandise revenue, shipping revenue, gross profit, contribution and operating profit.
3. Keep third-party delivery fees and in-house courier payroll separate at source level, then combine once.
4. Keep refunds, physical returns and incremental compensation separate.
5. Separate first-touch paid CAC from order-level attribution used for ROAS.
6. Compare cohorts at equal ages and exclude immature windows.
7. Aggregate one-to-many facts before joining to avoid fan-out.
8. Treat every business explanation as a hypothesis until supported by validated data.

---

*All companies, customers, transactions and business results in this case are fictional and synthetic. The project is independent educational work, not commercial client work.*
