# Synthetic source data

This directory is reserved for the event-level synthetic source tables and reproducible generation scripts planned for Phase 1.

**Current status:** generation has not started. No CSV files or scripts are published here yet.

Planned source tables include customers, products, orders, order_items, deliveries, couriers, courier_monthly, refunds, returns, compensations, fixed_costs, campaigns, marketing_spend, crm_activity and order_attribution.

Before publishing generated data:
1. Approve source grains, primary/foreign keys and reporting dates.
2. Create private ground truth outside this public repository.
3. Generate linked records without exposing the hidden answer.
4. Validate uniqueness, referential integrity, timestamp order and financial reconciliation.
5. Document random seeds and generation assumptions so the data can be reproduced.

All records will be synthetic and must not contain real personal data.
